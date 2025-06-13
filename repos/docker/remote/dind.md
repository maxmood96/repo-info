## `docker:dind`

```console
$ docker pull docker@sha256:8342e1d377d38ca6fa18b1ca57bf4e3507a991102013e76c19acfd33be3e01f4
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
$ docker pull docker@sha256:56d9817143209fce4693bc6b29a5840757b322b0b4403fe28a7348b0c0953bce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.0 MB (133022450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:220e70fcd60fe8ee4abc1fb3bf3cd97cc391dba27f321ad22659467e8536e9b8`
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
ENV DOCKER_COMPOSE_VERSION=2.37.0
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-x86_64'; 			sha256='e6e471b1e7bf0443592d3987dea6073f08db3e48ba0580199109aa7a44257e54'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-armv6'; 			sha256='f09294bd81119701f051733b45be487d55faa29d20fb9c54412975a6c7fd8696'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-armv7'; 			sha256='b1b592889f15f50ddc77685ed499c69599117e52240b196447cb82821da3f7f8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-aarch64'; 			sha256='664e8c532ac0dd54d14af4eb3fe4edce86ce27d970ec832a96b55bc2ef1dffdf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-ppc64le'; 			sha256='83c7cf5afffcc7944e23ba5c1c038aff4f2d760f08681d76b5271b66c9e2af5d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-riscv64'; 			sha256='0e6047d2b0f745f0bbb13d707cfb945295bf45e397e67ff756f8551043a1f5bc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-s390x'; 			sha256='381b5b77e6a91075e746167ac160062a1adf4d2a1121e433f1ca731ad08e2353'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:89f8c32f216879f685817a9e63a48cdc0223d0bc7c7d0c751a4be6ba6c73ef5e`  
		Last Modified: Thu, 05 Jun 2025 22:43:53 GMT  
		Size: 7.4 MB (7440639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66719bdda62b905eb93e4b3587c931c7f3e7f93eb8bff6205afb0552b6f21256`  
		Last Modified: Thu, 05 Jun 2025 22:43:52 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c925984b3abe923d5073eae366d96685c0e5c02bf2dbe8bd39c7b5c93b19a090`  
		Last Modified: Thu, 05 Jun 2025 22:43:55 GMT  
		Size: 18.1 MB (18089380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872d44dab7a46cdfe4e81d3b251341852e01d42db0576ce272955bf05096acf9`  
		Last Modified: Thu, 05 Jun 2025 22:43:56 GMT  
		Size: 19.9 MB (19927228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97e0d61d6c40b7aeca6fd9316eb34a635930bf7207daacfcd95d282f6227147`  
		Last Modified: Thu, 05 Jun 2025 22:43:56 GMT  
		Size: 19.8 MB (19815903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67724918cd46ffc0aa34973255dea8af10db6b7323f9e59e0544286ee79cbae7`  
		Last Modified: Thu, 05 Jun 2025 22:43:55 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e3051e0388231088407c785de69833b01ded126cc9d32135dd70c03c9628e2f`  
		Last Modified: Thu, 05 Jun 2025 22:50:48 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a0ae88edd91c6844cf8c45543adc21d1ebfbde0cec16cf22f72c34ca47af411`  
		Last Modified: Thu, 05 Jun 2025 22:50:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0497dad9a097e163c099df5264d9227fb0d6663f714934070c10c58f640a638`  
		Last Modified: Thu, 05 Jun 2025 23:08:07 GMT  
		Size: 6.5 MB (6538125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71f3ee354010723e2aa578ae86cbbc6481cc5569819c6075037a41ab20a03cbe`  
		Last Modified: Thu, 05 Jun 2025 23:08:07 GMT  
		Size: 86.5 KB (86499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:551cb1fdf6e16f89a105b4d22c638ba733115c87144229fb2f9c44ae811283c7`  
		Last Modified: Thu, 05 Jun 2025 23:08:06 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce4353f5b2e16087ecc60c993d5e54d6aa935f52b225402e07b9c8da1c073476`  
		Last Modified: Thu, 05 Jun 2025 23:08:10 GMT  
		Size: 57.9 MB (57897343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f0bc96bc38f9236e2260194feb32d2393f4f2fce8c58e9ef7b3ecf5a56f02a0`  
		Last Modified: Thu, 05 Jun 2025 23:14:11 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eacc23379106813fa1bdb96e6832ae68264cd7c08d6939c188ad781215a9ad05`  
		Last Modified: Thu, 05 Jun 2025 23:14:15 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:9fc59d299032ac04f6669fd061d6d4870519b7357ed90167a804ad34eb8618c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:106f518a6789bc8403a24ffbf5a89ab9263488839ae1b91746e15a712cf9d11f`

```dockerfile
```

-	Layers:
	-	`sha256:1d7fd3cbdbeff5f7accfc1f5a20a6b25ab1579b8e1064bd915b1d1bf94179ecf`  
		Last Modified: Fri, 06 Jun 2025 02:07:37 GMT  
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
