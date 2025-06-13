<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `docker`

-	[`docker:28`](#docker28)
-	[`docker:28-cli`](#docker28-cli)
-	[`docker:28-dind`](#docker28-dind)
-	[`docker:28-dind-rootless`](#docker28-dind-rootless)
-	[`docker:28-windowsservercore`](#docker28-windowsservercore)
-	[`docker:28-windowsservercore-ltsc2022`](#docker28-windowsservercore-ltsc2022)
-	[`docker:28-windowsservercore-ltsc2025`](#docker28-windowsservercore-ltsc2025)
-	[`docker:28.2`](#docker282)
-	[`docker:28.2-cli`](#docker282-cli)
-	[`docker:28.2-dind`](#docker282-dind)
-	[`docker:28.2-dind-rootless`](#docker282-dind-rootless)
-	[`docker:28.2-windowsservercore`](#docker282-windowsservercore)
-	[`docker:28.2-windowsservercore-ltsc2022`](#docker282-windowsservercore-ltsc2022)
-	[`docker:28.2-windowsservercore-ltsc2025`](#docker282-windowsservercore-ltsc2025)
-	[`docker:28.2.2`](#docker2822)
-	[`docker:28.2.2-alpine3.22`](#docker2822-alpine322)
-	[`docker:28.2.2-cli`](#docker2822-cli)
-	[`docker:28.2.2-cli-alpine3.22`](#docker2822-cli-alpine322)
-	[`docker:28.2.2-dind`](#docker2822-dind)
-	[`docker:28.2.2-dind-alpine3.22`](#docker2822-dind-alpine322)
-	[`docker:28.2.2-dind-rootless`](#docker2822-dind-rootless)
-	[`docker:28.2.2-windowsservercore`](#docker2822-windowsservercore)
-	[`docker:28.2.2-windowsservercore-ltsc2022`](#docker2822-windowsservercore-ltsc2022)
-	[`docker:28.2.2-windowsservercore-ltsc2025`](#docker2822-windowsservercore-ltsc2025)
-	[`docker:cli`](#dockercli)
-	[`docker:dind`](#dockerdind)
-	[`docker:dind-rootless`](#dockerdind-rootless)
-	[`docker:latest`](#dockerlatest)
-	[`docker:windowsservercore`](#dockerwindowsservercore)
-	[`docker:windowsservercore-ltsc2022`](#dockerwindowsservercore-ltsc2022)
-	[`docker:windowsservercore-ltsc2025`](#dockerwindowsservercore-ltsc2025)

## `docker:28`

```console
$ docker pull docker@sha256:ff052514f359111edd920b54581e7aca65629458607f9fbdbf82d7eefbe0602b
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
$ docker pull docker@sha256:8e32fae437051e392dc31f1bca659a14a6b8f341fa6dd131a9def0a9f315203c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.7 MB (143689092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:896cfe4b7aa87684cdbe7274a5a4efafa80c561662a935bd3a0432e2fcbaf46d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-x86_64'; 			sha256='6777247eb2947c48b46b1fc96602ac17e140fbac84e1043e6384a6c755fc6769'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv6'; 			sha256='1a7731a63ec845b4b4cf2510e68a8f3411386b1e4b5b03916a0d21a697596f03'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv7'; 			sha256='63e64d9aad9916771a947e4b77df6b2a5e70cdfdb412b2f0464806f4d63fabe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-aarch64'; 			sha256='36dfcc81ffff0ec2a76abaa4b66edf01d2db0d7f3fda342a26525eb72e4e9a80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-ppc64le'; 			sha256='4410f045bfc084fef1f0fcea2c3f8e665cad6c5055f57f1089dd009bb9b65151'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-riscv64'; 			sha256='6d551f86c2ab9155882f5a1067223d0c0c80b47669c826af4311c305cc637093'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-s390x'; 			sha256='6012d0bd529312d12937fd153583a90ddb29aec7a7a8cfaac8e7fb7d1ceabf6f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 05 Jun 2025 17:36:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
CMD ["sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
VOLUME [/var/lib/docker]
# Thu, 05 Jun 2025 17:36:11 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
CMD []
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f32e8d6f68009e4f81cdd4d2b7e6465c3cdc96e6addc90132dfdb88d08941a20`  
		Last Modified: Thu, 12 Jun 2025 22:36:53 GMT  
		Size: 8.2 MB (8207474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ac40e43aadc31b56fc943a7df1de7e7f5f06348ca89a108384ba3e9a805a89`  
		Last Modified: Thu, 12 Jun 2025 22:36:53 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3870806677ebd2c8113c069ad6c6f219c456246069bd2688c9cffe6d1736938`  
		Last Modified: Thu, 12 Jun 2025 22:36:55 GMT  
		Size: 20.1 MB (20083028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86f14a0f3d88cab9e631bd4dcf8f9a164306875132f95135fff3358e3a2a8d2`  
		Last Modified: Thu, 12 Jun 2025 22:36:56 GMT  
		Size: 21.3 MB (21290186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da67c6f5f9a3f4626ce69c1328bdacf4c370d20479d084f6415437dea4481db4`  
		Last Modified: Thu, 12 Jun 2025 22:36:56 GMT  
		Size: 21.1 MB (21100670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b94aef2e962e8f653820f39c328e9f31ab7a6e903d929b45f9fb82324f7633`  
		Last Modified: Thu, 12 Jun 2025 22:36:55 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a98583f050f0d3b9242c387626407b4c0affec19be6fafeb1c7135bd7303d86`  
		Last Modified: Thu, 12 Jun 2025 22:36:56 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a115214fbd18e2a1acb4699bd0d7f72d42bf84a1f4cd3d4b1cdae8248a2167fa`  
		Last Modified: Thu, 12 Jun 2025 22:36:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:212150b9078af2b8495b33e957823f54b179f41a22f2702f6fec1560c9d3f6f2`  
		Last Modified: Thu, 12 Jun 2025 23:07:54 GMT  
		Size: 6.9 MB (6905618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9212e721c88d6da1ed4b1e289f523f35a01e01885d1131cd34feceb518227abf`  
		Last Modified: Thu, 12 Jun 2025 23:07:53 GMT  
		Size: 90.5 KB (90494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b0253e449f82e84618065f5b74284cb93f7cc52668795f3590d41585c32012`  
		Last Modified: Thu, 12 Jun 2025 23:07:51 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811b046d83c5b8a6340f19f8d6acd494b2b028f5c1bf969e58cf6f0e350c7cea`  
		Last Modified: Thu, 12 Jun 2025 23:07:58 GMT  
		Size: 62.2 MB (62206627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68771551084500ee9ac3a4b32aa56d78b3d007c1986578b481436becbe8ae1a1`  
		Last Modified: Thu, 12 Jun 2025 23:07:51 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cae381f867a74a59e0d18562bd189fcc3560935254e57ceb2e247145c467a8b`  
		Last Modified: Thu, 12 Jun 2025 23:07:52 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28` - unknown; unknown

```console
$ docker pull docker@sha256:4c5431982a6f26acafc9a647e2a915e12fd2cb54c0d9fa6f5bed94ca07e186b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a1e46faf2561239606e7d796aac2f70a1bc3754ba1ff7200c43154e973515c8`

```dockerfile
```

-	Layers:
	-	`sha256:d5158885bee456f124624bc8808ba3f4ea82fc7ca56f260044b4d92a684498b1`  
		Last Modified: Fri, 13 Jun 2025 02:07:20 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28` - linux; arm variant v6

```console
$ docker pull docker@sha256:d692f151518fae2760b09152001cfba45f8bc770e1906d190d6eb2e3142b1a76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134722094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44d698360caa93e31e5563c2c622bbbeb75bd82d597a599776298366deb6aa32`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-x86_64'; 			sha256='6777247eb2947c48b46b1fc96602ac17e140fbac84e1043e6384a6c755fc6769'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv6'; 			sha256='1a7731a63ec845b4b4cf2510e68a8f3411386b1e4b5b03916a0d21a697596f03'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv7'; 			sha256='63e64d9aad9916771a947e4b77df6b2a5e70cdfdb412b2f0464806f4d63fabe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-aarch64'; 			sha256='36dfcc81ffff0ec2a76abaa4b66edf01d2db0d7f3fda342a26525eb72e4e9a80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-ppc64le'; 			sha256='4410f045bfc084fef1f0fcea2c3f8e665cad6c5055f57f1089dd009bb9b65151'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-riscv64'; 			sha256='6d551f86c2ab9155882f5a1067223d0c0c80b47669c826af4311c305cc637093'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-s390x'; 			sha256='6012d0bd529312d12937fd153583a90ddb29aec7a7a8cfaac8e7fb7d1ceabf6f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 05 Jun 2025 17:36:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
CMD ["sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
VOLUME [/var/lib/docker]
# Thu, 05 Jun 2025 17:36:11 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
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
	-	`sha256:3156c3bcd5598f721d5e807804df7256e282bd2897ea9f9f029b3cd93a5ff79b`  
		Last Modified: Thu, 05 Jun 2025 22:44:12 GMT  
		Size: 18.1 MB (18101909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:225abe8edcfa38ed05c3678afaa3fc7019381a300f823c874d6fdfd2a372c345`  
		Last Modified: Thu, 05 Jun 2025 22:44:12 GMT  
		Size: 19.9 MB (19943271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aaa4a492c5a8c6019873f7f10f4583b9134c81a74df09c55d664e88521c254c`  
		Last Modified: Thu, 12 Jun 2025 22:36:39 GMT  
		Size: 19.8 MB (19835400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d441ddcc7f77e2457e59e55a8a824b3b189eaa5a13fdaf65a914da194d6919b`  
		Last Modified: Thu, 12 Jun 2025 22:36:37 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c28d4afadc6fad8c6238b24d9a8dad8f8e7a8deb80839c1d3459890592b523f2`  
		Last Modified: Thu, 12 Jun 2025 22:36:38 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ebbefe72ea0510e4b225079670e073211f0b85e0fc4be94f42ca4ea57d54248`  
		Last Modified: Thu, 12 Jun 2025 22:36:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8241b18dc7eb679233e3250bbfb077dcd4f8778550fe3188d80dd91b7838a9bd`  
		Last Modified: Thu, 12 Jun 2025 22:54:58 GMT  
		Size: 7.2 MB (7230354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3cf946673d9726b4c5b57734c7dbf2e2e811f1b40e437ce7cc7bf5533df26a`  
		Last Modified: Thu, 12 Jun 2025 22:54:57 GMT  
		Size: 90.1 KB (90058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d08132e8b60b557ae762a779e816c58c6c366efd53ded71c9275533c8ec8f2d`  
		Last Modified: Thu, 12 Jun 2025 22:54:57 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d611e6743d4f047d30c66012bbac54fc821dc2ffefbbe8277a53e70060da2356`  
		Last Modified: Thu, 12 Jun 2025 22:55:00 GMT  
		Size: 57.9 MB (57897340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a783e6fb91bba730335ac30fbd49b93258f2e4d9d4c2a73dbe5c7663e5f497`  
		Last Modified: Thu, 12 Jun 2025 22:54:57 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b45b886f9c1b0ecbf83201757d3e791047d9cd0cbbdfc865a112256becf21ce4`  
		Last Modified: Thu, 12 Jun 2025 22:54:58 GMT  
		Size: 3.3 KB (3304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28` - unknown; unknown

```console
$ docker pull docker@sha256:d1a670e4e107e2e31f275813f1751ac249dec91fa3cfc6cc949e581bdb0c364e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb88dd0bcd267d48fad2fe5722c0bc382d70b8aa328b8a911562dc8081e3809d`

```dockerfile
```

-	Layers:
	-	`sha256:c75371d2b5d03d6fe0926a467c9d353d590b6db0765b2bc492cb0184dfe50817`  
		Last Modified: Thu, 12 Jun 2025 23:07:42 GMT  
		Size: 34.8 KB (34765 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28` - linux; arm variant v7

```console
$ docker pull docker@sha256:66277612b6b4d8230b45b06074b5716e61c90fee840cf8b7b4da8208329fe9d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.0 MB (133027832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55fe29bbf4d101c05a3d55a85a71baf6c7ae07a62cc6865b2fc5b8902a5978a6`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-x86_64'; 			sha256='6777247eb2947c48b46b1fc96602ac17e140fbac84e1043e6384a6c755fc6769'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv6'; 			sha256='1a7731a63ec845b4b4cf2510e68a8f3411386b1e4b5b03916a0d21a697596f03'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv7'; 			sha256='63e64d9aad9916771a947e4b77df6b2a5e70cdfdb412b2f0464806f4d63fabe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-aarch64'; 			sha256='36dfcc81ffff0ec2a76abaa4b66edf01d2db0d7f3fda342a26525eb72e4e9a80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-ppc64le'; 			sha256='4410f045bfc084fef1f0fcea2c3f8e665cad6c5055f57f1089dd009bb9b65151'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-riscv64'; 			sha256='6d551f86c2ab9155882f5a1067223d0c0c80b47669c826af4311c305cc637093'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-s390x'; 			sha256='6012d0bd529312d12937fd153583a90ddb29aec7a7a8cfaac8e7fb7d1ceabf6f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 05 Jun 2025 17:36:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
CMD ["sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
VOLUME [/var/lib/docker]
# Thu, 05 Jun 2025 17:36:11 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
CMD []
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b30f7212c67694cf480811a55ca551c13acaf23308660855c528140f72c862`  
		Last Modified: Fri, 13 Jun 2025 01:20:06 GMT  
		Size: 7.4 MB (7440617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3fca8ac4e435f25c24efea81db3a20417fad9d7c421bee5ce9e3b58996c8efa`  
		Last Modified: Fri, 13 Jun 2025 01:20:05 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68a306e9551e1b17a6ecb71be8147d67ef4f891736c4e69faee945e235107fc`  
		Last Modified: Fri, 13 Jun 2025 01:20:06 GMT  
		Size: 18.1 MB (18089377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44e8dff8b0583db9cb4fc33b75dec6c3d09dd8ce3a76c2a78fd8af411bce92c`  
		Last Modified: Fri, 13 Jun 2025 01:20:08 GMT  
		Size: 19.9 MB (19927230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c665168123ed7a9acc312ff431c35318ee6393642e3e2a8bb7fa2845208b64aa`  
		Last Modified: Fri, 13 Jun 2025 01:20:08 GMT  
		Size: 19.8 MB (19821284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f454bde5fc9b6055cf7fe14c89d2a03739341ccdde89409892b34630a79576`  
		Last Modified: Fri, 13 Jun 2025 01:26:31 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3159ba7c72c13cd717ca59937ae54ce16c3ef91f409e6ff1eb4ab88fc1db06c0`  
		Last Modified: Fri, 13 Jun 2025 01:26:33 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ef5f44369f56ae39826aaf9f89b54c9bf2d4d09a86c4eaf7af04c279812997`  
		Last Modified: Fri, 13 Jun 2025 01:26:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7236561f33fb7c50ca5d7c37b075afc53fe8e4088c95319dcde0bb8ad917eb0`  
		Last Modified: Fri, 13 Jun 2025 06:24:34 GMT  
		Size: 6.5 MB (6538120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98752e61e2dd86e562ed8c9de46d0e71b38f35fe7be163828be059624970c9e`  
		Last Modified: Fri, 13 Jun 2025 06:24:35 GMT  
		Size: 86.5 KB (86488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c1e6adc4b8f7742b913355688fb6e8dd3671bd9c49551a76f2dad8f0bfcf827`  
		Last Modified: Fri, 13 Jun 2025 06:24:35 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7760efd1d6901a24ed3199cf41b66c116f64c11736dcecc92c75040a0f68dea9`  
		Last Modified: Fri, 13 Jun 2025 06:24:39 GMT  
		Size: 57.9 MB (57897375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb6cd2d2e0725f775e9f508d900bb8bac548036c111ea8957a933fc7002b93e`  
		Last Modified: Fri, 13 Jun 2025 06:24:36 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcd8d4be9dc74189aefe21d876aec06706ad1fa1e7597dd49f2c2fc862477c51`  
		Last Modified: Fri, 13 Jun 2025 06:24:36 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28` - unknown; unknown

```console
$ docker pull docker@sha256:9c4cb9730947a3df8f10cb2052f42e9556fa8a3d55b8d9eb9df923d7467c4a6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4fa8b980b9e0ff354efd1a786e8ee1816d49966e8cb7f6c93a8a7182923f7fd`

```dockerfile
```

-	Layers:
	-	`sha256:4bc11f3d388f7184ad2e3f2d7090c73f569bc734a2691321b72cdcb0e3735d28`  
		Last Modified: Fri, 13 Jun 2025 08:07:23 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:b8d1c58eea384111a2c6646a55d6c57e11ce3527c44b26b17ba91e00f82530c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.5 MB (134502165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f7a08861e83333223ac02d5357e4d77380c819b320b98b1811d33973cd4cd5e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-x86_64'; 			sha256='6777247eb2947c48b46b1fc96602ac17e140fbac84e1043e6384a6c755fc6769'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv6'; 			sha256='1a7731a63ec845b4b4cf2510e68a8f3411386b1e4b5b03916a0d21a697596f03'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv7'; 			sha256='63e64d9aad9916771a947e4b77df6b2a5e70cdfdb412b2f0464806f4d63fabe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-aarch64'; 			sha256='36dfcc81ffff0ec2a76abaa4b66edf01d2db0d7f3fda342a26525eb72e4e9a80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-ppc64le'; 			sha256='4410f045bfc084fef1f0fcea2c3f8e665cad6c5055f57f1089dd009bb9b65151'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-riscv64'; 			sha256='6d551f86c2ab9155882f5a1067223d0c0c80b47669c826af4311c305cc637093'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-s390x'; 			sha256='6012d0bd529312d12937fd153583a90ddb29aec7a7a8cfaac8e7fb7d1ceabf6f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 05 Jun 2025 17:36:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
CMD ["sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
VOLUME [/var/lib/docker]
# Thu, 05 Jun 2025 17:36:11 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
CMD []
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375cb5234cd1a2b6b8f1aba00c28fc5d45ba0ecc0d3c8f130d5cdb5138ba6c09`  
		Last Modified: Fri, 13 Jun 2025 00:09:12 GMT  
		Size: 8.2 MB (8229005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ba114b122014764181bf833228533908f5eedbccce11b62f71d746ab1616ccc`  
		Last Modified: Fri, 13 Jun 2025 00:09:12 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5090356630719947eb3cfc865b4d6d8f4971f5e40c640070edd88a16ab0c486f`  
		Last Modified: Fri, 13 Jun 2025 00:09:13 GMT  
		Size: 18.9 MB (18902609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd89b3ff82b93c434d43d799f7f56e86b96409535e06f30c6bbc54456e99752d`  
		Last Modified: Fri, 13 Jun 2025 00:09:14 GMT  
		Size: 19.5 MB (19469847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb8a2de00a4f86825ec25a2f3ac1553ace626f97f529f17cda507233ec8f1a9a`  
		Last Modified: Fri, 13 Jun 2025 00:09:14 GMT  
		Size: 19.3 MB (19347260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ced3983ecfb78d04b5aefc0cf90f4a0b3ccd62ec5610841b0f7860259defda`  
		Last Modified: Fri, 13 Jun 2025 00:09:13 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3673e39b233f3bfe295c08f11dda44b40d801a0bb4f299fe81e1ec50851575`  
		Last Modified: Fri, 13 Jun 2025 00:09:13 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b219e20a46cafa0737e015b21a2525d3bb013d26dc4af6849c8f3586a8b10c5f`  
		Last Modified: Fri, 13 Jun 2025 00:09:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c6e05695096db67c5e6426307e8a652c5311da73d994e47d9580e886b837a10`  
		Last Modified: Fri, 13 Jun 2025 04:27:25 GMT  
		Size: 7.1 MB (7141507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891d71d9754311d78a8a473d578e3825acd68ce42cd0dbc623f6357a4e17c72b`  
		Last Modified: Fri, 13 Jun 2025 04:27:25 GMT  
		Size: 99.6 KB (99645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5d9a3e9b7f7718caa1aba176d0c009906cfdbf0beaabb63840d5743b89cc7f2`  
		Last Modified: Fri, 13 Jun 2025 04:27:26 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d489b833d40920f79c54667b28c6b5c28475bbdb198a31284fb082206828119a`  
		Last Modified: Fri, 13 Jun 2025 04:27:32 GMT  
		Size: 57.2 MB (57168194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e7d0e57cac200e9cb81bab37725356fb62116b7b3fb40855e245e59124702f2`  
		Last Modified: Fri, 13 Jun 2025 04:27:27 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc40c4cf8ec0a96212d48ae432d6342b219db9566141690970349c4e6140886`  
		Last Modified: Fri, 13 Jun 2025 04:27:27 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28` - unknown; unknown

```console
$ docker pull docker@sha256:e64e322c1cc45566807e6054fb529a1b90018a74d5599c9e524013622d5fd800
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30148cdfe5f84f758ae82d1f85d34d65c6e91c5167340993eaa3d924e06041f5`

```dockerfile
```

-	Layers:
	-	`sha256:a0dd369778c470b4b56994e10a017cc701a049c277738705f244ac7e5856bdd4`  
		Last Modified: Fri, 13 Jun 2025 05:07:36 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28-cli`

```console
$ docker pull docker@sha256:5d3725f5d2f52aafe8a2c49668a43eb7c681a5535a206ba28eccfd8a3013de86
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
$ docker pull docker@sha256:b65ad6989d6333212ce011be9684e2d8ae545ec1972b56588c7aff01dd3520d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74480359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c47dbf8612e5f69d7a6b634668d1fc578e0eca340ae1f8a00812e89d72e021a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 12 Jun 2025 11:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-x86_64'; 			sha256='6777247eb2947c48b46b1fc96602ac17e140fbac84e1043e6384a6c755fc6769'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv6'; 			sha256='1a7731a63ec845b4b4cf2510e68a8f3411386b1e4b5b03916a0d21a697596f03'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv7'; 			sha256='63e64d9aad9916771a947e4b77df6b2a5e70cdfdb412b2f0464806f4d63fabe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-aarch64'; 			sha256='36dfcc81ffff0ec2a76abaa4b66edf01d2db0d7f3fda342a26525eb72e4e9a80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-ppc64le'; 			sha256='4410f045bfc084fef1f0fcea2c3f8e665cad6c5055f57f1089dd009bb9b65151'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-riscv64'; 			sha256='6d551f86c2ab9155882f5a1067223d0c0c80b47669c826af4311c305cc637093'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-s390x'; 			sha256='6012d0bd529312d12937fd153583a90ddb29aec7a7a8cfaac8e7fb7d1ceabf6f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 12 Jun 2025 11:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Jun 2025 11:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f32e8d6f68009e4f81cdd4d2b7e6465c3cdc96e6addc90132dfdb88d08941a20`  
		Last Modified: Thu, 12 Jun 2025 22:36:53 GMT  
		Size: 8.2 MB (8207474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ac40e43aadc31b56fc943a7df1de7e7f5f06348ca89a108384ba3e9a805a89`  
		Last Modified: Thu, 12 Jun 2025 22:36:53 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3870806677ebd2c8113c069ad6c6f219c456246069bd2688c9cffe6d1736938`  
		Last Modified: Thu, 12 Jun 2025 22:36:55 GMT  
		Size: 20.1 MB (20083028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86f14a0f3d88cab9e631bd4dcf8f9a164306875132f95135fff3358e3a2a8d2`  
		Last Modified: Thu, 12 Jun 2025 22:36:56 GMT  
		Size: 21.3 MB (21290186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da67c6f5f9a3f4626ce69c1328bdacf4c370d20479d084f6415437dea4481db4`  
		Last Modified: Thu, 12 Jun 2025 22:36:56 GMT  
		Size: 21.1 MB (21100670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b94aef2e962e8f653820f39c328e9f31ab7a6e903d929b45f9fb82324f7633`  
		Last Modified: Thu, 12 Jun 2025 22:36:55 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a98583f050f0d3b9242c387626407b4c0affec19be6fafeb1c7135bd7303d86`  
		Last Modified: Thu, 12 Jun 2025 22:36:56 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a115214fbd18e2a1acb4699bd0d7f72d42bf84a1f4cd3d4b1cdae8248a2167fa`  
		Last Modified: Thu, 12 Jun 2025 22:36:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:1ebe76e61490c161294dbf222ba3f54e20b9c4ef88e3a419b69d6c9ea30d9cee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adb69d08e123464b3d3e1ca5fc247dafb6079c23e370b419c72f645720be223f`

```dockerfile
```

-	Layers:
	-	`sha256:c968c006dcee70140b54235857f7cdddd7486443dbd3175f36530d5404ebc8e2`  
		Last Modified: Thu, 12 Jun 2025 23:07:35 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:cbf1afecf10a316254346c8400aefe8e45ec33d0ca7d37e94acaf8df4c243108
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69498335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4b21f5d310fad2488ce7f6f0798a746c1018659fb7fce6a3975ebe40ba17364`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 12 Jun 2025 11:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-x86_64'; 			sha256='6777247eb2947c48b46b1fc96602ac17e140fbac84e1043e6384a6c755fc6769'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv6'; 			sha256='1a7731a63ec845b4b4cf2510e68a8f3411386b1e4b5b03916a0d21a697596f03'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv7'; 			sha256='63e64d9aad9916771a947e4b77df6b2a5e70cdfdb412b2f0464806f4d63fabe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-aarch64'; 			sha256='36dfcc81ffff0ec2a76abaa4b66edf01d2db0d7f3fda342a26525eb72e4e9a80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-ppc64le'; 			sha256='4410f045bfc084fef1f0fcea2c3f8e665cad6c5055f57f1089dd009bb9b65151'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-riscv64'; 			sha256='6d551f86c2ab9155882f5a1067223d0c0c80b47669c826af4311c305cc637093'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-s390x'; 			sha256='6012d0bd529312d12937fd153583a90ddb29aec7a7a8cfaac8e7fb7d1ceabf6f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 12 Jun 2025 11:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Jun 2025 11:04:16 GMT
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
	-	`sha256:3156c3bcd5598f721d5e807804df7256e282bd2897ea9f9f029b3cd93a5ff79b`  
		Last Modified: Thu, 05 Jun 2025 22:44:12 GMT  
		Size: 18.1 MB (18101909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:225abe8edcfa38ed05c3678afaa3fc7019381a300f823c874d6fdfd2a372c345`  
		Last Modified: Thu, 05 Jun 2025 22:44:12 GMT  
		Size: 19.9 MB (19943271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aaa4a492c5a8c6019873f7f10f4583b9134c81a74df09c55d664e88521c254c`  
		Last Modified: Thu, 12 Jun 2025 22:36:39 GMT  
		Size: 19.8 MB (19835400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d441ddcc7f77e2457e59e55a8a824b3b189eaa5a13fdaf65a914da194d6919b`  
		Last Modified: Thu, 12 Jun 2025 22:36:37 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c28d4afadc6fad8c6238b24d9a8dad8f8e7a8deb80839c1d3459890592b523f2`  
		Last Modified: Thu, 12 Jun 2025 22:36:38 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ebbefe72ea0510e4b225079670e073211f0b85e0fc4be94f42ca4ea57d54248`  
		Last Modified: Thu, 12 Jun 2025 22:36:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:37fab8abfd9b21a00df69a9d07c5ae68b8fdeb2d34ff544d116b57a663143a26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4395a2db76f1506365fb0eac51245b617ca30226db9bb3af6fa171e9e441302`

```dockerfile
```

-	Layers:
	-	`sha256:ad79c76406a54721aaaa4054e1b21be3980a141745279c1866556fad3f734fd2`  
		Last Modified: Thu, 12 Jun 2025 23:07:38 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:fb3724965534d54ce9da8a451424d81fb9e4d4538aeccd1da9b3917f10a8a822
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68499848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c4ad4e83728a898d4ea348a6ce14ceb59541c63a530e27e987d9fe358f1440b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 12 Jun 2025 11:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-x86_64'; 			sha256='6777247eb2947c48b46b1fc96602ac17e140fbac84e1043e6384a6c755fc6769'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv6'; 			sha256='1a7731a63ec845b4b4cf2510e68a8f3411386b1e4b5b03916a0d21a697596f03'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv7'; 			sha256='63e64d9aad9916771a947e4b77df6b2a5e70cdfdb412b2f0464806f4d63fabe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-aarch64'; 			sha256='36dfcc81ffff0ec2a76abaa4b66edf01d2db0d7f3fda342a26525eb72e4e9a80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-ppc64le'; 			sha256='4410f045bfc084fef1f0fcea2c3f8e665cad6c5055f57f1089dd009bb9b65151'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-riscv64'; 			sha256='6d551f86c2ab9155882f5a1067223d0c0c80b47669c826af4311c305cc637093'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-s390x'; 			sha256='6012d0bd529312d12937fd153583a90ddb29aec7a7a8cfaac8e7fb7d1ceabf6f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 12 Jun 2025 11:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Jun 2025 11:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b30f7212c67694cf480811a55ca551c13acaf23308660855c528140f72c862`  
		Last Modified: Fri, 13 Jun 2025 01:20:06 GMT  
		Size: 7.4 MB (7440617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3fca8ac4e435f25c24efea81db3a20417fad9d7c421bee5ce9e3b58996c8efa`  
		Last Modified: Fri, 13 Jun 2025 01:20:05 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68a306e9551e1b17a6ecb71be8147d67ef4f891736c4e69faee945e235107fc`  
		Last Modified: Fri, 13 Jun 2025 01:20:06 GMT  
		Size: 18.1 MB (18089377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44e8dff8b0583db9cb4fc33b75dec6c3d09dd8ce3a76c2a78fd8af411bce92c`  
		Last Modified: Fri, 13 Jun 2025 01:20:08 GMT  
		Size: 19.9 MB (19927230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c665168123ed7a9acc312ff431c35318ee6393642e3e2a8bb7fa2845208b64aa`  
		Last Modified: Fri, 13 Jun 2025 01:20:08 GMT  
		Size: 19.8 MB (19821284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f454bde5fc9b6055cf7fe14c89d2a03739341ccdde89409892b34630a79576`  
		Last Modified: Fri, 13 Jun 2025 01:26:31 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3159ba7c72c13cd717ca59937ae54ce16c3ef91f409e6ff1eb4ab88fc1db06c0`  
		Last Modified: Fri, 13 Jun 2025 01:26:33 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ef5f44369f56ae39826aaf9f89b54c9bf2d4d09a86c4eaf7af04c279812997`  
		Last Modified: Fri, 13 Jun 2025 01:26:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:17bce1271d7d0578a9245dd7fa91ca7dd2d6133e2d34320d3e8cdc818063c285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2eab113b229c25442c9ce7ca62b5528b3d19f6c315834a17499edc2b29f2c94`

```dockerfile
```

-	Layers:
	-	`sha256:f90f66106ac1cc7b0fabaf95162d064739ffbb6f6d97378a5324bcfff18516c3`  
		Last Modified: Fri, 13 Jun 2025 02:07:34 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:69d471e3a384a30ce1bc54407292e5f0b7cb0b7261bc36b61aa2eb5ec882db7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70086818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd6c4ddb71ce75a68aad923b7822e2edfe7e0c0cd87a9e2d99f4feffc8015393`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 12 Jun 2025 11:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-x86_64'; 			sha256='6777247eb2947c48b46b1fc96602ac17e140fbac84e1043e6384a6c755fc6769'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv6'; 			sha256='1a7731a63ec845b4b4cf2510e68a8f3411386b1e4b5b03916a0d21a697596f03'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv7'; 			sha256='63e64d9aad9916771a947e4b77df6b2a5e70cdfdb412b2f0464806f4d63fabe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-aarch64'; 			sha256='36dfcc81ffff0ec2a76abaa4b66edf01d2db0d7f3fda342a26525eb72e4e9a80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-ppc64le'; 			sha256='4410f045bfc084fef1f0fcea2c3f8e665cad6c5055f57f1089dd009bb9b65151'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-riscv64'; 			sha256='6d551f86c2ab9155882f5a1067223d0c0c80b47669c826af4311c305cc637093'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-s390x'; 			sha256='6012d0bd529312d12937fd153583a90ddb29aec7a7a8cfaac8e7fb7d1ceabf6f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 12 Jun 2025 11:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Jun 2025 11:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375cb5234cd1a2b6b8f1aba00c28fc5d45ba0ecc0d3c8f130d5cdb5138ba6c09`  
		Last Modified: Fri, 13 Jun 2025 00:09:12 GMT  
		Size: 8.2 MB (8229005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ba114b122014764181bf833228533908f5eedbccce11b62f71d746ab1616ccc`  
		Last Modified: Fri, 13 Jun 2025 00:09:12 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5090356630719947eb3cfc865b4d6d8f4971f5e40c640070edd88a16ab0c486f`  
		Last Modified: Fri, 13 Jun 2025 00:09:13 GMT  
		Size: 18.9 MB (18902609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd89b3ff82b93c434d43d799f7f56e86b96409535e06f30c6bbc54456e99752d`  
		Last Modified: Fri, 13 Jun 2025 00:09:14 GMT  
		Size: 19.5 MB (19469847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb8a2de00a4f86825ec25a2f3ac1553ace626f97f529f17cda507233ec8f1a9a`  
		Last Modified: Fri, 13 Jun 2025 00:09:14 GMT  
		Size: 19.3 MB (19347260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ced3983ecfb78d04b5aefc0cf90f4a0b3ccd62ec5610841b0f7860259defda`  
		Last Modified: Fri, 13 Jun 2025 00:09:13 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3673e39b233f3bfe295c08f11dda44b40d801a0bb4f299fe81e1ec50851575`  
		Last Modified: Fri, 13 Jun 2025 00:09:13 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b219e20a46cafa0737e015b21a2525d3bb013d26dc4af6849c8f3586a8b10c5f`  
		Last Modified: Fri, 13 Jun 2025 00:09:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:f4ad80ac0ebd1e61f59071330740a5cb04fcce43ee8dca6549fd765d5fb74f10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8152da6cbb3a8d4cbf91841ae5de344f2f6f46a451de0b36ffec8f81c859695d`

```dockerfile
```

-	Layers:
	-	`sha256:f8a046668b3f08af5f7ebc0544c42d2308112f3cbaa8603efab8638bb256e743`  
		Last Modified: Fri, 13 Jun 2025 02:07:38 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28-dind`

```console
$ docker pull docker@sha256:ff052514f359111edd920b54581e7aca65629458607f9fbdbf82d7eefbe0602b
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
$ docker pull docker@sha256:8e32fae437051e392dc31f1bca659a14a6b8f341fa6dd131a9def0a9f315203c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.7 MB (143689092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:896cfe4b7aa87684cdbe7274a5a4efafa80c561662a935bd3a0432e2fcbaf46d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-x86_64'; 			sha256='6777247eb2947c48b46b1fc96602ac17e140fbac84e1043e6384a6c755fc6769'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv6'; 			sha256='1a7731a63ec845b4b4cf2510e68a8f3411386b1e4b5b03916a0d21a697596f03'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv7'; 			sha256='63e64d9aad9916771a947e4b77df6b2a5e70cdfdb412b2f0464806f4d63fabe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-aarch64'; 			sha256='36dfcc81ffff0ec2a76abaa4b66edf01d2db0d7f3fda342a26525eb72e4e9a80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-ppc64le'; 			sha256='4410f045bfc084fef1f0fcea2c3f8e665cad6c5055f57f1089dd009bb9b65151'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-riscv64'; 			sha256='6d551f86c2ab9155882f5a1067223d0c0c80b47669c826af4311c305cc637093'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-s390x'; 			sha256='6012d0bd529312d12937fd153583a90ddb29aec7a7a8cfaac8e7fb7d1ceabf6f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 05 Jun 2025 17:36:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
CMD ["sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
VOLUME [/var/lib/docker]
# Thu, 05 Jun 2025 17:36:11 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
CMD []
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f32e8d6f68009e4f81cdd4d2b7e6465c3cdc96e6addc90132dfdb88d08941a20`  
		Last Modified: Thu, 12 Jun 2025 22:36:53 GMT  
		Size: 8.2 MB (8207474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ac40e43aadc31b56fc943a7df1de7e7f5f06348ca89a108384ba3e9a805a89`  
		Last Modified: Thu, 12 Jun 2025 22:36:53 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3870806677ebd2c8113c069ad6c6f219c456246069bd2688c9cffe6d1736938`  
		Last Modified: Thu, 12 Jun 2025 22:36:55 GMT  
		Size: 20.1 MB (20083028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86f14a0f3d88cab9e631bd4dcf8f9a164306875132f95135fff3358e3a2a8d2`  
		Last Modified: Thu, 12 Jun 2025 22:36:56 GMT  
		Size: 21.3 MB (21290186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da67c6f5f9a3f4626ce69c1328bdacf4c370d20479d084f6415437dea4481db4`  
		Last Modified: Thu, 12 Jun 2025 22:36:56 GMT  
		Size: 21.1 MB (21100670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b94aef2e962e8f653820f39c328e9f31ab7a6e903d929b45f9fb82324f7633`  
		Last Modified: Thu, 12 Jun 2025 22:36:55 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a98583f050f0d3b9242c387626407b4c0affec19be6fafeb1c7135bd7303d86`  
		Last Modified: Thu, 12 Jun 2025 22:36:56 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a115214fbd18e2a1acb4699bd0d7f72d42bf84a1f4cd3d4b1cdae8248a2167fa`  
		Last Modified: Thu, 12 Jun 2025 22:36:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:212150b9078af2b8495b33e957823f54b179f41a22f2702f6fec1560c9d3f6f2`  
		Last Modified: Thu, 12 Jun 2025 23:07:54 GMT  
		Size: 6.9 MB (6905618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9212e721c88d6da1ed4b1e289f523f35a01e01885d1131cd34feceb518227abf`  
		Last Modified: Thu, 12 Jun 2025 23:07:53 GMT  
		Size: 90.5 KB (90494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b0253e449f82e84618065f5b74284cb93f7cc52668795f3590d41585c32012`  
		Last Modified: Thu, 12 Jun 2025 23:07:51 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811b046d83c5b8a6340f19f8d6acd494b2b028f5c1bf969e58cf6f0e350c7cea`  
		Last Modified: Thu, 12 Jun 2025 23:07:58 GMT  
		Size: 62.2 MB (62206627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68771551084500ee9ac3a4b32aa56d78b3d007c1986578b481436becbe8ae1a1`  
		Last Modified: Thu, 12 Jun 2025 23:07:51 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cae381f867a74a59e0d18562bd189fcc3560935254e57ceb2e247145c467a8b`  
		Last Modified: Thu, 12 Jun 2025 23:07:52 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind` - unknown; unknown

```console
$ docker pull docker@sha256:4c5431982a6f26acafc9a647e2a915e12fd2cb54c0d9fa6f5bed94ca07e186b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a1e46faf2561239606e7d796aac2f70a1bc3754ba1ff7200c43154e973515c8`

```dockerfile
```

-	Layers:
	-	`sha256:d5158885bee456f124624bc8808ba3f4ea82fc7ca56f260044b4d92a684498b1`  
		Last Modified: Fri, 13 Jun 2025 02:07:20 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:d692f151518fae2760b09152001cfba45f8bc770e1906d190d6eb2e3142b1a76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134722094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44d698360caa93e31e5563c2c622bbbeb75bd82d597a599776298366deb6aa32`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-x86_64'; 			sha256='6777247eb2947c48b46b1fc96602ac17e140fbac84e1043e6384a6c755fc6769'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv6'; 			sha256='1a7731a63ec845b4b4cf2510e68a8f3411386b1e4b5b03916a0d21a697596f03'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv7'; 			sha256='63e64d9aad9916771a947e4b77df6b2a5e70cdfdb412b2f0464806f4d63fabe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-aarch64'; 			sha256='36dfcc81ffff0ec2a76abaa4b66edf01d2db0d7f3fda342a26525eb72e4e9a80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-ppc64le'; 			sha256='4410f045bfc084fef1f0fcea2c3f8e665cad6c5055f57f1089dd009bb9b65151'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-riscv64'; 			sha256='6d551f86c2ab9155882f5a1067223d0c0c80b47669c826af4311c305cc637093'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-s390x'; 			sha256='6012d0bd529312d12937fd153583a90ddb29aec7a7a8cfaac8e7fb7d1ceabf6f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 05 Jun 2025 17:36:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
CMD ["sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
VOLUME [/var/lib/docker]
# Thu, 05 Jun 2025 17:36:11 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
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
	-	`sha256:3156c3bcd5598f721d5e807804df7256e282bd2897ea9f9f029b3cd93a5ff79b`  
		Last Modified: Thu, 05 Jun 2025 22:44:12 GMT  
		Size: 18.1 MB (18101909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:225abe8edcfa38ed05c3678afaa3fc7019381a300f823c874d6fdfd2a372c345`  
		Last Modified: Thu, 05 Jun 2025 22:44:12 GMT  
		Size: 19.9 MB (19943271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aaa4a492c5a8c6019873f7f10f4583b9134c81a74df09c55d664e88521c254c`  
		Last Modified: Thu, 12 Jun 2025 22:36:39 GMT  
		Size: 19.8 MB (19835400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d441ddcc7f77e2457e59e55a8a824b3b189eaa5a13fdaf65a914da194d6919b`  
		Last Modified: Thu, 12 Jun 2025 22:36:37 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c28d4afadc6fad8c6238b24d9a8dad8f8e7a8deb80839c1d3459890592b523f2`  
		Last Modified: Thu, 12 Jun 2025 22:36:38 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ebbefe72ea0510e4b225079670e073211f0b85e0fc4be94f42ca4ea57d54248`  
		Last Modified: Thu, 12 Jun 2025 22:36:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8241b18dc7eb679233e3250bbfb077dcd4f8778550fe3188d80dd91b7838a9bd`  
		Last Modified: Thu, 12 Jun 2025 22:54:58 GMT  
		Size: 7.2 MB (7230354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3cf946673d9726b4c5b57734c7dbf2e2e811f1b40e437ce7cc7bf5533df26a`  
		Last Modified: Thu, 12 Jun 2025 22:54:57 GMT  
		Size: 90.1 KB (90058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d08132e8b60b557ae762a779e816c58c6c366efd53ded71c9275533c8ec8f2d`  
		Last Modified: Thu, 12 Jun 2025 22:54:57 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d611e6743d4f047d30c66012bbac54fc821dc2ffefbbe8277a53e70060da2356`  
		Last Modified: Thu, 12 Jun 2025 22:55:00 GMT  
		Size: 57.9 MB (57897340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a783e6fb91bba730335ac30fbd49b93258f2e4d9d4c2a73dbe5c7663e5f497`  
		Last Modified: Thu, 12 Jun 2025 22:54:57 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b45b886f9c1b0ecbf83201757d3e791047d9cd0cbbdfc865a112256becf21ce4`  
		Last Modified: Thu, 12 Jun 2025 22:54:58 GMT  
		Size: 3.3 KB (3304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind` - unknown; unknown

```console
$ docker pull docker@sha256:d1a670e4e107e2e31f275813f1751ac249dec91fa3cfc6cc949e581bdb0c364e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb88dd0bcd267d48fad2fe5722c0bc382d70b8aa328b8a911562dc8081e3809d`

```dockerfile
```

-	Layers:
	-	`sha256:c75371d2b5d03d6fe0926a467c9d353d590b6db0765b2bc492cb0184dfe50817`  
		Last Modified: Thu, 12 Jun 2025 23:07:42 GMT  
		Size: 34.8 KB (34765 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:66277612b6b4d8230b45b06074b5716e61c90fee840cf8b7b4da8208329fe9d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.0 MB (133027832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55fe29bbf4d101c05a3d55a85a71baf6c7ae07a62cc6865b2fc5b8902a5978a6`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-x86_64'; 			sha256='6777247eb2947c48b46b1fc96602ac17e140fbac84e1043e6384a6c755fc6769'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv6'; 			sha256='1a7731a63ec845b4b4cf2510e68a8f3411386b1e4b5b03916a0d21a697596f03'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv7'; 			sha256='63e64d9aad9916771a947e4b77df6b2a5e70cdfdb412b2f0464806f4d63fabe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-aarch64'; 			sha256='36dfcc81ffff0ec2a76abaa4b66edf01d2db0d7f3fda342a26525eb72e4e9a80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-ppc64le'; 			sha256='4410f045bfc084fef1f0fcea2c3f8e665cad6c5055f57f1089dd009bb9b65151'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-riscv64'; 			sha256='6d551f86c2ab9155882f5a1067223d0c0c80b47669c826af4311c305cc637093'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-s390x'; 			sha256='6012d0bd529312d12937fd153583a90ddb29aec7a7a8cfaac8e7fb7d1ceabf6f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 05 Jun 2025 17:36:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
CMD ["sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
VOLUME [/var/lib/docker]
# Thu, 05 Jun 2025 17:36:11 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
CMD []
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b30f7212c67694cf480811a55ca551c13acaf23308660855c528140f72c862`  
		Last Modified: Fri, 13 Jun 2025 01:20:06 GMT  
		Size: 7.4 MB (7440617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3fca8ac4e435f25c24efea81db3a20417fad9d7c421bee5ce9e3b58996c8efa`  
		Last Modified: Fri, 13 Jun 2025 01:20:05 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68a306e9551e1b17a6ecb71be8147d67ef4f891736c4e69faee945e235107fc`  
		Last Modified: Fri, 13 Jun 2025 01:20:06 GMT  
		Size: 18.1 MB (18089377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44e8dff8b0583db9cb4fc33b75dec6c3d09dd8ce3a76c2a78fd8af411bce92c`  
		Last Modified: Fri, 13 Jun 2025 01:20:08 GMT  
		Size: 19.9 MB (19927230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c665168123ed7a9acc312ff431c35318ee6393642e3e2a8bb7fa2845208b64aa`  
		Last Modified: Fri, 13 Jun 2025 01:20:08 GMT  
		Size: 19.8 MB (19821284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f454bde5fc9b6055cf7fe14c89d2a03739341ccdde89409892b34630a79576`  
		Last Modified: Fri, 13 Jun 2025 01:26:31 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3159ba7c72c13cd717ca59937ae54ce16c3ef91f409e6ff1eb4ab88fc1db06c0`  
		Last Modified: Fri, 13 Jun 2025 01:26:33 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ef5f44369f56ae39826aaf9f89b54c9bf2d4d09a86c4eaf7af04c279812997`  
		Last Modified: Fri, 13 Jun 2025 01:26:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7236561f33fb7c50ca5d7c37b075afc53fe8e4088c95319dcde0bb8ad917eb0`  
		Last Modified: Fri, 13 Jun 2025 06:24:34 GMT  
		Size: 6.5 MB (6538120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98752e61e2dd86e562ed8c9de46d0e71b38f35fe7be163828be059624970c9e`  
		Last Modified: Fri, 13 Jun 2025 06:24:35 GMT  
		Size: 86.5 KB (86488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c1e6adc4b8f7742b913355688fb6e8dd3671bd9c49551a76f2dad8f0bfcf827`  
		Last Modified: Fri, 13 Jun 2025 06:24:35 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7760efd1d6901a24ed3199cf41b66c116f64c11736dcecc92c75040a0f68dea9`  
		Last Modified: Fri, 13 Jun 2025 06:24:39 GMT  
		Size: 57.9 MB (57897375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb6cd2d2e0725f775e9f508d900bb8bac548036c111ea8957a933fc7002b93e`  
		Last Modified: Fri, 13 Jun 2025 06:24:36 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcd8d4be9dc74189aefe21d876aec06706ad1fa1e7597dd49f2c2fc862477c51`  
		Last Modified: Fri, 13 Jun 2025 06:24:36 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind` - unknown; unknown

```console
$ docker pull docker@sha256:9c4cb9730947a3df8f10cb2052f42e9556fa8a3d55b8d9eb9df923d7467c4a6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4fa8b980b9e0ff354efd1a786e8ee1816d49966e8cb7f6c93a8a7182923f7fd`

```dockerfile
```

-	Layers:
	-	`sha256:4bc11f3d388f7184ad2e3f2d7090c73f569bc734a2691321b72cdcb0e3735d28`  
		Last Modified: Fri, 13 Jun 2025 08:07:23 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:b8d1c58eea384111a2c6646a55d6c57e11ce3527c44b26b17ba91e00f82530c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.5 MB (134502165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f7a08861e83333223ac02d5357e4d77380c819b320b98b1811d33973cd4cd5e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-x86_64'; 			sha256='6777247eb2947c48b46b1fc96602ac17e140fbac84e1043e6384a6c755fc6769'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv6'; 			sha256='1a7731a63ec845b4b4cf2510e68a8f3411386b1e4b5b03916a0d21a697596f03'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv7'; 			sha256='63e64d9aad9916771a947e4b77df6b2a5e70cdfdb412b2f0464806f4d63fabe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-aarch64'; 			sha256='36dfcc81ffff0ec2a76abaa4b66edf01d2db0d7f3fda342a26525eb72e4e9a80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-ppc64le'; 			sha256='4410f045bfc084fef1f0fcea2c3f8e665cad6c5055f57f1089dd009bb9b65151'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-riscv64'; 			sha256='6d551f86c2ab9155882f5a1067223d0c0c80b47669c826af4311c305cc637093'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-s390x'; 			sha256='6012d0bd529312d12937fd153583a90ddb29aec7a7a8cfaac8e7fb7d1ceabf6f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 05 Jun 2025 17:36:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
CMD ["sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
VOLUME [/var/lib/docker]
# Thu, 05 Jun 2025 17:36:11 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
CMD []
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375cb5234cd1a2b6b8f1aba00c28fc5d45ba0ecc0d3c8f130d5cdb5138ba6c09`  
		Last Modified: Fri, 13 Jun 2025 00:09:12 GMT  
		Size: 8.2 MB (8229005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ba114b122014764181bf833228533908f5eedbccce11b62f71d746ab1616ccc`  
		Last Modified: Fri, 13 Jun 2025 00:09:12 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5090356630719947eb3cfc865b4d6d8f4971f5e40c640070edd88a16ab0c486f`  
		Last Modified: Fri, 13 Jun 2025 00:09:13 GMT  
		Size: 18.9 MB (18902609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd89b3ff82b93c434d43d799f7f56e86b96409535e06f30c6bbc54456e99752d`  
		Last Modified: Fri, 13 Jun 2025 00:09:14 GMT  
		Size: 19.5 MB (19469847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb8a2de00a4f86825ec25a2f3ac1553ace626f97f529f17cda507233ec8f1a9a`  
		Last Modified: Fri, 13 Jun 2025 00:09:14 GMT  
		Size: 19.3 MB (19347260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ced3983ecfb78d04b5aefc0cf90f4a0b3ccd62ec5610841b0f7860259defda`  
		Last Modified: Fri, 13 Jun 2025 00:09:13 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3673e39b233f3bfe295c08f11dda44b40d801a0bb4f299fe81e1ec50851575`  
		Last Modified: Fri, 13 Jun 2025 00:09:13 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b219e20a46cafa0737e015b21a2525d3bb013d26dc4af6849c8f3586a8b10c5f`  
		Last Modified: Fri, 13 Jun 2025 00:09:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c6e05695096db67c5e6426307e8a652c5311da73d994e47d9580e886b837a10`  
		Last Modified: Fri, 13 Jun 2025 04:27:25 GMT  
		Size: 7.1 MB (7141507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891d71d9754311d78a8a473d578e3825acd68ce42cd0dbc623f6357a4e17c72b`  
		Last Modified: Fri, 13 Jun 2025 04:27:25 GMT  
		Size: 99.6 KB (99645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5d9a3e9b7f7718caa1aba176d0c009906cfdbf0beaabb63840d5743b89cc7f2`  
		Last Modified: Fri, 13 Jun 2025 04:27:26 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d489b833d40920f79c54667b28c6b5c28475bbdb198a31284fb082206828119a`  
		Last Modified: Fri, 13 Jun 2025 04:27:32 GMT  
		Size: 57.2 MB (57168194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e7d0e57cac200e9cb81bab37725356fb62116b7b3fb40855e245e59124702f2`  
		Last Modified: Fri, 13 Jun 2025 04:27:27 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc40c4cf8ec0a96212d48ae432d6342b219db9566141690970349c4e6140886`  
		Last Modified: Fri, 13 Jun 2025 04:27:27 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind` - unknown; unknown

```console
$ docker pull docker@sha256:e64e322c1cc45566807e6054fb529a1b90018a74d5599c9e524013622d5fd800
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30148cdfe5f84f758ae82d1f85d34d65c6e91c5167340993eaa3d924e06041f5`

```dockerfile
```

-	Layers:
	-	`sha256:a0dd369778c470b4b56994e10a017cc701a049c277738705f244ac7e5856bdd4`  
		Last Modified: Fri, 13 Jun 2025 05:07:36 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28-dind-rootless`

```console
$ docker pull docker@sha256:c139111ddef9a8729f6be11c4f8f466526c9d9d282626ec42fe5681f14770ef1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:28-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:618707c0d004c07f5787c531d0d2b9cb07cc83c632842ec6b347811099ffc758
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.3 MB (162269674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c2a46a84fc8e55db5bd3a19a4017e96d28a0244e42500d3720717d4559dd307`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 17:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 30 May 2025 17:04:15 GMT
ENV DOCKER_VERSION=28.2.2
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 30 May 2025 17:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 30 May 2025 17:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-x86_64'; 			sha256='6777247eb2947c48b46b1fc96602ac17e140fbac84e1043e6384a6c755fc6769'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv6'; 			sha256='1a7731a63ec845b4b4cf2510e68a8f3411386b1e4b5b03916a0d21a697596f03'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv7'; 			sha256='63e64d9aad9916771a947e4b77df6b2a5e70cdfdb412b2f0464806f4d63fabe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-aarch64'; 			sha256='36dfcc81ffff0ec2a76abaa4b66edf01d2db0d7f3fda342a26525eb72e4e9a80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-ppc64le'; 			sha256='4410f045bfc084fef1f0fcea2c3f8e665cad6c5055f57f1089dd009bb9b65151'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-riscv64'; 			sha256='6d551f86c2ab9155882f5a1067223d0c0c80b47669c826af4311c305cc637093'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-s390x'; 			sha256='6012d0bd529312d12937fd153583a90ddb29aec7a7a8cfaac8e7fb7d1ceabf6f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 30 May 2025 17:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 30 May 2025 17:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 17:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 30 May 2025 17:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 30 May 2025 17:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 17:04:15 GMT
CMD ["sh"]
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 30 May 2025 17:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 30 May 2025 17:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 17:04:15 GMT
VOLUME [/var/lib/docker]
# Fri, 30 May 2025 17:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 30 May 2025 17:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 30 May 2025 17:04:15 GMT
CMD []
# Fri, 30 May 2025 17:04:15 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 30 May 2025 17:04:15 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 30 May 2025 17:04:15 GMT
USER rootless
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f32e8d6f68009e4f81cdd4d2b7e6465c3cdc96e6addc90132dfdb88d08941a20`  
		Last Modified: Thu, 12 Jun 2025 22:36:53 GMT  
		Size: 8.2 MB (8207474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ac40e43aadc31b56fc943a7df1de7e7f5f06348ca89a108384ba3e9a805a89`  
		Last Modified: Thu, 12 Jun 2025 22:36:53 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3870806677ebd2c8113c069ad6c6f219c456246069bd2688c9cffe6d1736938`  
		Last Modified: Thu, 12 Jun 2025 22:36:55 GMT  
		Size: 20.1 MB (20083028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86f14a0f3d88cab9e631bd4dcf8f9a164306875132f95135fff3358e3a2a8d2`  
		Last Modified: Thu, 12 Jun 2025 22:36:56 GMT  
		Size: 21.3 MB (21290186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da67c6f5f9a3f4626ce69c1328bdacf4c370d20479d084f6415437dea4481db4`  
		Last Modified: Thu, 12 Jun 2025 22:36:56 GMT  
		Size: 21.1 MB (21100670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b94aef2e962e8f653820f39c328e9f31ab7a6e903d929b45f9fb82324f7633`  
		Last Modified: Thu, 12 Jun 2025 22:36:55 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a98583f050f0d3b9242c387626407b4c0affec19be6fafeb1c7135bd7303d86`  
		Last Modified: Thu, 12 Jun 2025 22:36:56 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a115214fbd18e2a1acb4699bd0d7f72d42bf84a1f4cd3d4b1cdae8248a2167fa`  
		Last Modified: Thu, 12 Jun 2025 22:36:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:212150b9078af2b8495b33e957823f54b179f41a22f2702f6fec1560c9d3f6f2`  
		Last Modified: Thu, 12 Jun 2025 23:07:54 GMT  
		Size: 6.9 MB (6905618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9212e721c88d6da1ed4b1e289f523f35a01e01885d1131cd34feceb518227abf`  
		Last Modified: Thu, 12 Jun 2025 23:07:53 GMT  
		Size: 90.5 KB (90494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b0253e449f82e84618065f5b74284cb93f7cc52668795f3590d41585c32012`  
		Last Modified: Thu, 12 Jun 2025 23:07:51 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811b046d83c5b8a6340f19f8d6acd494b2b028f5c1bf969e58cf6f0e350c7cea`  
		Last Modified: Thu, 12 Jun 2025 23:07:58 GMT  
		Size: 62.2 MB (62206627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68771551084500ee9ac3a4b32aa56d78b3d007c1986578b481436becbe8ae1a1`  
		Last Modified: Thu, 12 Jun 2025 23:07:51 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cae381f867a74a59e0d18562bd189fcc3560935254e57ceb2e247145c467a8b`  
		Last Modified: Thu, 12 Jun 2025 23:07:52 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edcfb65cd16913d0735d91a3f41da46c772dc6128464cd3adef3509c06608cf3`  
		Last Modified: Fri, 13 Jun 2025 00:12:59 GMT  
		Size: 993.3 KB (993280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:969eb6fb622903c71c16e46ec5344d08043922bdd780c5d05f0149c738957108`  
		Last Modified: Fri, 13 Jun 2025 00:13:07 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5739660ee15831962b38500a68bc075c0420380781084109a21ac5085faa3d96`  
		Last Modified: Fri, 13 Jun 2025 00:13:10 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba46058072b4409214907ac1c19c90c67cc69a98dbe8bd0b997ee3be48d87947`  
		Last Modified: Fri, 13 Jun 2025 02:07:51 GMT  
		Size: 17.6 MB (17585962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10cb54f24b436f2e9ae244d4f7ad8d4d57968ee418008f027ea30581d65f6246`  
		Last Modified: Fri, 13 Jun 2025 00:13:14 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:9601e8bc1b00849768c14fe6044913853642441e3e9735dd9882c94946a62fe2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c02d3ef5cd053c5957bec70f4a8c28ab283ebf4a2bc5372947b08dfcc8d5f2e`

```dockerfile
```

-	Layers:
	-	`sha256:9fb42be545f7a062d87207720d7a980e0dac859ea3f6630e4c65ba6816b6297c`  
		Last Modified: Fri, 13 Jun 2025 02:07:38 GMT  
		Size: 30.5 KB (30452 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:35c3b834f6991d8ca48c0fb727e00538a23012ae1c854f988876906aaff64efa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.5 MB (153542694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e02b9699e685722cbc13f8e1a65cafa650145a9a599a5fa1eb750135e38e774`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 17:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 30 May 2025 17:04:15 GMT
ENV DOCKER_VERSION=28.2.2
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 30 May 2025 17:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 30 May 2025 17:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-x86_64'; 			sha256='6777247eb2947c48b46b1fc96602ac17e140fbac84e1043e6384a6c755fc6769'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv6'; 			sha256='1a7731a63ec845b4b4cf2510e68a8f3411386b1e4b5b03916a0d21a697596f03'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv7'; 			sha256='63e64d9aad9916771a947e4b77df6b2a5e70cdfdb412b2f0464806f4d63fabe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-aarch64'; 			sha256='36dfcc81ffff0ec2a76abaa4b66edf01d2db0d7f3fda342a26525eb72e4e9a80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-ppc64le'; 			sha256='4410f045bfc084fef1f0fcea2c3f8e665cad6c5055f57f1089dd009bb9b65151'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-riscv64'; 			sha256='6d551f86c2ab9155882f5a1067223d0c0c80b47669c826af4311c305cc637093'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-s390x'; 			sha256='6012d0bd529312d12937fd153583a90ddb29aec7a7a8cfaac8e7fb7d1ceabf6f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 30 May 2025 17:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 30 May 2025 17:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 17:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 30 May 2025 17:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 30 May 2025 17:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 17:04:15 GMT
CMD ["sh"]
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 30 May 2025 17:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 30 May 2025 17:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 17:04:15 GMT
VOLUME [/var/lib/docker]
# Fri, 30 May 2025 17:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 30 May 2025 17:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 30 May 2025 17:04:15 GMT
CMD []
# Fri, 30 May 2025 17:04:15 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 30 May 2025 17:04:15 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 30 May 2025 17:04:15 GMT
USER rootless
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375cb5234cd1a2b6b8f1aba00c28fc5d45ba0ecc0d3c8f130d5cdb5138ba6c09`  
		Last Modified: Fri, 13 Jun 2025 00:09:12 GMT  
		Size: 8.2 MB (8229005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ba114b122014764181bf833228533908f5eedbccce11b62f71d746ab1616ccc`  
		Last Modified: Fri, 13 Jun 2025 00:09:12 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5090356630719947eb3cfc865b4d6d8f4971f5e40c640070edd88a16ab0c486f`  
		Last Modified: Fri, 13 Jun 2025 00:09:13 GMT  
		Size: 18.9 MB (18902609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd89b3ff82b93c434d43d799f7f56e86b96409535e06f30c6bbc54456e99752d`  
		Last Modified: Fri, 13 Jun 2025 00:09:14 GMT  
		Size: 19.5 MB (19469847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb8a2de00a4f86825ec25a2f3ac1553ace626f97f529f17cda507233ec8f1a9a`  
		Last Modified: Fri, 13 Jun 2025 00:09:14 GMT  
		Size: 19.3 MB (19347260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ced3983ecfb78d04b5aefc0cf90f4a0b3ccd62ec5610841b0f7860259defda`  
		Last Modified: Fri, 13 Jun 2025 00:09:13 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3673e39b233f3bfe295c08f11dda44b40d801a0bb4f299fe81e1ec50851575`  
		Last Modified: Fri, 13 Jun 2025 00:09:13 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b219e20a46cafa0737e015b21a2525d3bb013d26dc4af6849c8f3586a8b10c5f`  
		Last Modified: Fri, 13 Jun 2025 00:09:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c6e05695096db67c5e6426307e8a652c5311da73d994e47d9580e886b837a10`  
		Last Modified: Fri, 13 Jun 2025 04:27:25 GMT  
		Size: 7.1 MB (7141507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891d71d9754311d78a8a473d578e3825acd68ce42cd0dbc623f6357a4e17c72b`  
		Last Modified: Fri, 13 Jun 2025 04:27:25 GMT  
		Size: 99.6 KB (99645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5d9a3e9b7f7718caa1aba176d0c009906cfdbf0beaabb63840d5743b89cc7f2`  
		Last Modified: Fri, 13 Jun 2025 04:27:26 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d489b833d40920f79c54667b28c6b5c28475bbdb198a31284fb082206828119a`  
		Last Modified: Fri, 13 Jun 2025 04:27:32 GMT  
		Size: 57.2 MB (57168194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e7d0e57cac200e9cb81bab37725356fb62116b7b3fb40855e245e59124702f2`  
		Last Modified: Fri, 13 Jun 2025 04:27:27 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc40c4cf8ec0a96212d48ae432d6342b219db9566141690970349c4e6140886`  
		Last Modified: Fri, 13 Jun 2025 04:27:27 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c1c853189a4f7b6c93d47fd98d9be0a95acfdbc8c0f8df18df4a175a65ce3b`  
		Last Modified: Fri, 13 Jun 2025 07:11:57 GMT  
		Size: 1.0 MB (1023005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe779df0e0efd82b4a777858dfbd3496808597c320e55ab766b45677649442a`  
		Last Modified: Fri, 13 Jun 2025 07:11:56 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a244027a6953dc0bf2fd363382ff7224e9f2c0bae6332d09c4e5e68511a3b7fb`  
		Last Modified: Fri, 13 Jun 2025 07:11:57 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40237444de5d3255f0f82947d5aa58daa8391b4d2fe9b8b6565e99969a09a8d6`  
		Last Modified: Fri, 13 Jun 2025 07:12:01 GMT  
		Size: 18.0 MB (18016184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b92f2d121a50edd33cc911db99177a3a185a452e7ec47f4751ead8e59a3bc3`  
		Last Modified: Fri, 13 Jun 2025 07:11:57 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:a9e0325277463e83ad33ae4cc4cf06e197918a3c651585f3a614fe7ddb944126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95a5b11d7826e81670044d1358d7f259365282306c1b8f9de1dbe8387517643c`

```dockerfile
```

-	Layers:
	-	`sha256:82a2387a357a58b3faf425641fd79df168694c9fdde196be68fb5632c4d7705e`  
		Last Modified: Fri, 13 Jun 2025 08:07:43 GMT  
		Size: 30.6 KB (30621 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28-windowsservercore`

```console
$ docker pull docker@sha256:c244e5c2c3cc3b906baab6f383a9e91fc102f866e209e7a40dee80b3f50687f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4349; amd64
	-	windows version 10.0.20348.3807; amd64

### `docker:28-windowsservercore` - windows version 10.0.26100.4349; amd64

```console
$ docker pull docker@sha256:87b6c37c78ebd3b4dffee917bf6ba9e8e61722d7cc42313c63bf2204cf297f29
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3541382992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebb204680d5c75607c3a852fb2ef3ed327b9ccc1566c1d6a059cb0259d1a3a22`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 07 Jun 2025 15:42:01 GMT
RUN Install update 10.0.26100.4349
# Thu, 12 Jun 2025 22:41:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Jun 2025 22:41:52 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 12 Jun 2025 22:41:53 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 12 Jun 2025 22:41:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.2.2.zip
# Thu, 12 Jun 2025 22:42:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 12 Jun 2025 22:42:05 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 12 Jun 2025 22:42:06 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Thu, 12 Jun 2025 22:42:06 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Thu, 12 Jun 2025 22:42:16 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 12 Jun 2025 22:42:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Thu, 12 Jun 2025 22:42:17 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-windows-x86_64.exe
# Thu, 12 Jun 2025 22:42:18 GMT
ENV DOCKER_COMPOSE_SHA256=132fb31ef7dc81a82d7b1429adf3fd76cc0a7128059af3a172945445a50f2801
# Thu, 12 Jun 2025 22:42:28 GMT
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
	-	`sha256:7505764e5850853ff3205e21d0c6c05dd9890fed17012225b1f33d9e79ef8f7b`  
		Last Modified: Thu, 12 Jun 2025 22:46:16 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75201e0022107e322d1abb29cdcd607860e0814d97801313713016a804c7ea29`  
		Last Modified: Thu, 12 Jun 2025 22:46:17 GMT  
		Size: 384.3 KB (384281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad1332a299d19362bbb194725e3d76167ba59837dbdb186edc8c88eb4fc584fc`  
		Last Modified: Thu, 12 Jun 2025 22:46:16 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee1c450bb560eb20733ee6f9c9eab001dcdca87a8a976d64320a006b6a8626e`  
		Last Modified: Thu, 12 Jun 2025 22:46:16 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:292280c51cf870fb93a78962a22141e9734918633eac0270479904b4e7fde431`  
		Last Modified: Thu, 12 Jun 2025 22:46:19 GMT  
		Size: 20.5 MB (20474220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce832f815f971edd09a31c7ae7e5e8f1511fd9100e257f6c46649f33661d080d`  
		Last Modified: Thu, 12 Jun 2025 22:46:18 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc0188db691ee242410ed95505f0c2b6bf11c2034274be14cc637917ce9576aa`  
		Last Modified: Thu, 12 Jun 2025 22:46:18 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6d4dfab47701ffe430c0efb0d9f5640976ec9b76c70fa9adf6d9a9e37a7605a`  
		Last Modified: Thu, 12 Jun 2025 22:46:18 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c2ad7bc7d5b79fafe6d4eda10030323f4f485027233019a33343bd50a265a59`  
		Last Modified: Thu, 12 Jun 2025 22:46:21 GMT  
		Size: 22.3 MB (22283596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9538a3dff1be138d1137eb9fc139dbda8255bde275ae8670c13253a3d1033575`  
		Last Modified: Thu, 12 Jun 2025 22:46:19 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfe10fbb6bc6101cc1d7a69d3deb8126160b5db04361e52404e83b438b2fa8b3`  
		Last Modified: Thu, 12 Jun 2025 22:46:20 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2dfee3af3890e8fd03beb55f71a85b48276c6bff5474ae597f001adbd26f779`  
		Last Modified: Thu, 12 Jun 2025 22:46:20 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:846e5ade10ef88ce7e3178a17fc7662922cb37bf8403257413f21ca0869ab29c`  
		Last Modified: Thu, 12 Jun 2025 22:46:23 GMT  
		Size: 22.1 MB (22054925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28-windowsservercore` - windows version 10.0.20348.3807; amd64

```console
$ docker pull docker@sha256:53498ccee3c78a70215add9ae3ef737168375a5c54328c792752c0e5fde4eabf
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2345354530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:485c313a4ef331fdb3d3de62a8679e0f3981409d24dfa2b371f0d9efb2c3ff07`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Jun 2025 01:01:39 GMT
RUN Install update 10.0.20348.3807
# Thu, 12 Jun 2025 22:40:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Jun 2025 22:40:42 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 12 Jun 2025 22:40:43 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 12 Jun 2025 22:40:44 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.2.2.zip
# Thu, 12 Jun 2025 22:40:53 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 12 Jun 2025 22:40:54 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 12 Jun 2025 22:40:55 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Thu, 12 Jun 2025 22:40:55 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Thu, 12 Jun 2025 22:41:04 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 12 Jun 2025 22:41:05 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Thu, 12 Jun 2025 22:41:05 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-windows-x86_64.exe
# Thu, 12 Jun 2025 22:41:06 GMT
ENV DOCKER_COMPOSE_SHA256=132fb31ef7dc81a82d7b1429adf3fd76cc0a7128059af3a172945445a50f2801
# Thu, 12 Jun 2025 22:41:14 GMT
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
	-	`sha256:e3ce7730719b3563f78c11a86c6e7ca9e7ecab63539d89528367a963b46668ee`  
		Last Modified: Thu, 12 Jun 2025 22:42:44 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa44face37189a26dfbb23b8d5da4e8ec912b0e7403fa7e57fe746ede8ca163`  
		Last Modified: Thu, 12 Jun 2025 22:42:47 GMT  
		Size: 351.9 KB (351892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b288554d751322bcbba469e2992e7ed3d7addecc28b36b87bb0ac57981ad64a`  
		Last Modified: Thu, 12 Jun 2025 22:42:46 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08b3bdb645c2944656eeb7ae7bf819f0cd63f9c83b2677298c9c21d710111eec`  
		Last Modified: Thu, 12 Jun 2025 22:42:47 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b59891c80d4b303cd1655e3255818d7a3cb47a43fe98781999d05abb780b0ed`  
		Last Modified: Thu, 12 Jun 2025 22:42:50 GMT  
		Size: 20.5 MB (20450522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1af8f19e40999102aa31f1f4406c7f15eeb18843036b70938f492dee65f6943`  
		Last Modified: Thu, 12 Jun 2025 22:42:49 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f07268cae3a2cdfcdce7a98218844be1e3ede2baa06062288c10119e5414b06`  
		Last Modified: Thu, 12 Jun 2025 22:42:50 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bea31ae088d4884385e4c9bf2ff15ca1ed5f8581b5d17cba15b96224a1533af`  
		Last Modified: Thu, 12 Jun 2025 22:42:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:428d152391bf0297baa1308e6b7a51fa8dfb41c8f2dd3071d1d21fa3e4f42d41`  
		Last Modified: Thu, 12 Jun 2025 22:42:54 GMT  
		Size: 22.3 MB (22261181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b28b4c745fe11d31b3e00254bc2bc9aec2a58ab17157f558834f43f95a248ea`  
		Last Modified: Thu, 12 Jun 2025 22:42:54 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aa41358ec814cca1a580968a15e80fadcab82f43e7c6b59aea4861acb3c83ad`  
		Last Modified: Thu, 12 Jun 2025 22:42:55 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10bc742c50fda0894e2260bf3f7eb9919c098581d407b6cf2a42e3a41062305b`  
		Last Modified: Thu, 12 Jun 2025 22:42:56 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f06dfd207ec226196bd2af1228c11187c3803b22f4c3f4ac01c21d67d7207e67`  
		Last Modified: Thu, 12 Jun 2025 22:42:58 GMT  
		Size: 22.0 MB (22027759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:f640af5c3e1bd4c0cb40cf589e9f2f5903fcff110a95226d0c3f09140b3962eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3807; amd64

### `docker:28-windowsservercore-ltsc2022` - windows version 10.0.20348.3807; amd64

```console
$ docker pull docker@sha256:53498ccee3c78a70215add9ae3ef737168375a5c54328c792752c0e5fde4eabf
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2345354530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:485c313a4ef331fdb3d3de62a8679e0f3981409d24dfa2b371f0d9efb2c3ff07`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Jun 2025 01:01:39 GMT
RUN Install update 10.0.20348.3807
# Thu, 12 Jun 2025 22:40:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Jun 2025 22:40:42 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 12 Jun 2025 22:40:43 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 12 Jun 2025 22:40:44 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.2.2.zip
# Thu, 12 Jun 2025 22:40:53 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 12 Jun 2025 22:40:54 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 12 Jun 2025 22:40:55 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Thu, 12 Jun 2025 22:40:55 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Thu, 12 Jun 2025 22:41:04 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 12 Jun 2025 22:41:05 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Thu, 12 Jun 2025 22:41:05 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-windows-x86_64.exe
# Thu, 12 Jun 2025 22:41:06 GMT
ENV DOCKER_COMPOSE_SHA256=132fb31ef7dc81a82d7b1429adf3fd76cc0a7128059af3a172945445a50f2801
# Thu, 12 Jun 2025 22:41:14 GMT
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
	-	`sha256:e3ce7730719b3563f78c11a86c6e7ca9e7ecab63539d89528367a963b46668ee`  
		Last Modified: Thu, 12 Jun 2025 22:42:44 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa44face37189a26dfbb23b8d5da4e8ec912b0e7403fa7e57fe746ede8ca163`  
		Last Modified: Thu, 12 Jun 2025 22:42:47 GMT  
		Size: 351.9 KB (351892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b288554d751322bcbba469e2992e7ed3d7addecc28b36b87bb0ac57981ad64a`  
		Last Modified: Thu, 12 Jun 2025 22:42:46 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08b3bdb645c2944656eeb7ae7bf819f0cd63f9c83b2677298c9c21d710111eec`  
		Last Modified: Thu, 12 Jun 2025 22:42:47 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b59891c80d4b303cd1655e3255818d7a3cb47a43fe98781999d05abb780b0ed`  
		Last Modified: Thu, 12 Jun 2025 22:42:50 GMT  
		Size: 20.5 MB (20450522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1af8f19e40999102aa31f1f4406c7f15eeb18843036b70938f492dee65f6943`  
		Last Modified: Thu, 12 Jun 2025 22:42:49 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f07268cae3a2cdfcdce7a98218844be1e3ede2baa06062288c10119e5414b06`  
		Last Modified: Thu, 12 Jun 2025 22:42:50 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bea31ae088d4884385e4c9bf2ff15ca1ed5f8581b5d17cba15b96224a1533af`  
		Last Modified: Thu, 12 Jun 2025 22:42:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:428d152391bf0297baa1308e6b7a51fa8dfb41c8f2dd3071d1d21fa3e4f42d41`  
		Last Modified: Thu, 12 Jun 2025 22:42:54 GMT  
		Size: 22.3 MB (22261181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b28b4c745fe11d31b3e00254bc2bc9aec2a58ab17157f558834f43f95a248ea`  
		Last Modified: Thu, 12 Jun 2025 22:42:54 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aa41358ec814cca1a580968a15e80fadcab82f43e7c6b59aea4861acb3c83ad`  
		Last Modified: Thu, 12 Jun 2025 22:42:55 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10bc742c50fda0894e2260bf3f7eb9919c098581d407b6cf2a42e3a41062305b`  
		Last Modified: Thu, 12 Jun 2025 22:42:56 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f06dfd207ec226196bd2af1228c11187c3803b22f4c3f4ac01c21d67d7207e67`  
		Last Modified: Thu, 12 Jun 2025 22:42:58 GMT  
		Size: 22.0 MB (22027759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:a9266b0f45c2b149896e562c8414e4edc2f32d5f40c73cc8e69a23ce4a967d7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4349; amd64

### `docker:28-windowsservercore-ltsc2025` - windows version 10.0.26100.4349; amd64

```console
$ docker pull docker@sha256:87b6c37c78ebd3b4dffee917bf6ba9e8e61722d7cc42313c63bf2204cf297f29
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3541382992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebb204680d5c75607c3a852fb2ef3ed327b9ccc1566c1d6a059cb0259d1a3a22`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 07 Jun 2025 15:42:01 GMT
RUN Install update 10.0.26100.4349
# Thu, 12 Jun 2025 22:41:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Jun 2025 22:41:52 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 12 Jun 2025 22:41:53 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 12 Jun 2025 22:41:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.2.2.zip
# Thu, 12 Jun 2025 22:42:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 12 Jun 2025 22:42:05 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 12 Jun 2025 22:42:06 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Thu, 12 Jun 2025 22:42:06 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Thu, 12 Jun 2025 22:42:16 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 12 Jun 2025 22:42:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Thu, 12 Jun 2025 22:42:17 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-windows-x86_64.exe
# Thu, 12 Jun 2025 22:42:18 GMT
ENV DOCKER_COMPOSE_SHA256=132fb31ef7dc81a82d7b1429adf3fd76cc0a7128059af3a172945445a50f2801
# Thu, 12 Jun 2025 22:42:28 GMT
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
	-	`sha256:7505764e5850853ff3205e21d0c6c05dd9890fed17012225b1f33d9e79ef8f7b`  
		Last Modified: Thu, 12 Jun 2025 22:46:16 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75201e0022107e322d1abb29cdcd607860e0814d97801313713016a804c7ea29`  
		Last Modified: Thu, 12 Jun 2025 22:46:17 GMT  
		Size: 384.3 KB (384281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad1332a299d19362bbb194725e3d76167ba59837dbdb186edc8c88eb4fc584fc`  
		Last Modified: Thu, 12 Jun 2025 22:46:16 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee1c450bb560eb20733ee6f9c9eab001dcdca87a8a976d64320a006b6a8626e`  
		Last Modified: Thu, 12 Jun 2025 22:46:16 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:292280c51cf870fb93a78962a22141e9734918633eac0270479904b4e7fde431`  
		Last Modified: Thu, 12 Jun 2025 22:46:19 GMT  
		Size: 20.5 MB (20474220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce832f815f971edd09a31c7ae7e5e8f1511fd9100e257f6c46649f33661d080d`  
		Last Modified: Thu, 12 Jun 2025 22:46:18 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc0188db691ee242410ed95505f0c2b6bf11c2034274be14cc637917ce9576aa`  
		Last Modified: Thu, 12 Jun 2025 22:46:18 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6d4dfab47701ffe430c0efb0d9f5640976ec9b76c70fa9adf6d9a9e37a7605a`  
		Last Modified: Thu, 12 Jun 2025 22:46:18 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c2ad7bc7d5b79fafe6d4eda10030323f4f485027233019a33343bd50a265a59`  
		Last Modified: Thu, 12 Jun 2025 22:46:21 GMT  
		Size: 22.3 MB (22283596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9538a3dff1be138d1137eb9fc139dbda8255bde275ae8670c13253a3d1033575`  
		Last Modified: Thu, 12 Jun 2025 22:46:19 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfe10fbb6bc6101cc1d7a69d3deb8126160b5db04361e52404e83b438b2fa8b3`  
		Last Modified: Thu, 12 Jun 2025 22:46:20 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2dfee3af3890e8fd03beb55f71a85b48276c6bff5474ae597f001adbd26f779`  
		Last Modified: Thu, 12 Jun 2025 22:46:20 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:846e5ade10ef88ce7e3178a17fc7662922cb37bf8403257413f21ca0869ab29c`  
		Last Modified: Thu, 12 Jun 2025 22:46:23 GMT  
		Size: 22.1 MB (22054925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.2`

```console
$ docker pull docker@sha256:ff052514f359111edd920b54581e7aca65629458607f9fbdbf82d7eefbe0602b
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

### `docker:28.2` - linux; amd64

```console
$ docker pull docker@sha256:8e32fae437051e392dc31f1bca659a14a6b8f341fa6dd131a9def0a9f315203c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.7 MB (143689092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:896cfe4b7aa87684cdbe7274a5a4efafa80c561662a935bd3a0432e2fcbaf46d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-x86_64'; 			sha256='6777247eb2947c48b46b1fc96602ac17e140fbac84e1043e6384a6c755fc6769'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv6'; 			sha256='1a7731a63ec845b4b4cf2510e68a8f3411386b1e4b5b03916a0d21a697596f03'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv7'; 			sha256='63e64d9aad9916771a947e4b77df6b2a5e70cdfdb412b2f0464806f4d63fabe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-aarch64'; 			sha256='36dfcc81ffff0ec2a76abaa4b66edf01d2db0d7f3fda342a26525eb72e4e9a80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-ppc64le'; 			sha256='4410f045bfc084fef1f0fcea2c3f8e665cad6c5055f57f1089dd009bb9b65151'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-riscv64'; 			sha256='6d551f86c2ab9155882f5a1067223d0c0c80b47669c826af4311c305cc637093'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-s390x'; 			sha256='6012d0bd529312d12937fd153583a90ddb29aec7a7a8cfaac8e7fb7d1ceabf6f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 05 Jun 2025 17:36:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
CMD ["sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
VOLUME [/var/lib/docker]
# Thu, 05 Jun 2025 17:36:11 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
CMD []
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f32e8d6f68009e4f81cdd4d2b7e6465c3cdc96e6addc90132dfdb88d08941a20`  
		Last Modified: Thu, 12 Jun 2025 22:36:53 GMT  
		Size: 8.2 MB (8207474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ac40e43aadc31b56fc943a7df1de7e7f5f06348ca89a108384ba3e9a805a89`  
		Last Modified: Thu, 12 Jun 2025 22:36:53 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3870806677ebd2c8113c069ad6c6f219c456246069bd2688c9cffe6d1736938`  
		Last Modified: Thu, 12 Jun 2025 22:36:55 GMT  
		Size: 20.1 MB (20083028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86f14a0f3d88cab9e631bd4dcf8f9a164306875132f95135fff3358e3a2a8d2`  
		Last Modified: Thu, 12 Jun 2025 22:36:56 GMT  
		Size: 21.3 MB (21290186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da67c6f5f9a3f4626ce69c1328bdacf4c370d20479d084f6415437dea4481db4`  
		Last Modified: Thu, 12 Jun 2025 22:36:56 GMT  
		Size: 21.1 MB (21100670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b94aef2e962e8f653820f39c328e9f31ab7a6e903d929b45f9fb82324f7633`  
		Last Modified: Thu, 12 Jun 2025 22:36:55 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a98583f050f0d3b9242c387626407b4c0affec19be6fafeb1c7135bd7303d86`  
		Last Modified: Thu, 12 Jun 2025 22:36:56 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a115214fbd18e2a1acb4699bd0d7f72d42bf84a1f4cd3d4b1cdae8248a2167fa`  
		Last Modified: Thu, 12 Jun 2025 22:36:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:212150b9078af2b8495b33e957823f54b179f41a22f2702f6fec1560c9d3f6f2`  
		Last Modified: Thu, 12 Jun 2025 23:07:54 GMT  
		Size: 6.9 MB (6905618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9212e721c88d6da1ed4b1e289f523f35a01e01885d1131cd34feceb518227abf`  
		Last Modified: Thu, 12 Jun 2025 23:07:53 GMT  
		Size: 90.5 KB (90494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b0253e449f82e84618065f5b74284cb93f7cc52668795f3590d41585c32012`  
		Last Modified: Thu, 12 Jun 2025 23:07:51 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811b046d83c5b8a6340f19f8d6acd494b2b028f5c1bf969e58cf6f0e350c7cea`  
		Last Modified: Thu, 12 Jun 2025 23:07:58 GMT  
		Size: 62.2 MB (62206627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68771551084500ee9ac3a4b32aa56d78b3d007c1986578b481436becbe8ae1a1`  
		Last Modified: Thu, 12 Jun 2025 23:07:51 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cae381f867a74a59e0d18562bd189fcc3560935254e57ceb2e247145c467a8b`  
		Last Modified: Thu, 12 Jun 2025 23:07:52 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2` - unknown; unknown

```console
$ docker pull docker@sha256:4c5431982a6f26acafc9a647e2a915e12fd2cb54c0d9fa6f5bed94ca07e186b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a1e46faf2561239606e7d796aac2f70a1bc3754ba1ff7200c43154e973515c8`

```dockerfile
```

-	Layers:
	-	`sha256:d5158885bee456f124624bc8808ba3f4ea82fc7ca56f260044b4d92a684498b1`  
		Last Modified: Fri, 13 Jun 2025 02:07:20 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.2` - linux; arm variant v6

```console
$ docker pull docker@sha256:d692f151518fae2760b09152001cfba45f8bc770e1906d190d6eb2e3142b1a76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134722094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44d698360caa93e31e5563c2c622bbbeb75bd82d597a599776298366deb6aa32`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-x86_64'; 			sha256='6777247eb2947c48b46b1fc96602ac17e140fbac84e1043e6384a6c755fc6769'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv6'; 			sha256='1a7731a63ec845b4b4cf2510e68a8f3411386b1e4b5b03916a0d21a697596f03'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv7'; 			sha256='63e64d9aad9916771a947e4b77df6b2a5e70cdfdb412b2f0464806f4d63fabe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-aarch64'; 			sha256='36dfcc81ffff0ec2a76abaa4b66edf01d2db0d7f3fda342a26525eb72e4e9a80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-ppc64le'; 			sha256='4410f045bfc084fef1f0fcea2c3f8e665cad6c5055f57f1089dd009bb9b65151'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-riscv64'; 			sha256='6d551f86c2ab9155882f5a1067223d0c0c80b47669c826af4311c305cc637093'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-s390x'; 			sha256='6012d0bd529312d12937fd153583a90ddb29aec7a7a8cfaac8e7fb7d1ceabf6f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 05 Jun 2025 17:36:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
CMD ["sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
VOLUME [/var/lib/docker]
# Thu, 05 Jun 2025 17:36:11 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
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
	-	`sha256:3156c3bcd5598f721d5e807804df7256e282bd2897ea9f9f029b3cd93a5ff79b`  
		Last Modified: Thu, 05 Jun 2025 22:44:12 GMT  
		Size: 18.1 MB (18101909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:225abe8edcfa38ed05c3678afaa3fc7019381a300f823c874d6fdfd2a372c345`  
		Last Modified: Thu, 05 Jun 2025 22:44:12 GMT  
		Size: 19.9 MB (19943271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aaa4a492c5a8c6019873f7f10f4583b9134c81a74df09c55d664e88521c254c`  
		Last Modified: Thu, 12 Jun 2025 22:36:39 GMT  
		Size: 19.8 MB (19835400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d441ddcc7f77e2457e59e55a8a824b3b189eaa5a13fdaf65a914da194d6919b`  
		Last Modified: Thu, 12 Jun 2025 22:36:37 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c28d4afadc6fad8c6238b24d9a8dad8f8e7a8deb80839c1d3459890592b523f2`  
		Last Modified: Thu, 12 Jun 2025 22:36:38 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ebbefe72ea0510e4b225079670e073211f0b85e0fc4be94f42ca4ea57d54248`  
		Last Modified: Thu, 12 Jun 2025 22:36:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8241b18dc7eb679233e3250bbfb077dcd4f8778550fe3188d80dd91b7838a9bd`  
		Last Modified: Thu, 12 Jun 2025 22:54:58 GMT  
		Size: 7.2 MB (7230354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3cf946673d9726b4c5b57734c7dbf2e2e811f1b40e437ce7cc7bf5533df26a`  
		Last Modified: Thu, 12 Jun 2025 22:54:57 GMT  
		Size: 90.1 KB (90058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d08132e8b60b557ae762a779e816c58c6c366efd53ded71c9275533c8ec8f2d`  
		Last Modified: Thu, 12 Jun 2025 22:54:57 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d611e6743d4f047d30c66012bbac54fc821dc2ffefbbe8277a53e70060da2356`  
		Last Modified: Thu, 12 Jun 2025 22:55:00 GMT  
		Size: 57.9 MB (57897340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a783e6fb91bba730335ac30fbd49b93258f2e4d9d4c2a73dbe5c7663e5f497`  
		Last Modified: Thu, 12 Jun 2025 22:54:57 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b45b886f9c1b0ecbf83201757d3e791047d9cd0cbbdfc865a112256becf21ce4`  
		Last Modified: Thu, 12 Jun 2025 22:54:58 GMT  
		Size: 3.3 KB (3304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2` - unknown; unknown

```console
$ docker pull docker@sha256:d1a670e4e107e2e31f275813f1751ac249dec91fa3cfc6cc949e581bdb0c364e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb88dd0bcd267d48fad2fe5722c0bc382d70b8aa328b8a911562dc8081e3809d`

```dockerfile
```

-	Layers:
	-	`sha256:c75371d2b5d03d6fe0926a467c9d353d590b6db0765b2bc492cb0184dfe50817`  
		Last Modified: Thu, 12 Jun 2025 23:07:42 GMT  
		Size: 34.8 KB (34765 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.2` - linux; arm variant v7

```console
$ docker pull docker@sha256:66277612b6b4d8230b45b06074b5716e61c90fee840cf8b7b4da8208329fe9d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.0 MB (133027832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55fe29bbf4d101c05a3d55a85a71baf6c7ae07a62cc6865b2fc5b8902a5978a6`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-x86_64'; 			sha256='6777247eb2947c48b46b1fc96602ac17e140fbac84e1043e6384a6c755fc6769'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv6'; 			sha256='1a7731a63ec845b4b4cf2510e68a8f3411386b1e4b5b03916a0d21a697596f03'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv7'; 			sha256='63e64d9aad9916771a947e4b77df6b2a5e70cdfdb412b2f0464806f4d63fabe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-aarch64'; 			sha256='36dfcc81ffff0ec2a76abaa4b66edf01d2db0d7f3fda342a26525eb72e4e9a80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-ppc64le'; 			sha256='4410f045bfc084fef1f0fcea2c3f8e665cad6c5055f57f1089dd009bb9b65151'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-riscv64'; 			sha256='6d551f86c2ab9155882f5a1067223d0c0c80b47669c826af4311c305cc637093'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-s390x'; 			sha256='6012d0bd529312d12937fd153583a90ddb29aec7a7a8cfaac8e7fb7d1ceabf6f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 05 Jun 2025 17:36:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
CMD ["sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
VOLUME [/var/lib/docker]
# Thu, 05 Jun 2025 17:36:11 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
CMD []
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b30f7212c67694cf480811a55ca551c13acaf23308660855c528140f72c862`  
		Last Modified: Fri, 13 Jun 2025 01:20:06 GMT  
		Size: 7.4 MB (7440617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3fca8ac4e435f25c24efea81db3a20417fad9d7c421bee5ce9e3b58996c8efa`  
		Last Modified: Fri, 13 Jun 2025 01:20:05 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68a306e9551e1b17a6ecb71be8147d67ef4f891736c4e69faee945e235107fc`  
		Last Modified: Fri, 13 Jun 2025 01:20:06 GMT  
		Size: 18.1 MB (18089377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44e8dff8b0583db9cb4fc33b75dec6c3d09dd8ce3a76c2a78fd8af411bce92c`  
		Last Modified: Fri, 13 Jun 2025 01:20:08 GMT  
		Size: 19.9 MB (19927230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c665168123ed7a9acc312ff431c35318ee6393642e3e2a8bb7fa2845208b64aa`  
		Last Modified: Fri, 13 Jun 2025 01:20:08 GMT  
		Size: 19.8 MB (19821284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f454bde5fc9b6055cf7fe14c89d2a03739341ccdde89409892b34630a79576`  
		Last Modified: Fri, 13 Jun 2025 01:26:31 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3159ba7c72c13cd717ca59937ae54ce16c3ef91f409e6ff1eb4ab88fc1db06c0`  
		Last Modified: Fri, 13 Jun 2025 01:26:33 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ef5f44369f56ae39826aaf9f89b54c9bf2d4d09a86c4eaf7af04c279812997`  
		Last Modified: Fri, 13 Jun 2025 01:26:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7236561f33fb7c50ca5d7c37b075afc53fe8e4088c95319dcde0bb8ad917eb0`  
		Last Modified: Fri, 13 Jun 2025 06:24:34 GMT  
		Size: 6.5 MB (6538120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98752e61e2dd86e562ed8c9de46d0e71b38f35fe7be163828be059624970c9e`  
		Last Modified: Fri, 13 Jun 2025 06:24:35 GMT  
		Size: 86.5 KB (86488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c1e6adc4b8f7742b913355688fb6e8dd3671bd9c49551a76f2dad8f0bfcf827`  
		Last Modified: Fri, 13 Jun 2025 06:24:35 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7760efd1d6901a24ed3199cf41b66c116f64c11736dcecc92c75040a0f68dea9`  
		Last Modified: Fri, 13 Jun 2025 06:24:39 GMT  
		Size: 57.9 MB (57897375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb6cd2d2e0725f775e9f508d900bb8bac548036c111ea8957a933fc7002b93e`  
		Last Modified: Fri, 13 Jun 2025 06:24:36 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcd8d4be9dc74189aefe21d876aec06706ad1fa1e7597dd49f2c2fc862477c51`  
		Last Modified: Fri, 13 Jun 2025 06:24:36 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2` - unknown; unknown

```console
$ docker pull docker@sha256:9c4cb9730947a3df8f10cb2052f42e9556fa8a3d55b8d9eb9df923d7467c4a6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4fa8b980b9e0ff354efd1a786e8ee1816d49966e8cb7f6c93a8a7182923f7fd`

```dockerfile
```

-	Layers:
	-	`sha256:4bc11f3d388f7184ad2e3f2d7090c73f569bc734a2691321b72cdcb0e3735d28`  
		Last Modified: Fri, 13 Jun 2025 08:07:23 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.2` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:b8d1c58eea384111a2c6646a55d6c57e11ce3527c44b26b17ba91e00f82530c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.5 MB (134502165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f7a08861e83333223ac02d5357e4d77380c819b320b98b1811d33973cd4cd5e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-x86_64'; 			sha256='6777247eb2947c48b46b1fc96602ac17e140fbac84e1043e6384a6c755fc6769'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv6'; 			sha256='1a7731a63ec845b4b4cf2510e68a8f3411386b1e4b5b03916a0d21a697596f03'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv7'; 			sha256='63e64d9aad9916771a947e4b77df6b2a5e70cdfdb412b2f0464806f4d63fabe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-aarch64'; 			sha256='36dfcc81ffff0ec2a76abaa4b66edf01d2db0d7f3fda342a26525eb72e4e9a80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-ppc64le'; 			sha256='4410f045bfc084fef1f0fcea2c3f8e665cad6c5055f57f1089dd009bb9b65151'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-riscv64'; 			sha256='6d551f86c2ab9155882f5a1067223d0c0c80b47669c826af4311c305cc637093'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-s390x'; 			sha256='6012d0bd529312d12937fd153583a90ddb29aec7a7a8cfaac8e7fb7d1ceabf6f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 05 Jun 2025 17:36:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
CMD ["sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
VOLUME [/var/lib/docker]
# Thu, 05 Jun 2025 17:36:11 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
CMD []
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375cb5234cd1a2b6b8f1aba00c28fc5d45ba0ecc0d3c8f130d5cdb5138ba6c09`  
		Last Modified: Fri, 13 Jun 2025 00:09:12 GMT  
		Size: 8.2 MB (8229005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ba114b122014764181bf833228533908f5eedbccce11b62f71d746ab1616ccc`  
		Last Modified: Fri, 13 Jun 2025 00:09:12 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5090356630719947eb3cfc865b4d6d8f4971f5e40c640070edd88a16ab0c486f`  
		Last Modified: Fri, 13 Jun 2025 00:09:13 GMT  
		Size: 18.9 MB (18902609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd89b3ff82b93c434d43d799f7f56e86b96409535e06f30c6bbc54456e99752d`  
		Last Modified: Fri, 13 Jun 2025 00:09:14 GMT  
		Size: 19.5 MB (19469847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb8a2de00a4f86825ec25a2f3ac1553ace626f97f529f17cda507233ec8f1a9a`  
		Last Modified: Fri, 13 Jun 2025 00:09:14 GMT  
		Size: 19.3 MB (19347260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ced3983ecfb78d04b5aefc0cf90f4a0b3ccd62ec5610841b0f7860259defda`  
		Last Modified: Fri, 13 Jun 2025 00:09:13 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3673e39b233f3bfe295c08f11dda44b40d801a0bb4f299fe81e1ec50851575`  
		Last Modified: Fri, 13 Jun 2025 00:09:13 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b219e20a46cafa0737e015b21a2525d3bb013d26dc4af6849c8f3586a8b10c5f`  
		Last Modified: Fri, 13 Jun 2025 00:09:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c6e05695096db67c5e6426307e8a652c5311da73d994e47d9580e886b837a10`  
		Last Modified: Fri, 13 Jun 2025 04:27:25 GMT  
		Size: 7.1 MB (7141507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891d71d9754311d78a8a473d578e3825acd68ce42cd0dbc623f6357a4e17c72b`  
		Last Modified: Fri, 13 Jun 2025 04:27:25 GMT  
		Size: 99.6 KB (99645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5d9a3e9b7f7718caa1aba176d0c009906cfdbf0beaabb63840d5743b89cc7f2`  
		Last Modified: Fri, 13 Jun 2025 04:27:26 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d489b833d40920f79c54667b28c6b5c28475bbdb198a31284fb082206828119a`  
		Last Modified: Fri, 13 Jun 2025 04:27:32 GMT  
		Size: 57.2 MB (57168194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e7d0e57cac200e9cb81bab37725356fb62116b7b3fb40855e245e59124702f2`  
		Last Modified: Fri, 13 Jun 2025 04:27:27 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc40c4cf8ec0a96212d48ae432d6342b219db9566141690970349c4e6140886`  
		Last Modified: Fri, 13 Jun 2025 04:27:27 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2` - unknown; unknown

```console
$ docker pull docker@sha256:e64e322c1cc45566807e6054fb529a1b90018a74d5599c9e524013622d5fd800
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30148cdfe5f84f758ae82d1f85d34d65c6e91c5167340993eaa3d924e06041f5`

```dockerfile
```

-	Layers:
	-	`sha256:a0dd369778c470b4b56994e10a017cc701a049c277738705f244ac7e5856bdd4`  
		Last Modified: Fri, 13 Jun 2025 05:07:36 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.2-cli`

```console
$ docker pull docker@sha256:5d3725f5d2f52aafe8a2c49668a43eb7c681a5535a206ba28eccfd8a3013de86
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

### `docker:28.2-cli` - linux; amd64

```console
$ docker pull docker@sha256:b65ad6989d6333212ce011be9684e2d8ae545ec1972b56588c7aff01dd3520d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74480359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c47dbf8612e5f69d7a6b634668d1fc578e0eca340ae1f8a00812e89d72e021a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 12 Jun 2025 11:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-x86_64'; 			sha256='6777247eb2947c48b46b1fc96602ac17e140fbac84e1043e6384a6c755fc6769'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv6'; 			sha256='1a7731a63ec845b4b4cf2510e68a8f3411386b1e4b5b03916a0d21a697596f03'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv7'; 			sha256='63e64d9aad9916771a947e4b77df6b2a5e70cdfdb412b2f0464806f4d63fabe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-aarch64'; 			sha256='36dfcc81ffff0ec2a76abaa4b66edf01d2db0d7f3fda342a26525eb72e4e9a80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-ppc64le'; 			sha256='4410f045bfc084fef1f0fcea2c3f8e665cad6c5055f57f1089dd009bb9b65151'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-riscv64'; 			sha256='6d551f86c2ab9155882f5a1067223d0c0c80b47669c826af4311c305cc637093'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-s390x'; 			sha256='6012d0bd529312d12937fd153583a90ddb29aec7a7a8cfaac8e7fb7d1ceabf6f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 12 Jun 2025 11:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Jun 2025 11:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f32e8d6f68009e4f81cdd4d2b7e6465c3cdc96e6addc90132dfdb88d08941a20`  
		Last Modified: Thu, 12 Jun 2025 22:36:53 GMT  
		Size: 8.2 MB (8207474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ac40e43aadc31b56fc943a7df1de7e7f5f06348ca89a108384ba3e9a805a89`  
		Last Modified: Thu, 12 Jun 2025 22:36:53 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3870806677ebd2c8113c069ad6c6f219c456246069bd2688c9cffe6d1736938`  
		Last Modified: Thu, 12 Jun 2025 22:36:55 GMT  
		Size: 20.1 MB (20083028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86f14a0f3d88cab9e631bd4dcf8f9a164306875132f95135fff3358e3a2a8d2`  
		Last Modified: Thu, 12 Jun 2025 22:36:56 GMT  
		Size: 21.3 MB (21290186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da67c6f5f9a3f4626ce69c1328bdacf4c370d20479d084f6415437dea4481db4`  
		Last Modified: Thu, 12 Jun 2025 22:36:56 GMT  
		Size: 21.1 MB (21100670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b94aef2e962e8f653820f39c328e9f31ab7a6e903d929b45f9fb82324f7633`  
		Last Modified: Thu, 12 Jun 2025 22:36:55 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a98583f050f0d3b9242c387626407b4c0affec19be6fafeb1c7135bd7303d86`  
		Last Modified: Thu, 12 Jun 2025 22:36:56 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a115214fbd18e2a1acb4699bd0d7f72d42bf84a1f4cd3d4b1cdae8248a2167fa`  
		Last Modified: Thu, 12 Jun 2025 22:36:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2-cli` - unknown; unknown

```console
$ docker pull docker@sha256:1ebe76e61490c161294dbf222ba3f54e20b9c4ef88e3a419b69d6c9ea30d9cee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adb69d08e123464b3d3e1ca5fc247dafb6079c23e370b419c72f645720be223f`

```dockerfile
```

-	Layers:
	-	`sha256:c968c006dcee70140b54235857f7cdddd7486443dbd3175f36530d5404ebc8e2`  
		Last Modified: Thu, 12 Jun 2025 23:07:35 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.2-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:cbf1afecf10a316254346c8400aefe8e45ec33d0ca7d37e94acaf8df4c243108
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69498335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4b21f5d310fad2488ce7f6f0798a746c1018659fb7fce6a3975ebe40ba17364`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 12 Jun 2025 11:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-x86_64'; 			sha256='6777247eb2947c48b46b1fc96602ac17e140fbac84e1043e6384a6c755fc6769'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv6'; 			sha256='1a7731a63ec845b4b4cf2510e68a8f3411386b1e4b5b03916a0d21a697596f03'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv7'; 			sha256='63e64d9aad9916771a947e4b77df6b2a5e70cdfdb412b2f0464806f4d63fabe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-aarch64'; 			sha256='36dfcc81ffff0ec2a76abaa4b66edf01d2db0d7f3fda342a26525eb72e4e9a80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-ppc64le'; 			sha256='4410f045bfc084fef1f0fcea2c3f8e665cad6c5055f57f1089dd009bb9b65151'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-riscv64'; 			sha256='6d551f86c2ab9155882f5a1067223d0c0c80b47669c826af4311c305cc637093'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-s390x'; 			sha256='6012d0bd529312d12937fd153583a90ddb29aec7a7a8cfaac8e7fb7d1ceabf6f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 12 Jun 2025 11:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Jun 2025 11:04:16 GMT
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
	-	`sha256:3156c3bcd5598f721d5e807804df7256e282bd2897ea9f9f029b3cd93a5ff79b`  
		Last Modified: Thu, 05 Jun 2025 22:44:12 GMT  
		Size: 18.1 MB (18101909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:225abe8edcfa38ed05c3678afaa3fc7019381a300f823c874d6fdfd2a372c345`  
		Last Modified: Thu, 05 Jun 2025 22:44:12 GMT  
		Size: 19.9 MB (19943271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aaa4a492c5a8c6019873f7f10f4583b9134c81a74df09c55d664e88521c254c`  
		Last Modified: Thu, 12 Jun 2025 22:36:39 GMT  
		Size: 19.8 MB (19835400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d441ddcc7f77e2457e59e55a8a824b3b189eaa5a13fdaf65a914da194d6919b`  
		Last Modified: Thu, 12 Jun 2025 22:36:37 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c28d4afadc6fad8c6238b24d9a8dad8f8e7a8deb80839c1d3459890592b523f2`  
		Last Modified: Thu, 12 Jun 2025 22:36:38 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ebbefe72ea0510e4b225079670e073211f0b85e0fc4be94f42ca4ea57d54248`  
		Last Modified: Thu, 12 Jun 2025 22:36:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2-cli` - unknown; unknown

```console
$ docker pull docker@sha256:37fab8abfd9b21a00df69a9d07c5ae68b8fdeb2d34ff544d116b57a663143a26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4395a2db76f1506365fb0eac51245b617ca30226db9bb3af6fa171e9e441302`

```dockerfile
```

-	Layers:
	-	`sha256:ad79c76406a54721aaaa4054e1b21be3980a141745279c1866556fad3f734fd2`  
		Last Modified: Thu, 12 Jun 2025 23:07:38 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.2-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:fb3724965534d54ce9da8a451424d81fb9e4d4538aeccd1da9b3917f10a8a822
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68499848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c4ad4e83728a898d4ea348a6ce14ceb59541c63a530e27e987d9fe358f1440b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 12 Jun 2025 11:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-x86_64'; 			sha256='6777247eb2947c48b46b1fc96602ac17e140fbac84e1043e6384a6c755fc6769'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv6'; 			sha256='1a7731a63ec845b4b4cf2510e68a8f3411386b1e4b5b03916a0d21a697596f03'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv7'; 			sha256='63e64d9aad9916771a947e4b77df6b2a5e70cdfdb412b2f0464806f4d63fabe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-aarch64'; 			sha256='36dfcc81ffff0ec2a76abaa4b66edf01d2db0d7f3fda342a26525eb72e4e9a80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-ppc64le'; 			sha256='4410f045bfc084fef1f0fcea2c3f8e665cad6c5055f57f1089dd009bb9b65151'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-riscv64'; 			sha256='6d551f86c2ab9155882f5a1067223d0c0c80b47669c826af4311c305cc637093'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-s390x'; 			sha256='6012d0bd529312d12937fd153583a90ddb29aec7a7a8cfaac8e7fb7d1ceabf6f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 12 Jun 2025 11:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Jun 2025 11:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b30f7212c67694cf480811a55ca551c13acaf23308660855c528140f72c862`  
		Last Modified: Fri, 13 Jun 2025 01:20:06 GMT  
		Size: 7.4 MB (7440617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3fca8ac4e435f25c24efea81db3a20417fad9d7c421bee5ce9e3b58996c8efa`  
		Last Modified: Fri, 13 Jun 2025 01:20:05 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68a306e9551e1b17a6ecb71be8147d67ef4f891736c4e69faee945e235107fc`  
		Last Modified: Fri, 13 Jun 2025 01:20:06 GMT  
		Size: 18.1 MB (18089377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44e8dff8b0583db9cb4fc33b75dec6c3d09dd8ce3a76c2a78fd8af411bce92c`  
		Last Modified: Fri, 13 Jun 2025 01:20:08 GMT  
		Size: 19.9 MB (19927230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c665168123ed7a9acc312ff431c35318ee6393642e3e2a8bb7fa2845208b64aa`  
		Last Modified: Fri, 13 Jun 2025 01:20:08 GMT  
		Size: 19.8 MB (19821284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f454bde5fc9b6055cf7fe14c89d2a03739341ccdde89409892b34630a79576`  
		Last Modified: Fri, 13 Jun 2025 01:26:31 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3159ba7c72c13cd717ca59937ae54ce16c3ef91f409e6ff1eb4ab88fc1db06c0`  
		Last Modified: Fri, 13 Jun 2025 01:26:33 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ef5f44369f56ae39826aaf9f89b54c9bf2d4d09a86c4eaf7af04c279812997`  
		Last Modified: Fri, 13 Jun 2025 01:26:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2-cli` - unknown; unknown

```console
$ docker pull docker@sha256:17bce1271d7d0578a9245dd7fa91ca7dd2d6133e2d34320d3e8cdc818063c285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2eab113b229c25442c9ce7ca62b5528b3d19f6c315834a17499edc2b29f2c94`

```dockerfile
```

-	Layers:
	-	`sha256:f90f66106ac1cc7b0fabaf95162d064739ffbb6f6d97378a5324bcfff18516c3`  
		Last Modified: Fri, 13 Jun 2025 02:07:34 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.2-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:69d471e3a384a30ce1bc54407292e5f0b7cb0b7261bc36b61aa2eb5ec882db7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70086818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd6c4ddb71ce75a68aad923b7822e2edfe7e0c0cd87a9e2d99f4feffc8015393`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 12 Jun 2025 11:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-x86_64'; 			sha256='6777247eb2947c48b46b1fc96602ac17e140fbac84e1043e6384a6c755fc6769'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv6'; 			sha256='1a7731a63ec845b4b4cf2510e68a8f3411386b1e4b5b03916a0d21a697596f03'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv7'; 			sha256='63e64d9aad9916771a947e4b77df6b2a5e70cdfdb412b2f0464806f4d63fabe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-aarch64'; 			sha256='36dfcc81ffff0ec2a76abaa4b66edf01d2db0d7f3fda342a26525eb72e4e9a80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-ppc64le'; 			sha256='4410f045bfc084fef1f0fcea2c3f8e665cad6c5055f57f1089dd009bb9b65151'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-riscv64'; 			sha256='6d551f86c2ab9155882f5a1067223d0c0c80b47669c826af4311c305cc637093'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-s390x'; 			sha256='6012d0bd529312d12937fd153583a90ddb29aec7a7a8cfaac8e7fb7d1ceabf6f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 12 Jun 2025 11:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Jun 2025 11:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375cb5234cd1a2b6b8f1aba00c28fc5d45ba0ecc0d3c8f130d5cdb5138ba6c09`  
		Last Modified: Fri, 13 Jun 2025 00:09:12 GMT  
		Size: 8.2 MB (8229005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ba114b122014764181bf833228533908f5eedbccce11b62f71d746ab1616ccc`  
		Last Modified: Fri, 13 Jun 2025 00:09:12 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5090356630719947eb3cfc865b4d6d8f4971f5e40c640070edd88a16ab0c486f`  
		Last Modified: Fri, 13 Jun 2025 00:09:13 GMT  
		Size: 18.9 MB (18902609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd89b3ff82b93c434d43d799f7f56e86b96409535e06f30c6bbc54456e99752d`  
		Last Modified: Fri, 13 Jun 2025 00:09:14 GMT  
		Size: 19.5 MB (19469847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb8a2de00a4f86825ec25a2f3ac1553ace626f97f529f17cda507233ec8f1a9a`  
		Last Modified: Fri, 13 Jun 2025 00:09:14 GMT  
		Size: 19.3 MB (19347260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ced3983ecfb78d04b5aefc0cf90f4a0b3ccd62ec5610841b0f7860259defda`  
		Last Modified: Fri, 13 Jun 2025 00:09:13 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3673e39b233f3bfe295c08f11dda44b40d801a0bb4f299fe81e1ec50851575`  
		Last Modified: Fri, 13 Jun 2025 00:09:13 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b219e20a46cafa0737e015b21a2525d3bb013d26dc4af6849c8f3586a8b10c5f`  
		Last Modified: Fri, 13 Jun 2025 00:09:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2-cli` - unknown; unknown

```console
$ docker pull docker@sha256:f4ad80ac0ebd1e61f59071330740a5cb04fcce43ee8dca6549fd765d5fb74f10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8152da6cbb3a8d4cbf91841ae5de344f2f6f46a451de0b36ffec8f81c859695d`

```dockerfile
```

-	Layers:
	-	`sha256:f8a046668b3f08af5f7ebc0544c42d2308112f3cbaa8603efab8638bb256e743`  
		Last Modified: Fri, 13 Jun 2025 02:07:38 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.2-dind`

```console
$ docker pull docker@sha256:ff052514f359111edd920b54581e7aca65629458607f9fbdbf82d7eefbe0602b
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

### `docker:28.2-dind` - linux; amd64

```console
$ docker pull docker@sha256:8e32fae437051e392dc31f1bca659a14a6b8f341fa6dd131a9def0a9f315203c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.7 MB (143689092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:896cfe4b7aa87684cdbe7274a5a4efafa80c561662a935bd3a0432e2fcbaf46d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-x86_64'; 			sha256='6777247eb2947c48b46b1fc96602ac17e140fbac84e1043e6384a6c755fc6769'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv6'; 			sha256='1a7731a63ec845b4b4cf2510e68a8f3411386b1e4b5b03916a0d21a697596f03'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv7'; 			sha256='63e64d9aad9916771a947e4b77df6b2a5e70cdfdb412b2f0464806f4d63fabe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-aarch64'; 			sha256='36dfcc81ffff0ec2a76abaa4b66edf01d2db0d7f3fda342a26525eb72e4e9a80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-ppc64le'; 			sha256='4410f045bfc084fef1f0fcea2c3f8e665cad6c5055f57f1089dd009bb9b65151'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-riscv64'; 			sha256='6d551f86c2ab9155882f5a1067223d0c0c80b47669c826af4311c305cc637093'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-s390x'; 			sha256='6012d0bd529312d12937fd153583a90ddb29aec7a7a8cfaac8e7fb7d1ceabf6f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 05 Jun 2025 17:36:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
CMD ["sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
VOLUME [/var/lib/docker]
# Thu, 05 Jun 2025 17:36:11 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
CMD []
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f32e8d6f68009e4f81cdd4d2b7e6465c3cdc96e6addc90132dfdb88d08941a20`  
		Last Modified: Thu, 12 Jun 2025 22:36:53 GMT  
		Size: 8.2 MB (8207474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ac40e43aadc31b56fc943a7df1de7e7f5f06348ca89a108384ba3e9a805a89`  
		Last Modified: Thu, 12 Jun 2025 22:36:53 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3870806677ebd2c8113c069ad6c6f219c456246069bd2688c9cffe6d1736938`  
		Last Modified: Thu, 12 Jun 2025 22:36:55 GMT  
		Size: 20.1 MB (20083028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86f14a0f3d88cab9e631bd4dcf8f9a164306875132f95135fff3358e3a2a8d2`  
		Last Modified: Thu, 12 Jun 2025 22:36:56 GMT  
		Size: 21.3 MB (21290186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da67c6f5f9a3f4626ce69c1328bdacf4c370d20479d084f6415437dea4481db4`  
		Last Modified: Thu, 12 Jun 2025 22:36:56 GMT  
		Size: 21.1 MB (21100670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b94aef2e962e8f653820f39c328e9f31ab7a6e903d929b45f9fb82324f7633`  
		Last Modified: Thu, 12 Jun 2025 22:36:55 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a98583f050f0d3b9242c387626407b4c0affec19be6fafeb1c7135bd7303d86`  
		Last Modified: Thu, 12 Jun 2025 22:36:56 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a115214fbd18e2a1acb4699bd0d7f72d42bf84a1f4cd3d4b1cdae8248a2167fa`  
		Last Modified: Thu, 12 Jun 2025 22:36:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:212150b9078af2b8495b33e957823f54b179f41a22f2702f6fec1560c9d3f6f2`  
		Last Modified: Thu, 12 Jun 2025 23:07:54 GMT  
		Size: 6.9 MB (6905618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9212e721c88d6da1ed4b1e289f523f35a01e01885d1131cd34feceb518227abf`  
		Last Modified: Thu, 12 Jun 2025 23:07:53 GMT  
		Size: 90.5 KB (90494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b0253e449f82e84618065f5b74284cb93f7cc52668795f3590d41585c32012`  
		Last Modified: Thu, 12 Jun 2025 23:07:51 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811b046d83c5b8a6340f19f8d6acd494b2b028f5c1bf969e58cf6f0e350c7cea`  
		Last Modified: Thu, 12 Jun 2025 23:07:58 GMT  
		Size: 62.2 MB (62206627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68771551084500ee9ac3a4b32aa56d78b3d007c1986578b481436becbe8ae1a1`  
		Last Modified: Thu, 12 Jun 2025 23:07:51 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cae381f867a74a59e0d18562bd189fcc3560935254e57ceb2e247145c467a8b`  
		Last Modified: Thu, 12 Jun 2025 23:07:52 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2-dind` - unknown; unknown

```console
$ docker pull docker@sha256:4c5431982a6f26acafc9a647e2a915e12fd2cb54c0d9fa6f5bed94ca07e186b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a1e46faf2561239606e7d796aac2f70a1bc3754ba1ff7200c43154e973515c8`

```dockerfile
```

-	Layers:
	-	`sha256:d5158885bee456f124624bc8808ba3f4ea82fc7ca56f260044b4d92a684498b1`  
		Last Modified: Fri, 13 Jun 2025 02:07:20 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.2-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:d692f151518fae2760b09152001cfba45f8bc770e1906d190d6eb2e3142b1a76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134722094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44d698360caa93e31e5563c2c622bbbeb75bd82d597a599776298366deb6aa32`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-x86_64'; 			sha256='6777247eb2947c48b46b1fc96602ac17e140fbac84e1043e6384a6c755fc6769'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv6'; 			sha256='1a7731a63ec845b4b4cf2510e68a8f3411386b1e4b5b03916a0d21a697596f03'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv7'; 			sha256='63e64d9aad9916771a947e4b77df6b2a5e70cdfdb412b2f0464806f4d63fabe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-aarch64'; 			sha256='36dfcc81ffff0ec2a76abaa4b66edf01d2db0d7f3fda342a26525eb72e4e9a80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-ppc64le'; 			sha256='4410f045bfc084fef1f0fcea2c3f8e665cad6c5055f57f1089dd009bb9b65151'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-riscv64'; 			sha256='6d551f86c2ab9155882f5a1067223d0c0c80b47669c826af4311c305cc637093'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-s390x'; 			sha256='6012d0bd529312d12937fd153583a90ddb29aec7a7a8cfaac8e7fb7d1ceabf6f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 05 Jun 2025 17:36:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
CMD ["sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
VOLUME [/var/lib/docker]
# Thu, 05 Jun 2025 17:36:11 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
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
	-	`sha256:3156c3bcd5598f721d5e807804df7256e282bd2897ea9f9f029b3cd93a5ff79b`  
		Last Modified: Thu, 05 Jun 2025 22:44:12 GMT  
		Size: 18.1 MB (18101909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:225abe8edcfa38ed05c3678afaa3fc7019381a300f823c874d6fdfd2a372c345`  
		Last Modified: Thu, 05 Jun 2025 22:44:12 GMT  
		Size: 19.9 MB (19943271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aaa4a492c5a8c6019873f7f10f4583b9134c81a74df09c55d664e88521c254c`  
		Last Modified: Thu, 12 Jun 2025 22:36:39 GMT  
		Size: 19.8 MB (19835400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d441ddcc7f77e2457e59e55a8a824b3b189eaa5a13fdaf65a914da194d6919b`  
		Last Modified: Thu, 12 Jun 2025 22:36:37 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c28d4afadc6fad8c6238b24d9a8dad8f8e7a8deb80839c1d3459890592b523f2`  
		Last Modified: Thu, 12 Jun 2025 22:36:38 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ebbefe72ea0510e4b225079670e073211f0b85e0fc4be94f42ca4ea57d54248`  
		Last Modified: Thu, 12 Jun 2025 22:36:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8241b18dc7eb679233e3250bbfb077dcd4f8778550fe3188d80dd91b7838a9bd`  
		Last Modified: Thu, 12 Jun 2025 22:54:58 GMT  
		Size: 7.2 MB (7230354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3cf946673d9726b4c5b57734c7dbf2e2e811f1b40e437ce7cc7bf5533df26a`  
		Last Modified: Thu, 12 Jun 2025 22:54:57 GMT  
		Size: 90.1 KB (90058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d08132e8b60b557ae762a779e816c58c6c366efd53ded71c9275533c8ec8f2d`  
		Last Modified: Thu, 12 Jun 2025 22:54:57 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d611e6743d4f047d30c66012bbac54fc821dc2ffefbbe8277a53e70060da2356`  
		Last Modified: Thu, 12 Jun 2025 22:55:00 GMT  
		Size: 57.9 MB (57897340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a783e6fb91bba730335ac30fbd49b93258f2e4d9d4c2a73dbe5c7663e5f497`  
		Last Modified: Thu, 12 Jun 2025 22:54:57 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b45b886f9c1b0ecbf83201757d3e791047d9cd0cbbdfc865a112256becf21ce4`  
		Last Modified: Thu, 12 Jun 2025 22:54:58 GMT  
		Size: 3.3 KB (3304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2-dind` - unknown; unknown

```console
$ docker pull docker@sha256:d1a670e4e107e2e31f275813f1751ac249dec91fa3cfc6cc949e581bdb0c364e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb88dd0bcd267d48fad2fe5722c0bc382d70b8aa328b8a911562dc8081e3809d`

```dockerfile
```

-	Layers:
	-	`sha256:c75371d2b5d03d6fe0926a467c9d353d590b6db0765b2bc492cb0184dfe50817`  
		Last Modified: Thu, 12 Jun 2025 23:07:42 GMT  
		Size: 34.8 KB (34765 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.2-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:66277612b6b4d8230b45b06074b5716e61c90fee840cf8b7b4da8208329fe9d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.0 MB (133027832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55fe29bbf4d101c05a3d55a85a71baf6c7ae07a62cc6865b2fc5b8902a5978a6`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-x86_64'; 			sha256='6777247eb2947c48b46b1fc96602ac17e140fbac84e1043e6384a6c755fc6769'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv6'; 			sha256='1a7731a63ec845b4b4cf2510e68a8f3411386b1e4b5b03916a0d21a697596f03'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv7'; 			sha256='63e64d9aad9916771a947e4b77df6b2a5e70cdfdb412b2f0464806f4d63fabe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-aarch64'; 			sha256='36dfcc81ffff0ec2a76abaa4b66edf01d2db0d7f3fda342a26525eb72e4e9a80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-ppc64le'; 			sha256='4410f045bfc084fef1f0fcea2c3f8e665cad6c5055f57f1089dd009bb9b65151'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-riscv64'; 			sha256='6d551f86c2ab9155882f5a1067223d0c0c80b47669c826af4311c305cc637093'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-s390x'; 			sha256='6012d0bd529312d12937fd153583a90ddb29aec7a7a8cfaac8e7fb7d1ceabf6f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 05 Jun 2025 17:36:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
CMD ["sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
VOLUME [/var/lib/docker]
# Thu, 05 Jun 2025 17:36:11 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
CMD []
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b30f7212c67694cf480811a55ca551c13acaf23308660855c528140f72c862`  
		Last Modified: Fri, 13 Jun 2025 01:20:06 GMT  
		Size: 7.4 MB (7440617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3fca8ac4e435f25c24efea81db3a20417fad9d7c421bee5ce9e3b58996c8efa`  
		Last Modified: Fri, 13 Jun 2025 01:20:05 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68a306e9551e1b17a6ecb71be8147d67ef4f891736c4e69faee945e235107fc`  
		Last Modified: Fri, 13 Jun 2025 01:20:06 GMT  
		Size: 18.1 MB (18089377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44e8dff8b0583db9cb4fc33b75dec6c3d09dd8ce3a76c2a78fd8af411bce92c`  
		Last Modified: Fri, 13 Jun 2025 01:20:08 GMT  
		Size: 19.9 MB (19927230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c665168123ed7a9acc312ff431c35318ee6393642e3e2a8bb7fa2845208b64aa`  
		Last Modified: Fri, 13 Jun 2025 01:20:08 GMT  
		Size: 19.8 MB (19821284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f454bde5fc9b6055cf7fe14c89d2a03739341ccdde89409892b34630a79576`  
		Last Modified: Fri, 13 Jun 2025 01:26:31 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3159ba7c72c13cd717ca59937ae54ce16c3ef91f409e6ff1eb4ab88fc1db06c0`  
		Last Modified: Fri, 13 Jun 2025 01:26:33 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ef5f44369f56ae39826aaf9f89b54c9bf2d4d09a86c4eaf7af04c279812997`  
		Last Modified: Fri, 13 Jun 2025 01:26:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7236561f33fb7c50ca5d7c37b075afc53fe8e4088c95319dcde0bb8ad917eb0`  
		Last Modified: Fri, 13 Jun 2025 06:24:34 GMT  
		Size: 6.5 MB (6538120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98752e61e2dd86e562ed8c9de46d0e71b38f35fe7be163828be059624970c9e`  
		Last Modified: Fri, 13 Jun 2025 06:24:35 GMT  
		Size: 86.5 KB (86488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c1e6adc4b8f7742b913355688fb6e8dd3671bd9c49551a76f2dad8f0bfcf827`  
		Last Modified: Fri, 13 Jun 2025 06:24:35 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7760efd1d6901a24ed3199cf41b66c116f64c11736dcecc92c75040a0f68dea9`  
		Last Modified: Fri, 13 Jun 2025 06:24:39 GMT  
		Size: 57.9 MB (57897375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb6cd2d2e0725f775e9f508d900bb8bac548036c111ea8957a933fc7002b93e`  
		Last Modified: Fri, 13 Jun 2025 06:24:36 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcd8d4be9dc74189aefe21d876aec06706ad1fa1e7597dd49f2c2fc862477c51`  
		Last Modified: Fri, 13 Jun 2025 06:24:36 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2-dind` - unknown; unknown

```console
$ docker pull docker@sha256:9c4cb9730947a3df8f10cb2052f42e9556fa8a3d55b8d9eb9df923d7467c4a6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4fa8b980b9e0ff354efd1a786e8ee1816d49966e8cb7f6c93a8a7182923f7fd`

```dockerfile
```

-	Layers:
	-	`sha256:4bc11f3d388f7184ad2e3f2d7090c73f569bc734a2691321b72cdcb0e3735d28`  
		Last Modified: Fri, 13 Jun 2025 08:07:23 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.2-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:b8d1c58eea384111a2c6646a55d6c57e11ce3527c44b26b17ba91e00f82530c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.5 MB (134502165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f7a08861e83333223ac02d5357e4d77380c819b320b98b1811d33973cd4cd5e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-x86_64'; 			sha256='6777247eb2947c48b46b1fc96602ac17e140fbac84e1043e6384a6c755fc6769'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv6'; 			sha256='1a7731a63ec845b4b4cf2510e68a8f3411386b1e4b5b03916a0d21a697596f03'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv7'; 			sha256='63e64d9aad9916771a947e4b77df6b2a5e70cdfdb412b2f0464806f4d63fabe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-aarch64'; 			sha256='36dfcc81ffff0ec2a76abaa4b66edf01d2db0d7f3fda342a26525eb72e4e9a80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-ppc64le'; 			sha256='4410f045bfc084fef1f0fcea2c3f8e665cad6c5055f57f1089dd009bb9b65151'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-riscv64'; 			sha256='6d551f86c2ab9155882f5a1067223d0c0c80b47669c826af4311c305cc637093'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-s390x'; 			sha256='6012d0bd529312d12937fd153583a90ddb29aec7a7a8cfaac8e7fb7d1ceabf6f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 05 Jun 2025 17:36:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
CMD ["sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
VOLUME [/var/lib/docker]
# Thu, 05 Jun 2025 17:36:11 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
CMD []
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375cb5234cd1a2b6b8f1aba00c28fc5d45ba0ecc0d3c8f130d5cdb5138ba6c09`  
		Last Modified: Fri, 13 Jun 2025 00:09:12 GMT  
		Size: 8.2 MB (8229005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ba114b122014764181bf833228533908f5eedbccce11b62f71d746ab1616ccc`  
		Last Modified: Fri, 13 Jun 2025 00:09:12 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5090356630719947eb3cfc865b4d6d8f4971f5e40c640070edd88a16ab0c486f`  
		Last Modified: Fri, 13 Jun 2025 00:09:13 GMT  
		Size: 18.9 MB (18902609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd89b3ff82b93c434d43d799f7f56e86b96409535e06f30c6bbc54456e99752d`  
		Last Modified: Fri, 13 Jun 2025 00:09:14 GMT  
		Size: 19.5 MB (19469847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb8a2de00a4f86825ec25a2f3ac1553ace626f97f529f17cda507233ec8f1a9a`  
		Last Modified: Fri, 13 Jun 2025 00:09:14 GMT  
		Size: 19.3 MB (19347260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ced3983ecfb78d04b5aefc0cf90f4a0b3ccd62ec5610841b0f7860259defda`  
		Last Modified: Fri, 13 Jun 2025 00:09:13 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3673e39b233f3bfe295c08f11dda44b40d801a0bb4f299fe81e1ec50851575`  
		Last Modified: Fri, 13 Jun 2025 00:09:13 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b219e20a46cafa0737e015b21a2525d3bb013d26dc4af6849c8f3586a8b10c5f`  
		Last Modified: Fri, 13 Jun 2025 00:09:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c6e05695096db67c5e6426307e8a652c5311da73d994e47d9580e886b837a10`  
		Last Modified: Fri, 13 Jun 2025 04:27:25 GMT  
		Size: 7.1 MB (7141507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891d71d9754311d78a8a473d578e3825acd68ce42cd0dbc623f6357a4e17c72b`  
		Last Modified: Fri, 13 Jun 2025 04:27:25 GMT  
		Size: 99.6 KB (99645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5d9a3e9b7f7718caa1aba176d0c009906cfdbf0beaabb63840d5743b89cc7f2`  
		Last Modified: Fri, 13 Jun 2025 04:27:26 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d489b833d40920f79c54667b28c6b5c28475bbdb198a31284fb082206828119a`  
		Last Modified: Fri, 13 Jun 2025 04:27:32 GMT  
		Size: 57.2 MB (57168194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e7d0e57cac200e9cb81bab37725356fb62116b7b3fb40855e245e59124702f2`  
		Last Modified: Fri, 13 Jun 2025 04:27:27 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc40c4cf8ec0a96212d48ae432d6342b219db9566141690970349c4e6140886`  
		Last Modified: Fri, 13 Jun 2025 04:27:27 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2-dind` - unknown; unknown

```console
$ docker pull docker@sha256:e64e322c1cc45566807e6054fb529a1b90018a74d5599c9e524013622d5fd800
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30148cdfe5f84f758ae82d1f85d34d65c6e91c5167340993eaa3d924e06041f5`

```dockerfile
```

-	Layers:
	-	`sha256:a0dd369778c470b4b56994e10a017cc701a049c277738705f244ac7e5856bdd4`  
		Last Modified: Fri, 13 Jun 2025 05:07:36 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.2-dind-rootless`

```console
$ docker pull docker@sha256:c139111ddef9a8729f6be11c4f8f466526c9d9d282626ec42fe5681f14770ef1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:28.2-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:618707c0d004c07f5787c531d0d2b9cb07cc83c632842ec6b347811099ffc758
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.3 MB (162269674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c2a46a84fc8e55db5bd3a19a4017e96d28a0244e42500d3720717d4559dd307`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 17:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 30 May 2025 17:04:15 GMT
ENV DOCKER_VERSION=28.2.2
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 30 May 2025 17:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 30 May 2025 17:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-x86_64'; 			sha256='6777247eb2947c48b46b1fc96602ac17e140fbac84e1043e6384a6c755fc6769'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv6'; 			sha256='1a7731a63ec845b4b4cf2510e68a8f3411386b1e4b5b03916a0d21a697596f03'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv7'; 			sha256='63e64d9aad9916771a947e4b77df6b2a5e70cdfdb412b2f0464806f4d63fabe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-aarch64'; 			sha256='36dfcc81ffff0ec2a76abaa4b66edf01d2db0d7f3fda342a26525eb72e4e9a80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-ppc64le'; 			sha256='4410f045bfc084fef1f0fcea2c3f8e665cad6c5055f57f1089dd009bb9b65151'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-riscv64'; 			sha256='6d551f86c2ab9155882f5a1067223d0c0c80b47669c826af4311c305cc637093'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-s390x'; 			sha256='6012d0bd529312d12937fd153583a90ddb29aec7a7a8cfaac8e7fb7d1ceabf6f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 30 May 2025 17:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 30 May 2025 17:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 17:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 30 May 2025 17:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 30 May 2025 17:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 17:04:15 GMT
CMD ["sh"]
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 30 May 2025 17:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 30 May 2025 17:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 17:04:15 GMT
VOLUME [/var/lib/docker]
# Fri, 30 May 2025 17:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 30 May 2025 17:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 30 May 2025 17:04:15 GMT
CMD []
# Fri, 30 May 2025 17:04:15 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 30 May 2025 17:04:15 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 30 May 2025 17:04:15 GMT
USER rootless
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f32e8d6f68009e4f81cdd4d2b7e6465c3cdc96e6addc90132dfdb88d08941a20`  
		Last Modified: Thu, 12 Jun 2025 22:36:53 GMT  
		Size: 8.2 MB (8207474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ac40e43aadc31b56fc943a7df1de7e7f5f06348ca89a108384ba3e9a805a89`  
		Last Modified: Thu, 12 Jun 2025 22:36:53 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3870806677ebd2c8113c069ad6c6f219c456246069bd2688c9cffe6d1736938`  
		Last Modified: Thu, 12 Jun 2025 22:36:55 GMT  
		Size: 20.1 MB (20083028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86f14a0f3d88cab9e631bd4dcf8f9a164306875132f95135fff3358e3a2a8d2`  
		Last Modified: Thu, 12 Jun 2025 22:36:56 GMT  
		Size: 21.3 MB (21290186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da67c6f5f9a3f4626ce69c1328bdacf4c370d20479d084f6415437dea4481db4`  
		Last Modified: Thu, 12 Jun 2025 22:36:56 GMT  
		Size: 21.1 MB (21100670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b94aef2e962e8f653820f39c328e9f31ab7a6e903d929b45f9fb82324f7633`  
		Last Modified: Thu, 12 Jun 2025 22:36:55 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a98583f050f0d3b9242c387626407b4c0affec19be6fafeb1c7135bd7303d86`  
		Last Modified: Thu, 12 Jun 2025 22:36:56 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a115214fbd18e2a1acb4699bd0d7f72d42bf84a1f4cd3d4b1cdae8248a2167fa`  
		Last Modified: Thu, 12 Jun 2025 22:36:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:212150b9078af2b8495b33e957823f54b179f41a22f2702f6fec1560c9d3f6f2`  
		Last Modified: Thu, 12 Jun 2025 23:07:54 GMT  
		Size: 6.9 MB (6905618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9212e721c88d6da1ed4b1e289f523f35a01e01885d1131cd34feceb518227abf`  
		Last Modified: Thu, 12 Jun 2025 23:07:53 GMT  
		Size: 90.5 KB (90494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b0253e449f82e84618065f5b74284cb93f7cc52668795f3590d41585c32012`  
		Last Modified: Thu, 12 Jun 2025 23:07:51 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811b046d83c5b8a6340f19f8d6acd494b2b028f5c1bf969e58cf6f0e350c7cea`  
		Last Modified: Thu, 12 Jun 2025 23:07:58 GMT  
		Size: 62.2 MB (62206627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68771551084500ee9ac3a4b32aa56d78b3d007c1986578b481436becbe8ae1a1`  
		Last Modified: Thu, 12 Jun 2025 23:07:51 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cae381f867a74a59e0d18562bd189fcc3560935254e57ceb2e247145c467a8b`  
		Last Modified: Thu, 12 Jun 2025 23:07:52 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edcfb65cd16913d0735d91a3f41da46c772dc6128464cd3adef3509c06608cf3`  
		Last Modified: Fri, 13 Jun 2025 00:12:59 GMT  
		Size: 993.3 KB (993280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:969eb6fb622903c71c16e46ec5344d08043922bdd780c5d05f0149c738957108`  
		Last Modified: Fri, 13 Jun 2025 00:13:07 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5739660ee15831962b38500a68bc075c0420380781084109a21ac5085faa3d96`  
		Last Modified: Fri, 13 Jun 2025 00:13:10 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba46058072b4409214907ac1c19c90c67cc69a98dbe8bd0b997ee3be48d87947`  
		Last Modified: Fri, 13 Jun 2025 02:07:51 GMT  
		Size: 17.6 MB (17585962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10cb54f24b436f2e9ae244d4f7ad8d4d57968ee418008f027ea30581d65f6246`  
		Last Modified: Fri, 13 Jun 2025 00:13:14 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:9601e8bc1b00849768c14fe6044913853642441e3e9735dd9882c94946a62fe2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c02d3ef5cd053c5957bec70f4a8c28ab283ebf4a2bc5372947b08dfcc8d5f2e`

```dockerfile
```

-	Layers:
	-	`sha256:9fb42be545f7a062d87207720d7a980e0dac859ea3f6630e4c65ba6816b6297c`  
		Last Modified: Fri, 13 Jun 2025 02:07:38 GMT  
		Size: 30.5 KB (30452 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.2-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:35c3b834f6991d8ca48c0fb727e00538a23012ae1c854f988876906aaff64efa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.5 MB (153542694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e02b9699e685722cbc13f8e1a65cafa650145a9a599a5fa1eb750135e38e774`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 17:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 30 May 2025 17:04:15 GMT
ENV DOCKER_VERSION=28.2.2
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 30 May 2025 17:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 30 May 2025 17:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-x86_64'; 			sha256='6777247eb2947c48b46b1fc96602ac17e140fbac84e1043e6384a6c755fc6769'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv6'; 			sha256='1a7731a63ec845b4b4cf2510e68a8f3411386b1e4b5b03916a0d21a697596f03'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv7'; 			sha256='63e64d9aad9916771a947e4b77df6b2a5e70cdfdb412b2f0464806f4d63fabe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-aarch64'; 			sha256='36dfcc81ffff0ec2a76abaa4b66edf01d2db0d7f3fda342a26525eb72e4e9a80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-ppc64le'; 			sha256='4410f045bfc084fef1f0fcea2c3f8e665cad6c5055f57f1089dd009bb9b65151'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-riscv64'; 			sha256='6d551f86c2ab9155882f5a1067223d0c0c80b47669c826af4311c305cc637093'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-s390x'; 			sha256='6012d0bd529312d12937fd153583a90ddb29aec7a7a8cfaac8e7fb7d1ceabf6f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 30 May 2025 17:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 30 May 2025 17:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 17:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 30 May 2025 17:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 30 May 2025 17:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 17:04:15 GMT
CMD ["sh"]
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 30 May 2025 17:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 30 May 2025 17:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 17:04:15 GMT
VOLUME [/var/lib/docker]
# Fri, 30 May 2025 17:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 30 May 2025 17:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 30 May 2025 17:04:15 GMT
CMD []
# Fri, 30 May 2025 17:04:15 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 30 May 2025 17:04:15 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 30 May 2025 17:04:15 GMT
USER rootless
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375cb5234cd1a2b6b8f1aba00c28fc5d45ba0ecc0d3c8f130d5cdb5138ba6c09`  
		Last Modified: Fri, 13 Jun 2025 00:09:12 GMT  
		Size: 8.2 MB (8229005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ba114b122014764181bf833228533908f5eedbccce11b62f71d746ab1616ccc`  
		Last Modified: Fri, 13 Jun 2025 00:09:12 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5090356630719947eb3cfc865b4d6d8f4971f5e40c640070edd88a16ab0c486f`  
		Last Modified: Fri, 13 Jun 2025 00:09:13 GMT  
		Size: 18.9 MB (18902609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd89b3ff82b93c434d43d799f7f56e86b96409535e06f30c6bbc54456e99752d`  
		Last Modified: Fri, 13 Jun 2025 00:09:14 GMT  
		Size: 19.5 MB (19469847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb8a2de00a4f86825ec25a2f3ac1553ace626f97f529f17cda507233ec8f1a9a`  
		Last Modified: Fri, 13 Jun 2025 00:09:14 GMT  
		Size: 19.3 MB (19347260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ced3983ecfb78d04b5aefc0cf90f4a0b3ccd62ec5610841b0f7860259defda`  
		Last Modified: Fri, 13 Jun 2025 00:09:13 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3673e39b233f3bfe295c08f11dda44b40d801a0bb4f299fe81e1ec50851575`  
		Last Modified: Fri, 13 Jun 2025 00:09:13 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b219e20a46cafa0737e015b21a2525d3bb013d26dc4af6849c8f3586a8b10c5f`  
		Last Modified: Fri, 13 Jun 2025 00:09:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c6e05695096db67c5e6426307e8a652c5311da73d994e47d9580e886b837a10`  
		Last Modified: Fri, 13 Jun 2025 04:27:25 GMT  
		Size: 7.1 MB (7141507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891d71d9754311d78a8a473d578e3825acd68ce42cd0dbc623f6357a4e17c72b`  
		Last Modified: Fri, 13 Jun 2025 04:27:25 GMT  
		Size: 99.6 KB (99645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5d9a3e9b7f7718caa1aba176d0c009906cfdbf0beaabb63840d5743b89cc7f2`  
		Last Modified: Fri, 13 Jun 2025 04:27:26 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d489b833d40920f79c54667b28c6b5c28475bbdb198a31284fb082206828119a`  
		Last Modified: Fri, 13 Jun 2025 04:27:32 GMT  
		Size: 57.2 MB (57168194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e7d0e57cac200e9cb81bab37725356fb62116b7b3fb40855e245e59124702f2`  
		Last Modified: Fri, 13 Jun 2025 04:27:27 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc40c4cf8ec0a96212d48ae432d6342b219db9566141690970349c4e6140886`  
		Last Modified: Fri, 13 Jun 2025 04:27:27 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c1c853189a4f7b6c93d47fd98d9be0a95acfdbc8c0f8df18df4a175a65ce3b`  
		Last Modified: Fri, 13 Jun 2025 07:11:57 GMT  
		Size: 1.0 MB (1023005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe779df0e0efd82b4a777858dfbd3496808597c320e55ab766b45677649442a`  
		Last Modified: Fri, 13 Jun 2025 07:11:56 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a244027a6953dc0bf2fd363382ff7224e9f2c0bae6332d09c4e5e68511a3b7fb`  
		Last Modified: Fri, 13 Jun 2025 07:11:57 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40237444de5d3255f0f82947d5aa58daa8391b4d2fe9b8b6565e99969a09a8d6`  
		Last Modified: Fri, 13 Jun 2025 07:12:01 GMT  
		Size: 18.0 MB (18016184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b92f2d121a50edd33cc911db99177a3a185a452e7ec47f4751ead8e59a3bc3`  
		Last Modified: Fri, 13 Jun 2025 07:11:57 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:a9e0325277463e83ad33ae4cc4cf06e197918a3c651585f3a614fe7ddb944126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95a5b11d7826e81670044d1358d7f259365282306c1b8f9de1dbe8387517643c`

```dockerfile
```

-	Layers:
	-	`sha256:82a2387a357a58b3faf425641fd79df168694c9fdde196be68fb5632c4d7705e`  
		Last Modified: Fri, 13 Jun 2025 08:07:43 GMT  
		Size: 30.6 KB (30621 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.2-windowsservercore`

```console
$ docker pull docker@sha256:c244e5c2c3cc3b906baab6f383a9e91fc102f866e209e7a40dee80b3f50687f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4349; amd64
	-	windows version 10.0.20348.3807; amd64

### `docker:28.2-windowsservercore` - windows version 10.0.26100.4349; amd64

```console
$ docker pull docker@sha256:87b6c37c78ebd3b4dffee917bf6ba9e8e61722d7cc42313c63bf2204cf297f29
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3541382992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebb204680d5c75607c3a852fb2ef3ed327b9ccc1566c1d6a059cb0259d1a3a22`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 07 Jun 2025 15:42:01 GMT
RUN Install update 10.0.26100.4349
# Thu, 12 Jun 2025 22:41:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Jun 2025 22:41:52 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 12 Jun 2025 22:41:53 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 12 Jun 2025 22:41:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.2.2.zip
# Thu, 12 Jun 2025 22:42:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 12 Jun 2025 22:42:05 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 12 Jun 2025 22:42:06 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Thu, 12 Jun 2025 22:42:06 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Thu, 12 Jun 2025 22:42:16 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 12 Jun 2025 22:42:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Thu, 12 Jun 2025 22:42:17 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-windows-x86_64.exe
# Thu, 12 Jun 2025 22:42:18 GMT
ENV DOCKER_COMPOSE_SHA256=132fb31ef7dc81a82d7b1429adf3fd76cc0a7128059af3a172945445a50f2801
# Thu, 12 Jun 2025 22:42:28 GMT
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
	-	`sha256:7505764e5850853ff3205e21d0c6c05dd9890fed17012225b1f33d9e79ef8f7b`  
		Last Modified: Thu, 12 Jun 2025 22:46:16 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75201e0022107e322d1abb29cdcd607860e0814d97801313713016a804c7ea29`  
		Last Modified: Thu, 12 Jun 2025 22:46:17 GMT  
		Size: 384.3 KB (384281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad1332a299d19362bbb194725e3d76167ba59837dbdb186edc8c88eb4fc584fc`  
		Last Modified: Thu, 12 Jun 2025 22:46:16 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee1c450bb560eb20733ee6f9c9eab001dcdca87a8a976d64320a006b6a8626e`  
		Last Modified: Thu, 12 Jun 2025 22:46:16 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:292280c51cf870fb93a78962a22141e9734918633eac0270479904b4e7fde431`  
		Last Modified: Thu, 12 Jun 2025 22:46:19 GMT  
		Size: 20.5 MB (20474220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce832f815f971edd09a31c7ae7e5e8f1511fd9100e257f6c46649f33661d080d`  
		Last Modified: Thu, 12 Jun 2025 22:46:18 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc0188db691ee242410ed95505f0c2b6bf11c2034274be14cc637917ce9576aa`  
		Last Modified: Thu, 12 Jun 2025 22:46:18 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6d4dfab47701ffe430c0efb0d9f5640976ec9b76c70fa9adf6d9a9e37a7605a`  
		Last Modified: Thu, 12 Jun 2025 22:46:18 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c2ad7bc7d5b79fafe6d4eda10030323f4f485027233019a33343bd50a265a59`  
		Last Modified: Thu, 12 Jun 2025 22:46:21 GMT  
		Size: 22.3 MB (22283596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9538a3dff1be138d1137eb9fc139dbda8255bde275ae8670c13253a3d1033575`  
		Last Modified: Thu, 12 Jun 2025 22:46:19 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfe10fbb6bc6101cc1d7a69d3deb8126160b5db04361e52404e83b438b2fa8b3`  
		Last Modified: Thu, 12 Jun 2025 22:46:20 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2dfee3af3890e8fd03beb55f71a85b48276c6bff5474ae597f001adbd26f779`  
		Last Modified: Thu, 12 Jun 2025 22:46:20 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:846e5ade10ef88ce7e3178a17fc7662922cb37bf8403257413f21ca0869ab29c`  
		Last Modified: Thu, 12 Jun 2025 22:46:23 GMT  
		Size: 22.1 MB (22054925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28.2-windowsservercore` - windows version 10.0.20348.3807; amd64

```console
$ docker pull docker@sha256:53498ccee3c78a70215add9ae3ef737168375a5c54328c792752c0e5fde4eabf
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2345354530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:485c313a4ef331fdb3d3de62a8679e0f3981409d24dfa2b371f0d9efb2c3ff07`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Jun 2025 01:01:39 GMT
RUN Install update 10.0.20348.3807
# Thu, 12 Jun 2025 22:40:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Jun 2025 22:40:42 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 12 Jun 2025 22:40:43 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 12 Jun 2025 22:40:44 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.2.2.zip
# Thu, 12 Jun 2025 22:40:53 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 12 Jun 2025 22:40:54 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 12 Jun 2025 22:40:55 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Thu, 12 Jun 2025 22:40:55 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Thu, 12 Jun 2025 22:41:04 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 12 Jun 2025 22:41:05 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Thu, 12 Jun 2025 22:41:05 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-windows-x86_64.exe
# Thu, 12 Jun 2025 22:41:06 GMT
ENV DOCKER_COMPOSE_SHA256=132fb31ef7dc81a82d7b1429adf3fd76cc0a7128059af3a172945445a50f2801
# Thu, 12 Jun 2025 22:41:14 GMT
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
	-	`sha256:e3ce7730719b3563f78c11a86c6e7ca9e7ecab63539d89528367a963b46668ee`  
		Last Modified: Thu, 12 Jun 2025 22:42:44 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa44face37189a26dfbb23b8d5da4e8ec912b0e7403fa7e57fe746ede8ca163`  
		Last Modified: Thu, 12 Jun 2025 22:42:47 GMT  
		Size: 351.9 KB (351892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b288554d751322bcbba469e2992e7ed3d7addecc28b36b87bb0ac57981ad64a`  
		Last Modified: Thu, 12 Jun 2025 22:42:46 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08b3bdb645c2944656eeb7ae7bf819f0cd63f9c83b2677298c9c21d710111eec`  
		Last Modified: Thu, 12 Jun 2025 22:42:47 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b59891c80d4b303cd1655e3255818d7a3cb47a43fe98781999d05abb780b0ed`  
		Last Modified: Thu, 12 Jun 2025 22:42:50 GMT  
		Size: 20.5 MB (20450522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1af8f19e40999102aa31f1f4406c7f15eeb18843036b70938f492dee65f6943`  
		Last Modified: Thu, 12 Jun 2025 22:42:49 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f07268cae3a2cdfcdce7a98218844be1e3ede2baa06062288c10119e5414b06`  
		Last Modified: Thu, 12 Jun 2025 22:42:50 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bea31ae088d4884385e4c9bf2ff15ca1ed5f8581b5d17cba15b96224a1533af`  
		Last Modified: Thu, 12 Jun 2025 22:42:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:428d152391bf0297baa1308e6b7a51fa8dfb41c8f2dd3071d1d21fa3e4f42d41`  
		Last Modified: Thu, 12 Jun 2025 22:42:54 GMT  
		Size: 22.3 MB (22261181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b28b4c745fe11d31b3e00254bc2bc9aec2a58ab17157f558834f43f95a248ea`  
		Last Modified: Thu, 12 Jun 2025 22:42:54 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aa41358ec814cca1a580968a15e80fadcab82f43e7c6b59aea4861acb3c83ad`  
		Last Modified: Thu, 12 Jun 2025 22:42:55 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10bc742c50fda0894e2260bf3f7eb9919c098581d407b6cf2a42e3a41062305b`  
		Last Modified: Thu, 12 Jun 2025 22:42:56 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f06dfd207ec226196bd2af1228c11187c3803b22f4c3f4ac01c21d67d7207e67`  
		Last Modified: Thu, 12 Jun 2025 22:42:58 GMT  
		Size: 22.0 MB (22027759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.2-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:f640af5c3e1bd4c0cb40cf589e9f2f5903fcff110a95226d0c3f09140b3962eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3807; amd64

### `docker:28.2-windowsservercore-ltsc2022` - windows version 10.0.20348.3807; amd64

```console
$ docker pull docker@sha256:53498ccee3c78a70215add9ae3ef737168375a5c54328c792752c0e5fde4eabf
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2345354530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:485c313a4ef331fdb3d3de62a8679e0f3981409d24dfa2b371f0d9efb2c3ff07`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Jun 2025 01:01:39 GMT
RUN Install update 10.0.20348.3807
# Thu, 12 Jun 2025 22:40:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Jun 2025 22:40:42 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 12 Jun 2025 22:40:43 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 12 Jun 2025 22:40:44 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.2.2.zip
# Thu, 12 Jun 2025 22:40:53 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 12 Jun 2025 22:40:54 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 12 Jun 2025 22:40:55 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Thu, 12 Jun 2025 22:40:55 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Thu, 12 Jun 2025 22:41:04 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 12 Jun 2025 22:41:05 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Thu, 12 Jun 2025 22:41:05 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-windows-x86_64.exe
# Thu, 12 Jun 2025 22:41:06 GMT
ENV DOCKER_COMPOSE_SHA256=132fb31ef7dc81a82d7b1429adf3fd76cc0a7128059af3a172945445a50f2801
# Thu, 12 Jun 2025 22:41:14 GMT
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
	-	`sha256:e3ce7730719b3563f78c11a86c6e7ca9e7ecab63539d89528367a963b46668ee`  
		Last Modified: Thu, 12 Jun 2025 22:42:44 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa44face37189a26dfbb23b8d5da4e8ec912b0e7403fa7e57fe746ede8ca163`  
		Last Modified: Thu, 12 Jun 2025 22:42:47 GMT  
		Size: 351.9 KB (351892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b288554d751322bcbba469e2992e7ed3d7addecc28b36b87bb0ac57981ad64a`  
		Last Modified: Thu, 12 Jun 2025 22:42:46 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08b3bdb645c2944656eeb7ae7bf819f0cd63f9c83b2677298c9c21d710111eec`  
		Last Modified: Thu, 12 Jun 2025 22:42:47 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b59891c80d4b303cd1655e3255818d7a3cb47a43fe98781999d05abb780b0ed`  
		Last Modified: Thu, 12 Jun 2025 22:42:50 GMT  
		Size: 20.5 MB (20450522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1af8f19e40999102aa31f1f4406c7f15eeb18843036b70938f492dee65f6943`  
		Last Modified: Thu, 12 Jun 2025 22:42:49 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f07268cae3a2cdfcdce7a98218844be1e3ede2baa06062288c10119e5414b06`  
		Last Modified: Thu, 12 Jun 2025 22:42:50 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bea31ae088d4884385e4c9bf2ff15ca1ed5f8581b5d17cba15b96224a1533af`  
		Last Modified: Thu, 12 Jun 2025 22:42:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:428d152391bf0297baa1308e6b7a51fa8dfb41c8f2dd3071d1d21fa3e4f42d41`  
		Last Modified: Thu, 12 Jun 2025 22:42:54 GMT  
		Size: 22.3 MB (22261181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b28b4c745fe11d31b3e00254bc2bc9aec2a58ab17157f558834f43f95a248ea`  
		Last Modified: Thu, 12 Jun 2025 22:42:54 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aa41358ec814cca1a580968a15e80fadcab82f43e7c6b59aea4861acb3c83ad`  
		Last Modified: Thu, 12 Jun 2025 22:42:55 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10bc742c50fda0894e2260bf3f7eb9919c098581d407b6cf2a42e3a41062305b`  
		Last Modified: Thu, 12 Jun 2025 22:42:56 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f06dfd207ec226196bd2af1228c11187c3803b22f4c3f4ac01c21d67d7207e67`  
		Last Modified: Thu, 12 Jun 2025 22:42:58 GMT  
		Size: 22.0 MB (22027759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.2-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:a9266b0f45c2b149896e562c8414e4edc2f32d5f40c73cc8e69a23ce4a967d7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4349; amd64

### `docker:28.2-windowsservercore-ltsc2025` - windows version 10.0.26100.4349; amd64

```console
$ docker pull docker@sha256:87b6c37c78ebd3b4dffee917bf6ba9e8e61722d7cc42313c63bf2204cf297f29
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3541382992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebb204680d5c75607c3a852fb2ef3ed327b9ccc1566c1d6a059cb0259d1a3a22`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 07 Jun 2025 15:42:01 GMT
RUN Install update 10.0.26100.4349
# Thu, 12 Jun 2025 22:41:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Jun 2025 22:41:52 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 12 Jun 2025 22:41:53 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 12 Jun 2025 22:41:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.2.2.zip
# Thu, 12 Jun 2025 22:42:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 12 Jun 2025 22:42:05 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 12 Jun 2025 22:42:06 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Thu, 12 Jun 2025 22:42:06 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Thu, 12 Jun 2025 22:42:16 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 12 Jun 2025 22:42:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Thu, 12 Jun 2025 22:42:17 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-windows-x86_64.exe
# Thu, 12 Jun 2025 22:42:18 GMT
ENV DOCKER_COMPOSE_SHA256=132fb31ef7dc81a82d7b1429adf3fd76cc0a7128059af3a172945445a50f2801
# Thu, 12 Jun 2025 22:42:28 GMT
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
	-	`sha256:7505764e5850853ff3205e21d0c6c05dd9890fed17012225b1f33d9e79ef8f7b`  
		Last Modified: Thu, 12 Jun 2025 22:46:16 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75201e0022107e322d1abb29cdcd607860e0814d97801313713016a804c7ea29`  
		Last Modified: Thu, 12 Jun 2025 22:46:17 GMT  
		Size: 384.3 KB (384281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad1332a299d19362bbb194725e3d76167ba59837dbdb186edc8c88eb4fc584fc`  
		Last Modified: Thu, 12 Jun 2025 22:46:16 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee1c450bb560eb20733ee6f9c9eab001dcdca87a8a976d64320a006b6a8626e`  
		Last Modified: Thu, 12 Jun 2025 22:46:16 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:292280c51cf870fb93a78962a22141e9734918633eac0270479904b4e7fde431`  
		Last Modified: Thu, 12 Jun 2025 22:46:19 GMT  
		Size: 20.5 MB (20474220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce832f815f971edd09a31c7ae7e5e8f1511fd9100e257f6c46649f33661d080d`  
		Last Modified: Thu, 12 Jun 2025 22:46:18 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc0188db691ee242410ed95505f0c2b6bf11c2034274be14cc637917ce9576aa`  
		Last Modified: Thu, 12 Jun 2025 22:46:18 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6d4dfab47701ffe430c0efb0d9f5640976ec9b76c70fa9adf6d9a9e37a7605a`  
		Last Modified: Thu, 12 Jun 2025 22:46:18 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c2ad7bc7d5b79fafe6d4eda10030323f4f485027233019a33343bd50a265a59`  
		Last Modified: Thu, 12 Jun 2025 22:46:21 GMT  
		Size: 22.3 MB (22283596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9538a3dff1be138d1137eb9fc139dbda8255bde275ae8670c13253a3d1033575`  
		Last Modified: Thu, 12 Jun 2025 22:46:19 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfe10fbb6bc6101cc1d7a69d3deb8126160b5db04361e52404e83b438b2fa8b3`  
		Last Modified: Thu, 12 Jun 2025 22:46:20 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2dfee3af3890e8fd03beb55f71a85b48276c6bff5474ae597f001adbd26f779`  
		Last Modified: Thu, 12 Jun 2025 22:46:20 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:846e5ade10ef88ce7e3178a17fc7662922cb37bf8403257413f21ca0869ab29c`  
		Last Modified: Thu, 12 Jun 2025 22:46:23 GMT  
		Size: 22.1 MB (22054925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.2.2`

```console
$ docker pull docker@sha256:ff052514f359111edd920b54581e7aca65629458607f9fbdbf82d7eefbe0602b
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

### `docker:28.2.2` - linux; amd64

```console
$ docker pull docker@sha256:8e32fae437051e392dc31f1bca659a14a6b8f341fa6dd131a9def0a9f315203c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.7 MB (143689092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:896cfe4b7aa87684cdbe7274a5a4efafa80c561662a935bd3a0432e2fcbaf46d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-x86_64'; 			sha256='6777247eb2947c48b46b1fc96602ac17e140fbac84e1043e6384a6c755fc6769'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv6'; 			sha256='1a7731a63ec845b4b4cf2510e68a8f3411386b1e4b5b03916a0d21a697596f03'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv7'; 			sha256='63e64d9aad9916771a947e4b77df6b2a5e70cdfdb412b2f0464806f4d63fabe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-aarch64'; 			sha256='36dfcc81ffff0ec2a76abaa4b66edf01d2db0d7f3fda342a26525eb72e4e9a80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-ppc64le'; 			sha256='4410f045bfc084fef1f0fcea2c3f8e665cad6c5055f57f1089dd009bb9b65151'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-riscv64'; 			sha256='6d551f86c2ab9155882f5a1067223d0c0c80b47669c826af4311c305cc637093'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-s390x'; 			sha256='6012d0bd529312d12937fd153583a90ddb29aec7a7a8cfaac8e7fb7d1ceabf6f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 05 Jun 2025 17:36:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
CMD ["sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
VOLUME [/var/lib/docker]
# Thu, 05 Jun 2025 17:36:11 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
CMD []
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f32e8d6f68009e4f81cdd4d2b7e6465c3cdc96e6addc90132dfdb88d08941a20`  
		Last Modified: Thu, 12 Jun 2025 22:36:53 GMT  
		Size: 8.2 MB (8207474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ac40e43aadc31b56fc943a7df1de7e7f5f06348ca89a108384ba3e9a805a89`  
		Last Modified: Thu, 12 Jun 2025 22:36:53 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3870806677ebd2c8113c069ad6c6f219c456246069bd2688c9cffe6d1736938`  
		Last Modified: Thu, 12 Jun 2025 22:36:55 GMT  
		Size: 20.1 MB (20083028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86f14a0f3d88cab9e631bd4dcf8f9a164306875132f95135fff3358e3a2a8d2`  
		Last Modified: Thu, 12 Jun 2025 22:36:56 GMT  
		Size: 21.3 MB (21290186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da67c6f5f9a3f4626ce69c1328bdacf4c370d20479d084f6415437dea4481db4`  
		Last Modified: Thu, 12 Jun 2025 22:36:56 GMT  
		Size: 21.1 MB (21100670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b94aef2e962e8f653820f39c328e9f31ab7a6e903d929b45f9fb82324f7633`  
		Last Modified: Thu, 12 Jun 2025 22:36:55 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a98583f050f0d3b9242c387626407b4c0affec19be6fafeb1c7135bd7303d86`  
		Last Modified: Thu, 12 Jun 2025 22:36:56 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a115214fbd18e2a1acb4699bd0d7f72d42bf84a1f4cd3d4b1cdae8248a2167fa`  
		Last Modified: Thu, 12 Jun 2025 22:36:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:212150b9078af2b8495b33e957823f54b179f41a22f2702f6fec1560c9d3f6f2`  
		Last Modified: Thu, 12 Jun 2025 23:07:54 GMT  
		Size: 6.9 MB (6905618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9212e721c88d6da1ed4b1e289f523f35a01e01885d1131cd34feceb518227abf`  
		Last Modified: Thu, 12 Jun 2025 23:07:53 GMT  
		Size: 90.5 KB (90494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b0253e449f82e84618065f5b74284cb93f7cc52668795f3590d41585c32012`  
		Last Modified: Thu, 12 Jun 2025 23:07:51 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811b046d83c5b8a6340f19f8d6acd494b2b028f5c1bf969e58cf6f0e350c7cea`  
		Last Modified: Thu, 12 Jun 2025 23:07:58 GMT  
		Size: 62.2 MB (62206627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68771551084500ee9ac3a4b32aa56d78b3d007c1986578b481436becbe8ae1a1`  
		Last Modified: Thu, 12 Jun 2025 23:07:51 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cae381f867a74a59e0d18562bd189fcc3560935254e57ceb2e247145c467a8b`  
		Last Modified: Thu, 12 Jun 2025 23:07:52 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2.2` - unknown; unknown

```console
$ docker pull docker@sha256:4c5431982a6f26acafc9a647e2a915e12fd2cb54c0d9fa6f5bed94ca07e186b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a1e46faf2561239606e7d796aac2f70a1bc3754ba1ff7200c43154e973515c8`

```dockerfile
```

-	Layers:
	-	`sha256:d5158885bee456f124624bc8808ba3f4ea82fc7ca56f260044b4d92a684498b1`  
		Last Modified: Fri, 13 Jun 2025 02:07:20 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.2.2` - linux; arm variant v6

```console
$ docker pull docker@sha256:d692f151518fae2760b09152001cfba45f8bc770e1906d190d6eb2e3142b1a76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134722094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44d698360caa93e31e5563c2c622bbbeb75bd82d597a599776298366deb6aa32`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-x86_64'; 			sha256='6777247eb2947c48b46b1fc96602ac17e140fbac84e1043e6384a6c755fc6769'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv6'; 			sha256='1a7731a63ec845b4b4cf2510e68a8f3411386b1e4b5b03916a0d21a697596f03'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv7'; 			sha256='63e64d9aad9916771a947e4b77df6b2a5e70cdfdb412b2f0464806f4d63fabe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-aarch64'; 			sha256='36dfcc81ffff0ec2a76abaa4b66edf01d2db0d7f3fda342a26525eb72e4e9a80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-ppc64le'; 			sha256='4410f045bfc084fef1f0fcea2c3f8e665cad6c5055f57f1089dd009bb9b65151'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-riscv64'; 			sha256='6d551f86c2ab9155882f5a1067223d0c0c80b47669c826af4311c305cc637093'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-s390x'; 			sha256='6012d0bd529312d12937fd153583a90ddb29aec7a7a8cfaac8e7fb7d1ceabf6f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 05 Jun 2025 17:36:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
CMD ["sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
VOLUME [/var/lib/docker]
# Thu, 05 Jun 2025 17:36:11 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
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
	-	`sha256:3156c3bcd5598f721d5e807804df7256e282bd2897ea9f9f029b3cd93a5ff79b`  
		Last Modified: Thu, 05 Jun 2025 22:44:12 GMT  
		Size: 18.1 MB (18101909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:225abe8edcfa38ed05c3678afaa3fc7019381a300f823c874d6fdfd2a372c345`  
		Last Modified: Thu, 05 Jun 2025 22:44:12 GMT  
		Size: 19.9 MB (19943271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aaa4a492c5a8c6019873f7f10f4583b9134c81a74df09c55d664e88521c254c`  
		Last Modified: Thu, 12 Jun 2025 22:36:39 GMT  
		Size: 19.8 MB (19835400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d441ddcc7f77e2457e59e55a8a824b3b189eaa5a13fdaf65a914da194d6919b`  
		Last Modified: Thu, 12 Jun 2025 22:36:37 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c28d4afadc6fad8c6238b24d9a8dad8f8e7a8deb80839c1d3459890592b523f2`  
		Last Modified: Thu, 12 Jun 2025 22:36:38 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ebbefe72ea0510e4b225079670e073211f0b85e0fc4be94f42ca4ea57d54248`  
		Last Modified: Thu, 12 Jun 2025 22:36:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8241b18dc7eb679233e3250bbfb077dcd4f8778550fe3188d80dd91b7838a9bd`  
		Last Modified: Thu, 12 Jun 2025 22:54:58 GMT  
		Size: 7.2 MB (7230354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3cf946673d9726b4c5b57734c7dbf2e2e811f1b40e437ce7cc7bf5533df26a`  
		Last Modified: Thu, 12 Jun 2025 22:54:57 GMT  
		Size: 90.1 KB (90058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d08132e8b60b557ae762a779e816c58c6c366efd53ded71c9275533c8ec8f2d`  
		Last Modified: Thu, 12 Jun 2025 22:54:57 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d611e6743d4f047d30c66012bbac54fc821dc2ffefbbe8277a53e70060da2356`  
		Last Modified: Thu, 12 Jun 2025 22:55:00 GMT  
		Size: 57.9 MB (57897340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a783e6fb91bba730335ac30fbd49b93258f2e4d9d4c2a73dbe5c7663e5f497`  
		Last Modified: Thu, 12 Jun 2025 22:54:57 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b45b886f9c1b0ecbf83201757d3e791047d9cd0cbbdfc865a112256becf21ce4`  
		Last Modified: Thu, 12 Jun 2025 22:54:58 GMT  
		Size: 3.3 KB (3304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2.2` - unknown; unknown

```console
$ docker pull docker@sha256:d1a670e4e107e2e31f275813f1751ac249dec91fa3cfc6cc949e581bdb0c364e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb88dd0bcd267d48fad2fe5722c0bc382d70b8aa328b8a911562dc8081e3809d`

```dockerfile
```

-	Layers:
	-	`sha256:c75371d2b5d03d6fe0926a467c9d353d590b6db0765b2bc492cb0184dfe50817`  
		Last Modified: Thu, 12 Jun 2025 23:07:42 GMT  
		Size: 34.8 KB (34765 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.2.2` - linux; arm variant v7

```console
$ docker pull docker@sha256:66277612b6b4d8230b45b06074b5716e61c90fee840cf8b7b4da8208329fe9d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.0 MB (133027832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55fe29bbf4d101c05a3d55a85a71baf6c7ae07a62cc6865b2fc5b8902a5978a6`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-x86_64'; 			sha256='6777247eb2947c48b46b1fc96602ac17e140fbac84e1043e6384a6c755fc6769'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv6'; 			sha256='1a7731a63ec845b4b4cf2510e68a8f3411386b1e4b5b03916a0d21a697596f03'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv7'; 			sha256='63e64d9aad9916771a947e4b77df6b2a5e70cdfdb412b2f0464806f4d63fabe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-aarch64'; 			sha256='36dfcc81ffff0ec2a76abaa4b66edf01d2db0d7f3fda342a26525eb72e4e9a80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-ppc64le'; 			sha256='4410f045bfc084fef1f0fcea2c3f8e665cad6c5055f57f1089dd009bb9b65151'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-riscv64'; 			sha256='6d551f86c2ab9155882f5a1067223d0c0c80b47669c826af4311c305cc637093'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-s390x'; 			sha256='6012d0bd529312d12937fd153583a90ddb29aec7a7a8cfaac8e7fb7d1ceabf6f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 05 Jun 2025 17:36:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
CMD ["sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
VOLUME [/var/lib/docker]
# Thu, 05 Jun 2025 17:36:11 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
CMD []
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b30f7212c67694cf480811a55ca551c13acaf23308660855c528140f72c862`  
		Last Modified: Fri, 13 Jun 2025 01:20:06 GMT  
		Size: 7.4 MB (7440617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3fca8ac4e435f25c24efea81db3a20417fad9d7c421bee5ce9e3b58996c8efa`  
		Last Modified: Fri, 13 Jun 2025 01:20:05 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68a306e9551e1b17a6ecb71be8147d67ef4f891736c4e69faee945e235107fc`  
		Last Modified: Fri, 13 Jun 2025 01:20:06 GMT  
		Size: 18.1 MB (18089377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44e8dff8b0583db9cb4fc33b75dec6c3d09dd8ce3a76c2a78fd8af411bce92c`  
		Last Modified: Fri, 13 Jun 2025 01:20:08 GMT  
		Size: 19.9 MB (19927230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c665168123ed7a9acc312ff431c35318ee6393642e3e2a8bb7fa2845208b64aa`  
		Last Modified: Fri, 13 Jun 2025 01:20:08 GMT  
		Size: 19.8 MB (19821284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f454bde5fc9b6055cf7fe14c89d2a03739341ccdde89409892b34630a79576`  
		Last Modified: Fri, 13 Jun 2025 01:26:31 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3159ba7c72c13cd717ca59937ae54ce16c3ef91f409e6ff1eb4ab88fc1db06c0`  
		Last Modified: Fri, 13 Jun 2025 01:26:33 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ef5f44369f56ae39826aaf9f89b54c9bf2d4d09a86c4eaf7af04c279812997`  
		Last Modified: Fri, 13 Jun 2025 01:26:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7236561f33fb7c50ca5d7c37b075afc53fe8e4088c95319dcde0bb8ad917eb0`  
		Last Modified: Fri, 13 Jun 2025 06:24:34 GMT  
		Size: 6.5 MB (6538120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98752e61e2dd86e562ed8c9de46d0e71b38f35fe7be163828be059624970c9e`  
		Last Modified: Fri, 13 Jun 2025 06:24:35 GMT  
		Size: 86.5 KB (86488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c1e6adc4b8f7742b913355688fb6e8dd3671bd9c49551a76f2dad8f0bfcf827`  
		Last Modified: Fri, 13 Jun 2025 06:24:35 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7760efd1d6901a24ed3199cf41b66c116f64c11736dcecc92c75040a0f68dea9`  
		Last Modified: Fri, 13 Jun 2025 06:24:39 GMT  
		Size: 57.9 MB (57897375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb6cd2d2e0725f775e9f508d900bb8bac548036c111ea8957a933fc7002b93e`  
		Last Modified: Fri, 13 Jun 2025 06:24:36 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcd8d4be9dc74189aefe21d876aec06706ad1fa1e7597dd49f2c2fc862477c51`  
		Last Modified: Fri, 13 Jun 2025 06:24:36 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2.2` - unknown; unknown

```console
$ docker pull docker@sha256:9c4cb9730947a3df8f10cb2052f42e9556fa8a3d55b8d9eb9df923d7467c4a6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4fa8b980b9e0ff354efd1a786e8ee1816d49966e8cb7f6c93a8a7182923f7fd`

```dockerfile
```

-	Layers:
	-	`sha256:4bc11f3d388f7184ad2e3f2d7090c73f569bc734a2691321b72cdcb0e3735d28`  
		Last Modified: Fri, 13 Jun 2025 08:07:23 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.2.2` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:b8d1c58eea384111a2c6646a55d6c57e11ce3527c44b26b17ba91e00f82530c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.5 MB (134502165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f7a08861e83333223ac02d5357e4d77380c819b320b98b1811d33973cd4cd5e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-x86_64'; 			sha256='6777247eb2947c48b46b1fc96602ac17e140fbac84e1043e6384a6c755fc6769'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv6'; 			sha256='1a7731a63ec845b4b4cf2510e68a8f3411386b1e4b5b03916a0d21a697596f03'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv7'; 			sha256='63e64d9aad9916771a947e4b77df6b2a5e70cdfdb412b2f0464806f4d63fabe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-aarch64'; 			sha256='36dfcc81ffff0ec2a76abaa4b66edf01d2db0d7f3fda342a26525eb72e4e9a80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-ppc64le'; 			sha256='4410f045bfc084fef1f0fcea2c3f8e665cad6c5055f57f1089dd009bb9b65151'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-riscv64'; 			sha256='6d551f86c2ab9155882f5a1067223d0c0c80b47669c826af4311c305cc637093'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-s390x'; 			sha256='6012d0bd529312d12937fd153583a90ddb29aec7a7a8cfaac8e7fb7d1ceabf6f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 05 Jun 2025 17:36:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
CMD ["sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
VOLUME [/var/lib/docker]
# Thu, 05 Jun 2025 17:36:11 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
CMD []
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375cb5234cd1a2b6b8f1aba00c28fc5d45ba0ecc0d3c8f130d5cdb5138ba6c09`  
		Last Modified: Fri, 13 Jun 2025 00:09:12 GMT  
		Size: 8.2 MB (8229005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ba114b122014764181bf833228533908f5eedbccce11b62f71d746ab1616ccc`  
		Last Modified: Fri, 13 Jun 2025 00:09:12 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5090356630719947eb3cfc865b4d6d8f4971f5e40c640070edd88a16ab0c486f`  
		Last Modified: Fri, 13 Jun 2025 00:09:13 GMT  
		Size: 18.9 MB (18902609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd89b3ff82b93c434d43d799f7f56e86b96409535e06f30c6bbc54456e99752d`  
		Last Modified: Fri, 13 Jun 2025 00:09:14 GMT  
		Size: 19.5 MB (19469847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb8a2de00a4f86825ec25a2f3ac1553ace626f97f529f17cda507233ec8f1a9a`  
		Last Modified: Fri, 13 Jun 2025 00:09:14 GMT  
		Size: 19.3 MB (19347260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ced3983ecfb78d04b5aefc0cf90f4a0b3ccd62ec5610841b0f7860259defda`  
		Last Modified: Fri, 13 Jun 2025 00:09:13 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3673e39b233f3bfe295c08f11dda44b40d801a0bb4f299fe81e1ec50851575`  
		Last Modified: Fri, 13 Jun 2025 00:09:13 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b219e20a46cafa0737e015b21a2525d3bb013d26dc4af6849c8f3586a8b10c5f`  
		Last Modified: Fri, 13 Jun 2025 00:09:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c6e05695096db67c5e6426307e8a652c5311da73d994e47d9580e886b837a10`  
		Last Modified: Fri, 13 Jun 2025 04:27:25 GMT  
		Size: 7.1 MB (7141507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891d71d9754311d78a8a473d578e3825acd68ce42cd0dbc623f6357a4e17c72b`  
		Last Modified: Fri, 13 Jun 2025 04:27:25 GMT  
		Size: 99.6 KB (99645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5d9a3e9b7f7718caa1aba176d0c009906cfdbf0beaabb63840d5743b89cc7f2`  
		Last Modified: Fri, 13 Jun 2025 04:27:26 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d489b833d40920f79c54667b28c6b5c28475bbdb198a31284fb082206828119a`  
		Last Modified: Fri, 13 Jun 2025 04:27:32 GMT  
		Size: 57.2 MB (57168194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e7d0e57cac200e9cb81bab37725356fb62116b7b3fb40855e245e59124702f2`  
		Last Modified: Fri, 13 Jun 2025 04:27:27 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc40c4cf8ec0a96212d48ae432d6342b219db9566141690970349c4e6140886`  
		Last Modified: Fri, 13 Jun 2025 04:27:27 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2.2` - unknown; unknown

```console
$ docker pull docker@sha256:e64e322c1cc45566807e6054fb529a1b90018a74d5599c9e524013622d5fd800
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30148cdfe5f84f758ae82d1f85d34d65c6e91c5167340993eaa3d924e06041f5`

```dockerfile
```

-	Layers:
	-	`sha256:a0dd369778c470b4b56994e10a017cc701a049c277738705f244ac7e5856bdd4`  
		Last Modified: Fri, 13 Jun 2025 05:07:36 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.2.2-alpine3.22`

```console
$ docker pull docker@sha256:ff052514f359111edd920b54581e7aca65629458607f9fbdbf82d7eefbe0602b
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

### `docker:28.2.2-alpine3.22` - linux; amd64

```console
$ docker pull docker@sha256:8e32fae437051e392dc31f1bca659a14a6b8f341fa6dd131a9def0a9f315203c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.7 MB (143689092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:896cfe4b7aa87684cdbe7274a5a4efafa80c561662a935bd3a0432e2fcbaf46d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-x86_64'; 			sha256='6777247eb2947c48b46b1fc96602ac17e140fbac84e1043e6384a6c755fc6769'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv6'; 			sha256='1a7731a63ec845b4b4cf2510e68a8f3411386b1e4b5b03916a0d21a697596f03'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv7'; 			sha256='63e64d9aad9916771a947e4b77df6b2a5e70cdfdb412b2f0464806f4d63fabe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-aarch64'; 			sha256='36dfcc81ffff0ec2a76abaa4b66edf01d2db0d7f3fda342a26525eb72e4e9a80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-ppc64le'; 			sha256='4410f045bfc084fef1f0fcea2c3f8e665cad6c5055f57f1089dd009bb9b65151'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-riscv64'; 			sha256='6d551f86c2ab9155882f5a1067223d0c0c80b47669c826af4311c305cc637093'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-s390x'; 			sha256='6012d0bd529312d12937fd153583a90ddb29aec7a7a8cfaac8e7fb7d1ceabf6f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 05 Jun 2025 17:36:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
CMD ["sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
VOLUME [/var/lib/docker]
# Thu, 05 Jun 2025 17:36:11 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
CMD []
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f32e8d6f68009e4f81cdd4d2b7e6465c3cdc96e6addc90132dfdb88d08941a20`  
		Last Modified: Thu, 12 Jun 2025 22:36:53 GMT  
		Size: 8.2 MB (8207474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ac40e43aadc31b56fc943a7df1de7e7f5f06348ca89a108384ba3e9a805a89`  
		Last Modified: Thu, 12 Jun 2025 22:36:53 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3870806677ebd2c8113c069ad6c6f219c456246069bd2688c9cffe6d1736938`  
		Last Modified: Thu, 12 Jun 2025 22:36:55 GMT  
		Size: 20.1 MB (20083028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86f14a0f3d88cab9e631bd4dcf8f9a164306875132f95135fff3358e3a2a8d2`  
		Last Modified: Thu, 12 Jun 2025 22:36:56 GMT  
		Size: 21.3 MB (21290186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da67c6f5f9a3f4626ce69c1328bdacf4c370d20479d084f6415437dea4481db4`  
		Last Modified: Thu, 12 Jun 2025 22:36:56 GMT  
		Size: 21.1 MB (21100670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b94aef2e962e8f653820f39c328e9f31ab7a6e903d929b45f9fb82324f7633`  
		Last Modified: Thu, 12 Jun 2025 22:36:55 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a98583f050f0d3b9242c387626407b4c0affec19be6fafeb1c7135bd7303d86`  
		Last Modified: Thu, 12 Jun 2025 22:36:56 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a115214fbd18e2a1acb4699bd0d7f72d42bf84a1f4cd3d4b1cdae8248a2167fa`  
		Last Modified: Thu, 12 Jun 2025 22:36:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:212150b9078af2b8495b33e957823f54b179f41a22f2702f6fec1560c9d3f6f2`  
		Last Modified: Thu, 12 Jun 2025 23:07:54 GMT  
		Size: 6.9 MB (6905618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9212e721c88d6da1ed4b1e289f523f35a01e01885d1131cd34feceb518227abf`  
		Last Modified: Thu, 12 Jun 2025 23:07:53 GMT  
		Size: 90.5 KB (90494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b0253e449f82e84618065f5b74284cb93f7cc52668795f3590d41585c32012`  
		Last Modified: Thu, 12 Jun 2025 23:07:51 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811b046d83c5b8a6340f19f8d6acd494b2b028f5c1bf969e58cf6f0e350c7cea`  
		Last Modified: Thu, 12 Jun 2025 23:07:58 GMT  
		Size: 62.2 MB (62206627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68771551084500ee9ac3a4b32aa56d78b3d007c1986578b481436becbe8ae1a1`  
		Last Modified: Thu, 12 Jun 2025 23:07:51 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cae381f867a74a59e0d18562bd189fcc3560935254e57ceb2e247145c467a8b`  
		Last Modified: Thu, 12 Jun 2025 23:07:52 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2.2-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:4c5431982a6f26acafc9a647e2a915e12fd2cb54c0d9fa6f5bed94ca07e186b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a1e46faf2561239606e7d796aac2f70a1bc3754ba1ff7200c43154e973515c8`

```dockerfile
```

-	Layers:
	-	`sha256:d5158885bee456f124624bc8808ba3f4ea82fc7ca56f260044b4d92a684498b1`  
		Last Modified: Fri, 13 Jun 2025 02:07:20 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.2.2-alpine3.22` - linux; arm variant v6

```console
$ docker pull docker@sha256:d692f151518fae2760b09152001cfba45f8bc770e1906d190d6eb2e3142b1a76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134722094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44d698360caa93e31e5563c2c622bbbeb75bd82d597a599776298366deb6aa32`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-x86_64'; 			sha256='6777247eb2947c48b46b1fc96602ac17e140fbac84e1043e6384a6c755fc6769'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv6'; 			sha256='1a7731a63ec845b4b4cf2510e68a8f3411386b1e4b5b03916a0d21a697596f03'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv7'; 			sha256='63e64d9aad9916771a947e4b77df6b2a5e70cdfdb412b2f0464806f4d63fabe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-aarch64'; 			sha256='36dfcc81ffff0ec2a76abaa4b66edf01d2db0d7f3fda342a26525eb72e4e9a80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-ppc64le'; 			sha256='4410f045bfc084fef1f0fcea2c3f8e665cad6c5055f57f1089dd009bb9b65151'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-riscv64'; 			sha256='6d551f86c2ab9155882f5a1067223d0c0c80b47669c826af4311c305cc637093'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-s390x'; 			sha256='6012d0bd529312d12937fd153583a90ddb29aec7a7a8cfaac8e7fb7d1ceabf6f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 05 Jun 2025 17:36:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
CMD ["sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
VOLUME [/var/lib/docker]
# Thu, 05 Jun 2025 17:36:11 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
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
	-	`sha256:3156c3bcd5598f721d5e807804df7256e282bd2897ea9f9f029b3cd93a5ff79b`  
		Last Modified: Thu, 05 Jun 2025 22:44:12 GMT  
		Size: 18.1 MB (18101909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:225abe8edcfa38ed05c3678afaa3fc7019381a300f823c874d6fdfd2a372c345`  
		Last Modified: Thu, 05 Jun 2025 22:44:12 GMT  
		Size: 19.9 MB (19943271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aaa4a492c5a8c6019873f7f10f4583b9134c81a74df09c55d664e88521c254c`  
		Last Modified: Thu, 12 Jun 2025 22:36:39 GMT  
		Size: 19.8 MB (19835400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d441ddcc7f77e2457e59e55a8a824b3b189eaa5a13fdaf65a914da194d6919b`  
		Last Modified: Thu, 12 Jun 2025 22:36:37 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c28d4afadc6fad8c6238b24d9a8dad8f8e7a8deb80839c1d3459890592b523f2`  
		Last Modified: Thu, 12 Jun 2025 22:36:38 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ebbefe72ea0510e4b225079670e073211f0b85e0fc4be94f42ca4ea57d54248`  
		Last Modified: Thu, 12 Jun 2025 22:36:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8241b18dc7eb679233e3250bbfb077dcd4f8778550fe3188d80dd91b7838a9bd`  
		Last Modified: Thu, 12 Jun 2025 22:54:58 GMT  
		Size: 7.2 MB (7230354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3cf946673d9726b4c5b57734c7dbf2e2e811f1b40e437ce7cc7bf5533df26a`  
		Last Modified: Thu, 12 Jun 2025 22:54:57 GMT  
		Size: 90.1 KB (90058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d08132e8b60b557ae762a779e816c58c6c366efd53ded71c9275533c8ec8f2d`  
		Last Modified: Thu, 12 Jun 2025 22:54:57 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d611e6743d4f047d30c66012bbac54fc821dc2ffefbbe8277a53e70060da2356`  
		Last Modified: Thu, 12 Jun 2025 22:55:00 GMT  
		Size: 57.9 MB (57897340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a783e6fb91bba730335ac30fbd49b93258f2e4d9d4c2a73dbe5c7663e5f497`  
		Last Modified: Thu, 12 Jun 2025 22:54:57 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b45b886f9c1b0ecbf83201757d3e791047d9cd0cbbdfc865a112256becf21ce4`  
		Last Modified: Thu, 12 Jun 2025 22:54:58 GMT  
		Size: 3.3 KB (3304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2.2-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:d1a670e4e107e2e31f275813f1751ac249dec91fa3cfc6cc949e581bdb0c364e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb88dd0bcd267d48fad2fe5722c0bc382d70b8aa328b8a911562dc8081e3809d`

```dockerfile
```

-	Layers:
	-	`sha256:c75371d2b5d03d6fe0926a467c9d353d590b6db0765b2bc492cb0184dfe50817`  
		Last Modified: Thu, 12 Jun 2025 23:07:42 GMT  
		Size: 34.8 KB (34765 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.2.2-alpine3.22` - linux; arm variant v7

```console
$ docker pull docker@sha256:66277612b6b4d8230b45b06074b5716e61c90fee840cf8b7b4da8208329fe9d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.0 MB (133027832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55fe29bbf4d101c05a3d55a85a71baf6c7ae07a62cc6865b2fc5b8902a5978a6`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-x86_64'; 			sha256='6777247eb2947c48b46b1fc96602ac17e140fbac84e1043e6384a6c755fc6769'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv6'; 			sha256='1a7731a63ec845b4b4cf2510e68a8f3411386b1e4b5b03916a0d21a697596f03'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv7'; 			sha256='63e64d9aad9916771a947e4b77df6b2a5e70cdfdb412b2f0464806f4d63fabe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-aarch64'; 			sha256='36dfcc81ffff0ec2a76abaa4b66edf01d2db0d7f3fda342a26525eb72e4e9a80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-ppc64le'; 			sha256='4410f045bfc084fef1f0fcea2c3f8e665cad6c5055f57f1089dd009bb9b65151'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-riscv64'; 			sha256='6d551f86c2ab9155882f5a1067223d0c0c80b47669c826af4311c305cc637093'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-s390x'; 			sha256='6012d0bd529312d12937fd153583a90ddb29aec7a7a8cfaac8e7fb7d1ceabf6f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 05 Jun 2025 17:36:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
CMD ["sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
VOLUME [/var/lib/docker]
# Thu, 05 Jun 2025 17:36:11 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
CMD []
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b30f7212c67694cf480811a55ca551c13acaf23308660855c528140f72c862`  
		Last Modified: Fri, 13 Jun 2025 01:20:06 GMT  
		Size: 7.4 MB (7440617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3fca8ac4e435f25c24efea81db3a20417fad9d7c421bee5ce9e3b58996c8efa`  
		Last Modified: Fri, 13 Jun 2025 01:20:05 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68a306e9551e1b17a6ecb71be8147d67ef4f891736c4e69faee945e235107fc`  
		Last Modified: Fri, 13 Jun 2025 01:20:06 GMT  
		Size: 18.1 MB (18089377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44e8dff8b0583db9cb4fc33b75dec6c3d09dd8ce3a76c2a78fd8af411bce92c`  
		Last Modified: Fri, 13 Jun 2025 01:20:08 GMT  
		Size: 19.9 MB (19927230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c665168123ed7a9acc312ff431c35318ee6393642e3e2a8bb7fa2845208b64aa`  
		Last Modified: Fri, 13 Jun 2025 01:20:08 GMT  
		Size: 19.8 MB (19821284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f454bde5fc9b6055cf7fe14c89d2a03739341ccdde89409892b34630a79576`  
		Last Modified: Fri, 13 Jun 2025 01:26:31 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3159ba7c72c13cd717ca59937ae54ce16c3ef91f409e6ff1eb4ab88fc1db06c0`  
		Last Modified: Fri, 13 Jun 2025 01:26:33 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ef5f44369f56ae39826aaf9f89b54c9bf2d4d09a86c4eaf7af04c279812997`  
		Last Modified: Fri, 13 Jun 2025 01:26:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7236561f33fb7c50ca5d7c37b075afc53fe8e4088c95319dcde0bb8ad917eb0`  
		Last Modified: Fri, 13 Jun 2025 06:24:34 GMT  
		Size: 6.5 MB (6538120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98752e61e2dd86e562ed8c9de46d0e71b38f35fe7be163828be059624970c9e`  
		Last Modified: Fri, 13 Jun 2025 06:24:35 GMT  
		Size: 86.5 KB (86488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c1e6adc4b8f7742b913355688fb6e8dd3671bd9c49551a76f2dad8f0bfcf827`  
		Last Modified: Fri, 13 Jun 2025 06:24:35 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7760efd1d6901a24ed3199cf41b66c116f64c11736dcecc92c75040a0f68dea9`  
		Last Modified: Fri, 13 Jun 2025 06:24:39 GMT  
		Size: 57.9 MB (57897375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb6cd2d2e0725f775e9f508d900bb8bac548036c111ea8957a933fc7002b93e`  
		Last Modified: Fri, 13 Jun 2025 06:24:36 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcd8d4be9dc74189aefe21d876aec06706ad1fa1e7597dd49f2c2fc862477c51`  
		Last Modified: Fri, 13 Jun 2025 06:24:36 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2.2-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:9c4cb9730947a3df8f10cb2052f42e9556fa8a3d55b8d9eb9df923d7467c4a6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4fa8b980b9e0ff354efd1a786e8ee1816d49966e8cb7f6c93a8a7182923f7fd`

```dockerfile
```

-	Layers:
	-	`sha256:4bc11f3d388f7184ad2e3f2d7090c73f569bc734a2691321b72cdcb0e3735d28`  
		Last Modified: Fri, 13 Jun 2025 08:07:23 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.2.2-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:b8d1c58eea384111a2c6646a55d6c57e11ce3527c44b26b17ba91e00f82530c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.5 MB (134502165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f7a08861e83333223ac02d5357e4d77380c819b320b98b1811d33973cd4cd5e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-x86_64'; 			sha256='6777247eb2947c48b46b1fc96602ac17e140fbac84e1043e6384a6c755fc6769'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv6'; 			sha256='1a7731a63ec845b4b4cf2510e68a8f3411386b1e4b5b03916a0d21a697596f03'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv7'; 			sha256='63e64d9aad9916771a947e4b77df6b2a5e70cdfdb412b2f0464806f4d63fabe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-aarch64'; 			sha256='36dfcc81ffff0ec2a76abaa4b66edf01d2db0d7f3fda342a26525eb72e4e9a80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-ppc64le'; 			sha256='4410f045bfc084fef1f0fcea2c3f8e665cad6c5055f57f1089dd009bb9b65151'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-riscv64'; 			sha256='6d551f86c2ab9155882f5a1067223d0c0c80b47669c826af4311c305cc637093'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-s390x'; 			sha256='6012d0bd529312d12937fd153583a90ddb29aec7a7a8cfaac8e7fb7d1ceabf6f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 05 Jun 2025 17:36:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
CMD ["sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
VOLUME [/var/lib/docker]
# Thu, 05 Jun 2025 17:36:11 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
CMD []
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375cb5234cd1a2b6b8f1aba00c28fc5d45ba0ecc0d3c8f130d5cdb5138ba6c09`  
		Last Modified: Fri, 13 Jun 2025 00:09:12 GMT  
		Size: 8.2 MB (8229005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ba114b122014764181bf833228533908f5eedbccce11b62f71d746ab1616ccc`  
		Last Modified: Fri, 13 Jun 2025 00:09:12 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5090356630719947eb3cfc865b4d6d8f4971f5e40c640070edd88a16ab0c486f`  
		Last Modified: Fri, 13 Jun 2025 00:09:13 GMT  
		Size: 18.9 MB (18902609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd89b3ff82b93c434d43d799f7f56e86b96409535e06f30c6bbc54456e99752d`  
		Last Modified: Fri, 13 Jun 2025 00:09:14 GMT  
		Size: 19.5 MB (19469847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb8a2de00a4f86825ec25a2f3ac1553ace626f97f529f17cda507233ec8f1a9a`  
		Last Modified: Fri, 13 Jun 2025 00:09:14 GMT  
		Size: 19.3 MB (19347260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ced3983ecfb78d04b5aefc0cf90f4a0b3ccd62ec5610841b0f7860259defda`  
		Last Modified: Fri, 13 Jun 2025 00:09:13 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3673e39b233f3bfe295c08f11dda44b40d801a0bb4f299fe81e1ec50851575`  
		Last Modified: Fri, 13 Jun 2025 00:09:13 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b219e20a46cafa0737e015b21a2525d3bb013d26dc4af6849c8f3586a8b10c5f`  
		Last Modified: Fri, 13 Jun 2025 00:09:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c6e05695096db67c5e6426307e8a652c5311da73d994e47d9580e886b837a10`  
		Last Modified: Fri, 13 Jun 2025 04:27:25 GMT  
		Size: 7.1 MB (7141507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891d71d9754311d78a8a473d578e3825acd68ce42cd0dbc623f6357a4e17c72b`  
		Last Modified: Fri, 13 Jun 2025 04:27:25 GMT  
		Size: 99.6 KB (99645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5d9a3e9b7f7718caa1aba176d0c009906cfdbf0beaabb63840d5743b89cc7f2`  
		Last Modified: Fri, 13 Jun 2025 04:27:26 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d489b833d40920f79c54667b28c6b5c28475bbdb198a31284fb082206828119a`  
		Last Modified: Fri, 13 Jun 2025 04:27:32 GMT  
		Size: 57.2 MB (57168194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e7d0e57cac200e9cb81bab37725356fb62116b7b3fb40855e245e59124702f2`  
		Last Modified: Fri, 13 Jun 2025 04:27:27 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc40c4cf8ec0a96212d48ae432d6342b219db9566141690970349c4e6140886`  
		Last Modified: Fri, 13 Jun 2025 04:27:27 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2.2-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:e64e322c1cc45566807e6054fb529a1b90018a74d5599c9e524013622d5fd800
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30148cdfe5f84f758ae82d1f85d34d65c6e91c5167340993eaa3d924e06041f5`

```dockerfile
```

-	Layers:
	-	`sha256:a0dd369778c470b4b56994e10a017cc701a049c277738705f244ac7e5856bdd4`  
		Last Modified: Fri, 13 Jun 2025 05:07:36 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.2.2-cli`

```console
$ docker pull docker@sha256:5d3725f5d2f52aafe8a2c49668a43eb7c681a5535a206ba28eccfd8a3013de86
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

### `docker:28.2.2-cli` - linux; amd64

```console
$ docker pull docker@sha256:b65ad6989d6333212ce011be9684e2d8ae545ec1972b56588c7aff01dd3520d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74480359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c47dbf8612e5f69d7a6b634668d1fc578e0eca340ae1f8a00812e89d72e021a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 12 Jun 2025 11:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-x86_64'; 			sha256='6777247eb2947c48b46b1fc96602ac17e140fbac84e1043e6384a6c755fc6769'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv6'; 			sha256='1a7731a63ec845b4b4cf2510e68a8f3411386b1e4b5b03916a0d21a697596f03'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv7'; 			sha256='63e64d9aad9916771a947e4b77df6b2a5e70cdfdb412b2f0464806f4d63fabe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-aarch64'; 			sha256='36dfcc81ffff0ec2a76abaa4b66edf01d2db0d7f3fda342a26525eb72e4e9a80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-ppc64le'; 			sha256='4410f045bfc084fef1f0fcea2c3f8e665cad6c5055f57f1089dd009bb9b65151'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-riscv64'; 			sha256='6d551f86c2ab9155882f5a1067223d0c0c80b47669c826af4311c305cc637093'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-s390x'; 			sha256='6012d0bd529312d12937fd153583a90ddb29aec7a7a8cfaac8e7fb7d1ceabf6f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 12 Jun 2025 11:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Jun 2025 11:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f32e8d6f68009e4f81cdd4d2b7e6465c3cdc96e6addc90132dfdb88d08941a20`  
		Last Modified: Thu, 12 Jun 2025 22:36:53 GMT  
		Size: 8.2 MB (8207474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ac40e43aadc31b56fc943a7df1de7e7f5f06348ca89a108384ba3e9a805a89`  
		Last Modified: Thu, 12 Jun 2025 22:36:53 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3870806677ebd2c8113c069ad6c6f219c456246069bd2688c9cffe6d1736938`  
		Last Modified: Thu, 12 Jun 2025 22:36:55 GMT  
		Size: 20.1 MB (20083028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86f14a0f3d88cab9e631bd4dcf8f9a164306875132f95135fff3358e3a2a8d2`  
		Last Modified: Thu, 12 Jun 2025 22:36:56 GMT  
		Size: 21.3 MB (21290186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da67c6f5f9a3f4626ce69c1328bdacf4c370d20479d084f6415437dea4481db4`  
		Last Modified: Thu, 12 Jun 2025 22:36:56 GMT  
		Size: 21.1 MB (21100670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b94aef2e962e8f653820f39c328e9f31ab7a6e903d929b45f9fb82324f7633`  
		Last Modified: Thu, 12 Jun 2025 22:36:55 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a98583f050f0d3b9242c387626407b4c0affec19be6fafeb1c7135bd7303d86`  
		Last Modified: Thu, 12 Jun 2025 22:36:56 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a115214fbd18e2a1acb4699bd0d7f72d42bf84a1f4cd3d4b1cdae8248a2167fa`  
		Last Modified: Thu, 12 Jun 2025 22:36:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2.2-cli` - unknown; unknown

```console
$ docker pull docker@sha256:1ebe76e61490c161294dbf222ba3f54e20b9c4ef88e3a419b69d6c9ea30d9cee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adb69d08e123464b3d3e1ca5fc247dafb6079c23e370b419c72f645720be223f`

```dockerfile
```

-	Layers:
	-	`sha256:c968c006dcee70140b54235857f7cdddd7486443dbd3175f36530d5404ebc8e2`  
		Last Modified: Thu, 12 Jun 2025 23:07:35 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.2.2-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:cbf1afecf10a316254346c8400aefe8e45ec33d0ca7d37e94acaf8df4c243108
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69498335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4b21f5d310fad2488ce7f6f0798a746c1018659fb7fce6a3975ebe40ba17364`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 12 Jun 2025 11:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-x86_64'; 			sha256='6777247eb2947c48b46b1fc96602ac17e140fbac84e1043e6384a6c755fc6769'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv6'; 			sha256='1a7731a63ec845b4b4cf2510e68a8f3411386b1e4b5b03916a0d21a697596f03'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv7'; 			sha256='63e64d9aad9916771a947e4b77df6b2a5e70cdfdb412b2f0464806f4d63fabe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-aarch64'; 			sha256='36dfcc81ffff0ec2a76abaa4b66edf01d2db0d7f3fda342a26525eb72e4e9a80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-ppc64le'; 			sha256='4410f045bfc084fef1f0fcea2c3f8e665cad6c5055f57f1089dd009bb9b65151'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-riscv64'; 			sha256='6d551f86c2ab9155882f5a1067223d0c0c80b47669c826af4311c305cc637093'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-s390x'; 			sha256='6012d0bd529312d12937fd153583a90ddb29aec7a7a8cfaac8e7fb7d1ceabf6f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 12 Jun 2025 11:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Jun 2025 11:04:16 GMT
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
	-	`sha256:3156c3bcd5598f721d5e807804df7256e282bd2897ea9f9f029b3cd93a5ff79b`  
		Last Modified: Thu, 05 Jun 2025 22:44:12 GMT  
		Size: 18.1 MB (18101909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:225abe8edcfa38ed05c3678afaa3fc7019381a300f823c874d6fdfd2a372c345`  
		Last Modified: Thu, 05 Jun 2025 22:44:12 GMT  
		Size: 19.9 MB (19943271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aaa4a492c5a8c6019873f7f10f4583b9134c81a74df09c55d664e88521c254c`  
		Last Modified: Thu, 12 Jun 2025 22:36:39 GMT  
		Size: 19.8 MB (19835400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d441ddcc7f77e2457e59e55a8a824b3b189eaa5a13fdaf65a914da194d6919b`  
		Last Modified: Thu, 12 Jun 2025 22:36:37 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c28d4afadc6fad8c6238b24d9a8dad8f8e7a8deb80839c1d3459890592b523f2`  
		Last Modified: Thu, 12 Jun 2025 22:36:38 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ebbefe72ea0510e4b225079670e073211f0b85e0fc4be94f42ca4ea57d54248`  
		Last Modified: Thu, 12 Jun 2025 22:36:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2.2-cli` - unknown; unknown

```console
$ docker pull docker@sha256:37fab8abfd9b21a00df69a9d07c5ae68b8fdeb2d34ff544d116b57a663143a26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4395a2db76f1506365fb0eac51245b617ca30226db9bb3af6fa171e9e441302`

```dockerfile
```

-	Layers:
	-	`sha256:ad79c76406a54721aaaa4054e1b21be3980a141745279c1866556fad3f734fd2`  
		Last Modified: Thu, 12 Jun 2025 23:07:38 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.2.2-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:fb3724965534d54ce9da8a451424d81fb9e4d4538aeccd1da9b3917f10a8a822
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68499848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c4ad4e83728a898d4ea348a6ce14ceb59541c63a530e27e987d9fe358f1440b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 12 Jun 2025 11:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-x86_64'; 			sha256='6777247eb2947c48b46b1fc96602ac17e140fbac84e1043e6384a6c755fc6769'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv6'; 			sha256='1a7731a63ec845b4b4cf2510e68a8f3411386b1e4b5b03916a0d21a697596f03'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv7'; 			sha256='63e64d9aad9916771a947e4b77df6b2a5e70cdfdb412b2f0464806f4d63fabe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-aarch64'; 			sha256='36dfcc81ffff0ec2a76abaa4b66edf01d2db0d7f3fda342a26525eb72e4e9a80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-ppc64le'; 			sha256='4410f045bfc084fef1f0fcea2c3f8e665cad6c5055f57f1089dd009bb9b65151'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-riscv64'; 			sha256='6d551f86c2ab9155882f5a1067223d0c0c80b47669c826af4311c305cc637093'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-s390x'; 			sha256='6012d0bd529312d12937fd153583a90ddb29aec7a7a8cfaac8e7fb7d1ceabf6f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 12 Jun 2025 11:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Jun 2025 11:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b30f7212c67694cf480811a55ca551c13acaf23308660855c528140f72c862`  
		Last Modified: Fri, 13 Jun 2025 01:20:06 GMT  
		Size: 7.4 MB (7440617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3fca8ac4e435f25c24efea81db3a20417fad9d7c421bee5ce9e3b58996c8efa`  
		Last Modified: Fri, 13 Jun 2025 01:20:05 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68a306e9551e1b17a6ecb71be8147d67ef4f891736c4e69faee945e235107fc`  
		Last Modified: Fri, 13 Jun 2025 01:20:06 GMT  
		Size: 18.1 MB (18089377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44e8dff8b0583db9cb4fc33b75dec6c3d09dd8ce3a76c2a78fd8af411bce92c`  
		Last Modified: Fri, 13 Jun 2025 01:20:08 GMT  
		Size: 19.9 MB (19927230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c665168123ed7a9acc312ff431c35318ee6393642e3e2a8bb7fa2845208b64aa`  
		Last Modified: Fri, 13 Jun 2025 01:20:08 GMT  
		Size: 19.8 MB (19821284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f454bde5fc9b6055cf7fe14c89d2a03739341ccdde89409892b34630a79576`  
		Last Modified: Fri, 13 Jun 2025 01:26:31 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3159ba7c72c13cd717ca59937ae54ce16c3ef91f409e6ff1eb4ab88fc1db06c0`  
		Last Modified: Fri, 13 Jun 2025 01:26:33 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ef5f44369f56ae39826aaf9f89b54c9bf2d4d09a86c4eaf7af04c279812997`  
		Last Modified: Fri, 13 Jun 2025 01:26:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2.2-cli` - unknown; unknown

```console
$ docker pull docker@sha256:17bce1271d7d0578a9245dd7fa91ca7dd2d6133e2d34320d3e8cdc818063c285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2eab113b229c25442c9ce7ca62b5528b3d19f6c315834a17499edc2b29f2c94`

```dockerfile
```

-	Layers:
	-	`sha256:f90f66106ac1cc7b0fabaf95162d064739ffbb6f6d97378a5324bcfff18516c3`  
		Last Modified: Fri, 13 Jun 2025 02:07:34 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.2.2-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:69d471e3a384a30ce1bc54407292e5f0b7cb0b7261bc36b61aa2eb5ec882db7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70086818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd6c4ddb71ce75a68aad923b7822e2edfe7e0c0cd87a9e2d99f4feffc8015393`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 12 Jun 2025 11:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-x86_64'; 			sha256='6777247eb2947c48b46b1fc96602ac17e140fbac84e1043e6384a6c755fc6769'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv6'; 			sha256='1a7731a63ec845b4b4cf2510e68a8f3411386b1e4b5b03916a0d21a697596f03'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv7'; 			sha256='63e64d9aad9916771a947e4b77df6b2a5e70cdfdb412b2f0464806f4d63fabe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-aarch64'; 			sha256='36dfcc81ffff0ec2a76abaa4b66edf01d2db0d7f3fda342a26525eb72e4e9a80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-ppc64le'; 			sha256='4410f045bfc084fef1f0fcea2c3f8e665cad6c5055f57f1089dd009bb9b65151'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-riscv64'; 			sha256='6d551f86c2ab9155882f5a1067223d0c0c80b47669c826af4311c305cc637093'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-s390x'; 			sha256='6012d0bd529312d12937fd153583a90ddb29aec7a7a8cfaac8e7fb7d1ceabf6f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 12 Jun 2025 11:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Jun 2025 11:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375cb5234cd1a2b6b8f1aba00c28fc5d45ba0ecc0d3c8f130d5cdb5138ba6c09`  
		Last Modified: Fri, 13 Jun 2025 00:09:12 GMT  
		Size: 8.2 MB (8229005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ba114b122014764181bf833228533908f5eedbccce11b62f71d746ab1616ccc`  
		Last Modified: Fri, 13 Jun 2025 00:09:12 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5090356630719947eb3cfc865b4d6d8f4971f5e40c640070edd88a16ab0c486f`  
		Last Modified: Fri, 13 Jun 2025 00:09:13 GMT  
		Size: 18.9 MB (18902609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd89b3ff82b93c434d43d799f7f56e86b96409535e06f30c6bbc54456e99752d`  
		Last Modified: Fri, 13 Jun 2025 00:09:14 GMT  
		Size: 19.5 MB (19469847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb8a2de00a4f86825ec25a2f3ac1553ace626f97f529f17cda507233ec8f1a9a`  
		Last Modified: Fri, 13 Jun 2025 00:09:14 GMT  
		Size: 19.3 MB (19347260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ced3983ecfb78d04b5aefc0cf90f4a0b3ccd62ec5610841b0f7860259defda`  
		Last Modified: Fri, 13 Jun 2025 00:09:13 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3673e39b233f3bfe295c08f11dda44b40d801a0bb4f299fe81e1ec50851575`  
		Last Modified: Fri, 13 Jun 2025 00:09:13 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b219e20a46cafa0737e015b21a2525d3bb013d26dc4af6849c8f3586a8b10c5f`  
		Last Modified: Fri, 13 Jun 2025 00:09:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2.2-cli` - unknown; unknown

```console
$ docker pull docker@sha256:f4ad80ac0ebd1e61f59071330740a5cb04fcce43ee8dca6549fd765d5fb74f10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8152da6cbb3a8d4cbf91841ae5de344f2f6f46a451de0b36ffec8f81c859695d`

```dockerfile
```

-	Layers:
	-	`sha256:f8a046668b3f08af5f7ebc0544c42d2308112f3cbaa8603efab8638bb256e743`  
		Last Modified: Fri, 13 Jun 2025 02:07:38 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.2.2-cli-alpine3.22`

```console
$ docker pull docker@sha256:5d3725f5d2f52aafe8a2c49668a43eb7c681a5535a206ba28eccfd8a3013de86
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

### `docker:28.2.2-cli-alpine3.22` - linux; amd64

```console
$ docker pull docker@sha256:b65ad6989d6333212ce011be9684e2d8ae545ec1972b56588c7aff01dd3520d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74480359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c47dbf8612e5f69d7a6b634668d1fc578e0eca340ae1f8a00812e89d72e021a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 12 Jun 2025 11:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-x86_64'; 			sha256='6777247eb2947c48b46b1fc96602ac17e140fbac84e1043e6384a6c755fc6769'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv6'; 			sha256='1a7731a63ec845b4b4cf2510e68a8f3411386b1e4b5b03916a0d21a697596f03'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv7'; 			sha256='63e64d9aad9916771a947e4b77df6b2a5e70cdfdb412b2f0464806f4d63fabe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-aarch64'; 			sha256='36dfcc81ffff0ec2a76abaa4b66edf01d2db0d7f3fda342a26525eb72e4e9a80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-ppc64le'; 			sha256='4410f045bfc084fef1f0fcea2c3f8e665cad6c5055f57f1089dd009bb9b65151'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-riscv64'; 			sha256='6d551f86c2ab9155882f5a1067223d0c0c80b47669c826af4311c305cc637093'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-s390x'; 			sha256='6012d0bd529312d12937fd153583a90ddb29aec7a7a8cfaac8e7fb7d1ceabf6f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 12 Jun 2025 11:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Jun 2025 11:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f32e8d6f68009e4f81cdd4d2b7e6465c3cdc96e6addc90132dfdb88d08941a20`  
		Last Modified: Thu, 12 Jun 2025 22:36:53 GMT  
		Size: 8.2 MB (8207474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ac40e43aadc31b56fc943a7df1de7e7f5f06348ca89a108384ba3e9a805a89`  
		Last Modified: Thu, 12 Jun 2025 22:36:53 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3870806677ebd2c8113c069ad6c6f219c456246069bd2688c9cffe6d1736938`  
		Last Modified: Thu, 12 Jun 2025 22:36:55 GMT  
		Size: 20.1 MB (20083028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86f14a0f3d88cab9e631bd4dcf8f9a164306875132f95135fff3358e3a2a8d2`  
		Last Modified: Thu, 12 Jun 2025 22:36:56 GMT  
		Size: 21.3 MB (21290186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da67c6f5f9a3f4626ce69c1328bdacf4c370d20479d084f6415437dea4481db4`  
		Last Modified: Thu, 12 Jun 2025 22:36:56 GMT  
		Size: 21.1 MB (21100670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b94aef2e962e8f653820f39c328e9f31ab7a6e903d929b45f9fb82324f7633`  
		Last Modified: Thu, 12 Jun 2025 22:36:55 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a98583f050f0d3b9242c387626407b4c0affec19be6fafeb1c7135bd7303d86`  
		Last Modified: Thu, 12 Jun 2025 22:36:56 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a115214fbd18e2a1acb4699bd0d7f72d42bf84a1f4cd3d4b1cdae8248a2167fa`  
		Last Modified: Thu, 12 Jun 2025 22:36:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2.2-cli-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:1ebe76e61490c161294dbf222ba3f54e20b9c4ef88e3a419b69d6c9ea30d9cee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adb69d08e123464b3d3e1ca5fc247dafb6079c23e370b419c72f645720be223f`

```dockerfile
```

-	Layers:
	-	`sha256:c968c006dcee70140b54235857f7cdddd7486443dbd3175f36530d5404ebc8e2`  
		Last Modified: Thu, 12 Jun 2025 23:07:35 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.2.2-cli-alpine3.22` - linux; arm variant v6

```console
$ docker pull docker@sha256:cbf1afecf10a316254346c8400aefe8e45ec33d0ca7d37e94acaf8df4c243108
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69498335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4b21f5d310fad2488ce7f6f0798a746c1018659fb7fce6a3975ebe40ba17364`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 12 Jun 2025 11:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-x86_64'; 			sha256='6777247eb2947c48b46b1fc96602ac17e140fbac84e1043e6384a6c755fc6769'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv6'; 			sha256='1a7731a63ec845b4b4cf2510e68a8f3411386b1e4b5b03916a0d21a697596f03'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv7'; 			sha256='63e64d9aad9916771a947e4b77df6b2a5e70cdfdb412b2f0464806f4d63fabe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-aarch64'; 			sha256='36dfcc81ffff0ec2a76abaa4b66edf01d2db0d7f3fda342a26525eb72e4e9a80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-ppc64le'; 			sha256='4410f045bfc084fef1f0fcea2c3f8e665cad6c5055f57f1089dd009bb9b65151'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-riscv64'; 			sha256='6d551f86c2ab9155882f5a1067223d0c0c80b47669c826af4311c305cc637093'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-s390x'; 			sha256='6012d0bd529312d12937fd153583a90ddb29aec7a7a8cfaac8e7fb7d1ceabf6f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 12 Jun 2025 11:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Jun 2025 11:04:16 GMT
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
	-	`sha256:3156c3bcd5598f721d5e807804df7256e282bd2897ea9f9f029b3cd93a5ff79b`  
		Last Modified: Thu, 05 Jun 2025 22:44:12 GMT  
		Size: 18.1 MB (18101909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:225abe8edcfa38ed05c3678afaa3fc7019381a300f823c874d6fdfd2a372c345`  
		Last Modified: Thu, 05 Jun 2025 22:44:12 GMT  
		Size: 19.9 MB (19943271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aaa4a492c5a8c6019873f7f10f4583b9134c81a74df09c55d664e88521c254c`  
		Last Modified: Thu, 12 Jun 2025 22:36:39 GMT  
		Size: 19.8 MB (19835400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d441ddcc7f77e2457e59e55a8a824b3b189eaa5a13fdaf65a914da194d6919b`  
		Last Modified: Thu, 12 Jun 2025 22:36:37 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c28d4afadc6fad8c6238b24d9a8dad8f8e7a8deb80839c1d3459890592b523f2`  
		Last Modified: Thu, 12 Jun 2025 22:36:38 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ebbefe72ea0510e4b225079670e073211f0b85e0fc4be94f42ca4ea57d54248`  
		Last Modified: Thu, 12 Jun 2025 22:36:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2.2-cli-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:37fab8abfd9b21a00df69a9d07c5ae68b8fdeb2d34ff544d116b57a663143a26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4395a2db76f1506365fb0eac51245b617ca30226db9bb3af6fa171e9e441302`

```dockerfile
```

-	Layers:
	-	`sha256:ad79c76406a54721aaaa4054e1b21be3980a141745279c1866556fad3f734fd2`  
		Last Modified: Thu, 12 Jun 2025 23:07:38 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.2.2-cli-alpine3.22` - linux; arm variant v7

```console
$ docker pull docker@sha256:fb3724965534d54ce9da8a451424d81fb9e4d4538aeccd1da9b3917f10a8a822
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68499848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c4ad4e83728a898d4ea348a6ce14ceb59541c63a530e27e987d9fe358f1440b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 12 Jun 2025 11:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-x86_64'; 			sha256='6777247eb2947c48b46b1fc96602ac17e140fbac84e1043e6384a6c755fc6769'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv6'; 			sha256='1a7731a63ec845b4b4cf2510e68a8f3411386b1e4b5b03916a0d21a697596f03'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv7'; 			sha256='63e64d9aad9916771a947e4b77df6b2a5e70cdfdb412b2f0464806f4d63fabe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-aarch64'; 			sha256='36dfcc81ffff0ec2a76abaa4b66edf01d2db0d7f3fda342a26525eb72e4e9a80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-ppc64le'; 			sha256='4410f045bfc084fef1f0fcea2c3f8e665cad6c5055f57f1089dd009bb9b65151'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-riscv64'; 			sha256='6d551f86c2ab9155882f5a1067223d0c0c80b47669c826af4311c305cc637093'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-s390x'; 			sha256='6012d0bd529312d12937fd153583a90ddb29aec7a7a8cfaac8e7fb7d1ceabf6f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 12 Jun 2025 11:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Jun 2025 11:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b30f7212c67694cf480811a55ca551c13acaf23308660855c528140f72c862`  
		Last Modified: Fri, 13 Jun 2025 01:20:06 GMT  
		Size: 7.4 MB (7440617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3fca8ac4e435f25c24efea81db3a20417fad9d7c421bee5ce9e3b58996c8efa`  
		Last Modified: Fri, 13 Jun 2025 01:20:05 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68a306e9551e1b17a6ecb71be8147d67ef4f891736c4e69faee945e235107fc`  
		Last Modified: Fri, 13 Jun 2025 01:20:06 GMT  
		Size: 18.1 MB (18089377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44e8dff8b0583db9cb4fc33b75dec6c3d09dd8ce3a76c2a78fd8af411bce92c`  
		Last Modified: Fri, 13 Jun 2025 01:20:08 GMT  
		Size: 19.9 MB (19927230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c665168123ed7a9acc312ff431c35318ee6393642e3e2a8bb7fa2845208b64aa`  
		Last Modified: Fri, 13 Jun 2025 01:20:08 GMT  
		Size: 19.8 MB (19821284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f454bde5fc9b6055cf7fe14c89d2a03739341ccdde89409892b34630a79576`  
		Last Modified: Fri, 13 Jun 2025 01:26:31 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3159ba7c72c13cd717ca59937ae54ce16c3ef91f409e6ff1eb4ab88fc1db06c0`  
		Last Modified: Fri, 13 Jun 2025 01:26:33 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ef5f44369f56ae39826aaf9f89b54c9bf2d4d09a86c4eaf7af04c279812997`  
		Last Modified: Fri, 13 Jun 2025 01:26:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2.2-cli-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:17bce1271d7d0578a9245dd7fa91ca7dd2d6133e2d34320d3e8cdc818063c285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2eab113b229c25442c9ce7ca62b5528b3d19f6c315834a17499edc2b29f2c94`

```dockerfile
```

-	Layers:
	-	`sha256:f90f66106ac1cc7b0fabaf95162d064739ffbb6f6d97378a5324bcfff18516c3`  
		Last Modified: Fri, 13 Jun 2025 02:07:34 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.2.2-cli-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:69d471e3a384a30ce1bc54407292e5f0b7cb0b7261bc36b61aa2eb5ec882db7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70086818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd6c4ddb71ce75a68aad923b7822e2edfe7e0c0cd87a9e2d99f4feffc8015393`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 12 Jun 2025 11:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-x86_64'; 			sha256='6777247eb2947c48b46b1fc96602ac17e140fbac84e1043e6384a6c755fc6769'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv6'; 			sha256='1a7731a63ec845b4b4cf2510e68a8f3411386b1e4b5b03916a0d21a697596f03'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv7'; 			sha256='63e64d9aad9916771a947e4b77df6b2a5e70cdfdb412b2f0464806f4d63fabe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-aarch64'; 			sha256='36dfcc81ffff0ec2a76abaa4b66edf01d2db0d7f3fda342a26525eb72e4e9a80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-ppc64le'; 			sha256='4410f045bfc084fef1f0fcea2c3f8e665cad6c5055f57f1089dd009bb9b65151'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-riscv64'; 			sha256='6d551f86c2ab9155882f5a1067223d0c0c80b47669c826af4311c305cc637093'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-s390x'; 			sha256='6012d0bd529312d12937fd153583a90ddb29aec7a7a8cfaac8e7fb7d1ceabf6f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 12 Jun 2025 11:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Jun 2025 11:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375cb5234cd1a2b6b8f1aba00c28fc5d45ba0ecc0d3c8f130d5cdb5138ba6c09`  
		Last Modified: Fri, 13 Jun 2025 00:09:12 GMT  
		Size: 8.2 MB (8229005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ba114b122014764181bf833228533908f5eedbccce11b62f71d746ab1616ccc`  
		Last Modified: Fri, 13 Jun 2025 00:09:12 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5090356630719947eb3cfc865b4d6d8f4971f5e40c640070edd88a16ab0c486f`  
		Last Modified: Fri, 13 Jun 2025 00:09:13 GMT  
		Size: 18.9 MB (18902609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd89b3ff82b93c434d43d799f7f56e86b96409535e06f30c6bbc54456e99752d`  
		Last Modified: Fri, 13 Jun 2025 00:09:14 GMT  
		Size: 19.5 MB (19469847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb8a2de00a4f86825ec25a2f3ac1553ace626f97f529f17cda507233ec8f1a9a`  
		Last Modified: Fri, 13 Jun 2025 00:09:14 GMT  
		Size: 19.3 MB (19347260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ced3983ecfb78d04b5aefc0cf90f4a0b3ccd62ec5610841b0f7860259defda`  
		Last Modified: Fri, 13 Jun 2025 00:09:13 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3673e39b233f3bfe295c08f11dda44b40d801a0bb4f299fe81e1ec50851575`  
		Last Modified: Fri, 13 Jun 2025 00:09:13 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b219e20a46cafa0737e015b21a2525d3bb013d26dc4af6849c8f3586a8b10c5f`  
		Last Modified: Fri, 13 Jun 2025 00:09:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2.2-cli-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:f4ad80ac0ebd1e61f59071330740a5cb04fcce43ee8dca6549fd765d5fb74f10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8152da6cbb3a8d4cbf91841ae5de344f2f6f46a451de0b36ffec8f81c859695d`

```dockerfile
```

-	Layers:
	-	`sha256:f8a046668b3f08af5f7ebc0544c42d2308112f3cbaa8603efab8638bb256e743`  
		Last Modified: Fri, 13 Jun 2025 02:07:38 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.2.2-dind`

```console
$ docker pull docker@sha256:ff052514f359111edd920b54581e7aca65629458607f9fbdbf82d7eefbe0602b
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

### `docker:28.2.2-dind` - linux; amd64

```console
$ docker pull docker@sha256:8e32fae437051e392dc31f1bca659a14a6b8f341fa6dd131a9def0a9f315203c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.7 MB (143689092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:896cfe4b7aa87684cdbe7274a5a4efafa80c561662a935bd3a0432e2fcbaf46d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-x86_64'; 			sha256='6777247eb2947c48b46b1fc96602ac17e140fbac84e1043e6384a6c755fc6769'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv6'; 			sha256='1a7731a63ec845b4b4cf2510e68a8f3411386b1e4b5b03916a0d21a697596f03'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv7'; 			sha256='63e64d9aad9916771a947e4b77df6b2a5e70cdfdb412b2f0464806f4d63fabe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-aarch64'; 			sha256='36dfcc81ffff0ec2a76abaa4b66edf01d2db0d7f3fda342a26525eb72e4e9a80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-ppc64le'; 			sha256='4410f045bfc084fef1f0fcea2c3f8e665cad6c5055f57f1089dd009bb9b65151'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-riscv64'; 			sha256='6d551f86c2ab9155882f5a1067223d0c0c80b47669c826af4311c305cc637093'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-s390x'; 			sha256='6012d0bd529312d12937fd153583a90ddb29aec7a7a8cfaac8e7fb7d1ceabf6f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 05 Jun 2025 17:36:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
CMD ["sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
VOLUME [/var/lib/docker]
# Thu, 05 Jun 2025 17:36:11 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
CMD []
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f32e8d6f68009e4f81cdd4d2b7e6465c3cdc96e6addc90132dfdb88d08941a20`  
		Last Modified: Thu, 12 Jun 2025 22:36:53 GMT  
		Size: 8.2 MB (8207474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ac40e43aadc31b56fc943a7df1de7e7f5f06348ca89a108384ba3e9a805a89`  
		Last Modified: Thu, 12 Jun 2025 22:36:53 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3870806677ebd2c8113c069ad6c6f219c456246069bd2688c9cffe6d1736938`  
		Last Modified: Thu, 12 Jun 2025 22:36:55 GMT  
		Size: 20.1 MB (20083028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86f14a0f3d88cab9e631bd4dcf8f9a164306875132f95135fff3358e3a2a8d2`  
		Last Modified: Thu, 12 Jun 2025 22:36:56 GMT  
		Size: 21.3 MB (21290186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da67c6f5f9a3f4626ce69c1328bdacf4c370d20479d084f6415437dea4481db4`  
		Last Modified: Thu, 12 Jun 2025 22:36:56 GMT  
		Size: 21.1 MB (21100670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b94aef2e962e8f653820f39c328e9f31ab7a6e903d929b45f9fb82324f7633`  
		Last Modified: Thu, 12 Jun 2025 22:36:55 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a98583f050f0d3b9242c387626407b4c0affec19be6fafeb1c7135bd7303d86`  
		Last Modified: Thu, 12 Jun 2025 22:36:56 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a115214fbd18e2a1acb4699bd0d7f72d42bf84a1f4cd3d4b1cdae8248a2167fa`  
		Last Modified: Thu, 12 Jun 2025 22:36:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:212150b9078af2b8495b33e957823f54b179f41a22f2702f6fec1560c9d3f6f2`  
		Last Modified: Thu, 12 Jun 2025 23:07:54 GMT  
		Size: 6.9 MB (6905618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9212e721c88d6da1ed4b1e289f523f35a01e01885d1131cd34feceb518227abf`  
		Last Modified: Thu, 12 Jun 2025 23:07:53 GMT  
		Size: 90.5 KB (90494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b0253e449f82e84618065f5b74284cb93f7cc52668795f3590d41585c32012`  
		Last Modified: Thu, 12 Jun 2025 23:07:51 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811b046d83c5b8a6340f19f8d6acd494b2b028f5c1bf969e58cf6f0e350c7cea`  
		Last Modified: Thu, 12 Jun 2025 23:07:58 GMT  
		Size: 62.2 MB (62206627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68771551084500ee9ac3a4b32aa56d78b3d007c1986578b481436becbe8ae1a1`  
		Last Modified: Thu, 12 Jun 2025 23:07:51 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cae381f867a74a59e0d18562bd189fcc3560935254e57ceb2e247145c467a8b`  
		Last Modified: Thu, 12 Jun 2025 23:07:52 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2.2-dind` - unknown; unknown

```console
$ docker pull docker@sha256:4c5431982a6f26acafc9a647e2a915e12fd2cb54c0d9fa6f5bed94ca07e186b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a1e46faf2561239606e7d796aac2f70a1bc3754ba1ff7200c43154e973515c8`

```dockerfile
```

-	Layers:
	-	`sha256:d5158885bee456f124624bc8808ba3f4ea82fc7ca56f260044b4d92a684498b1`  
		Last Modified: Fri, 13 Jun 2025 02:07:20 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.2.2-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:d692f151518fae2760b09152001cfba45f8bc770e1906d190d6eb2e3142b1a76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134722094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44d698360caa93e31e5563c2c622bbbeb75bd82d597a599776298366deb6aa32`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-x86_64'; 			sha256='6777247eb2947c48b46b1fc96602ac17e140fbac84e1043e6384a6c755fc6769'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv6'; 			sha256='1a7731a63ec845b4b4cf2510e68a8f3411386b1e4b5b03916a0d21a697596f03'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv7'; 			sha256='63e64d9aad9916771a947e4b77df6b2a5e70cdfdb412b2f0464806f4d63fabe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-aarch64'; 			sha256='36dfcc81ffff0ec2a76abaa4b66edf01d2db0d7f3fda342a26525eb72e4e9a80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-ppc64le'; 			sha256='4410f045bfc084fef1f0fcea2c3f8e665cad6c5055f57f1089dd009bb9b65151'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-riscv64'; 			sha256='6d551f86c2ab9155882f5a1067223d0c0c80b47669c826af4311c305cc637093'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-s390x'; 			sha256='6012d0bd529312d12937fd153583a90ddb29aec7a7a8cfaac8e7fb7d1ceabf6f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 05 Jun 2025 17:36:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
CMD ["sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
VOLUME [/var/lib/docker]
# Thu, 05 Jun 2025 17:36:11 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
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
	-	`sha256:3156c3bcd5598f721d5e807804df7256e282bd2897ea9f9f029b3cd93a5ff79b`  
		Last Modified: Thu, 05 Jun 2025 22:44:12 GMT  
		Size: 18.1 MB (18101909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:225abe8edcfa38ed05c3678afaa3fc7019381a300f823c874d6fdfd2a372c345`  
		Last Modified: Thu, 05 Jun 2025 22:44:12 GMT  
		Size: 19.9 MB (19943271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aaa4a492c5a8c6019873f7f10f4583b9134c81a74df09c55d664e88521c254c`  
		Last Modified: Thu, 12 Jun 2025 22:36:39 GMT  
		Size: 19.8 MB (19835400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d441ddcc7f77e2457e59e55a8a824b3b189eaa5a13fdaf65a914da194d6919b`  
		Last Modified: Thu, 12 Jun 2025 22:36:37 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c28d4afadc6fad8c6238b24d9a8dad8f8e7a8deb80839c1d3459890592b523f2`  
		Last Modified: Thu, 12 Jun 2025 22:36:38 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ebbefe72ea0510e4b225079670e073211f0b85e0fc4be94f42ca4ea57d54248`  
		Last Modified: Thu, 12 Jun 2025 22:36:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8241b18dc7eb679233e3250bbfb077dcd4f8778550fe3188d80dd91b7838a9bd`  
		Last Modified: Thu, 12 Jun 2025 22:54:58 GMT  
		Size: 7.2 MB (7230354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3cf946673d9726b4c5b57734c7dbf2e2e811f1b40e437ce7cc7bf5533df26a`  
		Last Modified: Thu, 12 Jun 2025 22:54:57 GMT  
		Size: 90.1 KB (90058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d08132e8b60b557ae762a779e816c58c6c366efd53ded71c9275533c8ec8f2d`  
		Last Modified: Thu, 12 Jun 2025 22:54:57 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d611e6743d4f047d30c66012bbac54fc821dc2ffefbbe8277a53e70060da2356`  
		Last Modified: Thu, 12 Jun 2025 22:55:00 GMT  
		Size: 57.9 MB (57897340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a783e6fb91bba730335ac30fbd49b93258f2e4d9d4c2a73dbe5c7663e5f497`  
		Last Modified: Thu, 12 Jun 2025 22:54:57 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b45b886f9c1b0ecbf83201757d3e791047d9cd0cbbdfc865a112256becf21ce4`  
		Last Modified: Thu, 12 Jun 2025 22:54:58 GMT  
		Size: 3.3 KB (3304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2.2-dind` - unknown; unknown

```console
$ docker pull docker@sha256:d1a670e4e107e2e31f275813f1751ac249dec91fa3cfc6cc949e581bdb0c364e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb88dd0bcd267d48fad2fe5722c0bc382d70b8aa328b8a911562dc8081e3809d`

```dockerfile
```

-	Layers:
	-	`sha256:c75371d2b5d03d6fe0926a467c9d353d590b6db0765b2bc492cb0184dfe50817`  
		Last Modified: Thu, 12 Jun 2025 23:07:42 GMT  
		Size: 34.8 KB (34765 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.2.2-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:66277612b6b4d8230b45b06074b5716e61c90fee840cf8b7b4da8208329fe9d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.0 MB (133027832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55fe29bbf4d101c05a3d55a85a71baf6c7ae07a62cc6865b2fc5b8902a5978a6`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-x86_64'; 			sha256='6777247eb2947c48b46b1fc96602ac17e140fbac84e1043e6384a6c755fc6769'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv6'; 			sha256='1a7731a63ec845b4b4cf2510e68a8f3411386b1e4b5b03916a0d21a697596f03'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv7'; 			sha256='63e64d9aad9916771a947e4b77df6b2a5e70cdfdb412b2f0464806f4d63fabe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-aarch64'; 			sha256='36dfcc81ffff0ec2a76abaa4b66edf01d2db0d7f3fda342a26525eb72e4e9a80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-ppc64le'; 			sha256='4410f045bfc084fef1f0fcea2c3f8e665cad6c5055f57f1089dd009bb9b65151'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-riscv64'; 			sha256='6d551f86c2ab9155882f5a1067223d0c0c80b47669c826af4311c305cc637093'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-s390x'; 			sha256='6012d0bd529312d12937fd153583a90ddb29aec7a7a8cfaac8e7fb7d1ceabf6f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 05 Jun 2025 17:36:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
CMD ["sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
VOLUME [/var/lib/docker]
# Thu, 05 Jun 2025 17:36:11 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
CMD []
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b30f7212c67694cf480811a55ca551c13acaf23308660855c528140f72c862`  
		Last Modified: Fri, 13 Jun 2025 01:20:06 GMT  
		Size: 7.4 MB (7440617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3fca8ac4e435f25c24efea81db3a20417fad9d7c421bee5ce9e3b58996c8efa`  
		Last Modified: Fri, 13 Jun 2025 01:20:05 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68a306e9551e1b17a6ecb71be8147d67ef4f891736c4e69faee945e235107fc`  
		Last Modified: Fri, 13 Jun 2025 01:20:06 GMT  
		Size: 18.1 MB (18089377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44e8dff8b0583db9cb4fc33b75dec6c3d09dd8ce3a76c2a78fd8af411bce92c`  
		Last Modified: Fri, 13 Jun 2025 01:20:08 GMT  
		Size: 19.9 MB (19927230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c665168123ed7a9acc312ff431c35318ee6393642e3e2a8bb7fa2845208b64aa`  
		Last Modified: Fri, 13 Jun 2025 01:20:08 GMT  
		Size: 19.8 MB (19821284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f454bde5fc9b6055cf7fe14c89d2a03739341ccdde89409892b34630a79576`  
		Last Modified: Fri, 13 Jun 2025 01:26:31 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3159ba7c72c13cd717ca59937ae54ce16c3ef91f409e6ff1eb4ab88fc1db06c0`  
		Last Modified: Fri, 13 Jun 2025 01:26:33 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ef5f44369f56ae39826aaf9f89b54c9bf2d4d09a86c4eaf7af04c279812997`  
		Last Modified: Fri, 13 Jun 2025 01:26:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7236561f33fb7c50ca5d7c37b075afc53fe8e4088c95319dcde0bb8ad917eb0`  
		Last Modified: Fri, 13 Jun 2025 06:24:34 GMT  
		Size: 6.5 MB (6538120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98752e61e2dd86e562ed8c9de46d0e71b38f35fe7be163828be059624970c9e`  
		Last Modified: Fri, 13 Jun 2025 06:24:35 GMT  
		Size: 86.5 KB (86488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c1e6adc4b8f7742b913355688fb6e8dd3671bd9c49551a76f2dad8f0bfcf827`  
		Last Modified: Fri, 13 Jun 2025 06:24:35 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7760efd1d6901a24ed3199cf41b66c116f64c11736dcecc92c75040a0f68dea9`  
		Last Modified: Fri, 13 Jun 2025 06:24:39 GMT  
		Size: 57.9 MB (57897375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb6cd2d2e0725f775e9f508d900bb8bac548036c111ea8957a933fc7002b93e`  
		Last Modified: Fri, 13 Jun 2025 06:24:36 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcd8d4be9dc74189aefe21d876aec06706ad1fa1e7597dd49f2c2fc862477c51`  
		Last Modified: Fri, 13 Jun 2025 06:24:36 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2.2-dind` - unknown; unknown

```console
$ docker pull docker@sha256:9c4cb9730947a3df8f10cb2052f42e9556fa8a3d55b8d9eb9df923d7467c4a6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4fa8b980b9e0ff354efd1a786e8ee1816d49966e8cb7f6c93a8a7182923f7fd`

```dockerfile
```

-	Layers:
	-	`sha256:4bc11f3d388f7184ad2e3f2d7090c73f569bc734a2691321b72cdcb0e3735d28`  
		Last Modified: Fri, 13 Jun 2025 08:07:23 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.2.2-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:b8d1c58eea384111a2c6646a55d6c57e11ce3527c44b26b17ba91e00f82530c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.5 MB (134502165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f7a08861e83333223ac02d5357e4d77380c819b320b98b1811d33973cd4cd5e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-x86_64'; 			sha256='6777247eb2947c48b46b1fc96602ac17e140fbac84e1043e6384a6c755fc6769'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv6'; 			sha256='1a7731a63ec845b4b4cf2510e68a8f3411386b1e4b5b03916a0d21a697596f03'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv7'; 			sha256='63e64d9aad9916771a947e4b77df6b2a5e70cdfdb412b2f0464806f4d63fabe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-aarch64'; 			sha256='36dfcc81ffff0ec2a76abaa4b66edf01d2db0d7f3fda342a26525eb72e4e9a80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-ppc64le'; 			sha256='4410f045bfc084fef1f0fcea2c3f8e665cad6c5055f57f1089dd009bb9b65151'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-riscv64'; 			sha256='6d551f86c2ab9155882f5a1067223d0c0c80b47669c826af4311c305cc637093'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-s390x'; 			sha256='6012d0bd529312d12937fd153583a90ddb29aec7a7a8cfaac8e7fb7d1ceabf6f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 05 Jun 2025 17:36:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
CMD ["sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
VOLUME [/var/lib/docker]
# Thu, 05 Jun 2025 17:36:11 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
CMD []
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375cb5234cd1a2b6b8f1aba00c28fc5d45ba0ecc0d3c8f130d5cdb5138ba6c09`  
		Last Modified: Fri, 13 Jun 2025 00:09:12 GMT  
		Size: 8.2 MB (8229005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ba114b122014764181bf833228533908f5eedbccce11b62f71d746ab1616ccc`  
		Last Modified: Fri, 13 Jun 2025 00:09:12 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5090356630719947eb3cfc865b4d6d8f4971f5e40c640070edd88a16ab0c486f`  
		Last Modified: Fri, 13 Jun 2025 00:09:13 GMT  
		Size: 18.9 MB (18902609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd89b3ff82b93c434d43d799f7f56e86b96409535e06f30c6bbc54456e99752d`  
		Last Modified: Fri, 13 Jun 2025 00:09:14 GMT  
		Size: 19.5 MB (19469847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb8a2de00a4f86825ec25a2f3ac1553ace626f97f529f17cda507233ec8f1a9a`  
		Last Modified: Fri, 13 Jun 2025 00:09:14 GMT  
		Size: 19.3 MB (19347260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ced3983ecfb78d04b5aefc0cf90f4a0b3ccd62ec5610841b0f7860259defda`  
		Last Modified: Fri, 13 Jun 2025 00:09:13 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3673e39b233f3bfe295c08f11dda44b40d801a0bb4f299fe81e1ec50851575`  
		Last Modified: Fri, 13 Jun 2025 00:09:13 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b219e20a46cafa0737e015b21a2525d3bb013d26dc4af6849c8f3586a8b10c5f`  
		Last Modified: Fri, 13 Jun 2025 00:09:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c6e05695096db67c5e6426307e8a652c5311da73d994e47d9580e886b837a10`  
		Last Modified: Fri, 13 Jun 2025 04:27:25 GMT  
		Size: 7.1 MB (7141507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891d71d9754311d78a8a473d578e3825acd68ce42cd0dbc623f6357a4e17c72b`  
		Last Modified: Fri, 13 Jun 2025 04:27:25 GMT  
		Size: 99.6 KB (99645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5d9a3e9b7f7718caa1aba176d0c009906cfdbf0beaabb63840d5743b89cc7f2`  
		Last Modified: Fri, 13 Jun 2025 04:27:26 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d489b833d40920f79c54667b28c6b5c28475bbdb198a31284fb082206828119a`  
		Last Modified: Fri, 13 Jun 2025 04:27:32 GMT  
		Size: 57.2 MB (57168194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e7d0e57cac200e9cb81bab37725356fb62116b7b3fb40855e245e59124702f2`  
		Last Modified: Fri, 13 Jun 2025 04:27:27 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc40c4cf8ec0a96212d48ae432d6342b219db9566141690970349c4e6140886`  
		Last Modified: Fri, 13 Jun 2025 04:27:27 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2.2-dind` - unknown; unknown

```console
$ docker pull docker@sha256:e64e322c1cc45566807e6054fb529a1b90018a74d5599c9e524013622d5fd800
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30148cdfe5f84f758ae82d1f85d34d65c6e91c5167340993eaa3d924e06041f5`

```dockerfile
```

-	Layers:
	-	`sha256:a0dd369778c470b4b56994e10a017cc701a049c277738705f244ac7e5856bdd4`  
		Last Modified: Fri, 13 Jun 2025 05:07:36 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.2.2-dind-alpine3.22`

```console
$ docker pull docker@sha256:ff052514f359111edd920b54581e7aca65629458607f9fbdbf82d7eefbe0602b
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

### `docker:28.2.2-dind-alpine3.22` - linux; amd64

```console
$ docker pull docker@sha256:8e32fae437051e392dc31f1bca659a14a6b8f341fa6dd131a9def0a9f315203c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.7 MB (143689092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:896cfe4b7aa87684cdbe7274a5a4efafa80c561662a935bd3a0432e2fcbaf46d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-x86_64'; 			sha256='6777247eb2947c48b46b1fc96602ac17e140fbac84e1043e6384a6c755fc6769'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv6'; 			sha256='1a7731a63ec845b4b4cf2510e68a8f3411386b1e4b5b03916a0d21a697596f03'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv7'; 			sha256='63e64d9aad9916771a947e4b77df6b2a5e70cdfdb412b2f0464806f4d63fabe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-aarch64'; 			sha256='36dfcc81ffff0ec2a76abaa4b66edf01d2db0d7f3fda342a26525eb72e4e9a80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-ppc64le'; 			sha256='4410f045bfc084fef1f0fcea2c3f8e665cad6c5055f57f1089dd009bb9b65151'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-riscv64'; 			sha256='6d551f86c2ab9155882f5a1067223d0c0c80b47669c826af4311c305cc637093'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-s390x'; 			sha256='6012d0bd529312d12937fd153583a90ddb29aec7a7a8cfaac8e7fb7d1ceabf6f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 05 Jun 2025 17:36:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
CMD ["sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
VOLUME [/var/lib/docker]
# Thu, 05 Jun 2025 17:36:11 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
CMD []
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f32e8d6f68009e4f81cdd4d2b7e6465c3cdc96e6addc90132dfdb88d08941a20`  
		Last Modified: Thu, 12 Jun 2025 22:36:53 GMT  
		Size: 8.2 MB (8207474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ac40e43aadc31b56fc943a7df1de7e7f5f06348ca89a108384ba3e9a805a89`  
		Last Modified: Thu, 12 Jun 2025 22:36:53 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3870806677ebd2c8113c069ad6c6f219c456246069bd2688c9cffe6d1736938`  
		Last Modified: Thu, 12 Jun 2025 22:36:55 GMT  
		Size: 20.1 MB (20083028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86f14a0f3d88cab9e631bd4dcf8f9a164306875132f95135fff3358e3a2a8d2`  
		Last Modified: Thu, 12 Jun 2025 22:36:56 GMT  
		Size: 21.3 MB (21290186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da67c6f5f9a3f4626ce69c1328bdacf4c370d20479d084f6415437dea4481db4`  
		Last Modified: Thu, 12 Jun 2025 22:36:56 GMT  
		Size: 21.1 MB (21100670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b94aef2e962e8f653820f39c328e9f31ab7a6e903d929b45f9fb82324f7633`  
		Last Modified: Thu, 12 Jun 2025 22:36:55 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a98583f050f0d3b9242c387626407b4c0affec19be6fafeb1c7135bd7303d86`  
		Last Modified: Thu, 12 Jun 2025 22:36:56 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a115214fbd18e2a1acb4699bd0d7f72d42bf84a1f4cd3d4b1cdae8248a2167fa`  
		Last Modified: Thu, 12 Jun 2025 22:36:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:212150b9078af2b8495b33e957823f54b179f41a22f2702f6fec1560c9d3f6f2`  
		Last Modified: Thu, 12 Jun 2025 23:07:54 GMT  
		Size: 6.9 MB (6905618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9212e721c88d6da1ed4b1e289f523f35a01e01885d1131cd34feceb518227abf`  
		Last Modified: Thu, 12 Jun 2025 23:07:53 GMT  
		Size: 90.5 KB (90494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b0253e449f82e84618065f5b74284cb93f7cc52668795f3590d41585c32012`  
		Last Modified: Thu, 12 Jun 2025 23:07:51 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811b046d83c5b8a6340f19f8d6acd494b2b028f5c1bf969e58cf6f0e350c7cea`  
		Last Modified: Thu, 12 Jun 2025 23:07:58 GMT  
		Size: 62.2 MB (62206627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68771551084500ee9ac3a4b32aa56d78b3d007c1986578b481436becbe8ae1a1`  
		Last Modified: Thu, 12 Jun 2025 23:07:51 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cae381f867a74a59e0d18562bd189fcc3560935254e57ceb2e247145c467a8b`  
		Last Modified: Thu, 12 Jun 2025 23:07:52 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2.2-dind-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:4c5431982a6f26acafc9a647e2a915e12fd2cb54c0d9fa6f5bed94ca07e186b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a1e46faf2561239606e7d796aac2f70a1bc3754ba1ff7200c43154e973515c8`

```dockerfile
```

-	Layers:
	-	`sha256:d5158885bee456f124624bc8808ba3f4ea82fc7ca56f260044b4d92a684498b1`  
		Last Modified: Fri, 13 Jun 2025 02:07:20 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.2.2-dind-alpine3.22` - linux; arm variant v6

```console
$ docker pull docker@sha256:d692f151518fae2760b09152001cfba45f8bc770e1906d190d6eb2e3142b1a76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134722094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44d698360caa93e31e5563c2c622bbbeb75bd82d597a599776298366deb6aa32`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-x86_64'; 			sha256='6777247eb2947c48b46b1fc96602ac17e140fbac84e1043e6384a6c755fc6769'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv6'; 			sha256='1a7731a63ec845b4b4cf2510e68a8f3411386b1e4b5b03916a0d21a697596f03'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv7'; 			sha256='63e64d9aad9916771a947e4b77df6b2a5e70cdfdb412b2f0464806f4d63fabe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-aarch64'; 			sha256='36dfcc81ffff0ec2a76abaa4b66edf01d2db0d7f3fda342a26525eb72e4e9a80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-ppc64le'; 			sha256='4410f045bfc084fef1f0fcea2c3f8e665cad6c5055f57f1089dd009bb9b65151'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-riscv64'; 			sha256='6d551f86c2ab9155882f5a1067223d0c0c80b47669c826af4311c305cc637093'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-s390x'; 			sha256='6012d0bd529312d12937fd153583a90ddb29aec7a7a8cfaac8e7fb7d1ceabf6f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 05 Jun 2025 17:36:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
CMD ["sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
VOLUME [/var/lib/docker]
# Thu, 05 Jun 2025 17:36:11 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
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
	-	`sha256:3156c3bcd5598f721d5e807804df7256e282bd2897ea9f9f029b3cd93a5ff79b`  
		Last Modified: Thu, 05 Jun 2025 22:44:12 GMT  
		Size: 18.1 MB (18101909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:225abe8edcfa38ed05c3678afaa3fc7019381a300f823c874d6fdfd2a372c345`  
		Last Modified: Thu, 05 Jun 2025 22:44:12 GMT  
		Size: 19.9 MB (19943271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aaa4a492c5a8c6019873f7f10f4583b9134c81a74df09c55d664e88521c254c`  
		Last Modified: Thu, 12 Jun 2025 22:36:39 GMT  
		Size: 19.8 MB (19835400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d441ddcc7f77e2457e59e55a8a824b3b189eaa5a13fdaf65a914da194d6919b`  
		Last Modified: Thu, 12 Jun 2025 22:36:37 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c28d4afadc6fad8c6238b24d9a8dad8f8e7a8deb80839c1d3459890592b523f2`  
		Last Modified: Thu, 12 Jun 2025 22:36:38 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ebbefe72ea0510e4b225079670e073211f0b85e0fc4be94f42ca4ea57d54248`  
		Last Modified: Thu, 12 Jun 2025 22:36:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8241b18dc7eb679233e3250bbfb077dcd4f8778550fe3188d80dd91b7838a9bd`  
		Last Modified: Thu, 12 Jun 2025 22:54:58 GMT  
		Size: 7.2 MB (7230354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3cf946673d9726b4c5b57734c7dbf2e2e811f1b40e437ce7cc7bf5533df26a`  
		Last Modified: Thu, 12 Jun 2025 22:54:57 GMT  
		Size: 90.1 KB (90058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d08132e8b60b557ae762a779e816c58c6c366efd53ded71c9275533c8ec8f2d`  
		Last Modified: Thu, 12 Jun 2025 22:54:57 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d611e6743d4f047d30c66012bbac54fc821dc2ffefbbe8277a53e70060da2356`  
		Last Modified: Thu, 12 Jun 2025 22:55:00 GMT  
		Size: 57.9 MB (57897340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a783e6fb91bba730335ac30fbd49b93258f2e4d9d4c2a73dbe5c7663e5f497`  
		Last Modified: Thu, 12 Jun 2025 22:54:57 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b45b886f9c1b0ecbf83201757d3e791047d9cd0cbbdfc865a112256becf21ce4`  
		Last Modified: Thu, 12 Jun 2025 22:54:58 GMT  
		Size: 3.3 KB (3304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2.2-dind-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:d1a670e4e107e2e31f275813f1751ac249dec91fa3cfc6cc949e581bdb0c364e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb88dd0bcd267d48fad2fe5722c0bc382d70b8aa328b8a911562dc8081e3809d`

```dockerfile
```

-	Layers:
	-	`sha256:c75371d2b5d03d6fe0926a467c9d353d590b6db0765b2bc492cb0184dfe50817`  
		Last Modified: Thu, 12 Jun 2025 23:07:42 GMT  
		Size: 34.8 KB (34765 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.2.2-dind-alpine3.22` - linux; arm variant v7

```console
$ docker pull docker@sha256:66277612b6b4d8230b45b06074b5716e61c90fee840cf8b7b4da8208329fe9d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.0 MB (133027832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55fe29bbf4d101c05a3d55a85a71baf6c7ae07a62cc6865b2fc5b8902a5978a6`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-x86_64'; 			sha256='6777247eb2947c48b46b1fc96602ac17e140fbac84e1043e6384a6c755fc6769'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv6'; 			sha256='1a7731a63ec845b4b4cf2510e68a8f3411386b1e4b5b03916a0d21a697596f03'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv7'; 			sha256='63e64d9aad9916771a947e4b77df6b2a5e70cdfdb412b2f0464806f4d63fabe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-aarch64'; 			sha256='36dfcc81ffff0ec2a76abaa4b66edf01d2db0d7f3fda342a26525eb72e4e9a80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-ppc64le'; 			sha256='4410f045bfc084fef1f0fcea2c3f8e665cad6c5055f57f1089dd009bb9b65151'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-riscv64'; 			sha256='6d551f86c2ab9155882f5a1067223d0c0c80b47669c826af4311c305cc637093'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-s390x'; 			sha256='6012d0bd529312d12937fd153583a90ddb29aec7a7a8cfaac8e7fb7d1ceabf6f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 05 Jun 2025 17:36:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
CMD ["sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
VOLUME [/var/lib/docker]
# Thu, 05 Jun 2025 17:36:11 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
CMD []
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b30f7212c67694cf480811a55ca551c13acaf23308660855c528140f72c862`  
		Last Modified: Fri, 13 Jun 2025 01:20:06 GMT  
		Size: 7.4 MB (7440617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3fca8ac4e435f25c24efea81db3a20417fad9d7c421bee5ce9e3b58996c8efa`  
		Last Modified: Fri, 13 Jun 2025 01:20:05 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68a306e9551e1b17a6ecb71be8147d67ef4f891736c4e69faee945e235107fc`  
		Last Modified: Fri, 13 Jun 2025 01:20:06 GMT  
		Size: 18.1 MB (18089377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44e8dff8b0583db9cb4fc33b75dec6c3d09dd8ce3a76c2a78fd8af411bce92c`  
		Last Modified: Fri, 13 Jun 2025 01:20:08 GMT  
		Size: 19.9 MB (19927230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c665168123ed7a9acc312ff431c35318ee6393642e3e2a8bb7fa2845208b64aa`  
		Last Modified: Fri, 13 Jun 2025 01:20:08 GMT  
		Size: 19.8 MB (19821284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f454bde5fc9b6055cf7fe14c89d2a03739341ccdde89409892b34630a79576`  
		Last Modified: Fri, 13 Jun 2025 01:26:31 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3159ba7c72c13cd717ca59937ae54ce16c3ef91f409e6ff1eb4ab88fc1db06c0`  
		Last Modified: Fri, 13 Jun 2025 01:26:33 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ef5f44369f56ae39826aaf9f89b54c9bf2d4d09a86c4eaf7af04c279812997`  
		Last Modified: Fri, 13 Jun 2025 01:26:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7236561f33fb7c50ca5d7c37b075afc53fe8e4088c95319dcde0bb8ad917eb0`  
		Last Modified: Fri, 13 Jun 2025 06:24:34 GMT  
		Size: 6.5 MB (6538120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98752e61e2dd86e562ed8c9de46d0e71b38f35fe7be163828be059624970c9e`  
		Last Modified: Fri, 13 Jun 2025 06:24:35 GMT  
		Size: 86.5 KB (86488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c1e6adc4b8f7742b913355688fb6e8dd3671bd9c49551a76f2dad8f0bfcf827`  
		Last Modified: Fri, 13 Jun 2025 06:24:35 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7760efd1d6901a24ed3199cf41b66c116f64c11736dcecc92c75040a0f68dea9`  
		Last Modified: Fri, 13 Jun 2025 06:24:39 GMT  
		Size: 57.9 MB (57897375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb6cd2d2e0725f775e9f508d900bb8bac548036c111ea8957a933fc7002b93e`  
		Last Modified: Fri, 13 Jun 2025 06:24:36 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcd8d4be9dc74189aefe21d876aec06706ad1fa1e7597dd49f2c2fc862477c51`  
		Last Modified: Fri, 13 Jun 2025 06:24:36 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2.2-dind-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:9c4cb9730947a3df8f10cb2052f42e9556fa8a3d55b8d9eb9df923d7467c4a6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4fa8b980b9e0ff354efd1a786e8ee1816d49966e8cb7f6c93a8a7182923f7fd`

```dockerfile
```

-	Layers:
	-	`sha256:4bc11f3d388f7184ad2e3f2d7090c73f569bc734a2691321b72cdcb0e3735d28`  
		Last Modified: Fri, 13 Jun 2025 08:07:23 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.2.2-dind-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:b8d1c58eea384111a2c6646a55d6c57e11ce3527c44b26b17ba91e00f82530c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.5 MB (134502165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f7a08861e83333223ac02d5357e4d77380c819b320b98b1811d33973cd4cd5e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-x86_64'; 			sha256='6777247eb2947c48b46b1fc96602ac17e140fbac84e1043e6384a6c755fc6769'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv6'; 			sha256='1a7731a63ec845b4b4cf2510e68a8f3411386b1e4b5b03916a0d21a697596f03'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv7'; 			sha256='63e64d9aad9916771a947e4b77df6b2a5e70cdfdb412b2f0464806f4d63fabe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-aarch64'; 			sha256='36dfcc81ffff0ec2a76abaa4b66edf01d2db0d7f3fda342a26525eb72e4e9a80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-ppc64le'; 			sha256='4410f045bfc084fef1f0fcea2c3f8e665cad6c5055f57f1089dd009bb9b65151'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-riscv64'; 			sha256='6d551f86c2ab9155882f5a1067223d0c0c80b47669c826af4311c305cc637093'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-s390x'; 			sha256='6012d0bd529312d12937fd153583a90ddb29aec7a7a8cfaac8e7fb7d1ceabf6f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 05 Jun 2025 17:36:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
CMD ["sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
VOLUME [/var/lib/docker]
# Thu, 05 Jun 2025 17:36:11 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
CMD []
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375cb5234cd1a2b6b8f1aba00c28fc5d45ba0ecc0d3c8f130d5cdb5138ba6c09`  
		Last Modified: Fri, 13 Jun 2025 00:09:12 GMT  
		Size: 8.2 MB (8229005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ba114b122014764181bf833228533908f5eedbccce11b62f71d746ab1616ccc`  
		Last Modified: Fri, 13 Jun 2025 00:09:12 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5090356630719947eb3cfc865b4d6d8f4971f5e40c640070edd88a16ab0c486f`  
		Last Modified: Fri, 13 Jun 2025 00:09:13 GMT  
		Size: 18.9 MB (18902609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd89b3ff82b93c434d43d799f7f56e86b96409535e06f30c6bbc54456e99752d`  
		Last Modified: Fri, 13 Jun 2025 00:09:14 GMT  
		Size: 19.5 MB (19469847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb8a2de00a4f86825ec25a2f3ac1553ace626f97f529f17cda507233ec8f1a9a`  
		Last Modified: Fri, 13 Jun 2025 00:09:14 GMT  
		Size: 19.3 MB (19347260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ced3983ecfb78d04b5aefc0cf90f4a0b3ccd62ec5610841b0f7860259defda`  
		Last Modified: Fri, 13 Jun 2025 00:09:13 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3673e39b233f3bfe295c08f11dda44b40d801a0bb4f299fe81e1ec50851575`  
		Last Modified: Fri, 13 Jun 2025 00:09:13 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b219e20a46cafa0737e015b21a2525d3bb013d26dc4af6849c8f3586a8b10c5f`  
		Last Modified: Fri, 13 Jun 2025 00:09:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c6e05695096db67c5e6426307e8a652c5311da73d994e47d9580e886b837a10`  
		Last Modified: Fri, 13 Jun 2025 04:27:25 GMT  
		Size: 7.1 MB (7141507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891d71d9754311d78a8a473d578e3825acd68ce42cd0dbc623f6357a4e17c72b`  
		Last Modified: Fri, 13 Jun 2025 04:27:25 GMT  
		Size: 99.6 KB (99645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5d9a3e9b7f7718caa1aba176d0c009906cfdbf0beaabb63840d5743b89cc7f2`  
		Last Modified: Fri, 13 Jun 2025 04:27:26 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d489b833d40920f79c54667b28c6b5c28475bbdb198a31284fb082206828119a`  
		Last Modified: Fri, 13 Jun 2025 04:27:32 GMT  
		Size: 57.2 MB (57168194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e7d0e57cac200e9cb81bab37725356fb62116b7b3fb40855e245e59124702f2`  
		Last Modified: Fri, 13 Jun 2025 04:27:27 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc40c4cf8ec0a96212d48ae432d6342b219db9566141690970349c4e6140886`  
		Last Modified: Fri, 13 Jun 2025 04:27:27 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2.2-dind-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:e64e322c1cc45566807e6054fb529a1b90018a74d5599c9e524013622d5fd800
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30148cdfe5f84f758ae82d1f85d34d65c6e91c5167340993eaa3d924e06041f5`

```dockerfile
```

-	Layers:
	-	`sha256:a0dd369778c470b4b56994e10a017cc701a049c277738705f244ac7e5856bdd4`  
		Last Modified: Fri, 13 Jun 2025 05:07:36 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.2.2-dind-rootless`

```console
$ docker pull docker@sha256:c139111ddef9a8729f6be11c4f8f466526c9d9d282626ec42fe5681f14770ef1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:28.2.2-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:618707c0d004c07f5787c531d0d2b9cb07cc83c632842ec6b347811099ffc758
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.3 MB (162269674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c2a46a84fc8e55db5bd3a19a4017e96d28a0244e42500d3720717d4559dd307`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 17:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 30 May 2025 17:04:15 GMT
ENV DOCKER_VERSION=28.2.2
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 30 May 2025 17:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 30 May 2025 17:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-x86_64'; 			sha256='6777247eb2947c48b46b1fc96602ac17e140fbac84e1043e6384a6c755fc6769'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv6'; 			sha256='1a7731a63ec845b4b4cf2510e68a8f3411386b1e4b5b03916a0d21a697596f03'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv7'; 			sha256='63e64d9aad9916771a947e4b77df6b2a5e70cdfdb412b2f0464806f4d63fabe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-aarch64'; 			sha256='36dfcc81ffff0ec2a76abaa4b66edf01d2db0d7f3fda342a26525eb72e4e9a80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-ppc64le'; 			sha256='4410f045bfc084fef1f0fcea2c3f8e665cad6c5055f57f1089dd009bb9b65151'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-riscv64'; 			sha256='6d551f86c2ab9155882f5a1067223d0c0c80b47669c826af4311c305cc637093'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-s390x'; 			sha256='6012d0bd529312d12937fd153583a90ddb29aec7a7a8cfaac8e7fb7d1ceabf6f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 30 May 2025 17:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 30 May 2025 17:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 17:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 30 May 2025 17:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 30 May 2025 17:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 17:04:15 GMT
CMD ["sh"]
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 30 May 2025 17:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 30 May 2025 17:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 17:04:15 GMT
VOLUME [/var/lib/docker]
# Fri, 30 May 2025 17:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 30 May 2025 17:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 30 May 2025 17:04:15 GMT
CMD []
# Fri, 30 May 2025 17:04:15 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 30 May 2025 17:04:15 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 30 May 2025 17:04:15 GMT
USER rootless
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f32e8d6f68009e4f81cdd4d2b7e6465c3cdc96e6addc90132dfdb88d08941a20`  
		Last Modified: Thu, 12 Jun 2025 22:36:53 GMT  
		Size: 8.2 MB (8207474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ac40e43aadc31b56fc943a7df1de7e7f5f06348ca89a108384ba3e9a805a89`  
		Last Modified: Thu, 12 Jun 2025 22:36:53 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3870806677ebd2c8113c069ad6c6f219c456246069bd2688c9cffe6d1736938`  
		Last Modified: Thu, 12 Jun 2025 22:36:55 GMT  
		Size: 20.1 MB (20083028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86f14a0f3d88cab9e631bd4dcf8f9a164306875132f95135fff3358e3a2a8d2`  
		Last Modified: Thu, 12 Jun 2025 22:36:56 GMT  
		Size: 21.3 MB (21290186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da67c6f5f9a3f4626ce69c1328bdacf4c370d20479d084f6415437dea4481db4`  
		Last Modified: Thu, 12 Jun 2025 22:36:56 GMT  
		Size: 21.1 MB (21100670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b94aef2e962e8f653820f39c328e9f31ab7a6e903d929b45f9fb82324f7633`  
		Last Modified: Thu, 12 Jun 2025 22:36:55 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a98583f050f0d3b9242c387626407b4c0affec19be6fafeb1c7135bd7303d86`  
		Last Modified: Thu, 12 Jun 2025 22:36:56 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a115214fbd18e2a1acb4699bd0d7f72d42bf84a1f4cd3d4b1cdae8248a2167fa`  
		Last Modified: Thu, 12 Jun 2025 22:36:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:212150b9078af2b8495b33e957823f54b179f41a22f2702f6fec1560c9d3f6f2`  
		Last Modified: Thu, 12 Jun 2025 23:07:54 GMT  
		Size: 6.9 MB (6905618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9212e721c88d6da1ed4b1e289f523f35a01e01885d1131cd34feceb518227abf`  
		Last Modified: Thu, 12 Jun 2025 23:07:53 GMT  
		Size: 90.5 KB (90494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b0253e449f82e84618065f5b74284cb93f7cc52668795f3590d41585c32012`  
		Last Modified: Thu, 12 Jun 2025 23:07:51 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811b046d83c5b8a6340f19f8d6acd494b2b028f5c1bf969e58cf6f0e350c7cea`  
		Last Modified: Thu, 12 Jun 2025 23:07:58 GMT  
		Size: 62.2 MB (62206627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68771551084500ee9ac3a4b32aa56d78b3d007c1986578b481436becbe8ae1a1`  
		Last Modified: Thu, 12 Jun 2025 23:07:51 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cae381f867a74a59e0d18562bd189fcc3560935254e57ceb2e247145c467a8b`  
		Last Modified: Thu, 12 Jun 2025 23:07:52 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edcfb65cd16913d0735d91a3f41da46c772dc6128464cd3adef3509c06608cf3`  
		Last Modified: Fri, 13 Jun 2025 00:12:59 GMT  
		Size: 993.3 KB (993280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:969eb6fb622903c71c16e46ec5344d08043922bdd780c5d05f0149c738957108`  
		Last Modified: Fri, 13 Jun 2025 00:13:07 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5739660ee15831962b38500a68bc075c0420380781084109a21ac5085faa3d96`  
		Last Modified: Fri, 13 Jun 2025 00:13:10 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba46058072b4409214907ac1c19c90c67cc69a98dbe8bd0b997ee3be48d87947`  
		Last Modified: Fri, 13 Jun 2025 02:07:51 GMT  
		Size: 17.6 MB (17585962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10cb54f24b436f2e9ae244d4f7ad8d4d57968ee418008f027ea30581d65f6246`  
		Last Modified: Fri, 13 Jun 2025 00:13:14 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2.2-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:9601e8bc1b00849768c14fe6044913853642441e3e9735dd9882c94946a62fe2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c02d3ef5cd053c5957bec70f4a8c28ab283ebf4a2bc5372947b08dfcc8d5f2e`

```dockerfile
```

-	Layers:
	-	`sha256:9fb42be545f7a062d87207720d7a980e0dac859ea3f6630e4c65ba6816b6297c`  
		Last Modified: Fri, 13 Jun 2025 02:07:38 GMT  
		Size: 30.5 KB (30452 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.2.2-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:35c3b834f6991d8ca48c0fb727e00538a23012ae1c854f988876906aaff64efa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.5 MB (153542694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e02b9699e685722cbc13f8e1a65cafa650145a9a599a5fa1eb750135e38e774`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 17:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 30 May 2025 17:04:15 GMT
ENV DOCKER_VERSION=28.2.2
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 30 May 2025 17:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 30 May 2025 17:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-x86_64'; 			sha256='6777247eb2947c48b46b1fc96602ac17e140fbac84e1043e6384a6c755fc6769'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv6'; 			sha256='1a7731a63ec845b4b4cf2510e68a8f3411386b1e4b5b03916a0d21a697596f03'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv7'; 			sha256='63e64d9aad9916771a947e4b77df6b2a5e70cdfdb412b2f0464806f4d63fabe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-aarch64'; 			sha256='36dfcc81ffff0ec2a76abaa4b66edf01d2db0d7f3fda342a26525eb72e4e9a80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-ppc64le'; 			sha256='4410f045bfc084fef1f0fcea2c3f8e665cad6c5055f57f1089dd009bb9b65151'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-riscv64'; 			sha256='6d551f86c2ab9155882f5a1067223d0c0c80b47669c826af4311c305cc637093'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-s390x'; 			sha256='6012d0bd529312d12937fd153583a90ddb29aec7a7a8cfaac8e7fb7d1ceabf6f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 30 May 2025 17:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 30 May 2025 17:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 17:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 30 May 2025 17:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 30 May 2025 17:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 17:04:15 GMT
CMD ["sh"]
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 30 May 2025 17:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 30 May 2025 17:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 17:04:15 GMT
VOLUME [/var/lib/docker]
# Fri, 30 May 2025 17:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 30 May 2025 17:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 30 May 2025 17:04:15 GMT
CMD []
# Fri, 30 May 2025 17:04:15 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 30 May 2025 17:04:15 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 30 May 2025 17:04:15 GMT
USER rootless
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375cb5234cd1a2b6b8f1aba00c28fc5d45ba0ecc0d3c8f130d5cdb5138ba6c09`  
		Last Modified: Fri, 13 Jun 2025 00:09:12 GMT  
		Size: 8.2 MB (8229005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ba114b122014764181bf833228533908f5eedbccce11b62f71d746ab1616ccc`  
		Last Modified: Fri, 13 Jun 2025 00:09:12 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5090356630719947eb3cfc865b4d6d8f4971f5e40c640070edd88a16ab0c486f`  
		Last Modified: Fri, 13 Jun 2025 00:09:13 GMT  
		Size: 18.9 MB (18902609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd89b3ff82b93c434d43d799f7f56e86b96409535e06f30c6bbc54456e99752d`  
		Last Modified: Fri, 13 Jun 2025 00:09:14 GMT  
		Size: 19.5 MB (19469847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb8a2de00a4f86825ec25a2f3ac1553ace626f97f529f17cda507233ec8f1a9a`  
		Last Modified: Fri, 13 Jun 2025 00:09:14 GMT  
		Size: 19.3 MB (19347260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ced3983ecfb78d04b5aefc0cf90f4a0b3ccd62ec5610841b0f7860259defda`  
		Last Modified: Fri, 13 Jun 2025 00:09:13 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3673e39b233f3bfe295c08f11dda44b40d801a0bb4f299fe81e1ec50851575`  
		Last Modified: Fri, 13 Jun 2025 00:09:13 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b219e20a46cafa0737e015b21a2525d3bb013d26dc4af6849c8f3586a8b10c5f`  
		Last Modified: Fri, 13 Jun 2025 00:09:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c6e05695096db67c5e6426307e8a652c5311da73d994e47d9580e886b837a10`  
		Last Modified: Fri, 13 Jun 2025 04:27:25 GMT  
		Size: 7.1 MB (7141507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891d71d9754311d78a8a473d578e3825acd68ce42cd0dbc623f6357a4e17c72b`  
		Last Modified: Fri, 13 Jun 2025 04:27:25 GMT  
		Size: 99.6 KB (99645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5d9a3e9b7f7718caa1aba176d0c009906cfdbf0beaabb63840d5743b89cc7f2`  
		Last Modified: Fri, 13 Jun 2025 04:27:26 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d489b833d40920f79c54667b28c6b5c28475bbdb198a31284fb082206828119a`  
		Last Modified: Fri, 13 Jun 2025 04:27:32 GMT  
		Size: 57.2 MB (57168194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e7d0e57cac200e9cb81bab37725356fb62116b7b3fb40855e245e59124702f2`  
		Last Modified: Fri, 13 Jun 2025 04:27:27 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc40c4cf8ec0a96212d48ae432d6342b219db9566141690970349c4e6140886`  
		Last Modified: Fri, 13 Jun 2025 04:27:27 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c1c853189a4f7b6c93d47fd98d9be0a95acfdbc8c0f8df18df4a175a65ce3b`  
		Last Modified: Fri, 13 Jun 2025 07:11:57 GMT  
		Size: 1.0 MB (1023005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe779df0e0efd82b4a777858dfbd3496808597c320e55ab766b45677649442a`  
		Last Modified: Fri, 13 Jun 2025 07:11:56 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a244027a6953dc0bf2fd363382ff7224e9f2c0bae6332d09c4e5e68511a3b7fb`  
		Last Modified: Fri, 13 Jun 2025 07:11:57 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40237444de5d3255f0f82947d5aa58daa8391b4d2fe9b8b6565e99969a09a8d6`  
		Last Modified: Fri, 13 Jun 2025 07:12:01 GMT  
		Size: 18.0 MB (18016184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b92f2d121a50edd33cc911db99177a3a185a452e7ec47f4751ead8e59a3bc3`  
		Last Modified: Fri, 13 Jun 2025 07:11:57 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2.2-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:a9e0325277463e83ad33ae4cc4cf06e197918a3c651585f3a614fe7ddb944126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95a5b11d7826e81670044d1358d7f259365282306c1b8f9de1dbe8387517643c`

```dockerfile
```

-	Layers:
	-	`sha256:82a2387a357a58b3faf425641fd79df168694c9fdde196be68fb5632c4d7705e`  
		Last Modified: Fri, 13 Jun 2025 08:07:43 GMT  
		Size: 30.6 KB (30621 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.2.2-windowsservercore`

```console
$ docker pull docker@sha256:c244e5c2c3cc3b906baab6f383a9e91fc102f866e209e7a40dee80b3f50687f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4349; amd64
	-	windows version 10.0.20348.3807; amd64

### `docker:28.2.2-windowsservercore` - windows version 10.0.26100.4349; amd64

```console
$ docker pull docker@sha256:87b6c37c78ebd3b4dffee917bf6ba9e8e61722d7cc42313c63bf2204cf297f29
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3541382992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebb204680d5c75607c3a852fb2ef3ed327b9ccc1566c1d6a059cb0259d1a3a22`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 07 Jun 2025 15:42:01 GMT
RUN Install update 10.0.26100.4349
# Thu, 12 Jun 2025 22:41:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Jun 2025 22:41:52 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 12 Jun 2025 22:41:53 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 12 Jun 2025 22:41:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.2.2.zip
# Thu, 12 Jun 2025 22:42:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 12 Jun 2025 22:42:05 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 12 Jun 2025 22:42:06 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Thu, 12 Jun 2025 22:42:06 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Thu, 12 Jun 2025 22:42:16 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 12 Jun 2025 22:42:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Thu, 12 Jun 2025 22:42:17 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-windows-x86_64.exe
# Thu, 12 Jun 2025 22:42:18 GMT
ENV DOCKER_COMPOSE_SHA256=132fb31ef7dc81a82d7b1429adf3fd76cc0a7128059af3a172945445a50f2801
# Thu, 12 Jun 2025 22:42:28 GMT
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
	-	`sha256:7505764e5850853ff3205e21d0c6c05dd9890fed17012225b1f33d9e79ef8f7b`  
		Last Modified: Thu, 12 Jun 2025 22:46:16 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75201e0022107e322d1abb29cdcd607860e0814d97801313713016a804c7ea29`  
		Last Modified: Thu, 12 Jun 2025 22:46:17 GMT  
		Size: 384.3 KB (384281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad1332a299d19362bbb194725e3d76167ba59837dbdb186edc8c88eb4fc584fc`  
		Last Modified: Thu, 12 Jun 2025 22:46:16 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee1c450bb560eb20733ee6f9c9eab001dcdca87a8a976d64320a006b6a8626e`  
		Last Modified: Thu, 12 Jun 2025 22:46:16 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:292280c51cf870fb93a78962a22141e9734918633eac0270479904b4e7fde431`  
		Last Modified: Thu, 12 Jun 2025 22:46:19 GMT  
		Size: 20.5 MB (20474220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce832f815f971edd09a31c7ae7e5e8f1511fd9100e257f6c46649f33661d080d`  
		Last Modified: Thu, 12 Jun 2025 22:46:18 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc0188db691ee242410ed95505f0c2b6bf11c2034274be14cc637917ce9576aa`  
		Last Modified: Thu, 12 Jun 2025 22:46:18 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6d4dfab47701ffe430c0efb0d9f5640976ec9b76c70fa9adf6d9a9e37a7605a`  
		Last Modified: Thu, 12 Jun 2025 22:46:18 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c2ad7bc7d5b79fafe6d4eda10030323f4f485027233019a33343bd50a265a59`  
		Last Modified: Thu, 12 Jun 2025 22:46:21 GMT  
		Size: 22.3 MB (22283596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9538a3dff1be138d1137eb9fc139dbda8255bde275ae8670c13253a3d1033575`  
		Last Modified: Thu, 12 Jun 2025 22:46:19 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfe10fbb6bc6101cc1d7a69d3deb8126160b5db04361e52404e83b438b2fa8b3`  
		Last Modified: Thu, 12 Jun 2025 22:46:20 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2dfee3af3890e8fd03beb55f71a85b48276c6bff5474ae597f001adbd26f779`  
		Last Modified: Thu, 12 Jun 2025 22:46:20 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:846e5ade10ef88ce7e3178a17fc7662922cb37bf8403257413f21ca0869ab29c`  
		Last Modified: Thu, 12 Jun 2025 22:46:23 GMT  
		Size: 22.1 MB (22054925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28.2.2-windowsservercore` - windows version 10.0.20348.3807; amd64

```console
$ docker pull docker@sha256:53498ccee3c78a70215add9ae3ef737168375a5c54328c792752c0e5fde4eabf
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2345354530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:485c313a4ef331fdb3d3de62a8679e0f3981409d24dfa2b371f0d9efb2c3ff07`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Jun 2025 01:01:39 GMT
RUN Install update 10.0.20348.3807
# Thu, 12 Jun 2025 22:40:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Jun 2025 22:40:42 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 12 Jun 2025 22:40:43 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 12 Jun 2025 22:40:44 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.2.2.zip
# Thu, 12 Jun 2025 22:40:53 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 12 Jun 2025 22:40:54 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 12 Jun 2025 22:40:55 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Thu, 12 Jun 2025 22:40:55 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Thu, 12 Jun 2025 22:41:04 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 12 Jun 2025 22:41:05 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Thu, 12 Jun 2025 22:41:05 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-windows-x86_64.exe
# Thu, 12 Jun 2025 22:41:06 GMT
ENV DOCKER_COMPOSE_SHA256=132fb31ef7dc81a82d7b1429adf3fd76cc0a7128059af3a172945445a50f2801
# Thu, 12 Jun 2025 22:41:14 GMT
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
	-	`sha256:e3ce7730719b3563f78c11a86c6e7ca9e7ecab63539d89528367a963b46668ee`  
		Last Modified: Thu, 12 Jun 2025 22:42:44 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa44face37189a26dfbb23b8d5da4e8ec912b0e7403fa7e57fe746ede8ca163`  
		Last Modified: Thu, 12 Jun 2025 22:42:47 GMT  
		Size: 351.9 KB (351892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b288554d751322bcbba469e2992e7ed3d7addecc28b36b87bb0ac57981ad64a`  
		Last Modified: Thu, 12 Jun 2025 22:42:46 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08b3bdb645c2944656eeb7ae7bf819f0cd63f9c83b2677298c9c21d710111eec`  
		Last Modified: Thu, 12 Jun 2025 22:42:47 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b59891c80d4b303cd1655e3255818d7a3cb47a43fe98781999d05abb780b0ed`  
		Last Modified: Thu, 12 Jun 2025 22:42:50 GMT  
		Size: 20.5 MB (20450522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1af8f19e40999102aa31f1f4406c7f15eeb18843036b70938f492dee65f6943`  
		Last Modified: Thu, 12 Jun 2025 22:42:49 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f07268cae3a2cdfcdce7a98218844be1e3ede2baa06062288c10119e5414b06`  
		Last Modified: Thu, 12 Jun 2025 22:42:50 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bea31ae088d4884385e4c9bf2ff15ca1ed5f8581b5d17cba15b96224a1533af`  
		Last Modified: Thu, 12 Jun 2025 22:42:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:428d152391bf0297baa1308e6b7a51fa8dfb41c8f2dd3071d1d21fa3e4f42d41`  
		Last Modified: Thu, 12 Jun 2025 22:42:54 GMT  
		Size: 22.3 MB (22261181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b28b4c745fe11d31b3e00254bc2bc9aec2a58ab17157f558834f43f95a248ea`  
		Last Modified: Thu, 12 Jun 2025 22:42:54 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aa41358ec814cca1a580968a15e80fadcab82f43e7c6b59aea4861acb3c83ad`  
		Last Modified: Thu, 12 Jun 2025 22:42:55 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10bc742c50fda0894e2260bf3f7eb9919c098581d407b6cf2a42e3a41062305b`  
		Last Modified: Thu, 12 Jun 2025 22:42:56 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f06dfd207ec226196bd2af1228c11187c3803b22f4c3f4ac01c21d67d7207e67`  
		Last Modified: Thu, 12 Jun 2025 22:42:58 GMT  
		Size: 22.0 MB (22027759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.2.2-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:f640af5c3e1bd4c0cb40cf589e9f2f5903fcff110a95226d0c3f09140b3962eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3807; amd64

### `docker:28.2.2-windowsservercore-ltsc2022` - windows version 10.0.20348.3807; amd64

```console
$ docker pull docker@sha256:53498ccee3c78a70215add9ae3ef737168375a5c54328c792752c0e5fde4eabf
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2345354530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:485c313a4ef331fdb3d3de62a8679e0f3981409d24dfa2b371f0d9efb2c3ff07`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Jun 2025 01:01:39 GMT
RUN Install update 10.0.20348.3807
# Thu, 12 Jun 2025 22:40:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Jun 2025 22:40:42 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 12 Jun 2025 22:40:43 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 12 Jun 2025 22:40:44 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.2.2.zip
# Thu, 12 Jun 2025 22:40:53 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 12 Jun 2025 22:40:54 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 12 Jun 2025 22:40:55 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Thu, 12 Jun 2025 22:40:55 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Thu, 12 Jun 2025 22:41:04 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 12 Jun 2025 22:41:05 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Thu, 12 Jun 2025 22:41:05 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-windows-x86_64.exe
# Thu, 12 Jun 2025 22:41:06 GMT
ENV DOCKER_COMPOSE_SHA256=132fb31ef7dc81a82d7b1429adf3fd76cc0a7128059af3a172945445a50f2801
# Thu, 12 Jun 2025 22:41:14 GMT
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
	-	`sha256:e3ce7730719b3563f78c11a86c6e7ca9e7ecab63539d89528367a963b46668ee`  
		Last Modified: Thu, 12 Jun 2025 22:42:44 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa44face37189a26dfbb23b8d5da4e8ec912b0e7403fa7e57fe746ede8ca163`  
		Last Modified: Thu, 12 Jun 2025 22:42:47 GMT  
		Size: 351.9 KB (351892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b288554d751322bcbba469e2992e7ed3d7addecc28b36b87bb0ac57981ad64a`  
		Last Modified: Thu, 12 Jun 2025 22:42:46 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08b3bdb645c2944656eeb7ae7bf819f0cd63f9c83b2677298c9c21d710111eec`  
		Last Modified: Thu, 12 Jun 2025 22:42:47 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b59891c80d4b303cd1655e3255818d7a3cb47a43fe98781999d05abb780b0ed`  
		Last Modified: Thu, 12 Jun 2025 22:42:50 GMT  
		Size: 20.5 MB (20450522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1af8f19e40999102aa31f1f4406c7f15eeb18843036b70938f492dee65f6943`  
		Last Modified: Thu, 12 Jun 2025 22:42:49 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f07268cae3a2cdfcdce7a98218844be1e3ede2baa06062288c10119e5414b06`  
		Last Modified: Thu, 12 Jun 2025 22:42:50 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bea31ae088d4884385e4c9bf2ff15ca1ed5f8581b5d17cba15b96224a1533af`  
		Last Modified: Thu, 12 Jun 2025 22:42:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:428d152391bf0297baa1308e6b7a51fa8dfb41c8f2dd3071d1d21fa3e4f42d41`  
		Last Modified: Thu, 12 Jun 2025 22:42:54 GMT  
		Size: 22.3 MB (22261181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b28b4c745fe11d31b3e00254bc2bc9aec2a58ab17157f558834f43f95a248ea`  
		Last Modified: Thu, 12 Jun 2025 22:42:54 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aa41358ec814cca1a580968a15e80fadcab82f43e7c6b59aea4861acb3c83ad`  
		Last Modified: Thu, 12 Jun 2025 22:42:55 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10bc742c50fda0894e2260bf3f7eb9919c098581d407b6cf2a42e3a41062305b`  
		Last Modified: Thu, 12 Jun 2025 22:42:56 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f06dfd207ec226196bd2af1228c11187c3803b22f4c3f4ac01c21d67d7207e67`  
		Last Modified: Thu, 12 Jun 2025 22:42:58 GMT  
		Size: 22.0 MB (22027759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.2.2-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:a9266b0f45c2b149896e562c8414e4edc2f32d5f40c73cc8e69a23ce4a967d7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4349; amd64

### `docker:28.2.2-windowsservercore-ltsc2025` - windows version 10.0.26100.4349; amd64

```console
$ docker pull docker@sha256:87b6c37c78ebd3b4dffee917bf6ba9e8e61722d7cc42313c63bf2204cf297f29
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3541382992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebb204680d5c75607c3a852fb2ef3ed327b9ccc1566c1d6a059cb0259d1a3a22`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 07 Jun 2025 15:42:01 GMT
RUN Install update 10.0.26100.4349
# Thu, 12 Jun 2025 22:41:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Jun 2025 22:41:52 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 12 Jun 2025 22:41:53 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 12 Jun 2025 22:41:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.2.2.zip
# Thu, 12 Jun 2025 22:42:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 12 Jun 2025 22:42:05 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 12 Jun 2025 22:42:06 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Thu, 12 Jun 2025 22:42:06 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Thu, 12 Jun 2025 22:42:16 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 12 Jun 2025 22:42:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Thu, 12 Jun 2025 22:42:17 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-windows-x86_64.exe
# Thu, 12 Jun 2025 22:42:18 GMT
ENV DOCKER_COMPOSE_SHA256=132fb31ef7dc81a82d7b1429adf3fd76cc0a7128059af3a172945445a50f2801
# Thu, 12 Jun 2025 22:42:28 GMT
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
	-	`sha256:7505764e5850853ff3205e21d0c6c05dd9890fed17012225b1f33d9e79ef8f7b`  
		Last Modified: Thu, 12 Jun 2025 22:46:16 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75201e0022107e322d1abb29cdcd607860e0814d97801313713016a804c7ea29`  
		Last Modified: Thu, 12 Jun 2025 22:46:17 GMT  
		Size: 384.3 KB (384281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad1332a299d19362bbb194725e3d76167ba59837dbdb186edc8c88eb4fc584fc`  
		Last Modified: Thu, 12 Jun 2025 22:46:16 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee1c450bb560eb20733ee6f9c9eab001dcdca87a8a976d64320a006b6a8626e`  
		Last Modified: Thu, 12 Jun 2025 22:46:16 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:292280c51cf870fb93a78962a22141e9734918633eac0270479904b4e7fde431`  
		Last Modified: Thu, 12 Jun 2025 22:46:19 GMT  
		Size: 20.5 MB (20474220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce832f815f971edd09a31c7ae7e5e8f1511fd9100e257f6c46649f33661d080d`  
		Last Modified: Thu, 12 Jun 2025 22:46:18 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc0188db691ee242410ed95505f0c2b6bf11c2034274be14cc637917ce9576aa`  
		Last Modified: Thu, 12 Jun 2025 22:46:18 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6d4dfab47701ffe430c0efb0d9f5640976ec9b76c70fa9adf6d9a9e37a7605a`  
		Last Modified: Thu, 12 Jun 2025 22:46:18 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c2ad7bc7d5b79fafe6d4eda10030323f4f485027233019a33343bd50a265a59`  
		Last Modified: Thu, 12 Jun 2025 22:46:21 GMT  
		Size: 22.3 MB (22283596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9538a3dff1be138d1137eb9fc139dbda8255bde275ae8670c13253a3d1033575`  
		Last Modified: Thu, 12 Jun 2025 22:46:19 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfe10fbb6bc6101cc1d7a69d3deb8126160b5db04361e52404e83b438b2fa8b3`  
		Last Modified: Thu, 12 Jun 2025 22:46:20 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2dfee3af3890e8fd03beb55f71a85b48276c6bff5474ae597f001adbd26f779`  
		Last Modified: Thu, 12 Jun 2025 22:46:20 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:846e5ade10ef88ce7e3178a17fc7662922cb37bf8403257413f21ca0869ab29c`  
		Last Modified: Thu, 12 Jun 2025 22:46:23 GMT  
		Size: 22.1 MB (22054925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:cli`

```console
$ docker pull docker@sha256:5d3725f5d2f52aafe8a2c49668a43eb7c681a5535a206ba28eccfd8a3013de86
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
$ docker pull docker@sha256:b65ad6989d6333212ce011be9684e2d8ae545ec1972b56588c7aff01dd3520d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74480359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c47dbf8612e5f69d7a6b634668d1fc578e0eca340ae1f8a00812e89d72e021a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 12 Jun 2025 11:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-x86_64'; 			sha256='6777247eb2947c48b46b1fc96602ac17e140fbac84e1043e6384a6c755fc6769'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv6'; 			sha256='1a7731a63ec845b4b4cf2510e68a8f3411386b1e4b5b03916a0d21a697596f03'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv7'; 			sha256='63e64d9aad9916771a947e4b77df6b2a5e70cdfdb412b2f0464806f4d63fabe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-aarch64'; 			sha256='36dfcc81ffff0ec2a76abaa4b66edf01d2db0d7f3fda342a26525eb72e4e9a80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-ppc64le'; 			sha256='4410f045bfc084fef1f0fcea2c3f8e665cad6c5055f57f1089dd009bb9b65151'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-riscv64'; 			sha256='6d551f86c2ab9155882f5a1067223d0c0c80b47669c826af4311c305cc637093'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-s390x'; 			sha256='6012d0bd529312d12937fd153583a90ddb29aec7a7a8cfaac8e7fb7d1ceabf6f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 12 Jun 2025 11:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Jun 2025 11:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f32e8d6f68009e4f81cdd4d2b7e6465c3cdc96e6addc90132dfdb88d08941a20`  
		Last Modified: Thu, 12 Jun 2025 22:36:53 GMT  
		Size: 8.2 MB (8207474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ac40e43aadc31b56fc943a7df1de7e7f5f06348ca89a108384ba3e9a805a89`  
		Last Modified: Thu, 12 Jun 2025 22:36:53 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3870806677ebd2c8113c069ad6c6f219c456246069bd2688c9cffe6d1736938`  
		Last Modified: Thu, 12 Jun 2025 22:36:55 GMT  
		Size: 20.1 MB (20083028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86f14a0f3d88cab9e631bd4dcf8f9a164306875132f95135fff3358e3a2a8d2`  
		Last Modified: Thu, 12 Jun 2025 22:36:56 GMT  
		Size: 21.3 MB (21290186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da67c6f5f9a3f4626ce69c1328bdacf4c370d20479d084f6415437dea4481db4`  
		Last Modified: Thu, 12 Jun 2025 22:36:56 GMT  
		Size: 21.1 MB (21100670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b94aef2e962e8f653820f39c328e9f31ab7a6e903d929b45f9fb82324f7633`  
		Last Modified: Thu, 12 Jun 2025 22:36:55 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a98583f050f0d3b9242c387626407b4c0affec19be6fafeb1c7135bd7303d86`  
		Last Modified: Thu, 12 Jun 2025 22:36:56 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a115214fbd18e2a1acb4699bd0d7f72d42bf84a1f4cd3d4b1cdae8248a2167fa`  
		Last Modified: Thu, 12 Jun 2025 22:36:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:1ebe76e61490c161294dbf222ba3f54e20b9c4ef88e3a419b69d6c9ea30d9cee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adb69d08e123464b3d3e1ca5fc247dafb6079c23e370b419c72f645720be223f`

```dockerfile
```

-	Layers:
	-	`sha256:c968c006dcee70140b54235857f7cdddd7486443dbd3175f36530d5404ebc8e2`  
		Last Modified: Thu, 12 Jun 2025 23:07:35 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:cbf1afecf10a316254346c8400aefe8e45ec33d0ca7d37e94acaf8df4c243108
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69498335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4b21f5d310fad2488ce7f6f0798a746c1018659fb7fce6a3975ebe40ba17364`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 12 Jun 2025 11:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-x86_64'; 			sha256='6777247eb2947c48b46b1fc96602ac17e140fbac84e1043e6384a6c755fc6769'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv6'; 			sha256='1a7731a63ec845b4b4cf2510e68a8f3411386b1e4b5b03916a0d21a697596f03'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv7'; 			sha256='63e64d9aad9916771a947e4b77df6b2a5e70cdfdb412b2f0464806f4d63fabe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-aarch64'; 			sha256='36dfcc81ffff0ec2a76abaa4b66edf01d2db0d7f3fda342a26525eb72e4e9a80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-ppc64le'; 			sha256='4410f045bfc084fef1f0fcea2c3f8e665cad6c5055f57f1089dd009bb9b65151'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-riscv64'; 			sha256='6d551f86c2ab9155882f5a1067223d0c0c80b47669c826af4311c305cc637093'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-s390x'; 			sha256='6012d0bd529312d12937fd153583a90ddb29aec7a7a8cfaac8e7fb7d1ceabf6f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 12 Jun 2025 11:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Jun 2025 11:04:16 GMT
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
	-	`sha256:3156c3bcd5598f721d5e807804df7256e282bd2897ea9f9f029b3cd93a5ff79b`  
		Last Modified: Thu, 05 Jun 2025 22:44:12 GMT  
		Size: 18.1 MB (18101909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:225abe8edcfa38ed05c3678afaa3fc7019381a300f823c874d6fdfd2a372c345`  
		Last Modified: Thu, 05 Jun 2025 22:44:12 GMT  
		Size: 19.9 MB (19943271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aaa4a492c5a8c6019873f7f10f4583b9134c81a74df09c55d664e88521c254c`  
		Last Modified: Thu, 12 Jun 2025 22:36:39 GMT  
		Size: 19.8 MB (19835400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d441ddcc7f77e2457e59e55a8a824b3b189eaa5a13fdaf65a914da194d6919b`  
		Last Modified: Thu, 12 Jun 2025 22:36:37 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c28d4afadc6fad8c6238b24d9a8dad8f8e7a8deb80839c1d3459890592b523f2`  
		Last Modified: Thu, 12 Jun 2025 22:36:38 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ebbefe72ea0510e4b225079670e073211f0b85e0fc4be94f42ca4ea57d54248`  
		Last Modified: Thu, 12 Jun 2025 22:36:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:37fab8abfd9b21a00df69a9d07c5ae68b8fdeb2d34ff544d116b57a663143a26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4395a2db76f1506365fb0eac51245b617ca30226db9bb3af6fa171e9e441302`

```dockerfile
```

-	Layers:
	-	`sha256:ad79c76406a54721aaaa4054e1b21be3980a141745279c1866556fad3f734fd2`  
		Last Modified: Thu, 12 Jun 2025 23:07:38 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:fb3724965534d54ce9da8a451424d81fb9e4d4538aeccd1da9b3917f10a8a822
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68499848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c4ad4e83728a898d4ea348a6ce14ceb59541c63a530e27e987d9fe358f1440b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 12 Jun 2025 11:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-x86_64'; 			sha256='6777247eb2947c48b46b1fc96602ac17e140fbac84e1043e6384a6c755fc6769'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv6'; 			sha256='1a7731a63ec845b4b4cf2510e68a8f3411386b1e4b5b03916a0d21a697596f03'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv7'; 			sha256='63e64d9aad9916771a947e4b77df6b2a5e70cdfdb412b2f0464806f4d63fabe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-aarch64'; 			sha256='36dfcc81ffff0ec2a76abaa4b66edf01d2db0d7f3fda342a26525eb72e4e9a80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-ppc64le'; 			sha256='4410f045bfc084fef1f0fcea2c3f8e665cad6c5055f57f1089dd009bb9b65151'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-riscv64'; 			sha256='6d551f86c2ab9155882f5a1067223d0c0c80b47669c826af4311c305cc637093'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-s390x'; 			sha256='6012d0bd529312d12937fd153583a90ddb29aec7a7a8cfaac8e7fb7d1ceabf6f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 12 Jun 2025 11:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Jun 2025 11:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b30f7212c67694cf480811a55ca551c13acaf23308660855c528140f72c862`  
		Last Modified: Fri, 13 Jun 2025 01:20:06 GMT  
		Size: 7.4 MB (7440617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3fca8ac4e435f25c24efea81db3a20417fad9d7c421bee5ce9e3b58996c8efa`  
		Last Modified: Fri, 13 Jun 2025 01:20:05 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68a306e9551e1b17a6ecb71be8147d67ef4f891736c4e69faee945e235107fc`  
		Last Modified: Fri, 13 Jun 2025 01:20:06 GMT  
		Size: 18.1 MB (18089377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44e8dff8b0583db9cb4fc33b75dec6c3d09dd8ce3a76c2a78fd8af411bce92c`  
		Last Modified: Fri, 13 Jun 2025 01:20:08 GMT  
		Size: 19.9 MB (19927230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c665168123ed7a9acc312ff431c35318ee6393642e3e2a8bb7fa2845208b64aa`  
		Last Modified: Fri, 13 Jun 2025 01:20:08 GMT  
		Size: 19.8 MB (19821284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f454bde5fc9b6055cf7fe14c89d2a03739341ccdde89409892b34630a79576`  
		Last Modified: Fri, 13 Jun 2025 01:26:31 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3159ba7c72c13cd717ca59937ae54ce16c3ef91f409e6ff1eb4ab88fc1db06c0`  
		Last Modified: Fri, 13 Jun 2025 01:26:33 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ef5f44369f56ae39826aaf9f89b54c9bf2d4d09a86c4eaf7af04c279812997`  
		Last Modified: Fri, 13 Jun 2025 01:26:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:17bce1271d7d0578a9245dd7fa91ca7dd2d6133e2d34320d3e8cdc818063c285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2eab113b229c25442c9ce7ca62b5528b3d19f6c315834a17499edc2b29f2c94`

```dockerfile
```

-	Layers:
	-	`sha256:f90f66106ac1cc7b0fabaf95162d064739ffbb6f6d97378a5324bcfff18516c3`  
		Last Modified: Fri, 13 Jun 2025 02:07:34 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:69d471e3a384a30ce1bc54407292e5f0b7cb0b7261bc36b61aa2eb5ec882db7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70086818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd6c4ddb71ce75a68aad923b7822e2edfe7e0c0cd87a9e2d99f4feffc8015393`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 12 Jun 2025 11:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Thu, 12 Jun 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-x86_64'; 			sha256='6777247eb2947c48b46b1fc96602ac17e140fbac84e1043e6384a6c755fc6769'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv6'; 			sha256='1a7731a63ec845b4b4cf2510e68a8f3411386b1e4b5b03916a0d21a697596f03'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv7'; 			sha256='63e64d9aad9916771a947e4b77df6b2a5e70cdfdb412b2f0464806f4d63fabe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-aarch64'; 			sha256='36dfcc81ffff0ec2a76abaa4b66edf01d2db0d7f3fda342a26525eb72e4e9a80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-ppc64le'; 			sha256='4410f045bfc084fef1f0fcea2c3f8e665cad6c5055f57f1089dd009bb9b65151'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-riscv64'; 			sha256='6d551f86c2ab9155882f5a1067223d0c0c80b47669c826af4311c305cc637093'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-s390x'; 			sha256='6012d0bd529312d12937fd153583a90ddb29aec7a7a8cfaac8e7fb7d1ceabf6f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 12 Jun 2025 11:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 12 Jun 2025 11:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Jun 2025 11:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375cb5234cd1a2b6b8f1aba00c28fc5d45ba0ecc0d3c8f130d5cdb5138ba6c09`  
		Last Modified: Fri, 13 Jun 2025 00:09:12 GMT  
		Size: 8.2 MB (8229005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ba114b122014764181bf833228533908f5eedbccce11b62f71d746ab1616ccc`  
		Last Modified: Fri, 13 Jun 2025 00:09:12 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5090356630719947eb3cfc865b4d6d8f4971f5e40c640070edd88a16ab0c486f`  
		Last Modified: Fri, 13 Jun 2025 00:09:13 GMT  
		Size: 18.9 MB (18902609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd89b3ff82b93c434d43d799f7f56e86b96409535e06f30c6bbc54456e99752d`  
		Last Modified: Fri, 13 Jun 2025 00:09:14 GMT  
		Size: 19.5 MB (19469847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb8a2de00a4f86825ec25a2f3ac1553ace626f97f529f17cda507233ec8f1a9a`  
		Last Modified: Fri, 13 Jun 2025 00:09:14 GMT  
		Size: 19.3 MB (19347260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ced3983ecfb78d04b5aefc0cf90f4a0b3ccd62ec5610841b0f7860259defda`  
		Last Modified: Fri, 13 Jun 2025 00:09:13 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3673e39b233f3bfe295c08f11dda44b40d801a0bb4f299fe81e1ec50851575`  
		Last Modified: Fri, 13 Jun 2025 00:09:13 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b219e20a46cafa0737e015b21a2525d3bb013d26dc4af6849c8f3586a8b10c5f`  
		Last Modified: Fri, 13 Jun 2025 00:09:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:f4ad80ac0ebd1e61f59071330740a5cb04fcce43ee8dca6549fd765d5fb74f10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8152da6cbb3a8d4cbf91841ae5de344f2f6f46a451de0b36ffec8f81c859695d`

```dockerfile
```

-	Layers:
	-	`sha256:f8a046668b3f08af5f7ebc0544c42d2308112f3cbaa8603efab8638bb256e743`  
		Last Modified: Fri, 13 Jun 2025 02:07:38 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind`

```console
$ docker pull docker@sha256:ff052514f359111edd920b54581e7aca65629458607f9fbdbf82d7eefbe0602b
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
$ docker pull docker@sha256:8e32fae437051e392dc31f1bca659a14a6b8f341fa6dd131a9def0a9f315203c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.7 MB (143689092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:896cfe4b7aa87684cdbe7274a5a4efafa80c561662a935bd3a0432e2fcbaf46d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-x86_64'; 			sha256='6777247eb2947c48b46b1fc96602ac17e140fbac84e1043e6384a6c755fc6769'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv6'; 			sha256='1a7731a63ec845b4b4cf2510e68a8f3411386b1e4b5b03916a0d21a697596f03'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv7'; 			sha256='63e64d9aad9916771a947e4b77df6b2a5e70cdfdb412b2f0464806f4d63fabe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-aarch64'; 			sha256='36dfcc81ffff0ec2a76abaa4b66edf01d2db0d7f3fda342a26525eb72e4e9a80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-ppc64le'; 			sha256='4410f045bfc084fef1f0fcea2c3f8e665cad6c5055f57f1089dd009bb9b65151'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-riscv64'; 			sha256='6d551f86c2ab9155882f5a1067223d0c0c80b47669c826af4311c305cc637093'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-s390x'; 			sha256='6012d0bd529312d12937fd153583a90ddb29aec7a7a8cfaac8e7fb7d1ceabf6f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 05 Jun 2025 17:36:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
CMD ["sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
VOLUME [/var/lib/docker]
# Thu, 05 Jun 2025 17:36:11 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
CMD []
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f32e8d6f68009e4f81cdd4d2b7e6465c3cdc96e6addc90132dfdb88d08941a20`  
		Last Modified: Thu, 12 Jun 2025 22:36:53 GMT  
		Size: 8.2 MB (8207474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ac40e43aadc31b56fc943a7df1de7e7f5f06348ca89a108384ba3e9a805a89`  
		Last Modified: Thu, 12 Jun 2025 22:36:53 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3870806677ebd2c8113c069ad6c6f219c456246069bd2688c9cffe6d1736938`  
		Last Modified: Thu, 12 Jun 2025 22:36:55 GMT  
		Size: 20.1 MB (20083028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86f14a0f3d88cab9e631bd4dcf8f9a164306875132f95135fff3358e3a2a8d2`  
		Last Modified: Thu, 12 Jun 2025 22:36:56 GMT  
		Size: 21.3 MB (21290186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da67c6f5f9a3f4626ce69c1328bdacf4c370d20479d084f6415437dea4481db4`  
		Last Modified: Thu, 12 Jun 2025 22:36:56 GMT  
		Size: 21.1 MB (21100670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b94aef2e962e8f653820f39c328e9f31ab7a6e903d929b45f9fb82324f7633`  
		Last Modified: Thu, 12 Jun 2025 22:36:55 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a98583f050f0d3b9242c387626407b4c0affec19be6fafeb1c7135bd7303d86`  
		Last Modified: Thu, 12 Jun 2025 22:36:56 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a115214fbd18e2a1acb4699bd0d7f72d42bf84a1f4cd3d4b1cdae8248a2167fa`  
		Last Modified: Thu, 12 Jun 2025 22:36:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:212150b9078af2b8495b33e957823f54b179f41a22f2702f6fec1560c9d3f6f2`  
		Last Modified: Thu, 12 Jun 2025 23:07:54 GMT  
		Size: 6.9 MB (6905618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9212e721c88d6da1ed4b1e289f523f35a01e01885d1131cd34feceb518227abf`  
		Last Modified: Thu, 12 Jun 2025 23:07:53 GMT  
		Size: 90.5 KB (90494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b0253e449f82e84618065f5b74284cb93f7cc52668795f3590d41585c32012`  
		Last Modified: Thu, 12 Jun 2025 23:07:51 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811b046d83c5b8a6340f19f8d6acd494b2b028f5c1bf969e58cf6f0e350c7cea`  
		Last Modified: Thu, 12 Jun 2025 23:07:58 GMT  
		Size: 62.2 MB (62206627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68771551084500ee9ac3a4b32aa56d78b3d007c1986578b481436becbe8ae1a1`  
		Last Modified: Thu, 12 Jun 2025 23:07:51 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cae381f867a74a59e0d18562bd189fcc3560935254e57ceb2e247145c467a8b`  
		Last Modified: Thu, 12 Jun 2025 23:07:52 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:4c5431982a6f26acafc9a647e2a915e12fd2cb54c0d9fa6f5bed94ca07e186b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a1e46faf2561239606e7d796aac2f70a1bc3754ba1ff7200c43154e973515c8`

```dockerfile
```

-	Layers:
	-	`sha256:d5158885bee456f124624bc8808ba3f4ea82fc7ca56f260044b4d92a684498b1`  
		Last Modified: Fri, 13 Jun 2025 02:07:20 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:d692f151518fae2760b09152001cfba45f8bc770e1906d190d6eb2e3142b1a76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134722094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44d698360caa93e31e5563c2c622bbbeb75bd82d597a599776298366deb6aa32`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-x86_64'; 			sha256='6777247eb2947c48b46b1fc96602ac17e140fbac84e1043e6384a6c755fc6769'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv6'; 			sha256='1a7731a63ec845b4b4cf2510e68a8f3411386b1e4b5b03916a0d21a697596f03'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv7'; 			sha256='63e64d9aad9916771a947e4b77df6b2a5e70cdfdb412b2f0464806f4d63fabe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-aarch64'; 			sha256='36dfcc81ffff0ec2a76abaa4b66edf01d2db0d7f3fda342a26525eb72e4e9a80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-ppc64le'; 			sha256='4410f045bfc084fef1f0fcea2c3f8e665cad6c5055f57f1089dd009bb9b65151'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-riscv64'; 			sha256='6d551f86c2ab9155882f5a1067223d0c0c80b47669c826af4311c305cc637093'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-s390x'; 			sha256='6012d0bd529312d12937fd153583a90ddb29aec7a7a8cfaac8e7fb7d1ceabf6f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 05 Jun 2025 17:36:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
CMD ["sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
VOLUME [/var/lib/docker]
# Thu, 05 Jun 2025 17:36:11 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
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
	-	`sha256:3156c3bcd5598f721d5e807804df7256e282bd2897ea9f9f029b3cd93a5ff79b`  
		Last Modified: Thu, 05 Jun 2025 22:44:12 GMT  
		Size: 18.1 MB (18101909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:225abe8edcfa38ed05c3678afaa3fc7019381a300f823c874d6fdfd2a372c345`  
		Last Modified: Thu, 05 Jun 2025 22:44:12 GMT  
		Size: 19.9 MB (19943271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aaa4a492c5a8c6019873f7f10f4583b9134c81a74df09c55d664e88521c254c`  
		Last Modified: Thu, 12 Jun 2025 22:36:39 GMT  
		Size: 19.8 MB (19835400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d441ddcc7f77e2457e59e55a8a824b3b189eaa5a13fdaf65a914da194d6919b`  
		Last Modified: Thu, 12 Jun 2025 22:36:37 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c28d4afadc6fad8c6238b24d9a8dad8f8e7a8deb80839c1d3459890592b523f2`  
		Last Modified: Thu, 12 Jun 2025 22:36:38 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ebbefe72ea0510e4b225079670e073211f0b85e0fc4be94f42ca4ea57d54248`  
		Last Modified: Thu, 12 Jun 2025 22:36:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8241b18dc7eb679233e3250bbfb077dcd4f8778550fe3188d80dd91b7838a9bd`  
		Last Modified: Thu, 12 Jun 2025 22:54:58 GMT  
		Size: 7.2 MB (7230354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3cf946673d9726b4c5b57734c7dbf2e2e811f1b40e437ce7cc7bf5533df26a`  
		Last Modified: Thu, 12 Jun 2025 22:54:57 GMT  
		Size: 90.1 KB (90058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d08132e8b60b557ae762a779e816c58c6c366efd53ded71c9275533c8ec8f2d`  
		Last Modified: Thu, 12 Jun 2025 22:54:57 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d611e6743d4f047d30c66012bbac54fc821dc2ffefbbe8277a53e70060da2356`  
		Last Modified: Thu, 12 Jun 2025 22:55:00 GMT  
		Size: 57.9 MB (57897340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a783e6fb91bba730335ac30fbd49b93258f2e4d9d4c2a73dbe5c7663e5f497`  
		Last Modified: Thu, 12 Jun 2025 22:54:57 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b45b886f9c1b0ecbf83201757d3e791047d9cd0cbbdfc865a112256becf21ce4`  
		Last Modified: Thu, 12 Jun 2025 22:54:58 GMT  
		Size: 3.3 KB (3304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:d1a670e4e107e2e31f275813f1751ac249dec91fa3cfc6cc949e581bdb0c364e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb88dd0bcd267d48fad2fe5722c0bc382d70b8aa328b8a911562dc8081e3809d`

```dockerfile
```

-	Layers:
	-	`sha256:c75371d2b5d03d6fe0926a467c9d353d590b6db0765b2bc492cb0184dfe50817`  
		Last Modified: Thu, 12 Jun 2025 23:07:42 GMT  
		Size: 34.8 KB (34765 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:66277612b6b4d8230b45b06074b5716e61c90fee840cf8b7b4da8208329fe9d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.0 MB (133027832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55fe29bbf4d101c05a3d55a85a71baf6c7ae07a62cc6865b2fc5b8902a5978a6`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-x86_64'; 			sha256='6777247eb2947c48b46b1fc96602ac17e140fbac84e1043e6384a6c755fc6769'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv6'; 			sha256='1a7731a63ec845b4b4cf2510e68a8f3411386b1e4b5b03916a0d21a697596f03'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv7'; 			sha256='63e64d9aad9916771a947e4b77df6b2a5e70cdfdb412b2f0464806f4d63fabe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-aarch64'; 			sha256='36dfcc81ffff0ec2a76abaa4b66edf01d2db0d7f3fda342a26525eb72e4e9a80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-ppc64le'; 			sha256='4410f045bfc084fef1f0fcea2c3f8e665cad6c5055f57f1089dd009bb9b65151'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-riscv64'; 			sha256='6d551f86c2ab9155882f5a1067223d0c0c80b47669c826af4311c305cc637093'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-s390x'; 			sha256='6012d0bd529312d12937fd153583a90ddb29aec7a7a8cfaac8e7fb7d1ceabf6f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 05 Jun 2025 17:36:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
CMD ["sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
VOLUME [/var/lib/docker]
# Thu, 05 Jun 2025 17:36:11 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
CMD []
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b30f7212c67694cf480811a55ca551c13acaf23308660855c528140f72c862`  
		Last Modified: Fri, 13 Jun 2025 01:20:06 GMT  
		Size: 7.4 MB (7440617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3fca8ac4e435f25c24efea81db3a20417fad9d7c421bee5ce9e3b58996c8efa`  
		Last Modified: Fri, 13 Jun 2025 01:20:05 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68a306e9551e1b17a6ecb71be8147d67ef4f891736c4e69faee945e235107fc`  
		Last Modified: Fri, 13 Jun 2025 01:20:06 GMT  
		Size: 18.1 MB (18089377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44e8dff8b0583db9cb4fc33b75dec6c3d09dd8ce3a76c2a78fd8af411bce92c`  
		Last Modified: Fri, 13 Jun 2025 01:20:08 GMT  
		Size: 19.9 MB (19927230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c665168123ed7a9acc312ff431c35318ee6393642e3e2a8bb7fa2845208b64aa`  
		Last Modified: Fri, 13 Jun 2025 01:20:08 GMT  
		Size: 19.8 MB (19821284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f454bde5fc9b6055cf7fe14c89d2a03739341ccdde89409892b34630a79576`  
		Last Modified: Fri, 13 Jun 2025 01:26:31 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3159ba7c72c13cd717ca59937ae54ce16c3ef91f409e6ff1eb4ab88fc1db06c0`  
		Last Modified: Fri, 13 Jun 2025 01:26:33 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ef5f44369f56ae39826aaf9f89b54c9bf2d4d09a86c4eaf7af04c279812997`  
		Last Modified: Fri, 13 Jun 2025 01:26:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7236561f33fb7c50ca5d7c37b075afc53fe8e4088c95319dcde0bb8ad917eb0`  
		Last Modified: Fri, 13 Jun 2025 06:24:34 GMT  
		Size: 6.5 MB (6538120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98752e61e2dd86e562ed8c9de46d0e71b38f35fe7be163828be059624970c9e`  
		Last Modified: Fri, 13 Jun 2025 06:24:35 GMT  
		Size: 86.5 KB (86488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c1e6adc4b8f7742b913355688fb6e8dd3671bd9c49551a76f2dad8f0bfcf827`  
		Last Modified: Fri, 13 Jun 2025 06:24:35 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7760efd1d6901a24ed3199cf41b66c116f64c11736dcecc92c75040a0f68dea9`  
		Last Modified: Fri, 13 Jun 2025 06:24:39 GMT  
		Size: 57.9 MB (57897375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb6cd2d2e0725f775e9f508d900bb8bac548036c111ea8957a933fc7002b93e`  
		Last Modified: Fri, 13 Jun 2025 06:24:36 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcd8d4be9dc74189aefe21d876aec06706ad1fa1e7597dd49f2c2fc862477c51`  
		Last Modified: Fri, 13 Jun 2025 06:24:36 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:9c4cb9730947a3df8f10cb2052f42e9556fa8a3d55b8d9eb9df923d7467c4a6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4fa8b980b9e0ff354efd1a786e8ee1816d49966e8cb7f6c93a8a7182923f7fd`

```dockerfile
```

-	Layers:
	-	`sha256:4bc11f3d388f7184ad2e3f2d7090c73f569bc734a2691321b72cdcb0e3735d28`  
		Last Modified: Fri, 13 Jun 2025 08:07:23 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:b8d1c58eea384111a2c6646a55d6c57e11ce3527c44b26b17ba91e00f82530c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.5 MB (134502165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f7a08861e83333223ac02d5357e4d77380c819b320b98b1811d33973cd4cd5e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-x86_64'; 			sha256='6777247eb2947c48b46b1fc96602ac17e140fbac84e1043e6384a6c755fc6769'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv6'; 			sha256='1a7731a63ec845b4b4cf2510e68a8f3411386b1e4b5b03916a0d21a697596f03'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv7'; 			sha256='63e64d9aad9916771a947e4b77df6b2a5e70cdfdb412b2f0464806f4d63fabe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-aarch64'; 			sha256='36dfcc81ffff0ec2a76abaa4b66edf01d2db0d7f3fda342a26525eb72e4e9a80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-ppc64le'; 			sha256='4410f045bfc084fef1f0fcea2c3f8e665cad6c5055f57f1089dd009bb9b65151'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-riscv64'; 			sha256='6d551f86c2ab9155882f5a1067223d0c0c80b47669c826af4311c305cc637093'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-s390x'; 			sha256='6012d0bd529312d12937fd153583a90ddb29aec7a7a8cfaac8e7fb7d1ceabf6f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 05 Jun 2025 17:36:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
CMD ["sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
VOLUME [/var/lib/docker]
# Thu, 05 Jun 2025 17:36:11 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
CMD []
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375cb5234cd1a2b6b8f1aba00c28fc5d45ba0ecc0d3c8f130d5cdb5138ba6c09`  
		Last Modified: Fri, 13 Jun 2025 00:09:12 GMT  
		Size: 8.2 MB (8229005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ba114b122014764181bf833228533908f5eedbccce11b62f71d746ab1616ccc`  
		Last Modified: Fri, 13 Jun 2025 00:09:12 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5090356630719947eb3cfc865b4d6d8f4971f5e40c640070edd88a16ab0c486f`  
		Last Modified: Fri, 13 Jun 2025 00:09:13 GMT  
		Size: 18.9 MB (18902609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd89b3ff82b93c434d43d799f7f56e86b96409535e06f30c6bbc54456e99752d`  
		Last Modified: Fri, 13 Jun 2025 00:09:14 GMT  
		Size: 19.5 MB (19469847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb8a2de00a4f86825ec25a2f3ac1553ace626f97f529f17cda507233ec8f1a9a`  
		Last Modified: Fri, 13 Jun 2025 00:09:14 GMT  
		Size: 19.3 MB (19347260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ced3983ecfb78d04b5aefc0cf90f4a0b3ccd62ec5610841b0f7860259defda`  
		Last Modified: Fri, 13 Jun 2025 00:09:13 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3673e39b233f3bfe295c08f11dda44b40d801a0bb4f299fe81e1ec50851575`  
		Last Modified: Fri, 13 Jun 2025 00:09:13 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b219e20a46cafa0737e015b21a2525d3bb013d26dc4af6849c8f3586a8b10c5f`  
		Last Modified: Fri, 13 Jun 2025 00:09:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c6e05695096db67c5e6426307e8a652c5311da73d994e47d9580e886b837a10`  
		Last Modified: Fri, 13 Jun 2025 04:27:25 GMT  
		Size: 7.1 MB (7141507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891d71d9754311d78a8a473d578e3825acd68ce42cd0dbc623f6357a4e17c72b`  
		Last Modified: Fri, 13 Jun 2025 04:27:25 GMT  
		Size: 99.6 KB (99645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5d9a3e9b7f7718caa1aba176d0c009906cfdbf0beaabb63840d5743b89cc7f2`  
		Last Modified: Fri, 13 Jun 2025 04:27:26 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d489b833d40920f79c54667b28c6b5c28475bbdb198a31284fb082206828119a`  
		Last Modified: Fri, 13 Jun 2025 04:27:32 GMT  
		Size: 57.2 MB (57168194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e7d0e57cac200e9cb81bab37725356fb62116b7b3fb40855e245e59124702f2`  
		Last Modified: Fri, 13 Jun 2025 04:27:27 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc40c4cf8ec0a96212d48ae432d6342b219db9566141690970349c4e6140886`  
		Last Modified: Fri, 13 Jun 2025 04:27:27 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:e64e322c1cc45566807e6054fb529a1b90018a74d5599c9e524013622d5fd800
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30148cdfe5f84f758ae82d1f85d34d65c6e91c5167340993eaa3d924e06041f5`

```dockerfile
```

-	Layers:
	-	`sha256:a0dd369778c470b4b56994e10a017cc701a049c277738705f244ac7e5856bdd4`  
		Last Modified: Fri, 13 Jun 2025 05:07:36 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind-rootless`

```console
$ docker pull docker@sha256:c139111ddef9a8729f6be11c4f8f466526c9d9d282626ec42fe5681f14770ef1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:618707c0d004c07f5787c531d0d2b9cb07cc83c632842ec6b347811099ffc758
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.3 MB (162269674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c2a46a84fc8e55db5bd3a19a4017e96d28a0244e42500d3720717d4559dd307`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 17:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 30 May 2025 17:04:15 GMT
ENV DOCKER_VERSION=28.2.2
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 30 May 2025 17:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 30 May 2025 17:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-x86_64'; 			sha256='6777247eb2947c48b46b1fc96602ac17e140fbac84e1043e6384a6c755fc6769'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv6'; 			sha256='1a7731a63ec845b4b4cf2510e68a8f3411386b1e4b5b03916a0d21a697596f03'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv7'; 			sha256='63e64d9aad9916771a947e4b77df6b2a5e70cdfdb412b2f0464806f4d63fabe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-aarch64'; 			sha256='36dfcc81ffff0ec2a76abaa4b66edf01d2db0d7f3fda342a26525eb72e4e9a80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-ppc64le'; 			sha256='4410f045bfc084fef1f0fcea2c3f8e665cad6c5055f57f1089dd009bb9b65151'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-riscv64'; 			sha256='6d551f86c2ab9155882f5a1067223d0c0c80b47669c826af4311c305cc637093'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-s390x'; 			sha256='6012d0bd529312d12937fd153583a90ddb29aec7a7a8cfaac8e7fb7d1ceabf6f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 30 May 2025 17:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 30 May 2025 17:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 17:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 30 May 2025 17:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 30 May 2025 17:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 17:04:15 GMT
CMD ["sh"]
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 30 May 2025 17:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 30 May 2025 17:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 17:04:15 GMT
VOLUME [/var/lib/docker]
# Fri, 30 May 2025 17:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 30 May 2025 17:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 30 May 2025 17:04:15 GMT
CMD []
# Fri, 30 May 2025 17:04:15 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 30 May 2025 17:04:15 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 30 May 2025 17:04:15 GMT
USER rootless
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f32e8d6f68009e4f81cdd4d2b7e6465c3cdc96e6addc90132dfdb88d08941a20`  
		Last Modified: Thu, 12 Jun 2025 22:36:53 GMT  
		Size: 8.2 MB (8207474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ac40e43aadc31b56fc943a7df1de7e7f5f06348ca89a108384ba3e9a805a89`  
		Last Modified: Thu, 12 Jun 2025 22:36:53 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3870806677ebd2c8113c069ad6c6f219c456246069bd2688c9cffe6d1736938`  
		Last Modified: Thu, 12 Jun 2025 22:36:55 GMT  
		Size: 20.1 MB (20083028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86f14a0f3d88cab9e631bd4dcf8f9a164306875132f95135fff3358e3a2a8d2`  
		Last Modified: Thu, 12 Jun 2025 22:36:56 GMT  
		Size: 21.3 MB (21290186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da67c6f5f9a3f4626ce69c1328bdacf4c370d20479d084f6415437dea4481db4`  
		Last Modified: Thu, 12 Jun 2025 22:36:56 GMT  
		Size: 21.1 MB (21100670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b94aef2e962e8f653820f39c328e9f31ab7a6e903d929b45f9fb82324f7633`  
		Last Modified: Thu, 12 Jun 2025 22:36:55 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a98583f050f0d3b9242c387626407b4c0affec19be6fafeb1c7135bd7303d86`  
		Last Modified: Thu, 12 Jun 2025 22:36:56 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a115214fbd18e2a1acb4699bd0d7f72d42bf84a1f4cd3d4b1cdae8248a2167fa`  
		Last Modified: Thu, 12 Jun 2025 22:36:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:212150b9078af2b8495b33e957823f54b179f41a22f2702f6fec1560c9d3f6f2`  
		Last Modified: Thu, 12 Jun 2025 23:07:54 GMT  
		Size: 6.9 MB (6905618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9212e721c88d6da1ed4b1e289f523f35a01e01885d1131cd34feceb518227abf`  
		Last Modified: Thu, 12 Jun 2025 23:07:53 GMT  
		Size: 90.5 KB (90494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b0253e449f82e84618065f5b74284cb93f7cc52668795f3590d41585c32012`  
		Last Modified: Thu, 12 Jun 2025 23:07:51 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811b046d83c5b8a6340f19f8d6acd494b2b028f5c1bf969e58cf6f0e350c7cea`  
		Last Modified: Thu, 12 Jun 2025 23:07:58 GMT  
		Size: 62.2 MB (62206627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68771551084500ee9ac3a4b32aa56d78b3d007c1986578b481436becbe8ae1a1`  
		Last Modified: Thu, 12 Jun 2025 23:07:51 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cae381f867a74a59e0d18562bd189fcc3560935254e57ceb2e247145c467a8b`  
		Last Modified: Thu, 12 Jun 2025 23:07:52 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edcfb65cd16913d0735d91a3f41da46c772dc6128464cd3adef3509c06608cf3`  
		Last Modified: Fri, 13 Jun 2025 00:12:59 GMT  
		Size: 993.3 KB (993280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:969eb6fb622903c71c16e46ec5344d08043922bdd780c5d05f0149c738957108`  
		Last Modified: Fri, 13 Jun 2025 00:13:07 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5739660ee15831962b38500a68bc075c0420380781084109a21ac5085faa3d96`  
		Last Modified: Fri, 13 Jun 2025 00:13:10 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba46058072b4409214907ac1c19c90c67cc69a98dbe8bd0b997ee3be48d87947`  
		Last Modified: Fri, 13 Jun 2025 02:07:51 GMT  
		Size: 17.6 MB (17585962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10cb54f24b436f2e9ae244d4f7ad8d4d57968ee418008f027ea30581d65f6246`  
		Last Modified: Fri, 13 Jun 2025 00:13:14 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:9601e8bc1b00849768c14fe6044913853642441e3e9735dd9882c94946a62fe2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c02d3ef5cd053c5957bec70f4a8c28ab283ebf4a2bc5372947b08dfcc8d5f2e`

```dockerfile
```

-	Layers:
	-	`sha256:9fb42be545f7a062d87207720d7a980e0dac859ea3f6630e4c65ba6816b6297c`  
		Last Modified: Fri, 13 Jun 2025 02:07:38 GMT  
		Size: 30.5 KB (30452 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:35c3b834f6991d8ca48c0fb727e00538a23012ae1c854f988876906aaff64efa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.5 MB (153542694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e02b9699e685722cbc13f8e1a65cafa650145a9a599a5fa1eb750135e38e774`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 17:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 30 May 2025 17:04:15 GMT
ENV DOCKER_VERSION=28.2.2
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 30 May 2025 17:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 30 May 2025 17:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-x86_64'; 			sha256='6777247eb2947c48b46b1fc96602ac17e140fbac84e1043e6384a6c755fc6769'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv6'; 			sha256='1a7731a63ec845b4b4cf2510e68a8f3411386b1e4b5b03916a0d21a697596f03'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv7'; 			sha256='63e64d9aad9916771a947e4b77df6b2a5e70cdfdb412b2f0464806f4d63fabe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-aarch64'; 			sha256='36dfcc81ffff0ec2a76abaa4b66edf01d2db0d7f3fda342a26525eb72e4e9a80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-ppc64le'; 			sha256='4410f045bfc084fef1f0fcea2c3f8e665cad6c5055f57f1089dd009bb9b65151'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-riscv64'; 			sha256='6d551f86c2ab9155882f5a1067223d0c0c80b47669c826af4311c305cc637093'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-s390x'; 			sha256='6012d0bd529312d12937fd153583a90ddb29aec7a7a8cfaac8e7fb7d1ceabf6f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 30 May 2025 17:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 30 May 2025 17:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 17:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 30 May 2025 17:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 30 May 2025 17:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 17:04:15 GMT
CMD ["sh"]
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 30 May 2025 17:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 30 May 2025 17:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 17:04:15 GMT
VOLUME [/var/lib/docker]
# Fri, 30 May 2025 17:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 30 May 2025 17:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 30 May 2025 17:04:15 GMT
CMD []
# Fri, 30 May 2025 17:04:15 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 30 May 2025 17:04:15 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 30 May 2025 17:04:15 GMT
USER rootless
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375cb5234cd1a2b6b8f1aba00c28fc5d45ba0ecc0d3c8f130d5cdb5138ba6c09`  
		Last Modified: Fri, 13 Jun 2025 00:09:12 GMT  
		Size: 8.2 MB (8229005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ba114b122014764181bf833228533908f5eedbccce11b62f71d746ab1616ccc`  
		Last Modified: Fri, 13 Jun 2025 00:09:12 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5090356630719947eb3cfc865b4d6d8f4971f5e40c640070edd88a16ab0c486f`  
		Last Modified: Fri, 13 Jun 2025 00:09:13 GMT  
		Size: 18.9 MB (18902609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd89b3ff82b93c434d43d799f7f56e86b96409535e06f30c6bbc54456e99752d`  
		Last Modified: Fri, 13 Jun 2025 00:09:14 GMT  
		Size: 19.5 MB (19469847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb8a2de00a4f86825ec25a2f3ac1553ace626f97f529f17cda507233ec8f1a9a`  
		Last Modified: Fri, 13 Jun 2025 00:09:14 GMT  
		Size: 19.3 MB (19347260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ced3983ecfb78d04b5aefc0cf90f4a0b3ccd62ec5610841b0f7860259defda`  
		Last Modified: Fri, 13 Jun 2025 00:09:13 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3673e39b233f3bfe295c08f11dda44b40d801a0bb4f299fe81e1ec50851575`  
		Last Modified: Fri, 13 Jun 2025 00:09:13 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b219e20a46cafa0737e015b21a2525d3bb013d26dc4af6849c8f3586a8b10c5f`  
		Last Modified: Fri, 13 Jun 2025 00:09:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c6e05695096db67c5e6426307e8a652c5311da73d994e47d9580e886b837a10`  
		Last Modified: Fri, 13 Jun 2025 04:27:25 GMT  
		Size: 7.1 MB (7141507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891d71d9754311d78a8a473d578e3825acd68ce42cd0dbc623f6357a4e17c72b`  
		Last Modified: Fri, 13 Jun 2025 04:27:25 GMT  
		Size: 99.6 KB (99645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5d9a3e9b7f7718caa1aba176d0c009906cfdbf0beaabb63840d5743b89cc7f2`  
		Last Modified: Fri, 13 Jun 2025 04:27:26 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d489b833d40920f79c54667b28c6b5c28475bbdb198a31284fb082206828119a`  
		Last Modified: Fri, 13 Jun 2025 04:27:32 GMT  
		Size: 57.2 MB (57168194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e7d0e57cac200e9cb81bab37725356fb62116b7b3fb40855e245e59124702f2`  
		Last Modified: Fri, 13 Jun 2025 04:27:27 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc40c4cf8ec0a96212d48ae432d6342b219db9566141690970349c4e6140886`  
		Last Modified: Fri, 13 Jun 2025 04:27:27 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c1c853189a4f7b6c93d47fd98d9be0a95acfdbc8c0f8df18df4a175a65ce3b`  
		Last Modified: Fri, 13 Jun 2025 07:11:57 GMT  
		Size: 1.0 MB (1023005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe779df0e0efd82b4a777858dfbd3496808597c320e55ab766b45677649442a`  
		Last Modified: Fri, 13 Jun 2025 07:11:56 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a244027a6953dc0bf2fd363382ff7224e9f2c0bae6332d09c4e5e68511a3b7fb`  
		Last Modified: Fri, 13 Jun 2025 07:11:57 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40237444de5d3255f0f82947d5aa58daa8391b4d2fe9b8b6565e99969a09a8d6`  
		Last Modified: Fri, 13 Jun 2025 07:12:01 GMT  
		Size: 18.0 MB (18016184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b92f2d121a50edd33cc911db99177a3a185a452e7ec47f4751ead8e59a3bc3`  
		Last Modified: Fri, 13 Jun 2025 07:11:57 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:a9e0325277463e83ad33ae4cc4cf06e197918a3c651585f3a614fe7ddb944126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95a5b11d7826e81670044d1358d7f259365282306c1b8f9de1dbe8387517643c`

```dockerfile
```

-	Layers:
	-	`sha256:82a2387a357a58b3faf425641fd79df168694c9fdde196be68fb5632c4d7705e`  
		Last Modified: Fri, 13 Jun 2025 08:07:43 GMT  
		Size: 30.6 KB (30621 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:latest`

```console
$ docker pull docker@sha256:ff052514f359111edd920b54581e7aca65629458607f9fbdbf82d7eefbe0602b
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
$ docker pull docker@sha256:8e32fae437051e392dc31f1bca659a14a6b8f341fa6dd131a9def0a9f315203c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.7 MB (143689092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:896cfe4b7aa87684cdbe7274a5a4efafa80c561662a935bd3a0432e2fcbaf46d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-x86_64'; 			sha256='6777247eb2947c48b46b1fc96602ac17e140fbac84e1043e6384a6c755fc6769'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv6'; 			sha256='1a7731a63ec845b4b4cf2510e68a8f3411386b1e4b5b03916a0d21a697596f03'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv7'; 			sha256='63e64d9aad9916771a947e4b77df6b2a5e70cdfdb412b2f0464806f4d63fabe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-aarch64'; 			sha256='36dfcc81ffff0ec2a76abaa4b66edf01d2db0d7f3fda342a26525eb72e4e9a80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-ppc64le'; 			sha256='4410f045bfc084fef1f0fcea2c3f8e665cad6c5055f57f1089dd009bb9b65151'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-riscv64'; 			sha256='6d551f86c2ab9155882f5a1067223d0c0c80b47669c826af4311c305cc637093'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-s390x'; 			sha256='6012d0bd529312d12937fd153583a90ddb29aec7a7a8cfaac8e7fb7d1ceabf6f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 05 Jun 2025 17:36:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
CMD ["sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
VOLUME [/var/lib/docker]
# Thu, 05 Jun 2025 17:36:11 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
CMD []
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f32e8d6f68009e4f81cdd4d2b7e6465c3cdc96e6addc90132dfdb88d08941a20`  
		Last Modified: Thu, 12 Jun 2025 22:36:53 GMT  
		Size: 8.2 MB (8207474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ac40e43aadc31b56fc943a7df1de7e7f5f06348ca89a108384ba3e9a805a89`  
		Last Modified: Thu, 12 Jun 2025 22:36:53 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3870806677ebd2c8113c069ad6c6f219c456246069bd2688c9cffe6d1736938`  
		Last Modified: Thu, 12 Jun 2025 22:36:55 GMT  
		Size: 20.1 MB (20083028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86f14a0f3d88cab9e631bd4dcf8f9a164306875132f95135fff3358e3a2a8d2`  
		Last Modified: Thu, 12 Jun 2025 22:36:56 GMT  
		Size: 21.3 MB (21290186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da67c6f5f9a3f4626ce69c1328bdacf4c370d20479d084f6415437dea4481db4`  
		Last Modified: Thu, 12 Jun 2025 22:36:56 GMT  
		Size: 21.1 MB (21100670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b94aef2e962e8f653820f39c328e9f31ab7a6e903d929b45f9fb82324f7633`  
		Last Modified: Thu, 12 Jun 2025 22:36:55 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a98583f050f0d3b9242c387626407b4c0affec19be6fafeb1c7135bd7303d86`  
		Last Modified: Thu, 12 Jun 2025 22:36:56 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a115214fbd18e2a1acb4699bd0d7f72d42bf84a1f4cd3d4b1cdae8248a2167fa`  
		Last Modified: Thu, 12 Jun 2025 22:36:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:212150b9078af2b8495b33e957823f54b179f41a22f2702f6fec1560c9d3f6f2`  
		Last Modified: Thu, 12 Jun 2025 23:07:54 GMT  
		Size: 6.9 MB (6905618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9212e721c88d6da1ed4b1e289f523f35a01e01885d1131cd34feceb518227abf`  
		Last Modified: Thu, 12 Jun 2025 23:07:53 GMT  
		Size: 90.5 KB (90494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b0253e449f82e84618065f5b74284cb93f7cc52668795f3590d41585c32012`  
		Last Modified: Thu, 12 Jun 2025 23:07:51 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811b046d83c5b8a6340f19f8d6acd494b2b028f5c1bf969e58cf6f0e350c7cea`  
		Last Modified: Thu, 12 Jun 2025 23:07:58 GMT  
		Size: 62.2 MB (62206627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68771551084500ee9ac3a4b32aa56d78b3d007c1986578b481436becbe8ae1a1`  
		Last Modified: Thu, 12 Jun 2025 23:07:51 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cae381f867a74a59e0d18562bd189fcc3560935254e57ceb2e247145c467a8b`  
		Last Modified: Thu, 12 Jun 2025 23:07:52 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:4c5431982a6f26acafc9a647e2a915e12fd2cb54c0d9fa6f5bed94ca07e186b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a1e46faf2561239606e7d796aac2f70a1bc3754ba1ff7200c43154e973515c8`

```dockerfile
```

-	Layers:
	-	`sha256:d5158885bee456f124624bc8808ba3f4ea82fc7ca56f260044b4d92a684498b1`  
		Last Modified: Fri, 13 Jun 2025 02:07:20 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v6

```console
$ docker pull docker@sha256:d692f151518fae2760b09152001cfba45f8bc770e1906d190d6eb2e3142b1a76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134722094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44d698360caa93e31e5563c2c622bbbeb75bd82d597a599776298366deb6aa32`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-x86_64'; 			sha256='6777247eb2947c48b46b1fc96602ac17e140fbac84e1043e6384a6c755fc6769'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv6'; 			sha256='1a7731a63ec845b4b4cf2510e68a8f3411386b1e4b5b03916a0d21a697596f03'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv7'; 			sha256='63e64d9aad9916771a947e4b77df6b2a5e70cdfdb412b2f0464806f4d63fabe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-aarch64'; 			sha256='36dfcc81ffff0ec2a76abaa4b66edf01d2db0d7f3fda342a26525eb72e4e9a80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-ppc64le'; 			sha256='4410f045bfc084fef1f0fcea2c3f8e665cad6c5055f57f1089dd009bb9b65151'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-riscv64'; 			sha256='6d551f86c2ab9155882f5a1067223d0c0c80b47669c826af4311c305cc637093'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-s390x'; 			sha256='6012d0bd529312d12937fd153583a90ddb29aec7a7a8cfaac8e7fb7d1ceabf6f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 05 Jun 2025 17:36:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
CMD ["sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
VOLUME [/var/lib/docker]
# Thu, 05 Jun 2025 17:36:11 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
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
	-	`sha256:3156c3bcd5598f721d5e807804df7256e282bd2897ea9f9f029b3cd93a5ff79b`  
		Last Modified: Thu, 05 Jun 2025 22:44:12 GMT  
		Size: 18.1 MB (18101909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:225abe8edcfa38ed05c3678afaa3fc7019381a300f823c874d6fdfd2a372c345`  
		Last Modified: Thu, 05 Jun 2025 22:44:12 GMT  
		Size: 19.9 MB (19943271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aaa4a492c5a8c6019873f7f10f4583b9134c81a74df09c55d664e88521c254c`  
		Last Modified: Thu, 12 Jun 2025 22:36:39 GMT  
		Size: 19.8 MB (19835400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d441ddcc7f77e2457e59e55a8a824b3b189eaa5a13fdaf65a914da194d6919b`  
		Last Modified: Thu, 12 Jun 2025 22:36:37 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c28d4afadc6fad8c6238b24d9a8dad8f8e7a8deb80839c1d3459890592b523f2`  
		Last Modified: Thu, 12 Jun 2025 22:36:38 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ebbefe72ea0510e4b225079670e073211f0b85e0fc4be94f42ca4ea57d54248`  
		Last Modified: Thu, 12 Jun 2025 22:36:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8241b18dc7eb679233e3250bbfb077dcd4f8778550fe3188d80dd91b7838a9bd`  
		Last Modified: Thu, 12 Jun 2025 22:54:58 GMT  
		Size: 7.2 MB (7230354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3cf946673d9726b4c5b57734c7dbf2e2e811f1b40e437ce7cc7bf5533df26a`  
		Last Modified: Thu, 12 Jun 2025 22:54:57 GMT  
		Size: 90.1 KB (90058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d08132e8b60b557ae762a779e816c58c6c366efd53ded71c9275533c8ec8f2d`  
		Last Modified: Thu, 12 Jun 2025 22:54:57 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d611e6743d4f047d30c66012bbac54fc821dc2ffefbbe8277a53e70060da2356`  
		Last Modified: Thu, 12 Jun 2025 22:55:00 GMT  
		Size: 57.9 MB (57897340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a783e6fb91bba730335ac30fbd49b93258f2e4d9d4c2a73dbe5c7663e5f497`  
		Last Modified: Thu, 12 Jun 2025 22:54:57 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b45b886f9c1b0ecbf83201757d3e791047d9cd0cbbdfc865a112256becf21ce4`  
		Last Modified: Thu, 12 Jun 2025 22:54:58 GMT  
		Size: 3.3 KB (3304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:d1a670e4e107e2e31f275813f1751ac249dec91fa3cfc6cc949e581bdb0c364e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb88dd0bcd267d48fad2fe5722c0bc382d70b8aa328b8a911562dc8081e3809d`

```dockerfile
```

-	Layers:
	-	`sha256:c75371d2b5d03d6fe0926a467c9d353d590b6db0765b2bc492cb0184dfe50817`  
		Last Modified: Thu, 12 Jun 2025 23:07:42 GMT  
		Size: 34.8 KB (34765 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v7

```console
$ docker pull docker@sha256:66277612b6b4d8230b45b06074b5716e61c90fee840cf8b7b4da8208329fe9d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.0 MB (133027832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55fe29bbf4d101c05a3d55a85a71baf6c7ae07a62cc6865b2fc5b8902a5978a6`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-x86_64'; 			sha256='6777247eb2947c48b46b1fc96602ac17e140fbac84e1043e6384a6c755fc6769'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv6'; 			sha256='1a7731a63ec845b4b4cf2510e68a8f3411386b1e4b5b03916a0d21a697596f03'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv7'; 			sha256='63e64d9aad9916771a947e4b77df6b2a5e70cdfdb412b2f0464806f4d63fabe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-aarch64'; 			sha256='36dfcc81ffff0ec2a76abaa4b66edf01d2db0d7f3fda342a26525eb72e4e9a80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-ppc64le'; 			sha256='4410f045bfc084fef1f0fcea2c3f8e665cad6c5055f57f1089dd009bb9b65151'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-riscv64'; 			sha256='6d551f86c2ab9155882f5a1067223d0c0c80b47669c826af4311c305cc637093'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-s390x'; 			sha256='6012d0bd529312d12937fd153583a90ddb29aec7a7a8cfaac8e7fb7d1ceabf6f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 05 Jun 2025 17:36:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
CMD ["sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
VOLUME [/var/lib/docker]
# Thu, 05 Jun 2025 17:36:11 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
CMD []
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b30f7212c67694cf480811a55ca551c13acaf23308660855c528140f72c862`  
		Last Modified: Fri, 13 Jun 2025 01:20:06 GMT  
		Size: 7.4 MB (7440617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3fca8ac4e435f25c24efea81db3a20417fad9d7c421bee5ce9e3b58996c8efa`  
		Last Modified: Fri, 13 Jun 2025 01:20:05 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68a306e9551e1b17a6ecb71be8147d67ef4f891736c4e69faee945e235107fc`  
		Last Modified: Fri, 13 Jun 2025 01:20:06 GMT  
		Size: 18.1 MB (18089377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44e8dff8b0583db9cb4fc33b75dec6c3d09dd8ce3a76c2a78fd8af411bce92c`  
		Last Modified: Fri, 13 Jun 2025 01:20:08 GMT  
		Size: 19.9 MB (19927230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c665168123ed7a9acc312ff431c35318ee6393642e3e2a8bb7fa2845208b64aa`  
		Last Modified: Fri, 13 Jun 2025 01:20:08 GMT  
		Size: 19.8 MB (19821284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f454bde5fc9b6055cf7fe14c89d2a03739341ccdde89409892b34630a79576`  
		Last Modified: Fri, 13 Jun 2025 01:26:31 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3159ba7c72c13cd717ca59937ae54ce16c3ef91f409e6ff1eb4ab88fc1db06c0`  
		Last Modified: Fri, 13 Jun 2025 01:26:33 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ef5f44369f56ae39826aaf9f89b54c9bf2d4d09a86c4eaf7af04c279812997`  
		Last Modified: Fri, 13 Jun 2025 01:26:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7236561f33fb7c50ca5d7c37b075afc53fe8e4088c95319dcde0bb8ad917eb0`  
		Last Modified: Fri, 13 Jun 2025 06:24:34 GMT  
		Size: 6.5 MB (6538120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98752e61e2dd86e562ed8c9de46d0e71b38f35fe7be163828be059624970c9e`  
		Last Modified: Fri, 13 Jun 2025 06:24:35 GMT  
		Size: 86.5 KB (86488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c1e6adc4b8f7742b913355688fb6e8dd3671bd9c49551a76f2dad8f0bfcf827`  
		Last Modified: Fri, 13 Jun 2025 06:24:35 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7760efd1d6901a24ed3199cf41b66c116f64c11736dcecc92c75040a0f68dea9`  
		Last Modified: Fri, 13 Jun 2025 06:24:39 GMT  
		Size: 57.9 MB (57897375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb6cd2d2e0725f775e9f508d900bb8bac548036c111ea8957a933fc7002b93e`  
		Last Modified: Fri, 13 Jun 2025 06:24:36 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcd8d4be9dc74189aefe21d876aec06706ad1fa1e7597dd49f2c2fc862477c51`  
		Last Modified: Fri, 13 Jun 2025 06:24:36 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:9c4cb9730947a3df8f10cb2052f42e9556fa8a3d55b8d9eb9df923d7467c4a6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4fa8b980b9e0ff354efd1a786e8ee1816d49966e8cb7f6c93a8a7182923f7fd`

```dockerfile
```

-	Layers:
	-	`sha256:4bc11f3d388f7184ad2e3f2d7090c73f569bc734a2691321b72cdcb0e3735d28`  
		Last Modified: Fri, 13 Jun 2025 08:07:23 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:b8d1c58eea384111a2c6646a55d6c57e11ce3527c44b26b17ba91e00f82530c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.5 MB (134502165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f7a08861e83333223ac02d5357e4d77380c819b320b98b1811d33973cd4cd5e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-x86_64'; 			sha256='6777247eb2947c48b46b1fc96602ac17e140fbac84e1043e6384a6c755fc6769'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv6'; 			sha256='1a7731a63ec845b4b4cf2510e68a8f3411386b1e4b5b03916a0d21a697596f03'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-armv7'; 			sha256='63e64d9aad9916771a947e4b77df6b2a5e70cdfdb412b2f0464806f4d63fabe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-aarch64'; 			sha256='36dfcc81ffff0ec2a76abaa4b66edf01d2db0d7f3fda342a26525eb72e4e9a80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-ppc64le'; 			sha256='4410f045bfc084fef1f0fcea2c3f8e665cad6c5055f57f1089dd009bb9b65151'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-riscv64'; 			sha256='6d551f86c2ab9155882f5a1067223d0c0c80b47669c826af4311c305cc637093'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-linux-s390x'; 			sha256='6012d0bd529312d12937fd153583a90ddb29aec7a7a8cfaac8e7fb7d1ceabf6f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 05 Jun 2025 17:36:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
CMD ["sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
VOLUME [/var/lib/docker]
# Thu, 05 Jun 2025 17:36:11 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
CMD []
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375cb5234cd1a2b6b8f1aba00c28fc5d45ba0ecc0d3c8f130d5cdb5138ba6c09`  
		Last Modified: Fri, 13 Jun 2025 00:09:12 GMT  
		Size: 8.2 MB (8229005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ba114b122014764181bf833228533908f5eedbccce11b62f71d746ab1616ccc`  
		Last Modified: Fri, 13 Jun 2025 00:09:12 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5090356630719947eb3cfc865b4d6d8f4971f5e40c640070edd88a16ab0c486f`  
		Last Modified: Fri, 13 Jun 2025 00:09:13 GMT  
		Size: 18.9 MB (18902609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd89b3ff82b93c434d43d799f7f56e86b96409535e06f30c6bbc54456e99752d`  
		Last Modified: Fri, 13 Jun 2025 00:09:14 GMT  
		Size: 19.5 MB (19469847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb8a2de00a4f86825ec25a2f3ac1553ace626f97f529f17cda507233ec8f1a9a`  
		Last Modified: Fri, 13 Jun 2025 00:09:14 GMT  
		Size: 19.3 MB (19347260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ced3983ecfb78d04b5aefc0cf90f4a0b3ccd62ec5610841b0f7860259defda`  
		Last Modified: Fri, 13 Jun 2025 00:09:13 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3673e39b233f3bfe295c08f11dda44b40d801a0bb4f299fe81e1ec50851575`  
		Last Modified: Fri, 13 Jun 2025 00:09:13 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b219e20a46cafa0737e015b21a2525d3bb013d26dc4af6849c8f3586a8b10c5f`  
		Last Modified: Fri, 13 Jun 2025 00:09:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c6e05695096db67c5e6426307e8a652c5311da73d994e47d9580e886b837a10`  
		Last Modified: Fri, 13 Jun 2025 04:27:25 GMT  
		Size: 7.1 MB (7141507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891d71d9754311d78a8a473d578e3825acd68ce42cd0dbc623f6357a4e17c72b`  
		Last Modified: Fri, 13 Jun 2025 04:27:25 GMT  
		Size: 99.6 KB (99645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5d9a3e9b7f7718caa1aba176d0c009906cfdbf0beaabb63840d5743b89cc7f2`  
		Last Modified: Fri, 13 Jun 2025 04:27:26 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d489b833d40920f79c54667b28c6b5c28475bbdb198a31284fb082206828119a`  
		Last Modified: Fri, 13 Jun 2025 04:27:32 GMT  
		Size: 57.2 MB (57168194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e7d0e57cac200e9cb81bab37725356fb62116b7b3fb40855e245e59124702f2`  
		Last Modified: Fri, 13 Jun 2025 04:27:27 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc40c4cf8ec0a96212d48ae432d6342b219db9566141690970349c4e6140886`  
		Last Modified: Fri, 13 Jun 2025 04:27:27 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:e64e322c1cc45566807e6054fb529a1b90018a74d5599c9e524013622d5fd800
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30148cdfe5f84f758ae82d1f85d34d65c6e91c5167340993eaa3d924e06041f5`

```dockerfile
```

-	Layers:
	-	`sha256:a0dd369778c470b4b56994e10a017cc701a049c277738705f244ac7e5856bdd4`  
		Last Modified: Fri, 13 Jun 2025 05:07:36 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:windowsservercore`

```console
$ docker pull docker@sha256:c244e5c2c3cc3b906baab6f383a9e91fc102f866e209e7a40dee80b3f50687f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4349; amd64
	-	windows version 10.0.20348.3807; amd64

### `docker:windowsservercore` - windows version 10.0.26100.4349; amd64

```console
$ docker pull docker@sha256:87b6c37c78ebd3b4dffee917bf6ba9e8e61722d7cc42313c63bf2204cf297f29
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3541382992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebb204680d5c75607c3a852fb2ef3ed327b9ccc1566c1d6a059cb0259d1a3a22`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 07 Jun 2025 15:42:01 GMT
RUN Install update 10.0.26100.4349
# Thu, 12 Jun 2025 22:41:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Jun 2025 22:41:52 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 12 Jun 2025 22:41:53 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 12 Jun 2025 22:41:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.2.2.zip
# Thu, 12 Jun 2025 22:42:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 12 Jun 2025 22:42:05 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 12 Jun 2025 22:42:06 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Thu, 12 Jun 2025 22:42:06 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Thu, 12 Jun 2025 22:42:16 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 12 Jun 2025 22:42:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Thu, 12 Jun 2025 22:42:17 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-windows-x86_64.exe
# Thu, 12 Jun 2025 22:42:18 GMT
ENV DOCKER_COMPOSE_SHA256=132fb31ef7dc81a82d7b1429adf3fd76cc0a7128059af3a172945445a50f2801
# Thu, 12 Jun 2025 22:42:28 GMT
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
	-	`sha256:7505764e5850853ff3205e21d0c6c05dd9890fed17012225b1f33d9e79ef8f7b`  
		Last Modified: Thu, 12 Jun 2025 22:46:16 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75201e0022107e322d1abb29cdcd607860e0814d97801313713016a804c7ea29`  
		Last Modified: Thu, 12 Jun 2025 22:46:17 GMT  
		Size: 384.3 KB (384281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad1332a299d19362bbb194725e3d76167ba59837dbdb186edc8c88eb4fc584fc`  
		Last Modified: Thu, 12 Jun 2025 22:46:16 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee1c450bb560eb20733ee6f9c9eab001dcdca87a8a976d64320a006b6a8626e`  
		Last Modified: Thu, 12 Jun 2025 22:46:16 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:292280c51cf870fb93a78962a22141e9734918633eac0270479904b4e7fde431`  
		Last Modified: Thu, 12 Jun 2025 22:46:19 GMT  
		Size: 20.5 MB (20474220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce832f815f971edd09a31c7ae7e5e8f1511fd9100e257f6c46649f33661d080d`  
		Last Modified: Thu, 12 Jun 2025 22:46:18 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc0188db691ee242410ed95505f0c2b6bf11c2034274be14cc637917ce9576aa`  
		Last Modified: Thu, 12 Jun 2025 22:46:18 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6d4dfab47701ffe430c0efb0d9f5640976ec9b76c70fa9adf6d9a9e37a7605a`  
		Last Modified: Thu, 12 Jun 2025 22:46:18 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c2ad7bc7d5b79fafe6d4eda10030323f4f485027233019a33343bd50a265a59`  
		Last Modified: Thu, 12 Jun 2025 22:46:21 GMT  
		Size: 22.3 MB (22283596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9538a3dff1be138d1137eb9fc139dbda8255bde275ae8670c13253a3d1033575`  
		Last Modified: Thu, 12 Jun 2025 22:46:19 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfe10fbb6bc6101cc1d7a69d3deb8126160b5db04361e52404e83b438b2fa8b3`  
		Last Modified: Thu, 12 Jun 2025 22:46:20 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2dfee3af3890e8fd03beb55f71a85b48276c6bff5474ae597f001adbd26f779`  
		Last Modified: Thu, 12 Jun 2025 22:46:20 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:846e5ade10ef88ce7e3178a17fc7662922cb37bf8403257413f21ca0869ab29c`  
		Last Modified: Thu, 12 Jun 2025 22:46:23 GMT  
		Size: 22.1 MB (22054925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.20348.3807; amd64

```console
$ docker pull docker@sha256:53498ccee3c78a70215add9ae3ef737168375a5c54328c792752c0e5fde4eabf
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2345354530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:485c313a4ef331fdb3d3de62a8679e0f3981409d24dfa2b371f0d9efb2c3ff07`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Jun 2025 01:01:39 GMT
RUN Install update 10.0.20348.3807
# Thu, 12 Jun 2025 22:40:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Jun 2025 22:40:42 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 12 Jun 2025 22:40:43 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 12 Jun 2025 22:40:44 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.2.2.zip
# Thu, 12 Jun 2025 22:40:53 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 12 Jun 2025 22:40:54 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 12 Jun 2025 22:40:55 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Thu, 12 Jun 2025 22:40:55 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Thu, 12 Jun 2025 22:41:04 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 12 Jun 2025 22:41:05 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Thu, 12 Jun 2025 22:41:05 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-windows-x86_64.exe
# Thu, 12 Jun 2025 22:41:06 GMT
ENV DOCKER_COMPOSE_SHA256=132fb31ef7dc81a82d7b1429adf3fd76cc0a7128059af3a172945445a50f2801
# Thu, 12 Jun 2025 22:41:14 GMT
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
	-	`sha256:e3ce7730719b3563f78c11a86c6e7ca9e7ecab63539d89528367a963b46668ee`  
		Last Modified: Thu, 12 Jun 2025 22:42:44 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa44face37189a26dfbb23b8d5da4e8ec912b0e7403fa7e57fe746ede8ca163`  
		Last Modified: Thu, 12 Jun 2025 22:42:47 GMT  
		Size: 351.9 KB (351892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b288554d751322bcbba469e2992e7ed3d7addecc28b36b87bb0ac57981ad64a`  
		Last Modified: Thu, 12 Jun 2025 22:42:46 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08b3bdb645c2944656eeb7ae7bf819f0cd63f9c83b2677298c9c21d710111eec`  
		Last Modified: Thu, 12 Jun 2025 22:42:47 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b59891c80d4b303cd1655e3255818d7a3cb47a43fe98781999d05abb780b0ed`  
		Last Modified: Thu, 12 Jun 2025 22:42:50 GMT  
		Size: 20.5 MB (20450522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1af8f19e40999102aa31f1f4406c7f15eeb18843036b70938f492dee65f6943`  
		Last Modified: Thu, 12 Jun 2025 22:42:49 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f07268cae3a2cdfcdce7a98218844be1e3ede2baa06062288c10119e5414b06`  
		Last Modified: Thu, 12 Jun 2025 22:42:50 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bea31ae088d4884385e4c9bf2ff15ca1ed5f8581b5d17cba15b96224a1533af`  
		Last Modified: Thu, 12 Jun 2025 22:42:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:428d152391bf0297baa1308e6b7a51fa8dfb41c8f2dd3071d1d21fa3e4f42d41`  
		Last Modified: Thu, 12 Jun 2025 22:42:54 GMT  
		Size: 22.3 MB (22261181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b28b4c745fe11d31b3e00254bc2bc9aec2a58ab17157f558834f43f95a248ea`  
		Last Modified: Thu, 12 Jun 2025 22:42:54 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aa41358ec814cca1a580968a15e80fadcab82f43e7c6b59aea4861acb3c83ad`  
		Last Modified: Thu, 12 Jun 2025 22:42:55 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10bc742c50fda0894e2260bf3f7eb9919c098581d407b6cf2a42e3a41062305b`  
		Last Modified: Thu, 12 Jun 2025 22:42:56 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f06dfd207ec226196bd2af1228c11187c3803b22f4c3f4ac01c21d67d7207e67`  
		Last Modified: Thu, 12 Jun 2025 22:42:58 GMT  
		Size: 22.0 MB (22027759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:f640af5c3e1bd4c0cb40cf589e9f2f5903fcff110a95226d0c3f09140b3962eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3807; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.3807; amd64

```console
$ docker pull docker@sha256:53498ccee3c78a70215add9ae3ef737168375a5c54328c792752c0e5fde4eabf
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2345354530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:485c313a4ef331fdb3d3de62a8679e0f3981409d24dfa2b371f0d9efb2c3ff07`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Jun 2025 01:01:39 GMT
RUN Install update 10.0.20348.3807
# Thu, 12 Jun 2025 22:40:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Jun 2025 22:40:42 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 12 Jun 2025 22:40:43 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 12 Jun 2025 22:40:44 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.2.2.zip
# Thu, 12 Jun 2025 22:40:53 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 12 Jun 2025 22:40:54 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 12 Jun 2025 22:40:55 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Thu, 12 Jun 2025 22:40:55 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Thu, 12 Jun 2025 22:41:04 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 12 Jun 2025 22:41:05 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Thu, 12 Jun 2025 22:41:05 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-windows-x86_64.exe
# Thu, 12 Jun 2025 22:41:06 GMT
ENV DOCKER_COMPOSE_SHA256=132fb31ef7dc81a82d7b1429adf3fd76cc0a7128059af3a172945445a50f2801
# Thu, 12 Jun 2025 22:41:14 GMT
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
	-	`sha256:e3ce7730719b3563f78c11a86c6e7ca9e7ecab63539d89528367a963b46668ee`  
		Last Modified: Thu, 12 Jun 2025 22:42:44 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa44face37189a26dfbb23b8d5da4e8ec912b0e7403fa7e57fe746ede8ca163`  
		Last Modified: Thu, 12 Jun 2025 22:42:47 GMT  
		Size: 351.9 KB (351892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b288554d751322bcbba469e2992e7ed3d7addecc28b36b87bb0ac57981ad64a`  
		Last Modified: Thu, 12 Jun 2025 22:42:46 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08b3bdb645c2944656eeb7ae7bf819f0cd63f9c83b2677298c9c21d710111eec`  
		Last Modified: Thu, 12 Jun 2025 22:42:47 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b59891c80d4b303cd1655e3255818d7a3cb47a43fe98781999d05abb780b0ed`  
		Last Modified: Thu, 12 Jun 2025 22:42:50 GMT  
		Size: 20.5 MB (20450522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1af8f19e40999102aa31f1f4406c7f15eeb18843036b70938f492dee65f6943`  
		Last Modified: Thu, 12 Jun 2025 22:42:49 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f07268cae3a2cdfcdce7a98218844be1e3ede2baa06062288c10119e5414b06`  
		Last Modified: Thu, 12 Jun 2025 22:42:50 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bea31ae088d4884385e4c9bf2ff15ca1ed5f8581b5d17cba15b96224a1533af`  
		Last Modified: Thu, 12 Jun 2025 22:42:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:428d152391bf0297baa1308e6b7a51fa8dfb41c8f2dd3071d1d21fa3e4f42d41`  
		Last Modified: Thu, 12 Jun 2025 22:42:54 GMT  
		Size: 22.3 MB (22261181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b28b4c745fe11d31b3e00254bc2bc9aec2a58ab17157f558834f43f95a248ea`  
		Last Modified: Thu, 12 Jun 2025 22:42:54 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aa41358ec814cca1a580968a15e80fadcab82f43e7c6b59aea4861acb3c83ad`  
		Last Modified: Thu, 12 Jun 2025 22:42:55 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10bc742c50fda0894e2260bf3f7eb9919c098581d407b6cf2a42e3a41062305b`  
		Last Modified: Thu, 12 Jun 2025 22:42:56 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f06dfd207ec226196bd2af1228c11187c3803b22f4c3f4ac01c21d67d7207e67`  
		Last Modified: Thu, 12 Jun 2025 22:42:58 GMT  
		Size: 22.0 MB (22027759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:a9266b0f45c2b149896e562c8414e4edc2f32d5f40c73cc8e69a23ce4a967d7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4349; amd64

### `docker:windowsservercore-ltsc2025` - windows version 10.0.26100.4349; amd64

```console
$ docker pull docker@sha256:87b6c37c78ebd3b4dffee917bf6ba9e8e61722d7cc42313c63bf2204cf297f29
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3541382992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebb204680d5c75607c3a852fb2ef3ed327b9ccc1566c1d6a059cb0259d1a3a22`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 07 Jun 2025 15:42:01 GMT
RUN Install update 10.0.26100.4349
# Thu, 12 Jun 2025 22:41:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Jun 2025 22:41:52 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 12 Jun 2025 22:41:53 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 12 Jun 2025 22:41:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.2.2.zip
# Thu, 12 Jun 2025 22:42:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 12 Jun 2025 22:42:05 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 12 Jun 2025 22:42:06 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Thu, 12 Jun 2025 22:42:06 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Thu, 12 Jun 2025 22:42:16 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 12 Jun 2025 22:42:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.1
# Thu, 12 Jun 2025 22:42:17 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.37.1/docker-compose-windows-x86_64.exe
# Thu, 12 Jun 2025 22:42:18 GMT
ENV DOCKER_COMPOSE_SHA256=132fb31ef7dc81a82d7b1429adf3fd76cc0a7128059af3a172945445a50f2801
# Thu, 12 Jun 2025 22:42:28 GMT
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
	-	`sha256:7505764e5850853ff3205e21d0c6c05dd9890fed17012225b1f33d9e79ef8f7b`  
		Last Modified: Thu, 12 Jun 2025 22:46:16 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75201e0022107e322d1abb29cdcd607860e0814d97801313713016a804c7ea29`  
		Last Modified: Thu, 12 Jun 2025 22:46:17 GMT  
		Size: 384.3 KB (384281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad1332a299d19362bbb194725e3d76167ba59837dbdb186edc8c88eb4fc584fc`  
		Last Modified: Thu, 12 Jun 2025 22:46:16 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee1c450bb560eb20733ee6f9c9eab001dcdca87a8a976d64320a006b6a8626e`  
		Last Modified: Thu, 12 Jun 2025 22:46:16 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:292280c51cf870fb93a78962a22141e9734918633eac0270479904b4e7fde431`  
		Last Modified: Thu, 12 Jun 2025 22:46:19 GMT  
		Size: 20.5 MB (20474220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce832f815f971edd09a31c7ae7e5e8f1511fd9100e257f6c46649f33661d080d`  
		Last Modified: Thu, 12 Jun 2025 22:46:18 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc0188db691ee242410ed95505f0c2b6bf11c2034274be14cc637917ce9576aa`  
		Last Modified: Thu, 12 Jun 2025 22:46:18 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6d4dfab47701ffe430c0efb0d9f5640976ec9b76c70fa9adf6d9a9e37a7605a`  
		Last Modified: Thu, 12 Jun 2025 22:46:18 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c2ad7bc7d5b79fafe6d4eda10030323f4f485027233019a33343bd50a265a59`  
		Last Modified: Thu, 12 Jun 2025 22:46:21 GMT  
		Size: 22.3 MB (22283596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9538a3dff1be138d1137eb9fc139dbda8255bde275ae8670c13253a3d1033575`  
		Last Modified: Thu, 12 Jun 2025 22:46:19 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfe10fbb6bc6101cc1d7a69d3deb8126160b5db04361e52404e83b438b2fa8b3`  
		Last Modified: Thu, 12 Jun 2025 22:46:20 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2dfee3af3890e8fd03beb55f71a85b48276c6bff5474ae597f001adbd26f779`  
		Last Modified: Thu, 12 Jun 2025 22:46:20 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:846e5ade10ef88ce7e3178a17fc7662922cb37bf8403257413f21ca0869ab29c`  
		Last Modified: Thu, 12 Jun 2025 22:46:23 GMT  
		Size: 22.1 MB (22054925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
