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
