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
$ docker pull docker@sha256:d4668861cabc1691635d98e827a81cfa834a416f8fe0f4efc609f9f806d86d82
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
$ docker pull docker@sha256:8c9502da312e1595a696775bea7d4e6e7b18102d62c413b43f9d3f9d353eb323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.7 MB (143680550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e1cee4b3a3c0bfea53084cb7708d24f3314dd7ce46631888127d8037a4158d9`
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
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99164a65e1f060513df17430a291c788a5801cc0364c3cf0abaf9dd47e9d891c`  
		Last Modified: Thu, 05 Jun 2025 22:44:25 GMT  
		Size: 8.2 MB (8207469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a930b44823eb85c484514670f94fa0fadf7649aa34a692072e953b86cff998`  
		Last Modified: Thu, 05 Jun 2025 22:44:24 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89fad9bfb8f24abcb392b00c918762036dedf67787dc8a32b43aec570f3557f4`  
		Last Modified: Thu, 05 Jun 2025 22:44:28 GMT  
		Size: 20.1 MB (20083033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e993a5c36c8c13b622945142edd4bdf6b5d03775d8e91196856e50e0512650a`  
		Last Modified: Thu, 05 Jun 2025 22:44:27 GMT  
		Size: 21.3 MB (21290182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd58cf00359048abfc4f447feefe1373db7fd84dfe136fb751689b640844dd4b`  
		Last Modified: Thu, 05 Jun 2025 22:44:27 GMT  
		Size: 21.1 MB (21092192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bd9fc81ec33be8d5693955225a870888bf988fe35871af701d05810a7718b9`  
		Last Modified: Thu, 05 Jun 2025 22:44:26 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7dc70da6730815a90c517d43ed51312bc13932b65a288bbb8952f74df9d763a`  
		Last Modified: Thu, 05 Jun 2025 22:44:26 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2483cd3bb024143d65a844f930ffb5aa01cb0932a660abcaa0fcd68ddc0810`  
		Last Modified: Thu, 05 Jun 2025 22:44:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:232671b8d6c574d91a514e1073ddb00bd37e47ba17cfeefc0a4e078e392e4a00`  
		Last Modified: Thu, 05 Jun 2025 23:10:12 GMT  
		Size: 6.9 MB (6905563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8947c15ddd39c2ad279e9f5b5180a071aa948c04d248e2dcf4cb13585d9b47b8`  
		Last Modified: Thu, 05 Jun 2025 23:10:12 GMT  
		Size: 90.5 KB (90492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f7e4c6039fec8c4db67902febab1ae735352d758ffb76367f1e3e68a0b04b9d`  
		Last Modified: Thu, 05 Jun 2025 23:10:11 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:369f3cb80e373dbeee03da49ca69ce93f7c63f165704f929f0a040a4de56ed8e`  
		Last Modified: Thu, 05 Jun 2025 23:10:16 GMT  
		Size: 62.2 MB (62206624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7a0f373a71bb7b7e7a3be4baa2472d2850c4c9549c66b58e70a59a51b696ee`  
		Last Modified: Thu, 05 Jun 2025 23:10:11 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4dbe5b0725a180af25ab3d235ff1a32980b060cb2e263d0362d2baa5b73d858`  
		Last Modified: Thu, 05 Jun 2025 23:10:11 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28` - unknown; unknown

```console
$ docker pull docker@sha256:227416a58467a90d61d00571bea5da05930524bab4cb82350e892b245e0d2e6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:125d3c52d0be767b8d0f76f67d0acd7adb2635cac747795240c64e1792d2f95e`

```dockerfile
```

-	Layers:
	-	`sha256:06c3e6cf1c5d56e7cb2fe109c0aa850bd00d57c61602118e103dbffd829369a6`  
		Last Modified: Fri, 06 Jun 2025 02:07:30 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28` - linux; arm variant v6

```console
$ docker pull docker@sha256:7920dd4fb3d5c69b32f5a8fdad7bc083113e1eb057daf9551d3bec928642d2d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134721385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f04c9bfb20a7623a34894618839c13fd1bf730153cc94bc61f9b9d60dbc8dc6`
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
	-	`sha256:b18e44e663f768131c50d79640817a860ca8c20877f41bfc7e788ede7276f121`  
		Last Modified: Thu, 05 Jun 2025 22:44:12 GMT  
		Size: 19.8 MB (19834728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b7cf9bb5cb3a10f219b307b2ff9f67f54ab05208492bbe13e06a74ca78e54d`  
		Last Modified: Thu, 05 Jun 2025 22:44:13 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7393d30c6bcbe757d4919545933b9de1b6f48c9a46a3ed4a0ae9281792fbd51`  
		Last Modified: Thu, 05 Jun 2025 22:51:09 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe877f07f4d94074494db81efb5c5e890ab77b7ce09fa3952f972953a436545d`  
		Last Modified: Thu, 05 Jun 2025 22:51:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9526e4c6fe05aa09bd1848ecd6d91b389e046a9da41b839528a0f104ba7e6b`  
		Last Modified: Fri, 06 Jun 2025 01:05:46 GMT  
		Size: 7.2 MB (7230299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7741447d38cadd971edc0ea8d19ec995a5929dad7df81e579060cf95a0a66e0e`  
		Last Modified: Thu, 05 Jun 2025 23:14:04 GMT  
		Size: 90.1 KB (90052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eabb360d9297b2af61c701c3a02f961b3210cdb6c3a4119c7a03d703fd26c6b`  
		Last Modified: Thu, 05 Jun 2025 23:14:08 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c250f611b5a5d3e13bac22e1a236ffb37d10345c511e869b539265c145ebc1`  
		Last Modified: Fri, 06 Jun 2025 01:05:49 GMT  
		Size: 57.9 MB (57897379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b907cd35da6b2acf22cf12c6849885f91becbd5836560543543e4df0b7e4ede`  
		Last Modified: Thu, 05 Jun 2025 23:14:11 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b319c010975a1f690900a80187653a3834b1a65ec15f73ccd7edf9c103bc8eb`  
		Last Modified: Thu, 05 Jun 2025 23:14:13 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28` - unknown; unknown

```console
$ docker pull docker@sha256:918e10532d5d49ad3d988b0f42404e4e65b4ff96c9f47d1de4c3bb238edfaf26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc5e34ba8e1767c238c0ca97f2315e8d15bc7d875be15383aa1599e4d71188d2`

```dockerfile
```

-	Layers:
	-	`sha256:21bc1dae29bbc15eda321d47bbd61a416fa4a9175b7a84d90debd5063a161db7`  
		Last Modified: Fri, 06 Jun 2025 02:07:34 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28` - linux; arm variant v7

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

### `docker:28` - unknown; unknown

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

### `docker:28` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:0de688aa942b05b1ca86e80e9e87a92cab8690ca4d00819b777253ca12fd05b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.5 MB (134498975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e07111220cfca840da6105d81020ea43df6b1c90921916a1cd65417e1101d6e`
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
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38a584a1da307e1ac31b3fd852369ae8a8176a1baa2e783b7e72077d8318364`  
		Last Modified: Thu, 05 Jun 2025 23:07:15 GMT  
		Size: 8.2 MB (8229004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122792206f35c9e929c0c28c585fd195a84012e2d9bea1522c579660e013f3a5`  
		Last Modified: Thu, 05 Jun 2025 22:50:09 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e5a5c767d7cf27a922e7c99956942414d9e65453df45e3500e05adf80db19d`  
		Last Modified: Thu, 05 Jun 2025 23:07:16 GMT  
		Size: 18.9 MB (18902608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2fc5aa8a4cd07adf8f84bd323a5d415f9ca2c5c158b74f9382a0b369265fe2`  
		Last Modified: Thu, 05 Jun 2025 23:07:14 GMT  
		Size: 19.5 MB (19469838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba639502cad797b5554e57bbdc209e0c34366d2a40e0b51a2fa20dfce1a5b337`  
		Last Modified: Thu, 05 Jun 2025 23:07:13 GMT  
		Size: 19.3 MB (19344051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda0f9c86634c1a6b9059d179ed7e6ead432e9b8bcddfb0e980660053ccaef13`  
		Last Modified: Thu, 05 Jun 2025 22:50:11 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef143fe66bfdc5598981ca016d8e3884fde63a7858eb245932bb9745217e515a`  
		Last Modified: Thu, 05 Jun 2025 22:50:14 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69e2c1a5fdbb4dad365dd880c4621563cfe56068eb2e2541c0de0b1de1353676`  
		Last Modified: Thu, 05 Jun 2025 22:50:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b81c7606e8dcfe2fd4ea847b572c410188a1a61c1b7b1cda6ba28a64e97f159`  
		Last Modified: Thu, 05 Jun 2025 23:08:03 GMT  
		Size: 7.1 MB (7141567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e3f3d3d88e3f3363a8a38c1a676767483806a513d0552d4772a08e36257b1c`  
		Last Modified: Thu, 05 Jun 2025 23:08:04 GMT  
		Size: 99.6 KB (99634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abefbbf9a5b4d4cca3ef794fb554ab4acac7277079ebf9e0403cc7bb13360683`  
		Last Modified: Thu, 05 Jun 2025 23:08:03 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15537da54888f9d1dd7c82127a2affc9eaa21eec06bc9938606f42434884b95d`  
		Last Modified: Thu, 05 Jun 2025 23:08:12 GMT  
		Size: 57.2 MB (57168179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b5eff1498a195bfe23aea7da2bcdf6de5f313f4140c8715a32acf14d62d62cd`  
		Last Modified: Thu, 05 Jun 2025 23:08:04 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b4cb7df5229fcce96acdc6de42d98aa670436a784a0e59417a1584407b6bb8`  
		Last Modified: Thu, 05 Jun 2025 23:08:05 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28` - unknown; unknown

```console
$ docker pull docker@sha256:5cad50c6b3b442444f6651f5c8b4d33a9f66b976fd04acda0c3b54328ac14556
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeded159db72e188c1c71b241cf1c67644293d460aa0a7d23d1fd5424dc510de`

```dockerfile
```

-	Layers:
	-	`sha256:431922ef17f88491b0a295b18dd805f113ce40a500def3af5b4651f0b1b77da1`  
		Last Modified: Fri, 06 Jun 2025 02:07:41 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28-cli`

```console
$ docker pull docker@sha256:c2e49a065e45c462dda70b65b1a50a74c75804091fae15b7e4fbec6b114996d1
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
$ docker pull docker@sha256:29ac2aff504532e72efca1a58f229c0e05f928828e62156fb304d391e82f7f49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74471875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd02548899f2c001be05193b91d116511f57fb7e8f5cec5f7b58cce36fed0303`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99164a65e1f060513df17430a291c788a5801cc0364c3cf0abaf9dd47e9d891c`  
		Last Modified: Thu, 05 Jun 2025 22:44:25 GMT  
		Size: 8.2 MB (8207469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a930b44823eb85c484514670f94fa0fadf7649aa34a692072e953b86cff998`  
		Last Modified: Thu, 05 Jun 2025 22:44:24 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89fad9bfb8f24abcb392b00c918762036dedf67787dc8a32b43aec570f3557f4`  
		Last Modified: Thu, 05 Jun 2025 22:44:28 GMT  
		Size: 20.1 MB (20083033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e993a5c36c8c13b622945142edd4bdf6b5d03775d8e91196856e50e0512650a`  
		Last Modified: Thu, 05 Jun 2025 22:44:27 GMT  
		Size: 21.3 MB (21290182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd58cf00359048abfc4f447feefe1373db7fd84dfe136fb751689b640844dd4b`  
		Last Modified: Thu, 05 Jun 2025 22:44:27 GMT  
		Size: 21.1 MB (21092192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bd9fc81ec33be8d5693955225a870888bf988fe35871af701d05810a7718b9`  
		Last Modified: Thu, 05 Jun 2025 22:44:26 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7dc70da6730815a90c517d43ed51312bc13932b65a288bbb8952f74df9d763a`  
		Last Modified: Thu, 05 Jun 2025 22:44:26 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2483cd3bb024143d65a844f930ffb5aa01cb0932a660abcaa0fcd68ddc0810`  
		Last Modified: Thu, 05 Jun 2025 22:44:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:e3c92c354188244e1e651ab7c9384326a36594dbf3e27427328aa209be1c1e7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de64116684520fb5473d5fee53d9f710a283fa5926d23334bbeb9a13ece30127`

```dockerfile
```

-	Layers:
	-	`sha256:9f1baaf1f40a67141a0489af913841dd7e9427be207fe398702581c569cd1c20`  
		Last Modified: Thu, 05 Jun 2025 23:07:43 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:6f76795bf488400672b314ad95bc4add17d3871c369454a410a6072cd1f7fe6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69497654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4905167d30157f311983a0f0fbb87d96647db6c5478ae0071e5e9d717c22247`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
	-	`sha256:b18e44e663f768131c50d79640817a860ca8c20877f41bfc7e788ede7276f121`  
		Last Modified: Thu, 05 Jun 2025 22:44:12 GMT  
		Size: 19.8 MB (19834728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b7cf9bb5cb3a10f219b307b2ff9f67f54ab05208492bbe13e06a74ca78e54d`  
		Last Modified: Thu, 05 Jun 2025 22:44:13 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7393d30c6bcbe757d4919545933b9de1b6f48c9a46a3ed4a0ae9281792fbd51`  
		Last Modified: Thu, 05 Jun 2025 22:51:09 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe877f07f4d94074494db81efb5c5e890ab77b7ce09fa3952f972953a436545d`  
		Last Modified: Thu, 05 Jun 2025 22:51:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:9c9ad38782ad3e5c053ed8c736f10e9589825748a8c4233619fb70a2ec23af36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86ca6472c159b81f34510b55fdadf12635ed814ad061552012b01cc7622021dd`

```dockerfile
```

-	Layers:
	-	`sha256:c58766a24b3303a1f1acf7a634a2134383f4aa8fc7b6223cb9497695c7739a5f`  
		Last Modified: Thu, 05 Jun 2025 23:07:47 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:1e48b83f7392bb14bec910d025f2b5ba1a759fff65845d925284236bc07d4fe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68494484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61de327c238ebb7ad778ea80f8124ffd3e79271ceb1c162b0fbdfb43ad4a56f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:c13cadb351384ad992f27483f70dba162d9c5b57e6643cec3c37598aebb9ff47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ef1b27ab22635d8c650664a7ff740383003126f39daab1972f0db14de9fe5af`

```dockerfile
```

-	Layers:
	-	`sha256:efca98ea4b9f81656feedd1b0eb5f97c37873667b5a92fa941594dad0570afc7`  
		Last Modified: Thu, 05 Jun 2025 23:07:51 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:050e38ffb61f1a397a300e2c027858126865eb5c53026a10a231ea8c71637cf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70083597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:049c11c099d31b1b16a8eec2d4744a8baa44341b7f6489e7c2a70a8c597e17d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38a584a1da307e1ac31b3fd852369ae8a8176a1baa2e783b7e72077d8318364`  
		Last Modified: Thu, 05 Jun 2025 23:07:15 GMT  
		Size: 8.2 MB (8229004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122792206f35c9e929c0c28c585fd195a84012e2d9bea1522c579660e013f3a5`  
		Last Modified: Thu, 05 Jun 2025 22:50:09 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e5a5c767d7cf27a922e7c99956942414d9e65453df45e3500e05adf80db19d`  
		Last Modified: Thu, 05 Jun 2025 23:07:16 GMT  
		Size: 18.9 MB (18902608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2fc5aa8a4cd07adf8f84bd323a5d415f9ca2c5c158b74f9382a0b369265fe2`  
		Last Modified: Thu, 05 Jun 2025 23:07:14 GMT  
		Size: 19.5 MB (19469838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba639502cad797b5554e57bbdc209e0c34366d2a40e0b51a2fa20dfce1a5b337`  
		Last Modified: Thu, 05 Jun 2025 23:07:13 GMT  
		Size: 19.3 MB (19344051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda0f9c86634c1a6b9059d179ed7e6ead432e9b8bcddfb0e980660053ccaef13`  
		Last Modified: Thu, 05 Jun 2025 22:50:11 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef143fe66bfdc5598981ca016d8e3884fde63a7858eb245932bb9745217e515a`  
		Last Modified: Thu, 05 Jun 2025 22:50:14 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69e2c1a5fdbb4dad365dd880c4621563cfe56068eb2e2541c0de0b1de1353676`  
		Last Modified: Thu, 05 Jun 2025 22:50:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:3d9117cfb4076144f396a04008c8592792765eb725010db68b4fc6a3e9d07a3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8f618e6cdf0288b0248e4b6b48f1bd5324300dfd40ccfdcc2698737d569f539`

```dockerfile
```

-	Layers:
	-	`sha256:07a44b113f5c5d8eb65a6af4b53f0ae0869dcbfdd809ec06739500831432a0db`  
		Last Modified: Thu, 05 Jun 2025 23:07:55 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28-dind`

```console
$ docker pull docker@sha256:d4668861cabc1691635d98e827a81cfa834a416f8fe0f4efc609f9f806d86d82
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
$ docker pull docker@sha256:8c9502da312e1595a696775bea7d4e6e7b18102d62c413b43f9d3f9d353eb323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.7 MB (143680550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e1cee4b3a3c0bfea53084cb7708d24f3314dd7ce46631888127d8037a4158d9`
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
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99164a65e1f060513df17430a291c788a5801cc0364c3cf0abaf9dd47e9d891c`  
		Last Modified: Thu, 05 Jun 2025 22:44:25 GMT  
		Size: 8.2 MB (8207469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a930b44823eb85c484514670f94fa0fadf7649aa34a692072e953b86cff998`  
		Last Modified: Thu, 05 Jun 2025 22:44:24 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89fad9bfb8f24abcb392b00c918762036dedf67787dc8a32b43aec570f3557f4`  
		Last Modified: Thu, 05 Jun 2025 22:44:28 GMT  
		Size: 20.1 MB (20083033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e993a5c36c8c13b622945142edd4bdf6b5d03775d8e91196856e50e0512650a`  
		Last Modified: Thu, 05 Jun 2025 22:44:27 GMT  
		Size: 21.3 MB (21290182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd58cf00359048abfc4f447feefe1373db7fd84dfe136fb751689b640844dd4b`  
		Last Modified: Thu, 05 Jun 2025 22:44:27 GMT  
		Size: 21.1 MB (21092192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bd9fc81ec33be8d5693955225a870888bf988fe35871af701d05810a7718b9`  
		Last Modified: Thu, 05 Jun 2025 22:44:26 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7dc70da6730815a90c517d43ed51312bc13932b65a288bbb8952f74df9d763a`  
		Last Modified: Thu, 05 Jun 2025 22:44:26 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2483cd3bb024143d65a844f930ffb5aa01cb0932a660abcaa0fcd68ddc0810`  
		Last Modified: Thu, 05 Jun 2025 22:44:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:232671b8d6c574d91a514e1073ddb00bd37e47ba17cfeefc0a4e078e392e4a00`  
		Last Modified: Thu, 05 Jun 2025 23:10:12 GMT  
		Size: 6.9 MB (6905563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8947c15ddd39c2ad279e9f5b5180a071aa948c04d248e2dcf4cb13585d9b47b8`  
		Last Modified: Thu, 05 Jun 2025 23:10:12 GMT  
		Size: 90.5 KB (90492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f7e4c6039fec8c4db67902febab1ae735352d758ffb76367f1e3e68a0b04b9d`  
		Last Modified: Thu, 05 Jun 2025 23:10:11 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:369f3cb80e373dbeee03da49ca69ce93f7c63f165704f929f0a040a4de56ed8e`  
		Last Modified: Thu, 05 Jun 2025 23:10:16 GMT  
		Size: 62.2 MB (62206624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7a0f373a71bb7b7e7a3be4baa2472d2850c4c9549c66b58e70a59a51b696ee`  
		Last Modified: Thu, 05 Jun 2025 23:10:11 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4dbe5b0725a180af25ab3d235ff1a32980b060cb2e263d0362d2baa5b73d858`  
		Last Modified: Thu, 05 Jun 2025 23:10:11 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind` - unknown; unknown

```console
$ docker pull docker@sha256:227416a58467a90d61d00571bea5da05930524bab4cb82350e892b245e0d2e6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:125d3c52d0be767b8d0f76f67d0acd7adb2635cac747795240c64e1792d2f95e`

```dockerfile
```

-	Layers:
	-	`sha256:06c3e6cf1c5d56e7cb2fe109c0aa850bd00d57c61602118e103dbffd829369a6`  
		Last Modified: Fri, 06 Jun 2025 02:07:30 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:7920dd4fb3d5c69b32f5a8fdad7bc083113e1eb057daf9551d3bec928642d2d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134721385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f04c9bfb20a7623a34894618839c13fd1bf730153cc94bc61f9b9d60dbc8dc6`
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
	-	`sha256:b18e44e663f768131c50d79640817a860ca8c20877f41bfc7e788ede7276f121`  
		Last Modified: Thu, 05 Jun 2025 22:44:12 GMT  
		Size: 19.8 MB (19834728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b7cf9bb5cb3a10f219b307b2ff9f67f54ab05208492bbe13e06a74ca78e54d`  
		Last Modified: Thu, 05 Jun 2025 22:44:13 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7393d30c6bcbe757d4919545933b9de1b6f48c9a46a3ed4a0ae9281792fbd51`  
		Last Modified: Thu, 05 Jun 2025 22:51:09 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe877f07f4d94074494db81efb5c5e890ab77b7ce09fa3952f972953a436545d`  
		Last Modified: Thu, 05 Jun 2025 22:51:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9526e4c6fe05aa09bd1848ecd6d91b389e046a9da41b839528a0f104ba7e6b`  
		Last Modified: Fri, 06 Jun 2025 01:05:46 GMT  
		Size: 7.2 MB (7230299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7741447d38cadd971edc0ea8d19ec995a5929dad7df81e579060cf95a0a66e0e`  
		Last Modified: Thu, 05 Jun 2025 23:14:04 GMT  
		Size: 90.1 KB (90052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eabb360d9297b2af61c701c3a02f961b3210cdb6c3a4119c7a03d703fd26c6b`  
		Last Modified: Thu, 05 Jun 2025 23:14:08 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c250f611b5a5d3e13bac22e1a236ffb37d10345c511e869b539265c145ebc1`  
		Last Modified: Fri, 06 Jun 2025 01:05:49 GMT  
		Size: 57.9 MB (57897379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b907cd35da6b2acf22cf12c6849885f91becbd5836560543543e4df0b7e4ede`  
		Last Modified: Thu, 05 Jun 2025 23:14:11 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b319c010975a1f690900a80187653a3834b1a65ec15f73ccd7edf9c103bc8eb`  
		Last Modified: Thu, 05 Jun 2025 23:14:13 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind` - unknown; unknown

```console
$ docker pull docker@sha256:918e10532d5d49ad3d988b0f42404e4e65b4ff96c9f47d1de4c3bb238edfaf26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc5e34ba8e1767c238c0ca97f2315e8d15bc7d875be15383aa1599e4d71188d2`

```dockerfile
```

-	Layers:
	-	`sha256:21bc1dae29bbc15eda321d47bbd61a416fa4a9175b7a84d90debd5063a161db7`  
		Last Modified: Fri, 06 Jun 2025 02:07:34 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-dind` - linux; arm variant v7

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

### `docker:28-dind` - unknown; unknown

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

### `docker:28-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:0de688aa942b05b1ca86e80e9e87a92cab8690ca4d00819b777253ca12fd05b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.5 MB (134498975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e07111220cfca840da6105d81020ea43df6b1c90921916a1cd65417e1101d6e`
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
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38a584a1da307e1ac31b3fd852369ae8a8176a1baa2e783b7e72077d8318364`  
		Last Modified: Thu, 05 Jun 2025 23:07:15 GMT  
		Size: 8.2 MB (8229004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122792206f35c9e929c0c28c585fd195a84012e2d9bea1522c579660e013f3a5`  
		Last Modified: Thu, 05 Jun 2025 22:50:09 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e5a5c767d7cf27a922e7c99956942414d9e65453df45e3500e05adf80db19d`  
		Last Modified: Thu, 05 Jun 2025 23:07:16 GMT  
		Size: 18.9 MB (18902608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2fc5aa8a4cd07adf8f84bd323a5d415f9ca2c5c158b74f9382a0b369265fe2`  
		Last Modified: Thu, 05 Jun 2025 23:07:14 GMT  
		Size: 19.5 MB (19469838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba639502cad797b5554e57bbdc209e0c34366d2a40e0b51a2fa20dfce1a5b337`  
		Last Modified: Thu, 05 Jun 2025 23:07:13 GMT  
		Size: 19.3 MB (19344051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda0f9c86634c1a6b9059d179ed7e6ead432e9b8bcddfb0e980660053ccaef13`  
		Last Modified: Thu, 05 Jun 2025 22:50:11 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef143fe66bfdc5598981ca016d8e3884fde63a7858eb245932bb9745217e515a`  
		Last Modified: Thu, 05 Jun 2025 22:50:14 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69e2c1a5fdbb4dad365dd880c4621563cfe56068eb2e2541c0de0b1de1353676`  
		Last Modified: Thu, 05 Jun 2025 22:50:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b81c7606e8dcfe2fd4ea847b572c410188a1a61c1b7b1cda6ba28a64e97f159`  
		Last Modified: Thu, 05 Jun 2025 23:08:03 GMT  
		Size: 7.1 MB (7141567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e3f3d3d88e3f3363a8a38c1a676767483806a513d0552d4772a08e36257b1c`  
		Last Modified: Thu, 05 Jun 2025 23:08:04 GMT  
		Size: 99.6 KB (99634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abefbbf9a5b4d4cca3ef794fb554ab4acac7277079ebf9e0403cc7bb13360683`  
		Last Modified: Thu, 05 Jun 2025 23:08:03 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15537da54888f9d1dd7c82127a2affc9eaa21eec06bc9938606f42434884b95d`  
		Last Modified: Thu, 05 Jun 2025 23:08:12 GMT  
		Size: 57.2 MB (57168179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b5eff1498a195bfe23aea7da2bcdf6de5f313f4140c8715a32acf14d62d62cd`  
		Last Modified: Thu, 05 Jun 2025 23:08:04 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b4cb7df5229fcce96acdc6de42d98aa670436a784a0e59417a1584407b6bb8`  
		Last Modified: Thu, 05 Jun 2025 23:08:05 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind` - unknown; unknown

```console
$ docker pull docker@sha256:5cad50c6b3b442444f6651f5c8b4d33a9f66b976fd04acda0c3b54328ac14556
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeded159db72e188c1c71b241cf1c67644293d460aa0a7d23d1fd5424dc510de`

```dockerfile
```

-	Layers:
	-	`sha256:431922ef17f88491b0a295b18dd805f113ce40a500def3af5b4651f0b1b77da1`  
		Last Modified: Fri, 06 Jun 2025 02:07:41 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28-dind-rootless`

```console
$ docker pull docker@sha256:8fc8c7e252d63e2280415a0520caf2a014c86b5c8fd25c910fe8adc77aeb94ca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:28-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:abd2dd1debd13881cb395d987a48ef2db49e904f9260e691cdd8fb3f40c8c810
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.3 MB (162261128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:515c53634a6d629377edd34a1fa5f3f6977b9ff51a6afb4aa84a220a5f27d5c4`
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
ENV DOCKER_COMPOSE_VERSION=2.37.0
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-x86_64'; 			sha256='e6e471b1e7bf0443592d3987dea6073f08db3e48ba0580199109aa7a44257e54'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-armv6'; 			sha256='f09294bd81119701f051733b45be487d55faa29d20fb9c54412975a6c7fd8696'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-armv7'; 			sha256='b1b592889f15f50ddc77685ed499c69599117e52240b196447cb82821da3f7f8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-aarch64'; 			sha256='664e8c532ac0dd54d14af4eb3fe4edce86ce27d970ec832a96b55bc2ef1dffdf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-ppc64le'; 			sha256='83c7cf5afffcc7944e23ba5c1c038aff4f2d760f08681d76b5271b66c9e2af5d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-riscv64'; 			sha256='0e6047d2b0f745f0bbb13d707cfb945295bf45e397e67ff756f8551043a1f5bc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-s390x'; 			sha256='381b5b77e6a91075e746167ac160062a1adf4d2a1121e433f1ca731ad08e2353'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:99164a65e1f060513df17430a291c788a5801cc0364c3cf0abaf9dd47e9d891c`  
		Last Modified: Thu, 05 Jun 2025 22:44:25 GMT  
		Size: 8.2 MB (8207469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a930b44823eb85c484514670f94fa0fadf7649aa34a692072e953b86cff998`  
		Last Modified: Thu, 05 Jun 2025 22:44:24 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89fad9bfb8f24abcb392b00c918762036dedf67787dc8a32b43aec570f3557f4`  
		Last Modified: Thu, 05 Jun 2025 22:44:28 GMT  
		Size: 20.1 MB (20083033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e993a5c36c8c13b622945142edd4bdf6b5d03775d8e91196856e50e0512650a`  
		Last Modified: Thu, 05 Jun 2025 22:44:27 GMT  
		Size: 21.3 MB (21290182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd58cf00359048abfc4f447feefe1373db7fd84dfe136fb751689b640844dd4b`  
		Last Modified: Thu, 05 Jun 2025 22:44:27 GMT  
		Size: 21.1 MB (21092192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bd9fc81ec33be8d5693955225a870888bf988fe35871af701d05810a7718b9`  
		Last Modified: Thu, 05 Jun 2025 22:44:26 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7dc70da6730815a90c517d43ed51312bc13932b65a288bbb8952f74df9d763a`  
		Last Modified: Thu, 05 Jun 2025 22:44:26 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2483cd3bb024143d65a844f930ffb5aa01cb0932a660abcaa0fcd68ddc0810`  
		Last Modified: Thu, 05 Jun 2025 22:44:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:232671b8d6c574d91a514e1073ddb00bd37e47ba17cfeefc0a4e078e392e4a00`  
		Last Modified: Thu, 05 Jun 2025 23:10:12 GMT  
		Size: 6.9 MB (6905563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8947c15ddd39c2ad279e9f5b5180a071aa948c04d248e2dcf4cb13585d9b47b8`  
		Last Modified: Thu, 05 Jun 2025 23:10:12 GMT  
		Size: 90.5 KB (90492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f7e4c6039fec8c4db67902febab1ae735352d758ffb76367f1e3e68a0b04b9d`  
		Last Modified: Thu, 05 Jun 2025 23:10:11 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:369f3cb80e373dbeee03da49ca69ce93f7c63f165704f929f0a040a4de56ed8e`  
		Last Modified: Thu, 05 Jun 2025 23:10:16 GMT  
		Size: 62.2 MB (62206624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7a0f373a71bb7b7e7a3be4baa2472d2850c4c9549c66b58e70a59a51b696ee`  
		Last Modified: Thu, 05 Jun 2025 23:10:11 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4dbe5b0725a180af25ab3d235ff1a32980b060cb2e263d0362d2baa5b73d858`  
		Last Modified: Thu, 05 Jun 2025 23:10:11 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f64aa3fd56b6d8303e9c2e032693fa69765ebe0ca402c8652e2e4be4bd9b8a2f`  
		Last Modified: Fri, 06 Jun 2025 00:13:41 GMT  
		Size: 993.3 KB (993270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9ac68c4bd4a09936531af4a567ee2065e73f798766ad456aef07aa86555af1`  
		Last Modified: Fri, 06 Jun 2025 00:13:48 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e79fe881b6f2ad1dc6bfdf95095a21b2a9400b5098d82da1be17d678d59226`  
		Last Modified: Fri, 06 Jun 2025 00:13:51 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91260bbdd96570e120d536ac928e3f77c4f858234e17f2ba9abb34a416109116`  
		Last Modified: Fri, 06 Jun 2025 02:08:01 GMT  
		Size: 17.6 MB (17585969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e31b397060352f80943b2c245dfb2b9014d8caaaefa979cba711e233412315`  
		Last Modified: Fri, 06 Jun 2025 00:13:54 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:0c4804528defa4555b2fadbd0044e12d0585c45979692580e6f2793f2e1eea66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.4 KB (30450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f33f1746b3d799c576bbbfea37de0b6f65df618daea063dddc5c07da8dfdd129`

```dockerfile
```

-	Layers:
	-	`sha256:4faecdc253478ec516ca521def628c3524f48440edfd20522bf779744323317c`  
		Last Modified: Fri, 06 Jun 2025 02:07:42 GMT  
		Size: 30.4 KB (30450 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:8f8a0cd4395a6ab286a0630f776e920239e6a01f6de484c2c23292ef76381bec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.5 MB (153539458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63acc824e3021e35e0fbed5808986ced5616f6da68905d273709d210e4a8ade6`
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
ENV DOCKER_COMPOSE_VERSION=2.37.0
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-x86_64'; 			sha256='e6e471b1e7bf0443592d3987dea6073f08db3e48ba0580199109aa7a44257e54'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-armv6'; 			sha256='f09294bd81119701f051733b45be487d55faa29d20fb9c54412975a6c7fd8696'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-armv7'; 			sha256='b1b592889f15f50ddc77685ed499c69599117e52240b196447cb82821da3f7f8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-aarch64'; 			sha256='664e8c532ac0dd54d14af4eb3fe4edce86ce27d970ec832a96b55bc2ef1dffdf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-ppc64le'; 			sha256='83c7cf5afffcc7944e23ba5c1c038aff4f2d760f08681d76b5271b66c9e2af5d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-riscv64'; 			sha256='0e6047d2b0f745f0bbb13d707cfb945295bf45e397e67ff756f8551043a1f5bc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-s390x'; 			sha256='381b5b77e6a91075e746167ac160062a1adf4d2a1121e433f1ca731ad08e2353'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:d38a584a1da307e1ac31b3fd852369ae8a8176a1baa2e783b7e72077d8318364`  
		Last Modified: Thu, 05 Jun 2025 23:07:15 GMT  
		Size: 8.2 MB (8229004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122792206f35c9e929c0c28c585fd195a84012e2d9bea1522c579660e013f3a5`  
		Last Modified: Thu, 05 Jun 2025 22:50:09 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e5a5c767d7cf27a922e7c99956942414d9e65453df45e3500e05adf80db19d`  
		Last Modified: Thu, 05 Jun 2025 23:07:16 GMT  
		Size: 18.9 MB (18902608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2fc5aa8a4cd07adf8f84bd323a5d415f9ca2c5c158b74f9382a0b369265fe2`  
		Last Modified: Thu, 05 Jun 2025 23:07:14 GMT  
		Size: 19.5 MB (19469838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba639502cad797b5554e57bbdc209e0c34366d2a40e0b51a2fa20dfce1a5b337`  
		Last Modified: Thu, 05 Jun 2025 23:07:13 GMT  
		Size: 19.3 MB (19344051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda0f9c86634c1a6b9059d179ed7e6ead432e9b8bcddfb0e980660053ccaef13`  
		Last Modified: Thu, 05 Jun 2025 22:50:11 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef143fe66bfdc5598981ca016d8e3884fde63a7858eb245932bb9745217e515a`  
		Last Modified: Thu, 05 Jun 2025 22:50:14 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69e2c1a5fdbb4dad365dd880c4621563cfe56068eb2e2541c0de0b1de1353676`  
		Last Modified: Thu, 05 Jun 2025 22:50:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b81c7606e8dcfe2fd4ea847b572c410188a1a61c1b7b1cda6ba28a64e97f159`  
		Last Modified: Thu, 05 Jun 2025 23:08:03 GMT  
		Size: 7.1 MB (7141567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e3f3d3d88e3f3363a8a38c1a676767483806a513d0552d4772a08e36257b1c`  
		Last Modified: Thu, 05 Jun 2025 23:08:04 GMT  
		Size: 99.6 KB (99634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abefbbf9a5b4d4cca3ef794fb554ab4acac7277079ebf9e0403cc7bb13360683`  
		Last Modified: Thu, 05 Jun 2025 23:08:03 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15537da54888f9d1dd7c82127a2affc9eaa21eec06bc9938606f42434884b95d`  
		Last Modified: Thu, 05 Jun 2025 23:08:12 GMT  
		Size: 57.2 MB (57168179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b5eff1498a195bfe23aea7da2bcdf6de5f313f4140c8715a32acf14d62d62cd`  
		Last Modified: Thu, 05 Jun 2025 23:08:04 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b4cb7df5229fcce96acdc6de42d98aa670436a784a0e59417a1584407b6bb8`  
		Last Modified: Thu, 05 Jun 2025 23:08:05 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b640b4b96d1a9d3b71ca7172efbfc7644661ed859290a1ef70f6efb5ae8646b6`  
		Last Modified: Thu, 05 Jun 2025 23:10:53 GMT  
		Size: 1.0 MB (1022994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3954fdd9c5b6656129957c10bf87d54fb3f5abd93ddb09065d380cb210a5077`  
		Last Modified: Thu, 05 Jun 2025 23:10:53 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4258e800a40d5a0144bf5289d6469124b4dcd57aa4a07ebfe0b4d51a68c8176e`  
		Last Modified: Thu, 05 Jun 2025 23:10:54 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603a03c83db0af7bcffad6809d5df5087ed7fc636e484590aa7baf42f257b2f2`  
		Last Modified: Thu, 05 Jun 2025 23:10:56 GMT  
		Size: 18.0 MB (18016150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ced063cb74820e91a874efbb44b00db32b5453e8cf96c0082bfe9265f119ad2`  
		Last Modified: Thu, 05 Jun 2025 23:14:26 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:84c0fd5fb3a3c2479438611da949f104f724c986c93c76c12541d88382d56a73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2929db2e0b226bded3985c6262f564307858288cba598d29b2ed0fa3c11f193`

```dockerfile
```

-	Layers:
	-	`sha256:fb773e2f1f91681ce7adadf4bf3c53895f7c309689fbb9874a70b1ce0fc12347`  
		Last Modified: Fri, 06 Jun 2025 02:07:46 GMT  
		Size: 30.6 KB (30621 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28-windowsservercore`

```console
$ docker pull docker@sha256:0869de84e82e8707faa2238d565cea70e111fd670a2699eb7ed746f424fac81f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4061; amd64
	-	windows version 10.0.20348.3692; amd64

### `docker:28-windowsservercore` - windows version 10.0.26100.4061; amd64

```console
$ docker pull docker@sha256:25b529d707052438ef4b12929192d89e568c602554eff61b838530e3ba0862d0
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3496004439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5af2557ed6bf90b5a556401cda31f5e80c741723bd7d8d8dd85f75c9edb2beee`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 10 May 2025 01:13:32 GMT
RUN Install update 10.0.26100.4061
# Thu, 05 Jun 2025 22:49:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 05 Jun 2025 22:49:27 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 05 Jun 2025 22:49:29 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 05 Jun 2025 22:49:31 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.2.2.zip
# Thu, 05 Jun 2025 22:49:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 05 Jun 2025 22:49:45 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 05 Jun 2025 22:49:46 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Thu, 05 Jun 2025 22:49:48 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Thu, 05 Jun 2025 22:50:00 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 05 Jun 2025 22:50:02 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.0
# Thu, 05 Jun 2025 22:50:03 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-windows-x86_64.exe
# Thu, 05 Jun 2025 22:50:04 GMT
ENV DOCKER_COMPOSE_SHA256=5ddd1ff588eb7251381cf6257b9be44fbb92c02d984ccfc94b4280e8c33d0f8f
# Thu, 05 Jun 2025 22:50:15 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc834e13e71633c2d66ec6513d57c31a3157fc5933859d492ecf45fc8a7476c3`  
		Last Modified: Thu, 15 May 2025 19:25:03 GMT  
		Size: 1.2 GB (1215458626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90e49ef0e985b81e99d8b31a019b88aee89866bfb5c61dca46c36db719f75f72`  
		Last Modified: Thu, 05 Jun 2025 22:54:09 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35e4e87c87497c1f6d87a7f50d5b5d0f1d0cc7d219c6ce8eafc2a68e833177e3`  
		Last Modified: Thu, 05 Jun 2025 22:54:10 GMT  
		Size: 389.0 KB (389032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc34a02ab083801559a9993b8b75ebf1889f6ee4406ace24d67068a1db6d394`  
		Last Modified: Thu, 05 Jun 2025 22:54:09 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460eb4eabe732c14d4ba4780e91bfae9ce2f88f06d471caa6eaec23d33259db7`  
		Last Modified: Thu, 05 Jun 2025 22:54:10 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48921f27b31821d44d89e3376996fbcef78628b7c234b417f58afb6186212ee6`  
		Last Modified: Thu, 05 Jun 2025 22:54:12 GMT  
		Size: 20.5 MB (20482824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3fa9bcfc9c100af95e701bc8db63daa6762e21200bcbcfeacf780ceff4ac0a5`  
		Last Modified: Thu, 05 Jun 2025 23:02:29 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f73ddc322ec88bd49ef2ed8da74c0a7037d94bb1649764c3a424b89b9ba72f5`  
		Last Modified: Thu, 05 Jun 2025 23:02:32 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bee619612444d3cd3f98593f7912090ea8ebeaa7537f88e6ef0df6381f43660`  
		Last Modified: Thu, 05 Jun 2025 23:08:02 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aab9f1404ae5f4d3919e9d9b3989dc637b5461c0d61a0a8914464ac3efef61c`  
		Last Modified: Thu, 05 Jun 2025 23:08:03 GMT  
		Size: 22.3 MB (22293165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ffe3877611fd0a573d09a62990e99adc779e2ecfb7a0a99352b6097f1aedfa`  
		Last Modified: Thu, 05 Jun 2025 23:02:39 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c74c3be6ed0d6a50023b6597b4c73f7c8a6edf1bf15689254c3030e49379b3b`  
		Last Modified: Thu, 05 Jun 2025 23:02:42 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4546e8211fc088c3925f2b673074dc5a6d27527caf92983c56600ac02ceec30`  
		Last Modified: Thu, 05 Jun 2025 23:02:45 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:281c5b22c80200de8cb5cd27b59777a1a0c02818b3d09d937cc6ff99e29f8305`  
		Last Modified: Thu, 05 Jun 2025 23:08:07 GMT  
		Size: 22.1 MB (22061869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28-windowsservercore` - windows version 10.0.20348.3692; amd64

```console
$ docker pull docker@sha256:213ffc624913105fa7ee59720002de6a40b9768db21a5d09ec3f292a45573596
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2338596324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af09b10c562d5ce89c47cb4db81986d086849844eb9ea5e334925da4e6e60501`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Thu, 05 Jun 2025 22:44:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 05 Jun 2025 22:46:25 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 05 Jun 2025 22:46:26 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 05 Jun 2025 22:46:27 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.2.2.zip
# Thu, 05 Jun 2025 22:46:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 05 Jun 2025 22:46:51 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 05 Jun 2025 22:46:52 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Thu, 05 Jun 2025 22:46:52 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Thu, 05 Jun 2025 22:47:01 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 05 Jun 2025 22:47:02 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.0
# Thu, 05 Jun 2025 22:47:02 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-windows-x86_64.exe
# Thu, 05 Jun 2025 22:47:03 GMT
ENV DOCKER_COMPOSE_SHA256=5ddd1ff588eb7251381cf6257b9be44fbb92c02d984ccfc94b4280e8c33d0f8f
# Thu, 05 Jun 2025 22:47:14 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Thu, 15 May 2025 19:25:06 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69792782d0247e3e22c67f6096a5c5ac4096e3039e9902b31095ada21a3a3992`  
		Last Modified: Thu, 05 Jun 2025 22:47:55 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1528406f9d6a747555a27165ae52a9ade5da9bafe09faedc813fc9978410ebb1`  
		Last Modified: Thu, 05 Jun 2025 22:47:57 GMT  
		Size: 347.0 KB (347048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44599b0e57d9512be310c8211fc1db3c2b2f26d186b1f4fa5f41cb3239e83e08`  
		Last Modified: Thu, 05 Jun 2025 22:47:57 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5946a2c5ebb15f702288c926ad33ec3e48dc514e959828483bf2515343b8164`  
		Last Modified: Thu, 05 Jun 2025 22:47:58 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5950ebf7245c1e012f8bedfc8e4f944900fbb4429057e997700cbfc430e71db`  
		Last Modified: Thu, 05 Jun 2025 23:08:02 GMT  
		Size: 20.4 MB (20407814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e4979217510eb7de8d35cf3a6a4ea0d48a38fccd55990459ede40e90555a91`  
		Last Modified: Thu, 05 Jun 2025 22:50:52 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bee3bf1d9c1e36c3c62244bbf0b25abd4d3848230da86f8eb7ab9e87bfcce25`  
		Last Modified: Thu, 05 Jun 2025 22:50:55 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dd6d131f13751da51b0a0640902b80152d4626d65b68249d48306530f6af710`  
		Last Modified: Thu, 05 Jun 2025 22:50:58 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809edd0f0043024cc3f263278554b9d43f0af10b1ff965b9e755e7f504cc9448`  
		Last Modified: Thu, 05 Jun 2025 23:08:01 GMT  
		Size: 22.2 MB (22218481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3644edf37145bf3243218f63e04734da0ee41b17a3db4580ac428852159a95b4`  
		Last Modified: Thu, 05 Jun 2025 22:51:01 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f3f405f8fc75b4dbb8e568437773842a367615ed3dbe41b6be647fdbcb3756e`  
		Last Modified: Thu, 05 Jun 2025 22:51:04 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4701c8fc8cca7fb8a5a1d7d575fa186deff56c45e248857b3ed475c698ed20c8`  
		Last Modified: Thu, 05 Jun 2025 22:51:08 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b4da056663f41259b84270c9d8dc6b48fb2b7d53922c07335a68a8dc178b488`  
		Last Modified: Thu, 05 Jun 2025 23:08:02 GMT  
		Size: 22.0 MB (21983289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:bc2b0152ecb9f33a768c3b3a7ba14c8206d2b7f60077c28a3546b40efb6dd9c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `docker:28-windowsservercore-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull docker@sha256:213ffc624913105fa7ee59720002de6a40b9768db21a5d09ec3f292a45573596
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2338596324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af09b10c562d5ce89c47cb4db81986d086849844eb9ea5e334925da4e6e60501`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Thu, 05 Jun 2025 22:44:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 05 Jun 2025 22:46:25 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 05 Jun 2025 22:46:26 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 05 Jun 2025 22:46:27 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.2.2.zip
# Thu, 05 Jun 2025 22:46:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 05 Jun 2025 22:46:51 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 05 Jun 2025 22:46:52 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Thu, 05 Jun 2025 22:46:52 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Thu, 05 Jun 2025 22:47:01 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 05 Jun 2025 22:47:02 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.0
# Thu, 05 Jun 2025 22:47:02 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-windows-x86_64.exe
# Thu, 05 Jun 2025 22:47:03 GMT
ENV DOCKER_COMPOSE_SHA256=5ddd1ff588eb7251381cf6257b9be44fbb92c02d984ccfc94b4280e8c33d0f8f
# Thu, 05 Jun 2025 22:47:14 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Thu, 15 May 2025 19:25:06 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69792782d0247e3e22c67f6096a5c5ac4096e3039e9902b31095ada21a3a3992`  
		Last Modified: Thu, 05 Jun 2025 22:47:55 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1528406f9d6a747555a27165ae52a9ade5da9bafe09faedc813fc9978410ebb1`  
		Last Modified: Thu, 05 Jun 2025 22:47:57 GMT  
		Size: 347.0 KB (347048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44599b0e57d9512be310c8211fc1db3c2b2f26d186b1f4fa5f41cb3239e83e08`  
		Last Modified: Thu, 05 Jun 2025 22:47:57 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5946a2c5ebb15f702288c926ad33ec3e48dc514e959828483bf2515343b8164`  
		Last Modified: Thu, 05 Jun 2025 22:47:58 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5950ebf7245c1e012f8bedfc8e4f944900fbb4429057e997700cbfc430e71db`  
		Last Modified: Thu, 05 Jun 2025 23:08:02 GMT  
		Size: 20.4 MB (20407814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e4979217510eb7de8d35cf3a6a4ea0d48a38fccd55990459ede40e90555a91`  
		Last Modified: Thu, 05 Jun 2025 22:50:52 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bee3bf1d9c1e36c3c62244bbf0b25abd4d3848230da86f8eb7ab9e87bfcce25`  
		Last Modified: Thu, 05 Jun 2025 22:50:55 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dd6d131f13751da51b0a0640902b80152d4626d65b68249d48306530f6af710`  
		Last Modified: Thu, 05 Jun 2025 22:50:58 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809edd0f0043024cc3f263278554b9d43f0af10b1ff965b9e755e7f504cc9448`  
		Last Modified: Thu, 05 Jun 2025 23:08:01 GMT  
		Size: 22.2 MB (22218481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3644edf37145bf3243218f63e04734da0ee41b17a3db4580ac428852159a95b4`  
		Last Modified: Thu, 05 Jun 2025 22:51:01 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f3f405f8fc75b4dbb8e568437773842a367615ed3dbe41b6be647fdbcb3756e`  
		Last Modified: Thu, 05 Jun 2025 22:51:04 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4701c8fc8cca7fb8a5a1d7d575fa186deff56c45e248857b3ed475c698ed20c8`  
		Last Modified: Thu, 05 Jun 2025 22:51:08 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b4da056663f41259b84270c9d8dc6b48fb2b7d53922c07335a68a8dc178b488`  
		Last Modified: Thu, 05 Jun 2025 23:08:02 GMT  
		Size: 22.0 MB (21983289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:5f0071c24f8a2426413b698206c5a415be20f1024483d31ea54cd904e41465df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4061; amd64

### `docker:28-windowsservercore-ltsc2025` - windows version 10.0.26100.4061; amd64

```console
$ docker pull docker@sha256:25b529d707052438ef4b12929192d89e568c602554eff61b838530e3ba0862d0
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3496004439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5af2557ed6bf90b5a556401cda31f5e80c741723bd7d8d8dd85f75c9edb2beee`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 10 May 2025 01:13:32 GMT
RUN Install update 10.0.26100.4061
# Thu, 05 Jun 2025 22:49:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 05 Jun 2025 22:49:27 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 05 Jun 2025 22:49:29 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 05 Jun 2025 22:49:31 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.2.2.zip
# Thu, 05 Jun 2025 22:49:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 05 Jun 2025 22:49:45 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 05 Jun 2025 22:49:46 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Thu, 05 Jun 2025 22:49:48 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Thu, 05 Jun 2025 22:50:00 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 05 Jun 2025 22:50:02 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.0
# Thu, 05 Jun 2025 22:50:03 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-windows-x86_64.exe
# Thu, 05 Jun 2025 22:50:04 GMT
ENV DOCKER_COMPOSE_SHA256=5ddd1ff588eb7251381cf6257b9be44fbb92c02d984ccfc94b4280e8c33d0f8f
# Thu, 05 Jun 2025 22:50:15 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc834e13e71633c2d66ec6513d57c31a3157fc5933859d492ecf45fc8a7476c3`  
		Last Modified: Thu, 15 May 2025 19:25:03 GMT  
		Size: 1.2 GB (1215458626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90e49ef0e985b81e99d8b31a019b88aee89866bfb5c61dca46c36db719f75f72`  
		Last Modified: Thu, 05 Jun 2025 22:54:09 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35e4e87c87497c1f6d87a7f50d5b5d0f1d0cc7d219c6ce8eafc2a68e833177e3`  
		Last Modified: Thu, 05 Jun 2025 22:54:10 GMT  
		Size: 389.0 KB (389032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc34a02ab083801559a9993b8b75ebf1889f6ee4406ace24d67068a1db6d394`  
		Last Modified: Thu, 05 Jun 2025 22:54:09 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460eb4eabe732c14d4ba4780e91bfae9ce2f88f06d471caa6eaec23d33259db7`  
		Last Modified: Thu, 05 Jun 2025 22:54:10 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48921f27b31821d44d89e3376996fbcef78628b7c234b417f58afb6186212ee6`  
		Last Modified: Thu, 05 Jun 2025 22:54:12 GMT  
		Size: 20.5 MB (20482824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3fa9bcfc9c100af95e701bc8db63daa6762e21200bcbcfeacf780ceff4ac0a5`  
		Last Modified: Thu, 05 Jun 2025 23:02:29 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f73ddc322ec88bd49ef2ed8da74c0a7037d94bb1649764c3a424b89b9ba72f5`  
		Last Modified: Thu, 05 Jun 2025 23:02:32 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bee619612444d3cd3f98593f7912090ea8ebeaa7537f88e6ef0df6381f43660`  
		Last Modified: Thu, 05 Jun 2025 23:08:02 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aab9f1404ae5f4d3919e9d9b3989dc637b5461c0d61a0a8914464ac3efef61c`  
		Last Modified: Thu, 05 Jun 2025 23:08:03 GMT  
		Size: 22.3 MB (22293165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ffe3877611fd0a573d09a62990e99adc779e2ecfb7a0a99352b6097f1aedfa`  
		Last Modified: Thu, 05 Jun 2025 23:02:39 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c74c3be6ed0d6a50023b6597b4c73f7c8a6edf1bf15689254c3030e49379b3b`  
		Last Modified: Thu, 05 Jun 2025 23:02:42 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4546e8211fc088c3925f2b673074dc5a6d27527caf92983c56600ac02ceec30`  
		Last Modified: Thu, 05 Jun 2025 23:02:45 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:281c5b22c80200de8cb5cd27b59777a1a0c02818b3d09d937cc6ff99e29f8305`  
		Last Modified: Thu, 05 Jun 2025 23:08:07 GMT  
		Size: 22.1 MB (22061869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.2`

```console
$ docker pull docker@sha256:d4668861cabc1691635d98e827a81cfa834a416f8fe0f4efc609f9f806d86d82
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
$ docker pull docker@sha256:8c9502da312e1595a696775bea7d4e6e7b18102d62c413b43f9d3f9d353eb323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.7 MB (143680550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e1cee4b3a3c0bfea53084cb7708d24f3314dd7ce46631888127d8037a4158d9`
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
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99164a65e1f060513df17430a291c788a5801cc0364c3cf0abaf9dd47e9d891c`  
		Last Modified: Thu, 05 Jun 2025 22:44:25 GMT  
		Size: 8.2 MB (8207469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a930b44823eb85c484514670f94fa0fadf7649aa34a692072e953b86cff998`  
		Last Modified: Thu, 05 Jun 2025 22:44:24 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89fad9bfb8f24abcb392b00c918762036dedf67787dc8a32b43aec570f3557f4`  
		Last Modified: Thu, 05 Jun 2025 22:44:28 GMT  
		Size: 20.1 MB (20083033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e993a5c36c8c13b622945142edd4bdf6b5d03775d8e91196856e50e0512650a`  
		Last Modified: Thu, 05 Jun 2025 22:44:27 GMT  
		Size: 21.3 MB (21290182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd58cf00359048abfc4f447feefe1373db7fd84dfe136fb751689b640844dd4b`  
		Last Modified: Thu, 05 Jun 2025 22:44:27 GMT  
		Size: 21.1 MB (21092192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bd9fc81ec33be8d5693955225a870888bf988fe35871af701d05810a7718b9`  
		Last Modified: Thu, 05 Jun 2025 22:44:26 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7dc70da6730815a90c517d43ed51312bc13932b65a288bbb8952f74df9d763a`  
		Last Modified: Thu, 05 Jun 2025 22:44:26 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2483cd3bb024143d65a844f930ffb5aa01cb0932a660abcaa0fcd68ddc0810`  
		Last Modified: Thu, 05 Jun 2025 22:44:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:232671b8d6c574d91a514e1073ddb00bd37e47ba17cfeefc0a4e078e392e4a00`  
		Last Modified: Thu, 05 Jun 2025 23:10:12 GMT  
		Size: 6.9 MB (6905563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8947c15ddd39c2ad279e9f5b5180a071aa948c04d248e2dcf4cb13585d9b47b8`  
		Last Modified: Thu, 05 Jun 2025 23:10:12 GMT  
		Size: 90.5 KB (90492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f7e4c6039fec8c4db67902febab1ae735352d758ffb76367f1e3e68a0b04b9d`  
		Last Modified: Thu, 05 Jun 2025 23:10:11 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:369f3cb80e373dbeee03da49ca69ce93f7c63f165704f929f0a040a4de56ed8e`  
		Last Modified: Thu, 05 Jun 2025 23:10:16 GMT  
		Size: 62.2 MB (62206624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7a0f373a71bb7b7e7a3be4baa2472d2850c4c9549c66b58e70a59a51b696ee`  
		Last Modified: Thu, 05 Jun 2025 23:10:11 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4dbe5b0725a180af25ab3d235ff1a32980b060cb2e263d0362d2baa5b73d858`  
		Last Modified: Thu, 05 Jun 2025 23:10:11 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2` - unknown; unknown

```console
$ docker pull docker@sha256:227416a58467a90d61d00571bea5da05930524bab4cb82350e892b245e0d2e6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:125d3c52d0be767b8d0f76f67d0acd7adb2635cac747795240c64e1792d2f95e`

```dockerfile
```

-	Layers:
	-	`sha256:06c3e6cf1c5d56e7cb2fe109c0aa850bd00d57c61602118e103dbffd829369a6`  
		Last Modified: Fri, 06 Jun 2025 02:07:30 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.2` - linux; arm variant v6

```console
$ docker pull docker@sha256:7920dd4fb3d5c69b32f5a8fdad7bc083113e1eb057daf9551d3bec928642d2d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134721385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f04c9bfb20a7623a34894618839c13fd1bf730153cc94bc61f9b9d60dbc8dc6`
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
	-	`sha256:b18e44e663f768131c50d79640817a860ca8c20877f41bfc7e788ede7276f121`  
		Last Modified: Thu, 05 Jun 2025 22:44:12 GMT  
		Size: 19.8 MB (19834728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b7cf9bb5cb3a10f219b307b2ff9f67f54ab05208492bbe13e06a74ca78e54d`  
		Last Modified: Thu, 05 Jun 2025 22:44:13 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7393d30c6bcbe757d4919545933b9de1b6f48c9a46a3ed4a0ae9281792fbd51`  
		Last Modified: Thu, 05 Jun 2025 22:51:09 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe877f07f4d94074494db81efb5c5e890ab77b7ce09fa3952f972953a436545d`  
		Last Modified: Thu, 05 Jun 2025 22:51:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9526e4c6fe05aa09bd1848ecd6d91b389e046a9da41b839528a0f104ba7e6b`  
		Last Modified: Fri, 06 Jun 2025 01:05:46 GMT  
		Size: 7.2 MB (7230299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7741447d38cadd971edc0ea8d19ec995a5929dad7df81e579060cf95a0a66e0e`  
		Last Modified: Thu, 05 Jun 2025 23:14:04 GMT  
		Size: 90.1 KB (90052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eabb360d9297b2af61c701c3a02f961b3210cdb6c3a4119c7a03d703fd26c6b`  
		Last Modified: Thu, 05 Jun 2025 23:14:08 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c250f611b5a5d3e13bac22e1a236ffb37d10345c511e869b539265c145ebc1`  
		Last Modified: Fri, 06 Jun 2025 01:05:49 GMT  
		Size: 57.9 MB (57897379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b907cd35da6b2acf22cf12c6849885f91becbd5836560543543e4df0b7e4ede`  
		Last Modified: Thu, 05 Jun 2025 23:14:11 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b319c010975a1f690900a80187653a3834b1a65ec15f73ccd7edf9c103bc8eb`  
		Last Modified: Thu, 05 Jun 2025 23:14:13 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2` - unknown; unknown

```console
$ docker pull docker@sha256:918e10532d5d49ad3d988b0f42404e4e65b4ff96c9f47d1de4c3bb238edfaf26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc5e34ba8e1767c238c0ca97f2315e8d15bc7d875be15383aa1599e4d71188d2`

```dockerfile
```

-	Layers:
	-	`sha256:21bc1dae29bbc15eda321d47bbd61a416fa4a9175b7a84d90debd5063a161db7`  
		Last Modified: Fri, 06 Jun 2025 02:07:34 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.2` - linux; arm variant v7

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

### `docker:28.2` - unknown; unknown

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

### `docker:28.2` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:0de688aa942b05b1ca86e80e9e87a92cab8690ca4d00819b777253ca12fd05b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.5 MB (134498975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e07111220cfca840da6105d81020ea43df6b1c90921916a1cd65417e1101d6e`
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
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38a584a1da307e1ac31b3fd852369ae8a8176a1baa2e783b7e72077d8318364`  
		Last Modified: Thu, 05 Jun 2025 23:07:15 GMT  
		Size: 8.2 MB (8229004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122792206f35c9e929c0c28c585fd195a84012e2d9bea1522c579660e013f3a5`  
		Last Modified: Thu, 05 Jun 2025 22:50:09 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e5a5c767d7cf27a922e7c99956942414d9e65453df45e3500e05adf80db19d`  
		Last Modified: Thu, 05 Jun 2025 23:07:16 GMT  
		Size: 18.9 MB (18902608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2fc5aa8a4cd07adf8f84bd323a5d415f9ca2c5c158b74f9382a0b369265fe2`  
		Last Modified: Thu, 05 Jun 2025 23:07:14 GMT  
		Size: 19.5 MB (19469838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba639502cad797b5554e57bbdc209e0c34366d2a40e0b51a2fa20dfce1a5b337`  
		Last Modified: Thu, 05 Jun 2025 23:07:13 GMT  
		Size: 19.3 MB (19344051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda0f9c86634c1a6b9059d179ed7e6ead432e9b8bcddfb0e980660053ccaef13`  
		Last Modified: Thu, 05 Jun 2025 22:50:11 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef143fe66bfdc5598981ca016d8e3884fde63a7858eb245932bb9745217e515a`  
		Last Modified: Thu, 05 Jun 2025 22:50:14 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69e2c1a5fdbb4dad365dd880c4621563cfe56068eb2e2541c0de0b1de1353676`  
		Last Modified: Thu, 05 Jun 2025 22:50:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b81c7606e8dcfe2fd4ea847b572c410188a1a61c1b7b1cda6ba28a64e97f159`  
		Last Modified: Thu, 05 Jun 2025 23:08:03 GMT  
		Size: 7.1 MB (7141567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e3f3d3d88e3f3363a8a38c1a676767483806a513d0552d4772a08e36257b1c`  
		Last Modified: Thu, 05 Jun 2025 23:08:04 GMT  
		Size: 99.6 KB (99634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abefbbf9a5b4d4cca3ef794fb554ab4acac7277079ebf9e0403cc7bb13360683`  
		Last Modified: Thu, 05 Jun 2025 23:08:03 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15537da54888f9d1dd7c82127a2affc9eaa21eec06bc9938606f42434884b95d`  
		Last Modified: Thu, 05 Jun 2025 23:08:12 GMT  
		Size: 57.2 MB (57168179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b5eff1498a195bfe23aea7da2bcdf6de5f313f4140c8715a32acf14d62d62cd`  
		Last Modified: Thu, 05 Jun 2025 23:08:04 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b4cb7df5229fcce96acdc6de42d98aa670436a784a0e59417a1584407b6bb8`  
		Last Modified: Thu, 05 Jun 2025 23:08:05 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2` - unknown; unknown

```console
$ docker pull docker@sha256:5cad50c6b3b442444f6651f5c8b4d33a9f66b976fd04acda0c3b54328ac14556
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeded159db72e188c1c71b241cf1c67644293d460aa0a7d23d1fd5424dc510de`

```dockerfile
```

-	Layers:
	-	`sha256:431922ef17f88491b0a295b18dd805f113ce40a500def3af5b4651f0b1b77da1`  
		Last Modified: Fri, 06 Jun 2025 02:07:41 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.2-cli`

```console
$ docker pull docker@sha256:c2e49a065e45c462dda70b65b1a50a74c75804091fae15b7e4fbec6b114996d1
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
$ docker pull docker@sha256:29ac2aff504532e72efca1a58f229c0e05f928828e62156fb304d391e82f7f49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74471875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd02548899f2c001be05193b91d116511f57fb7e8f5cec5f7b58cce36fed0303`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99164a65e1f060513df17430a291c788a5801cc0364c3cf0abaf9dd47e9d891c`  
		Last Modified: Thu, 05 Jun 2025 22:44:25 GMT  
		Size: 8.2 MB (8207469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a930b44823eb85c484514670f94fa0fadf7649aa34a692072e953b86cff998`  
		Last Modified: Thu, 05 Jun 2025 22:44:24 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89fad9bfb8f24abcb392b00c918762036dedf67787dc8a32b43aec570f3557f4`  
		Last Modified: Thu, 05 Jun 2025 22:44:28 GMT  
		Size: 20.1 MB (20083033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e993a5c36c8c13b622945142edd4bdf6b5d03775d8e91196856e50e0512650a`  
		Last Modified: Thu, 05 Jun 2025 22:44:27 GMT  
		Size: 21.3 MB (21290182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd58cf00359048abfc4f447feefe1373db7fd84dfe136fb751689b640844dd4b`  
		Last Modified: Thu, 05 Jun 2025 22:44:27 GMT  
		Size: 21.1 MB (21092192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bd9fc81ec33be8d5693955225a870888bf988fe35871af701d05810a7718b9`  
		Last Modified: Thu, 05 Jun 2025 22:44:26 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7dc70da6730815a90c517d43ed51312bc13932b65a288bbb8952f74df9d763a`  
		Last Modified: Thu, 05 Jun 2025 22:44:26 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2483cd3bb024143d65a844f930ffb5aa01cb0932a660abcaa0fcd68ddc0810`  
		Last Modified: Thu, 05 Jun 2025 22:44:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2-cli` - unknown; unknown

```console
$ docker pull docker@sha256:e3c92c354188244e1e651ab7c9384326a36594dbf3e27427328aa209be1c1e7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de64116684520fb5473d5fee53d9f710a283fa5926d23334bbeb9a13ece30127`

```dockerfile
```

-	Layers:
	-	`sha256:9f1baaf1f40a67141a0489af913841dd7e9427be207fe398702581c569cd1c20`  
		Last Modified: Thu, 05 Jun 2025 23:07:43 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.2-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:6f76795bf488400672b314ad95bc4add17d3871c369454a410a6072cd1f7fe6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69497654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4905167d30157f311983a0f0fbb87d96647db6c5478ae0071e5e9d717c22247`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
	-	`sha256:b18e44e663f768131c50d79640817a860ca8c20877f41bfc7e788ede7276f121`  
		Last Modified: Thu, 05 Jun 2025 22:44:12 GMT  
		Size: 19.8 MB (19834728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b7cf9bb5cb3a10f219b307b2ff9f67f54ab05208492bbe13e06a74ca78e54d`  
		Last Modified: Thu, 05 Jun 2025 22:44:13 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7393d30c6bcbe757d4919545933b9de1b6f48c9a46a3ed4a0ae9281792fbd51`  
		Last Modified: Thu, 05 Jun 2025 22:51:09 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe877f07f4d94074494db81efb5c5e890ab77b7ce09fa3952f972953a436545d`  
		Last Modified: Thu, 05 Jun 2025 22:51:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2-cli` - unknown; unknown

```console
$ docker pull docker@sha256:9c9ad38782ad3e5c053ed8c736f10e9589825748a8c4233619fb70a2ec23af36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86ca6472c159b81f34510b55fdadf12635ed814ad061552012b01cc7622021dd`

```dockerfile
```

-	Layers:
	-	`sha256:c58766a24b3303a1f1acf7a634a2134383f4aa8fc7b6223cb9497695c7739a5f`  
		Last Modified: Thu, 05 Jun 2025 23:07:47 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.2-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:1e48b83f7392bb14bec910d025f2b5ba1a759fff65845d925284236bc07d4fe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68494484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61de327c238ebb7ad778ea80f8124ffd3e79271ceb1c162b0fbdfb43ad4a56f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:28.2-cli` - unknown; unknown

```console
$ docker pull docker@sha256:c13cadb351384ad992f27483f70dba162d9c5b57e6643cec3c37598aebb9ff47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ef1b27ab22635d8c650664a7ff740383003126f39daab1972f0db14de9fe5af`

```dockerfile
```

-	Layers:
	-	`sha256:efca98ea4b9f81656feedd1b0eb5f97c37873667b5a92fa941594dad0570afc7`  
		Last Modified: Thu, 05 Jun 2025 23:07:51 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.2-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:050e38ffb61f1a397a300e2c027858126865eb5c53026a10a231ea8c71637cf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70083597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:049c11c099d31b1b16a8eec2d4744a8baa44341b7f6489e7c2a70a8c597e17d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38a584a1da307e1ac31b3fd852369ae8a8176a1baa2e783b7e72077d8318364`  
		Last Modified: Thu, 05 Jun 2025 23:07:15 GMT  
		Size: 8.2 MB (8229004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122792206f35c9e929c0c28c585fd195a84012e2d9bea1522c579660e013f3a5`  
		Last Modified: Thu, 05 Jun 2025 22:50:09 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e5a5c767d7cf27a922e7c99956942414d9e65453df45e3500e05adf80db19d`  
		Last Modified: Thu, 05 Jun 2025 23:07:16 GMT  
		Size: 18.9 MB (18902608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2fc5aa8a4cd07adf8f84bd323a5d415f9ca2c5c158b74f9382a0b369265fe2`  
		Last Modified: Thu, 05 Jun 2025 23:07:14 GMT  
		Size: 19.5 MB (19469838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba639502cad797b5554e57bbdc209e0c34366d2a40e0b51a2fa20dfce1a5b337`  
		Last Modified: Thu, 05 Jun 2025 23:07:13 GMT  
		Size: 19.3 MB (19344051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda0f9c86634c1a6b9059d179ed7e6ead432e9b8bcddfb0e980660053ccaef13`  
		Last Modified: Thu, 05 Jun 2025 22:50:11 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef143fe66bfdc5598981ca016d8e3884fde63a7858eb245932bb9745217e515a`  
		Last Modified: Thu, 05 Jun 2025 22:50:14 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69e2c1a5fdbb4dad365dd880c4621563cfe56068eb2e2541c0de0b1de1353676`  
		Last Modified: Thu, 05 Jun 2025 22:50:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2-cli` - unknown; unknown

```console
$ docker pull docker@sha256:3d9117cfb4076144f396a04008c8592792765eb725010db68b4fc6a3e9d07a3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8f618e6cdf0288b0248e4b6b48f1bd5324300dfd40ccfdcc2698737d569f539`

```dockerfile
```

-	Layers:
	-	`sha256:07a44b113f5c5d8eb65a6af4b53f0ae0869dcbfdd809ec06739500831432a0db`  
		Last Modified: Thu, 05 Jun 2025 23:07:55 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.2-dind`

```console
$ docker pull docker@sha256:d4668861cabc1691635d98e827a81cfa834a416f8fe0f4efc609f9f806d86d82
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
$ docker pull docker@sha256:8c9502da312e1595a696775bea7d4e6e7b18102d62c413b43f9d3f9d353eb323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.7 MB (143680550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e1cee4b3a3c0bfea53084cb7708d24f3314dd7ce46631888127d8037a4158d9`
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
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99164a65e1f060513df17430a291c788a5801cc0364c3cf0abaf9dd47e9d891c`  
		Last Modified: Thu, 05 Jun 2025 22:44:25 GMT  
		Size: 8.2 MB (8207469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a930b44823eb85c484514670f94fa0fadf7649aa34a692072e953b86cff998`  
		Last Modified: Thu, 05 Jun 2025 22:44:24 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89fad9bfb8f24abcb392b00c918762036dedf67787dc8a32b43aec570f3557f4`  
		Last Modified: Thu, 05 Jun 2025 22:44:28 GMT  
		Size: 20.1 MB (20083033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e993a5c36c8c13b622945142edd4bdf6b5d03775d8e91196856e50e0512650a`  
		Last Modified: Thu, 05 Jun 2025 22:44:27 GMT  
		Size: 21.3 MB (21290182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd58cf00359048abfc4f447feefe1373db7fd84dfe136fb751689b640844dd4b`  
		Last Modified: Thu, 05 Jun 2025 22:44:27 GMT  
		Size: 21.1 MB (21092192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bd9fc81ec33be8d5693955225a870888bf988fe35871af701d05810a7718b9`  
		Last Modified: Thu, 05 Jun 2025 22:44:26 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7dc70da6730815a90c517d43ed51312bc13932b65a288bbb8952f74df9d763a`  
		Last Modified: Thu, 05 Jun 2025 22:44:26 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2483cd3bb024143d65a844f930ffb5aa01cb0932a660abcaa0fcd68ddc0810`  
		Last Modified: Thu, 05 Jun 2025 22:44:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:232671b8d6c574d91a514e1073ddb00bd37e47ba17cfeefc0a4e078e392e4a00`  
		Last Modified: Thu, 05 Jun 2025 23:10:12 GMT  
		Size: 6.9 MB (6905563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8947c15ddd39c2ad279e9f5b5180a071aa948c04d248e2dcf4cb13585d9b47b8`  
		Last Modified: Thu, 05 Jun 2025 23:10:12 GMT  
		Size: 90.5 KB (90492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f7e4c6039fec8c4db67902febab1ae735352d758ffb76367f1e3e68a0b04b9d`  
		Last Modified: Thu, 05 Jun 2025 23:10:11 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:369f3cb80e373dbeee03da49ca69ce93f7c63f165704f929f0a040a4de56ed8e`  
		Last Modified: Thu, 05 Jun 2025 23:10:16 GMT  
		Size: 62.2 MB (62206624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7a0f373a71bb7b7e7a3be4baa2472d2850c4c9549c66b58e70a59a51b696ee`  
		Last Modified: Thu, 05 Jun 2025 23:10:11 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4dbe5b0725a180af25ab3d235ff1a32980b060cb2e263d0362d2baa5b73d858`  
		Last Modified: Thu, 05 Jun 2025 23:10:11 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2-dind` - unknown; unknown

```console
$ docker pull docker@sha256:227416a58467a90d61d00571bea5da05930524bab4cb82350e892b245e0d2e6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:125d3c52d0be767b8d0f76f67d0acd7adb2635cac747795240c64e1792d2f95e`

```dockerfile
```

-	Layers:
	-	`sha256:06c3e6cf1c5d56e7cb2fe109c0aa850bd00d57c61602118e103dbffd829369a6`  
		Last Modified: Fri, 06 Jun 2025 02:07:30 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.2-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:7920dd4fb3d5c69b32f5a8fdad7bc083113e1eb057daf9551d3bec928642d2d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134721385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f04c9bfb20a7623a34894618839c13fd1bf730153cc94bc61f9b9d60dbc8dc6`
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
	-	`sha256:b18e44e663f768131c50d79640817a860ca8c20877f41bfc7e788ede7276f121`  
		Last Modified: Thu, 05 Jun 2025 22:44:12 GMT  
		Size: 19.8 MB (19834728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b7cf9bb5cb3a10f219b307b2ff9f67f54ab05208492bbe13e06a74ca78e54d`  
		Last Modified: Thu, 05 Jun 2025 22:44:13 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7393d30c6bcbe757d4919545933b9de1b6f48c9a46a3ed4a0ae9281792fbd51`  
		Last Modified: Thu, 05 Jun 2025 22:51:09 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe877f07f4d94074494db81efb5c5e890ab77b7ce09fa3952f972953a436545d`  
		Last Modified: Thu, 05 Jun 2025 22:51:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9526e4c6fe05aa09bd1848ecd6d91b389e046a9da41b839528a0f104ba7e6b`  
		Last Modified: Fri, 06 Jun 2025 01:05:46 GMT  
		Size: 7.2 MB (7230299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7741447d38cadd971edc0ea8d19ec995a5929dad7df81e579060cf95a0a66e0e`  
		Last Modified: Thu, 05 Jun 2025 23:14:04 GMT  
		Size: 90.1 KB (90052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eabb360d9297b2af61c701c3a02f961b3210cdb6c3a4119c7a03d703fd26c6b`  
		Last Modified: Thu, 05 Jun 2025 23:14:08 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c250f611b5a5d3e13bac22e1a236ffb37d10345c511e869b539265c145ebc1`  
		Last Modified: Fri, 06 Jun 2025 01:05:49 GMT  
		Size: 57.9 MB (57897379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b907cd35da6b2acf22cf12c6849885f91becbd5836560543543e4df0b7e4ede`  
		Last Modified: Thu, 05 Jun 2025 23:14:11 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b319c010975a1f690900a80187653a3834b1a65ec15f73ccd7edf9c103bc8eb`  
		Last Modified: Thu, 05 Jun 2025 23:14:13 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2-dind` - unknown; unknown

```console
$ docker pull docker@sha256:918e10532d5d49ad3d988b0f42404e4e65b4ff96c9f47d1de4c3bb238edfaf26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc5e34ba8e1767c238c0ca97f2315e8d15bc7d875be15383aa1599e4d71188d2`

```dockerfile
```

-	Layers:
	-	`sha256:21bc1dae29bbc15eda321d47bbd61a416fa4a9175b7a84d90debd5063a161db7`  
		Last Modified: Fri, 06 Jun 2025 02:07:34 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.2-dind` - linux; arm variant v7

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

### `docker:28.2-dind` - unknown; unknown

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

### `docker:28.2-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:0de688aa942b05b1ca86e80e9e87a92cab8690ca4d00819b777253ca12fd05b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.5 MB (134498975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e07111220cfca840da6105d81020ea43df6b1c90921916a1cd65417e1101d6e`
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
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38a584a1da307e1ac31b3fd852369ae8a8176a1baa2e783b7e72077d8318364`  
		Last Modified: Thu, 05 Jun 2025 23:07:15 GMT  
		Size: 8.2 MB (8229004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122792206f35c9e929c0c28c585fd195a84012e2d9bea1522c579660e013f3a5`  
		Last Modified: Thu, 05 Jun 2025 22:50:09 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e5a5c767d7cf27a922e7c99956942414d9e65453df45e3500e05adf80db19d`  
		Last Modified: Thu, 05 Jun 2025 23:07:16 GMT  
		Size: 18.9 MB (18902608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2fc5aa8a4cd07adf8f84bd323a5d415f9ca2c5c158b74f9382a0b369265fe2`  
		Last Modified: Thu, 05 Jun 2025 23:07:14 GMT  
		Size: 19.5 MB (19469838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba639502cad797b5554e57bbdc209e0c34366d2a40e0b51a2fa20dfce1a5b337`  
		Last Modified: Thu, 05 Jun 2025 23:07:13 GMT  
		Size: 19.3 MB (19344051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda0f9c86634c1a6b9059d179ed7e6ead432e9b8bcddfb0e980660053ccaef13`  
		Last Modified: Thu, 05 Jun 2025 22:50:11 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef143fe66bfdc5598981ca016d8e3884fde63a7858eb245932bb9745217e515a`  
		Last Modified: Thu, 05 Jun 2025 22:50:14 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69e2c1a5fdbb4dad365dd880c4621563cfe56068eb2e2541c0de0b1de1353676`  
		Last Modified: Thu, 05 Jun 2025 22:50:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b81c7606e8dcfe2fd4ea847b572c410188a1a61c1b7b1cda6ba28a64e97f159`  
		Last Modified: Thu, 05 Jun 2025 23:08:03 GMT  
		Size: 7.1 MB (7141567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e3f3d3d88e3f3363a8a38c1a676767483806a513d0552d4772a08e36257b1c`  
		Last Modified: Thu, 05 Jun 2025 23:08:04 GMT  
		Size: 99.6 KB (99634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abefbbf9a5b4d4cca3ef794fb554ab4acac7277079ebf9e0403cc7bb13360683`  
		Last Modified: Thu, 05 Jun 2025 23:08:03 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15537da54888f9d1dd7c82127a2affc9eaa21eec06bc9938606f42434884b95d`  
		Last Modified: Thu, 05 Jun 2025 23:08:12 GMT  
		Size: 57.2 MB (57168179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b5eff1498a195bfe23aea7da2bcdf6de5f313f4140c8715a32acf14d62d62cd`  
		Last Modified: Thu, 05 Jun 2025 23:08:04 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b4cb7df5229fcce96acdc6de42d98aa670436a784a0e59417a1584407b6bb8`  
		Last Modified: Thu, 05 Jun 2025 23:08:05 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2-dind` - unknown; unknown

```console
$ docker pull docker@sha256:5cad50c6b3b442444f6651f5c8b4d33a9f66b976fd04acda0c3b54328ac14556
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeded159db72e188c1c71b241cf1c67644293d460aa0a7d23d1fd5424dc510de`

```dockerfile
```

-	Layers:
	-	`sha256:431922ef17f88491b0a295b18dd805f113ce40a500def3af5b4651f0b1b77da1`  
		Last Modified: Fri, 06 Jun 2025 02:07:41 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.2-dind-rootless`

```console
$ docker pull docker@sha256:8fc8c7e252d63e2280415a0520caf2a014c86b5c8fd25c910fe8adc77aeb94ca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:28.2-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:abd2dd1debd13881cb395d987a48ef2db49e904f9260e691cdd8fb3f40c8c810
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.3 MB (162261128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:515c53634a6d629377edd34a1fa5f3f6977b9ff51a6afb4aa84a220a5f27d5c4`
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
ENV DOCKER_COMPOSE_VERSION=2.37.0
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-x86_64'; 			sha256='e6e471b1e7bf0443592d3987dea6073f08db3e48ba0580199109aa7a44257e54'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-armv6'; 			sha256='f09294bd81119701f051733b45be487d55faa29d20fb9c54412975a6c7fd8696'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-armv7'; 			sha256='b1b592889f15f50ddc77685ed499c69599117e52240b196447cb82821da3f7f8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-aarch64'; 			sha256='664e8c532ac0dd54d14af4eb3fe4edce86ce27d970ec832a96b55bc2ef1dffdf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-ppc64le'; 			sha256='83c7cf5afffcc7944e23ba5c1c038aff4f2d760f08681d76b5271b66c9e2af5d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-riscv64'; 			sha256='0e6047d2b0f745f0bbb13d707cfb945295bf45e397e67ff756f8551043a1f5bc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-s390x'; 			sha256='381b5b77e6a91075e746167ac160062a1adf4d2a1121e433f1ca731ad08e2353'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:99164a65e1f060513df17430a291c788a5801cc0364c3cf0abaf9dd47e9d891c`  
		Last Modified: Thu, 05 Jun 2025 22:44:25 GMT  
		Size: 8.2 MB (8207469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a930b44823eb85c484514670f94fa0fadf7649aa34a692072e953b86cff998`  
		Last Modified: Thu, 05 Jun 2025 22:44:24 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89fad9bfb8f24abcb392b00c918762036dedf67787dc8a32b43aec570f3557f4`  
		Last Modified: Thu, 05 Jun 2025 22:44:28 GMT  
		Size: 20.1 MB (20083033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e993a5c36c8c13b622945142edd4bdf6b5d03775d8e91196856e50e0512650a`  
		Last Modified: Thu, 05 Jun 2025 22:44:27 GMT  
		Size: 21.3 MB (21290182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd58cf00359048abfc4f447feefe1373db7fd84dfe136fb751689b640844dd4b`  
		Last Modified: Thu, 05 Jun 2025 22:44:27 GMT  
		Size: 21.1 MB (21092192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bd9fc81ec33be8d5693955225a870888bf988fe35871af701d05810a7718b9`  
		Last Modified: Thu, 05 Jun 2025 22:44:26 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7dc70da6730815a90c517d43ed51312bc13932b65a288bbb8952f74df9d763a`  
		Last Modified: Thu, 05 Jun 2025 22:44:26 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2483cd3bb024143d65a844f930ffb5aa01cb0932a660abcaa0fcd68ddc0810`  
		Last Modified: Thu, 05 Jun 2025 22:44:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:232671b8d6c574d91a514e1073ddb00bd37e47ba17cfeefc0a4e078e392e4a00`  
		Last Modified: Thu, 05 Jun 2025 23:10:12 GMT  
		Size: 6.9 MB (6905563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8947c15ddd39c2ad279e9f5b5180a071aa948c04d248e2dcf4cb13585d9b47b8`  
		Last Modified: Thu, 05 Jun 2025 23:10:12 GMT  
		Size: 90.5 KB (90492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f7e4c6039fec8c4db67902febab1ae735352d758ffb76367f1e3e68a0b04b9d`  
		Last Modified: Thu, 05 Jun 2025 23:10:11 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:369f3cb80e373dbeee03da49ca69ce93f7c63f165704f929f0a040a4de56ed8e`  
		Last Modified: Thu, 05 Jun 2025 23:10:16 GMT  
		Size: 62.2 MB (62206624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7a0f373a71bb7b7e7a3be4baa2472d2850c4c9549c66b58e70a59a51b696ee`  
		Last Modified: Thu, 05 Jun 2025 23:10:11 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4dbe5b0725a180af25ab3d235ff1a32980b060cb2e263d0362d2baa5b73d858`  
		Last Modified: Thu, 05 Jun 2025 23:10:11 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f64aa3fd56b6d8303e9c2e032693fa69765ebe0ca402c8652e2e4be4bd9b8a2f`  
		Last Modified: Fri, 06 Jun 2025 00:13:41 GMT  
		Size: 993.3 KB (993270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9ac68c4bd4a09936531af4a567ee2065e73f798766ad456aef07aa86555af1`  
		Last Modified: Fri, 06 Jun 2025 00:13:48 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e79fe881b6f2ad1dc6bfdf95095a21b2a9400b5098d82da1be17d678d59226`  
		Last Modified: Fri, 06 Jun 2025 00:13:51 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91260bbdd96570e120d536ac928e3f77c4f858234e17f2ba9abb34a416109116`  
		Last Modified: Fri, 06 Jun 2025 02:08:01 GMT  
		Size: 17.6 MB (17585969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e31b397060352f80943b2c245dfb2b9014d8caaaefa979cba711e233412315`  
		Last Modified: Fri, 06 Jun 2025 00:13:54 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:0c4804528defa4555b2fadbd0044e12d0585c45979692580e6f2793f2e1eea66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.4 KB (30450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f33f1746b3d799c576bbbfea37de0b6f65df618daea063dddc5c07da8dfdd129`

```dockerfile
```

-	Layers:
	-	`sha256:4faecdc253478ec516ca521def628c3524f48440edfd20522bf779744323317c`  
		Last Modified: Fri, 06 Jun 2025 02:07:42 GMT  
		Size: 30.4 KB (30450 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.2-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:8f8a0cd4395a6ab286a0630f776e920239e6a01f6de484c2c23292ef76381bec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.5 MB (153539458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63acc824e3021e35e0fbed5808986ced5616f6da68905d273709d210e4a8ade6`
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
ENV DOCKER_COMPOSE_VERSION=2.37.0
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-x86_64'; 			sha256='e6e471b1e7bf0443592d3987dea6073f08db3e48ba0580199109aa7a44257e54'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-armv6'; 			sha256='f09294bd81119701f051733b45be487d55faa29d20fb9c54412975a6c7fd8696'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-armv7'; 			sha256='b1b592889f15f50ddc77685ed499c69599117e52240b196447cb82821da3f7f8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-aarch64'; 			sha256='664e8c532ac0dd54d14af4eb3fe4edce86ce27d970ec832a96b55bc2ef1dffdf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-ppc64le'; 			sha256='83c7cf5afffcc7944e23ba5c1c038aff4f2d760f08681d76b5271b66c9e2af5d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-riscv64'; 			sha256='0e6047d2b0f745f0bbb13d707cfb945295bf45e397e67ff756f8551043a1f5bc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-s390x'; 			sha256='381b5b77e6a91075e746167ac160062a1adf4d2a1121e433f1ca731ad08e2353'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:d38a584a1da307e1ac31b3fd852369ae8a8176a1baa2e783b7e72077d8318364`  
		Last Modified: Thu, 05 Jun 2025 23:07:15 GMT  
		Size: 8.2 MB (8229004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122792206f35c9e929c0c28c585fd195a84012e2d9bea1522c579660e013f3a5`  
		Last Modified: Thu, 05 Jun 2025 22:50:09 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e5a5c767d7cf27a922e7c99956942414d9e65453df45e3500e05adf80db19d`  
		Last Modified: Thu, 05 Jun 2025 23:07:16 GMT  
		Size: 18.9 MB (18902608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2fc5aa8a4cd07adf8f84bd323a5d415f9ca2c5c158b74f9382a0b369265fe2`  
		Last Modified: Thu, 05 Jun 2025 23:07:14 GMT  
		Size: 19.5 MB (19469838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba639502cad797b5554e57bbdc209e0c34366d2a40e0b51a2fa20dfce1a5b337`  
		Last Modified: Thu, 05 Jun 2025 23:07:13 GMT  
		Size: 19.3 MB (19344051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda0f9c86634c1a6b9059d179ed7e6ead432e9b8bcddfb0e980660053ccaef13`  
		Last Modified: Thu, 05 Jun 2025 22:50:11 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef143fe66bfdc5598981ca016d8e3884fde63a7858eb245932bb9745217e515a`  
		Last Modified: Thu, 05 Jun 2025 22:50:14 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69e2c1a5fdbb4dad365dd880c4621563cfe56068eb2e2541c0de0b1de1353676`  
		Last Modified: Thu, 05 Jun 2025 22:50:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b81c7606e8dcfe2fd4ea847b572c410188a1a61c1b7b1cda6ba28a64e97f159`  
		Last Modified: Thu, 05 Jun 2025 23:08:03 GMT  
		Size: 7.1 MB (7141567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e3f3d3d88e3f3363a8a38c1a676767483806a513d0552d4772a08e36257b1c`  
		Last Modified: Thu, 05 Jun 2025 23:08:04 GMT  
		Size: 99.6 KB (99634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abefbbf9a5b4d4cca3ef794fb554ab4acac7277079ebf9e0403cc7bb13360683`  
		Last Modified: Thu, 05 Jun 2025 23:08:03 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15537da54888f9d1dd7c82127a2affc9eaa21eec06bc9938606f42434884b95d`  
		Last Modified: Thu, 05 Jun 2025 23:08:12 GMT  
		Size: 57.2 MB (57168179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b5eff1498a195bfe23aea7da2bcdf6de5f313f4140c8715a32acf14d62d62cd`  
		Last Modified: Thu, 05 Jun 2025 23:08:04 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b4cb7df5229fcce96acdc6de42d98aa670436a784a0e59417a1584407b6bb8`  
		Last Modified: Thu, 05 Jun 2025 23:08:05 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b640b4b96d1a9d3b71ca7172efbfc7644661ed859290a1ef70f6efb5ae8646b6`  
		Last Modified: Thu, 05 Jun 2025 23:10:53 GMT  
		Size: 1.0 MB (1022994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3954fdd9c5b6656129957c10bf87d54fb3f5abd93ddb09065d380cb210a5077`  
		Last Modified: Thu, 05 Jun 2025 23:10:53 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4258e800a40d5a0144bf5289d6469124b4dcd57aa4a07ebfe0b4d51a68c8176e`  
		Last Modified: Thu, 05 Jun 2025 23:10:54 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603a03c83db0af7bcffad6809d5df5087ed7fc636e484590aa7baf42f257b2f2`  
		Last Modified: Thu, 05 Jun 2025 23:10:56 GMT  
		Size: 18.0 MB (18016150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ced063cb74820e91a874efbb44b00db32b5453e8cf96c0082bfe9265f119ad2`  
		Last Modified: Thu, 05 Jun 2025 23:14:26 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:84c0fd5fb3a3c2479438611da949f104f724c986c93c76c12541d88382d56a73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2929db2e0b226bded3985c6262f564307858288cba598d29b2ed0fa3c11f193`

```dockerfile
```

-	Layers:
	-	`sha256:fb773e2f1f91681ce7adadf4bf3c53895f7c309689fbb9874a70b1ce0fc12347`  
		Last Modified: Fri, 06 Jun 2025 02:07:46 GMT  
		Size: 30.6 KB (30621 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.2-windowsservercore`

```console
$ docker pull docker@sha256:0869de84e82e8707faa2238d565cea70e111fd670a2699eb7ed746f424fac81f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4061; amd64
	-	windows version 10.0.20348.3692; amd64

### `docker:28.2-windowsservercore` - windows version 10.0.26100.4061; amd64

```console
$ docker pull docker@sha256:25b529d707052438ef4b12929192d89e568c602554eff61b838530e3ba0862d0
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3496004439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5af2557ed6bf90b5a556401cda31f5e80c741723bd7d8d8dd85f75c9edb2beee`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 10 May 2025 01:13:32 GMT
RUN Install update 10.0.26100.4061
# Thu, 05 Jun 2025 22:49:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 05 Jun 2025 22:49:27 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 05 Jun 2025 22:49:29 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 05 Jun 2025 22:49:31 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.2.2.zip
# Thu, 05 Jun 2025 22:49:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 05 Jun 2025 22:49:45 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 05 Jun 2025 22:49:46 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Thu, 05 Jun 2025 22:49:48 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Thu, 05 Jun 2025 22:50:00 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 05 Jun 2025 22:50:02 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.0
# Thu, 05 Jun 2025 22:50:03 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-windows-x86_64.exe
# Thu, 05 Jun 2025 22:50:04 GMT
ENV DOCKER_COMPOSE_SHA256=5ddd1ff588eb7251381cf6257b9be44fbb92c02d984ccfc94b4280e8c33d0f8f
# Thu, 05 Jun 2025 22:50:15 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc834e13e71633c2d66ec6513d57c31a3157fc5933859d492ecf45fc8a7476c3`  
		Last Modified: Thu, 15 May 2025 19:25:03 GMT  
		Size: 1.2 GB (1215458626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90e49ef0e985b81e99d8b31a019b88aee89866bfb5c61dca46c36db719f75f72`  
		Last Modified: Thu, 05 Jun 2025 22:54:09 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35e4e87c87497c1f6d87a7f50d5b5d0f1d0cc7d219c6ce8eafc2a68e833177e3`  
		Last Modified: Thu, 05 Jun 2025 22:54:10 GMT  
		Size: 389.0 KB (389032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc34a02ab083801559a9993b8b75ebf1889f6ee4406ace24d67068a1db6d394`  
		Last Modified: Thu, 05 Jun 2025 22:54:09 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460eb4eabe732c14d4ba4780e91bfae9ce2f88f06d471caa6eaec23d33259db7`  
		Last Modified: Thu, 05 Jun 2025 22:54:10 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48921f27b31821d44d89e3376996fbcef78628b7c234b417f58afb6186212ee6`  
		Last Modified: Thu, 05 Jun 2025 22:54:12 GMT  
		Size: 20.5 MB (20482824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3fa9bcfc9c100af95e701bc8db63daa6762e21200bcbcfeacf780ceff4ac0a5`  
		Last Modified: Thu, 05 Jun 2025 23:02:29 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f73ddc322ec88bd49ef2ed8da74c0a7037d94bb1649764c3a424b89b9ba72f5`  
		Last Modified: Thu, 05 Jun 2025 23:02:32 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bee619612444d3cd3f98593f7912090ea8ebeaa7537f88e6ef0df6381f43660`  
		Last Modified: Thu, 05 Jun 2025 23:08:02 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aab9f1404ae5f4d3919e9d9b3989dc637b5461c0d61a0a8914464ac3efef61c`  
		Last Modified: Thu, 05 Jun 2025 23:08:03 GMT  
		Size: 22.3 MB (22293165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ffe3877611fd0a573d09a62990e99adc779e2ecfb7a0a99352b6097f1aedfa`  
		Last Modified: Thu, 05 Jun 2025 23:02:39 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c74c3be6ed0d6a50023b6597b4c73f7c8a6edf1bf15689254c3030e49379b3b`  
		Last Modified: Thu, 05 Jun 2025 23:02:42 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4546e8211fc088c3925f2b673074dc5a6d27527caf92983c56600ac02ceec30`  
		Last Modified: Thu, 05 Jun 2025 23:02:45 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:281c5b22c80200de8cb5cd27b59777a1a0c02818b3d09d937cc6ff99e29f8305`  
		Last Modified: Thu, 05 Jun 2025 23:08:07 GMT  
		Size: 22.1 MB (22061869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28.2-windowsservercore` - windows version 10.0.20348.3692; amd64

```console
$ docker pull docker@sha256:213ffc624913105fa7ee59720002de6a40b9768db21a5d09ec3f292a45573596
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2338596324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af09b10c562d5ce89c47cb4db81986d086849844eb9ea5e334925da4e6e60501`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Thu, 05 Jun 2025 22:44:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 05 Jun 2025 22:46:25 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 05 Jun 2025 22:46:26 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 05 Jun 2025 22:46:27 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.2.2.zip
# Thu, 05 Jun 2025 22:46:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 05 Jun 2025 22:46:51 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 05 Jun 2025 22:46:52 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Thu, 05 Jun 2025 22:46:52 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Thu, 05 Jun 2025 22:47:01 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 05 Jun 2025 22:47:02 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.0
# Thu, 05 Jun 2025 22:47:02 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-windows-x86_64.exe
# Thu, 05 Jun 2025 22:47:03 GMT
ENV DOCKER_COMPOSE_SHA256=5ddd1ff588eb7251381cf6257b9be44fbb92c02d984ccfc94b4280e8c33d0f8f
# Thu, 05 Jun 2025 22:47:14 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Thu, 15 May 2025 19:25:06 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69792782d0247e3e22c67f6096a5c5ac4096e3039e9902b31095ada21a3a3992`  
		Last Modified: Thu, 05 Jun 2025 22:47:55 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1528406f9d6a747555a27165ae52a9ade5da9bafe09faedc813fc9978410ebb1`  
		Last Modified: Thu, 05 Jun 2025 22:47:57 GMT  
		Size: 347.0 KB (347048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44599b0e57d9512be310c8211fc1db3c2b2f26d186b1f4fa5f41cb3239e83e08`  
		Last Modified: Thu, 05 Jun 2025 22:47:57 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5946a2c5ebb15f702288c926ad33ec3e48dc514e959828483bf2515343b8164`  
		Last Modified: Thu, 05 Jun 2025 22:47:58 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5950ebf7245c1e012f8bedfc8e4f944900fbb4429057e997700cbfc430e71db`  
		Last Modified: Thu, 05 Jun 2025 23:08:02 GMT  
		Size: 20.4 MB (20407814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e4979217510eb7de8d35cf3a6a4ea0d48a38fccd55990459ede40e90555a91`  
		Last Modified: Thu, 05 Jun 2025 22:50:52 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bee3bf1d9c1e36c3c62244bbf0b25abd4d3848230da86f8eb7ab9e87bfcce25`  
		Last Modified: Thu, 05 Jun 2025 22:50:55 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dd6d131f13751da51b0a0640902b80152d4626d65b68249d48306530f6af710`  
		Last Modified: Thu, 05 Jun 2025 22:50:58 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809edd0f0043024cc3f263278554b9d43f0af10b1ff965b9e755e7f504cc9448`  
		Last Modified: Thu, 05 Jun 2025 23:08:01 GMT  
		Size: 22.2 MB (22218481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3644edf37145bf3243218f63e04734da0ee41b17a3db4580ac428852159a95b4`  
		Last Modified: Thu, 05 Jun 2025 22:51:01 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f3f405f8fc75b4dbb8e568437773842a367615ed3dbe41b6be647fdbcb3756e`  
		Last Modified: Thu, 05 Jun 2025 22:51:04 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4701c8fc8cca7fb8a5a1d7d575fa186deff56c45e248857b3ed475c698ed20c8`  
		Last Modified: Thu, 05 Jun 2025 22:51:08 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b4da056663f41259b84270c9d8dc6b48fb2b7d53922c07335a68a8dc178b488`  
		Last Modified: Thu, 05 Jun 2025 23:08:02 GMT  
		Size: 22.0 MB (21983289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.2-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:bc2b0152ecb9f33a768c3b3a7ba14c8206d2b7f60077c28a3546b40efb6dd9c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `docker:28.2-windowsservercore-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull docker@sha256:213ffc624913105fa7ee59720002de6a40b9768db21a5d09ec3f292a45573596
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2338596324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af09b10c562d5ce89c47cb4db81986d086849844eb9ea5e334925da4e6e60501`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Thu, 05 Jun 2025 22:44:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 05 Jun 2025 22:46:25 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 05 Jun 2025 22:46:26 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 05 Jun 2025 22:46:27 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.2.2.zip
# Thu, 05 Jun 2025 22:46:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 05 Jun 2025 22:46:51 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 05 Jun 2025 22:46:52 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Thu, 05 Jun 2025 22:46:52 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Thu, 05 Jun 2025 22:47:01 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 05 Jun 2025 22:47:02 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.0
# Thu, 05 Jun 2025 22:47:02 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-windows-x86_64.exe
# Thu, 05 Jun 2025 22:47:03 GMT
ENV DOCKER_COMPOSE_SHA256=5ddd1ff588eb7251381cf6257b9be44fbb92c02d984ccfc94b4280e8c33d0f8f
# Thu, 05 Jun 2025 22:47:14 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Thu, 15 May 2025 19:25:06 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69792782d0247e3e22c67f6096a5c5ac4096e3039e9902b31095ada21a3a3992`  
		Last Modified: Thu, 05 Jun 2025 22:47:55 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1528406f9d6a747555a27165ae52a9ade5da9bafe09faedc813fc9978410ebb1`  
		Last Modified: Thu, 05 Jun 2025 22:47:57 GMT  
		Size: 347.0 KB (347048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44599b0e57d9512be310c8211fc1db3c2b2f26d186b1f4fa5f41cb3239e83e08`  
		Last Modified: Thu, 05 Jun 2025 22:47:57 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5946a2c5ebb15f702288c926ad33ec3e48dc514e959828483bf2515343b8164`  
		Last Modified: Thu, 05 Jun 2025 22:47:58 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5950ebf7245c1e012f8bedfc8e4f944900fbb4429057e997700cbfc430e71db`  
		Last Modified: Thu, 05 Jun 2025 23:08:02 GMT  
		Size: 20.4 MB (20407814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e4979217510eb7de8d35cf3a6a4ea0d48a38fccd55990459ede40e90555a91`  
		Last Modified: Thu, 05 Jun 2025 22:50:52 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bee3bf1d9c1e36c3c62244bbf0b25abd4d3848230da86f8eb7ab9e87bfcce25`  
		Last Modified: Thu, 05 Jun 2025 22:50:55 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dd6d131f13751da51b0a0640902b80152d4626d65b68249d48306530f6af710`  
		Last Modified: Thu, 05 Jun 2025 22:50:58 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809edd0f0043024cc3f263278554b9d43f0af10b1ff965b9e755e7f504cc9448`  
		Last Modified: Thu, 05 Jun 2025 23:08:01 GMT  
		Size: 22.2 MB (22218481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3644edf37145bf3243218f63e04734da0ee41b17a3db4580ac428852159a95b4`  
		Last Modified: Thu, 05 Jun 2025 22:51:01 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f3f405f8fc75b4dbb8e568437773842a367615ed3dbe41b6be647fdbcb3756e`  
		Last Modified: Thu, 05 Jun 2025 22:51:04 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4701c8fc8cca7fb8a5a1d7d575fa186deff56c45e248857b3ed475c698ed20c8`  
		Last Modified: Thu, 05 Jun 2025 22:51:08 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b4da056663f41259b84270c9d8dc6b48fb2b7d53922c07335a68a8dc178b488`  
		Last Modified: Thu, 05 Jun 2025 23:08:02 GMT  
		Size: 22.0 MB (21983289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.2-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:5f0071c24f8a2426413b698206c5a415be20f1024483d31ea54cd904e41465df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4061; amd64

### `docker:28.2-windowsservercore-ltsc2025` - windows version 10.0.26100.4061; amd64

```console
$ docker pull docker@sha256:25b529d707052438ef4b12929192d89e568c602554eff61b838530e3ba0862d0
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3496004439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5af2557ed6bf90b5a556401cda31f5e80c741723bd7d8d8dd85f75c9edb2beee`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 10 May 2025 01:13:32 GMT
RUN Install update 10.0.26100.4061
# Thu, 05 Jun 2025 22:49:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 05 Jun 2025 22:49:27 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 05 Jun 2025 22:49:29 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 05 Jun 2025 22:49:31 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.2.2.zip
# Thu, 05 Jun 2025 22:49:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 05 Jun 2025 22:49:45 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 05 Jun 2025 22:49:46 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Thu, 05 Jun 2025 22:49:48 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Thu, 05 Jun 2025 22:50:00 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 05 Jun 2025 22:50:02 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.0
# Thu, 05 Jun 2025 22:50:03 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-windows-x86_64.exe
# Thu, 05 Jun 2025 22:50:04 GMT
ENV DOCKER_COMPOSE_SHA256=5ddd1ff588eb7251381cf6257b9be44fbb92c02d984ccfc94b4280e8c33d0f8f
# Thu, 05 Jun 2025 22:50:15 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc834e13e71633c2d66ec6513d57c31a3157fc5933859d492ecf45fc8a7476c3`  
		Last Modified: Thu, 15 May 2025 19:25:03 GMT  
		Size: 1.2 GB (1215458626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90e49ef0e985b81e99d8b31a019b88aee89866bfb5c61dca46c36db719f75f72`  
		Last Modified: Thu, 05 Jun 2025 22:54:09 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35e4e87c87497c1f6d87a7f50d5b5d0f1d0cc7d219c6ce8eafc2a68e833177e3`  
		Last Modified: Thu, 05 Jun 2025 22:54:10 GMT  
		Size: 389.0 KB (389032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc34a02ab083801559a9993b8b75ebf1889f6ee4406ace24d67068a1db6d394`  
		Last Modified: Thu, 05 Jun 2025 22:54:09 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460eb4eabe732c14d4ba4780e91bfae9ce2f88f06d471caa6eaec23d33259db7`  
		Last Modified: Thu, 05 Jun 2025 22:54:10 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48921f27b31821d44d89e3376996fbcef78628b7c234b417f58afb6186212ee6`  
		Last Modified: Thu, 05 Jun 2025 22:54:12 GMT  
		Size: 20.5 MB (20482824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3fa9bcfc9c100af95e701bc8db63daa6762e21200bcbcfeacf780ceff4ac0a5`  
		Last Modified: Thu, 05 Jun 2025 23:02:29 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f73ddc322ec88bd49ef2ed8da74c0a7037d94bb1649764c3a424b89b9ba72f5`  
		Last Modified: Thu, 05 Jun 2025 23:02:32 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bee619612444d3cd3f98593f7912090ea8ebeaa7537f88e6ef0df6381f43660`  
		Last Modified: Thu, 05 Jun 2025 23:08:02 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aab9f1404ae5f4d3919e9d9b3989dc637b5461c0d61a0a8914464ac3efef61c`  
		Last Modified: Thu, 05 Jun 2025 23:08:03 GMT  
		Size: 22.3 MB (22293165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ffe3877611fd0a573d09a62990e99adc779e2ecfb7a0a99352b6097f1aedfa`  
		Last Modified: Thu, 05 Jun 2025 23:02:39 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c74c3be6ed0d6a50023b6597b4c73f7c8a6edf1bf15689254c3030e49379b3b`  
		Last Modified: Thu, 05 Jun 2025 23:02:42 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4546e8211fc088c3925f2b673074dc5a6d27527caf92983c56600ac02ceec30`  
		Last Modified: Thu, 05 Jun 2025 23:02:45 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:281c5b22c80200de8cb5cd27b59777a1a0c02818b3d09d937cc6ff99e29f8305`  
		Last Modified: Thu, 05 Jun 2025 23:08:07 GMT  
		Size: 22.1 MB (22061869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.2.2`

```console
$ docker pull docker@sha256:d4668861cabc1691635d98e827a81cfa834a416f8fe0f4efc609f9f806d86d82
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
$ docker pull docker@sha256:8c9502da312e1595a696775bea7d4e6e7b18102d62c413b43f9d3f9d353eb323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.7 MB (143680550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e1cee4b3a3c0bfea53084cb7708d24f3314dd7ce46631888127d8037a4158d9`
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
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99164a65e1f060513df17430a291c788a5801cc0364c3cf0abaf9dd47e9d891c`  
		Last Modified: Thu, 05 Jun 2025 22:44:25 GMT  
		Size: 8.2 MB (8207469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a930b44823eb85c484514670f94fa0fadf7649aa34a692072e953b86cff998`  
		Last Modified: Thu, 05 Jun 2025 22:44:24 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89fad9bfb8f24abcb392b00c918762036dedf67787dc8a32b43aec570f3557f4`  
		Last Modified: Thu, 05 Jun 2025 22:44:28 GMT  
		Size: 20.1 MB (20083033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e993a5c36c8c13b622945142edd4bdf6b5d03775d8e91196856e50e0512650a`  
		Last Modified: Thu, 05 Jun 2025 22:44:27 GMT  
		Size: 21.3 MB (21290182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd58cf00359048abfc4f447feefe1373db7fd84dfe136fb751689b640844dd4b`  
		Last Modified: Thu, 05 Jun 2025 22:44:27 GMT  
		Size: 21.1 MB (21092192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bd9fc81ec33be8d5693955225a870888bf988fe35871af701d05810a7718b9`  
		Last Modified: Thu, 05 Jun 2025 22:44:26 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7dc70da6730815a90c517d43ed51312bc13932b65a288bbb8952f74df9d763a`  
		Last Modified: Thu, 05 Jun 2025 22:44:26 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2483cd3bb024143d65a844f930ffb5aa01cb0932a660abcaa0fcd68ddc0810`  
		Last Modified: Thu, 05 Jun 2025 22:44:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:232671b8d6c574d91a514e1073ddb00bd37e47ba17cfeefc0a4e078e392e4a00`  
		Last Modified: Thu, 05 Jun 2025 23:10:12 GMT  
		Size: 6.9 MB (6905563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8947c15ddd39c2ad279e9f5b5180a071aa948c04d248e2dcf4cb13585d9b47b8`  
		Last Modified: Thu, 05 Jun 2025 23:10:12 GMT  
		Size: 90.5 KB (90492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f7e4c6039fec8c4db67902febab1ae735352d758ffb76367f1e3e68a0b04b9d`  
		Last Modified: Thu, 05 Jun 2025 23:10:11 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:369f3cb80e373dbeee03da49ca69ce93f7c63f165704f929f0a040a4de56ed8e`  
		Last Modified: Thu, 05 Jun 2025 23:10:16 GMT  
		Size: 62.2 MB (62206624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7a0f373a71bb7b7e7a3be4baa2472d2850c4c9549c66b58e70a59a51b696ee`  
		Last Modified: Thu, 05 Jun 2025 23:10:11 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4dbe5b0725a180af25ab3d235ff1a32980b060cb2e263d0362d2baa5b73d858`  
		Last Modified: Thu, 05 Jun 2025 23:10:11 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2.2` - unknown; unknown

```console
$ docker pull docker@sha256:227416a58467a90d61d00571bea5da05930524bab4cb82350e892b245e0d2e6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:125d3c52d0be767b8d0f76f67d0acd7adb2635cac747795240c64e1792d2f95e`

```dockerfile
```

-	Layers:
	-	`sha256:06c3e6cf1c5d56e7cb2fe109c0aa850bd00d57c61602118e103dbffd829369a6`  
		Last Modified: Fri, 06 Jun 2025 02:07:30 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.2.2` - linux; arm variant v6

```console
$ docker pull docker@sha256:7920dd4fb3d5c69b32f5a8fdad7bc083113e1eb057daf9551d3bec928642d2d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134721385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f04c9bfb20a7623a34894618839c13fd1bf730153cc94bc61f9b9d60dbc8dc6`
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
	-	`sha256:b18e44e663f768131c50d79640817a860ca8c20877f41bfc7e788ede7276f121`  
		Last Modified: Thu, 05 Jun 2025 22:44:12 GMT  
		Size: 19.8 MB (19834728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b7cf9bb5cb3a10f219b307b2ff9f67f54ab05208492bbe13e06a74ca78e54d`  
		Last Modified: Thu, 05 Jun 2025 22:44:13 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7393d30c6bcbe757d4919545933b9de1b6f48c9a46a3ed4a0ae9281792fbd51`  
		Last Modified: Thu, 05 Jun 2025 22:51:09 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe877f07f4d94074494db81efb5c5e890ab77b7ce09fa3952f972953a436545d`  
		Last Modified: Thu, 05 Jun 2025 22:51:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9526e4c6fe05aa09bd1848ecd6d91b389e046a9da41b839528a0f104ba7e6b`  
		Last Modified: Fri, 06 Jun 2025 01:05:46 GMT  
		Size: 7.2 MB (7230299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7741447d38cadd971edc0ea8d19ec995a5929dad7df81e579060cf95a0a66e0e`  
		Last Modified: Thu, 05 Jun 2025 23:14:04 GMT  
		Size: 90.1 KB (90052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eabb360d9297b2af61c701c3a02f961b3210cdb6c3a4119c7a03d703fd26c6b`  
		Last Modified: Thu, 05 Jun 2025 23:14:08 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c250f611b5a5d3e13bac22e1a236ffb37d10345c511e869b539265c145ebc1`  
		Last Modified: Fri, 06 Jun 2025 01:05:49 GMT  
		Size: 57.9 MB (57897379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b907cd35da6b2acf22cf12c6849885f91becbd5836560543543e4df0b7e4ede`  
		Last Modified: Thu, 05 Jun 2025 23:14:11 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b319c010975a1f690900a80187653a3834b1a65ec15f73ccd7edf9c103bc8eb`  
		Last Modified: Thu, 05 Jun 2025 23:14:13 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2.2` - unknown; unknown

```console
$ docker pull docker@sha256:918e10532d5d49ad3d988b0f42404e4e65b4ff96c9f47d1de4c3bb238edfaf26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc5e34ba8e1767c238c0ca97f2315e8d15bc7d875be15383aa1599e4d71188d2`

```dockerfile
```

-	Layers:
	-	`sha256:21bc1dae29bbc15eda321d47bbd61a416fa4a9175b7a84d90debd5063a161db7`  
		Last Modified: Fri, 06 Jun 2025 02:07:34 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.2.2` - linux; arm variant v7

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

### `docker:28.2.2` - unknown; unknown

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

### `docker:28.2.2` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:0de688aa942b05b1ca86e80e9e87a92cab8690ca4d00819b777253ca12fd05b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.5 MB (134498975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e07111220cfca840da6105d81020ea43df6b1c90921916a1cd65417e1101d6e`
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
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38a584a1da307e1ac31b3fd852369ae8a8176a1baa2e783b7e72077d8318364`  
		Last Modified: Thu, 05 Jun 2025 23:07:15 GMT  
		Size: 8.2 MB (8229004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122792206f35c9e929c0c28c585fd195a84012e2d9bea1522c579660e013f3a5`  
		Last Modified: Thu, 05 Jun 2025 22:50:09 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e5a5c767d7cf27a922e7c99956942414d9e65453df45e3500e05adf80db19d`  
		Last Modified: Thu, 05 Jun 2025 23:07:16 GMT  
		Size: 18.9 MB (18902608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2fc5aa8a4cd07adf8f84bd323a5d415f9ca2c5c158b74f9382a0b369265fe2`  
		Last Modified: Thu, 05 Jun 2025 23:07:14 GMT  
		Size: 19.5 MB (19469838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba639502cad797b5554e57bbdc209e0c34366d2a40e0b51a2fa20dfce1a5b337`  
		Last Modified: Thu, 05 Jun 2025 23:07:13 GMT  
		Size: 19.3 MB (19344051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda0f9c86634c1a6b9059d179ed7e6ead432e9b8bcddfb0e980660053ccaef13`  
		Last Modified: Thu, 05 Jun 2025 22:50:11 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef143fe66bfdc5598981ca016d8e3884fde63a7858eb245932bb9745217e515a`  
		Last Modified: Thu, 05 Jun 2025 22:50:14 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69e2c1a5fdbb4dad365dd880c4621563cfe56068eb2e2541c0de0b1de1353676`  
		Last Modified: Thu, 05 Jun 2025 22:50:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b81c7606e8dcfe2fd4ea847b572c410188a1a61c1b7b1cda6ba28a64e97f159`  
		Last Modified: Thu, 05 Jun 2025 23:08:03 GMT  
		Size: 7.1 MB (7141567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e3f3d3d88e3f3363a8a38c1a676767483806a513d0552d4772a08e36257b1c`  
		Last Modified: Thu, 05 Jun 2025 23:08:04 GMT  
		Size: 99.6 KB (99634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abefbbf9a5b4d4cca3ef794fb554ab4acac7277079ebf9e0403cc7bb13360683`  
		Last Modified: Thu, 05 Jun 2025 23:08:03 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15537da54888f9d1dd7c82127a2affc9eaa21eec06bc9938606f42434884b95d`  
		Last Modified: Thu, 05 Jun 2025 23:08:12 GMT  
		Size: 57.2 MB (57168179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b5eff1498a195bfe23aea7da2bcdf6de5f313f4140c8715a32acf14d62d62cd`  
		Last Modified: Thu, 05 Jun 2025 23:08:04 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b4cb7df5229fcce96acdc6de42d98aa670436a784a0e59417a1584407b6bb8`  
		Last Modified: Thu, 05 Jun 2025 23:08:05 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2.2` - unknown; unknown

```console
$ docker pull docker@sha256:5cad50c6b3b442444f6651f5c8b4d33a9f66b976fd04acda0c3b54328ac14556
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeded159db72e188c1c71b241cf1c67644293d460aa0a7d23d1fd5424dc510de`

```dockerfile
```

-	Layers:
	-	`sha256:431922ef17f88491b0a295b18dd805f113ce40a500def3af5b4651f0b1b77da1`  
		Last Modified: Fri, 06 Jun 2025 02:07:41 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.2.2-alpine3.22`

```console
$ docker pull docker@sha256:d4668861cabc1691635d98e827a81cfa834a416f8fe0f4efc609f9f806d86d82
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
$ docker pull docker@sha256:8c9502da312e1595a696775bea7d4e6e7b18102d62c413b43f9d3f9d353eb323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.7 MB (143680550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e1cee4b3a3c0bfea53084cb7708d24f3314dd7ce46631888127d8037a4158d9`
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
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99164a65e1f060513df17430a291c788a5801cc0364c3cf0abaf9dd47e9d891c`  
		Last Modified: Thu, 05 Jun 2025 22:44:25 GMT  
		Size: 8.2 MB (8207469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a930b44823eb85c484514670f94fa0fadf7649aa34a692072e953b86cff998`  
		Last Modified: Thu, 05 Jun 2025 22:44:24 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89fad9bfb8f24abcb392b00c918762036dedf67787dc8a32b43aec570f3557f4`  
		Last Modified: Thu, 05 Jun 2025 22:44:28 GMT  
		Size: 20.1 MB (20083033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e993a5c36c8c13b622945142edd4bdf6b5d03775d8e91196856e50e0512650a`  
		Last Modified: Thu, 05 Jun 2025 22:44:27 GMT  
		Size: 21.3 MB (21290182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd58cf00359048abfc4f447feefe1373db7fd84dfe136fb751689b640844dd4b`  
		Last Modified: Thu, 05 Jun 2025 22:44:27 GMT  
		Size: 21.1 MB (21092192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bd9fc81ec33be8d5693955225a870888bf988fe35871af701d05810a7718b9`  
		Last Modified: Thu, 05 Jun 2025 22:44:26 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7dc70da6730815a90c517d43ed51312bc13932b65a288bbb8952f74df9d763a`  
		Last Modified: Thu, 05 Jun 2025 22:44:26 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2483cd3bb024143d65a844f930ffb5aa01cb0932a660abcaa0fcd68ddc0810`  
		Last Modified: Thu, 05 Jun 2025 22:44:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:232671b8d6c574d91a514e1073ddb00bd37e47ba17cfeefc0a4e078e392e4a00`  
		Last Modified: Thu, 05 Jun 2025 23:10:12 GMT  
		Size: 6.9 MB (6905563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8947c15ddd39c2ad279e9f5b5180a071aa948c04d248e2dcf4cb13585d9b47b8`  
		Last Modified: Thu, 05 Jun 2025 23:10:12 GMT  
		Size: 90.5 KB (90492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f7e4c6039fec8c4db67902febab1ae735352d758ffb76367f1e3e68a0b04b9d`  
		Last Modified: Thu, 05 Jun 2025 23:10:11 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:369f3cb80e373dbeee03da49ca69ce93f7c63f165704f929f0a040a4de56ed8e`  
		Last Modified: Thu, 05 Jun 2025 23:10:16 GMT  
		Size: 62.2 MB (62206624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7a0f373a71bb7b7e7a3be4baa2472d2850c4c9549c66b58e70a59a51b696ee`  
		Last Modified: Thu, 05 Jun 2025 23:10:11 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4dbe5b0725a180af25ab3d235ff1a32980b060cb2e263d0362d2baa5b73d858`  
		Last Modified: Thu, 05 Jun 2025 23:10:11 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2.2-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:227416a58467a90d61d00571bea5da05930524bab4cb82350e892b245e0d2e6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:125d3c52d0be767b8d0f76f67d0acd7adb2635cac747795240c64e1792d2f95e`

```dockerfile
```

-	Layers:
	-	`sha256:06c3e6cf1c5d56e7cb2fe109c0aa850bd00d57c61602118e103dbffd829369a6`  
		Last Modified: Fri, 06 Jun 2025 02:07:30 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.2.2-alpine3.22` - linux; arm variant v6

```console
$ docker pull docker@sha256:7920dd4fb3d5c69b32f5a8fdad7bc083113e1eb057daf9551d3bec928642d2d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134721385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f04c9bfb20a7623a34894618839c13fd1bf730153cc94bc61f9b9d60dbc8dc6`
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
	-	`sha256:b18e44e663f768131c50d79640817a860ca8c20877f41bfc7e788ede7276f121`  
		Last Modified: Thu, 05 Jun 2025 22:44:12 GMT  
		Size: 19.8 MB (19834728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b7cf9bb5cb3a10f219b307b2ff9f67f54ab05208492bbe13e06a74ca78e54d`  
		Last Modified: Thu, 05 Jun 2025 22:44:13 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7393d30c6bcbe757d4919545933b9de1b6f48c9a46a3ed4a0ae9281792fbd51`  
		Last Modified: Thu, 05 Jun 2025 22:51:09 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe877f07f4d94074494db81efb5c5e890ab77b7ce09fa3952f972953a436545d`  
		Last Modified: Thu, 05 Jun 2025 22:51:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9526e4c6fe05aa09bd1848ecd6d91b389e046a9da41b839528a0f104ba7e6b`  
		Last Modified: Fri, 06 Jun 2025 01:05:46 GMT  
		Size: 7.2 MB (7230299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7741447d38cadd971edc0ea8d19ec995a5929dad7df81e579060cf95a0a66e0e`  
		Last Modified: Thu, 05 Jun 2025 23:14:04 GMT  
		Size: 90.1 KB (90052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eabb360d9297b2af61c701c3a02f961b3210cdb6c3a4119c7a03d703fd26c6b`  
		Last Modified: Thu, 05 Jun 2025 23:14:08 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c250f611b5a5d3e13bac22e1a236ffb37d10345c511e869b539265c145ebc1`  
		Last Modified: Fri, 06 Jun 2025 01:05:49 GMT  
		Size: 57.9 MB (57897379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b907cd35da6b2acf22cf12c6849885f91becbd5836560543543e4df0b7e4ede`  
		Last Modified: Thu, 05 Jun 2025 23:14:11 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b319c010975a1f690900a80187653a3834b1a65ec15f73ccd7edf9c103bc8eb`  
		Last Modified: Thu, 05 Jun 2025 23:14:13 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2.2-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:918e10532d5d49ad3d988b0f42404e4e65b4ff96c9f47d1de4c3bb238edfaf26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc5e34ba8e1767c238c0ca97f2315e8d15bc7d875be15383aa1599e4d71188d2`

```dockerfile
```

-	Layers:
	-	`sha256:21bc1dae29bbc15eda321d47bbd61a416fa4a9175b7a84d90debd5063a161db7`  
		Last Modified: Fri, 06 Jun 2025 02:07:34 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.2.2-alpine3.22` - linux; arm variant v7

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

### `docker:28.2.2-alpine3.22` - unknown; unknown

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

### `docker:28.2.2-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:0de688aa942b05b1ca86e80e9e87a92cab8690ca4d00819b777253ca12fd05b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.5 MB (134498975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e07111220cfca840da6105d81020ea43df6b1c90921916a1cd65417e1101d6e`
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
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38a584a1da307e1ac31b3fd852369ae8a8176a1baa2e783b7e72077d8318364`  
		Last Modified: Thu, 05 Jun 2025 23:07:15 GMT  
		Size: 8.2 MB (8229004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122792206f35c9e929c0c28c585fd195a84012e2d9bea1522c579660e013f3a5`  
		Last Modified: Thu, 05 Jun 2025 22:50:09 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e5a5c767d7cf27a922e7c99956942414d9e65453df45e3500e05adf80db19d`  
		Last Modified: Thu, 05 Jun 2025 23:07:16 GMT  
		Size: 18.9 MB (18902608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2fc5aa8a4cd07adf8f84bd323a5d415f9ca2c5c158b74f9382a0b369265fe2`  
		Last Modified: Thu, 05 Jun 2025 23:07:14 GMT  
		Size: 19.5 MB (19469838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba639502cad797b5554e57bbdc209e0c34366d2a40e0b51a2fa20dfce1a5b337`  
		Last Modified: Thu, 05 Jun 2025 23:07:13 GMT  
		Size: 19.3 MB (19344051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda0f9c86634c1a6b9059d179ed7e6ead432e9b8bcddfb0e980660053ccaef13`  
		Last Modified: Thu, 05 Jun 2025 22:50:11 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef143fe66bfdc5598981ca016d8e3884fde63a7858eb245932bb9745217e515a`  
		Last Modified: Thu, 05 Jun 2025 22:50:14 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69e2c1a5fdbb4dad365dd880c4621563cfe56068eb2e2541c0de0b1de1353676`  
		Last Modified: Thu, 05 Jun 2025 22:50:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b81c7606e8dcfe2fd4ea847b572c410188a1a61c1b7b1cda6ba28a64e97f159`  
		Last Modified: Thu, 05 Jun 2025 23:08:03 GMT  
		Size: 7.1 MB (7141567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e3f3d3d88e3f3363a8a38c1a676767483806a513d0552d4772a08e36257b1c`  
		Last Modified: Thu, 05 Jun 2025 23:08:04 GMT  
		Size: 99.6 KB (99634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abefbbf9a5b4d4cca3ef794fb554ab4acac7277079ebf9e0403cc7bb13360683`  
		Last Modified: Thu, 05 Jun 2025 23:08:03 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15537da54888f9d1dd7c82127a2affc9eaa21eec06bc9938606f42434884b95d`  
		Last Modified: Thu, 05 Jun 2025 23:08:12 GMT  
		Size: 57.2 MB (57168179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b5eff1498a195bfe23aea7da2bcdf6de5f313f4140c8715a32acf14d62d62cd`  
		Last Modified: Thu, 05 Jun 2025 23:08:04 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b4cb7df5229fcce96acdc6de42d98aa670436a784a0e59417a1584407b6bb8`  
		Last Modified: Thu, 05 Jun 2025 23:08:05 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2.2-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:5cad50c6b3b442444f6651f5c8b4d33a9f66b976fd04acda0c3b54328ac14556
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeded159db72e188c1c71b241cf1c67644293d460aa0a7d23d1fd5424dc510de`

```dockerfile
```

-	Layers:
	-	`sha256:431922ef17f88491b0a295b18dd805f113ce40a500def3af5b4651f0b1b77da1`  
		Last Modified: Fri, 06 Jun 2025 02:07:41 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.2.2-cli`

```console
$ docker pull docker@sha256:c2e49a065e45c462dda70b65b1a50a74c75804091fae15b7e4fbec6b114996d1
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
$ docker pull docker@sha256:29ac2aff504532e72efca1a58f229c0e05f928828e62156fb304d391e82f7f49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74471875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd02548899f2c001be05193b91d116511f57fb7e8f5cec5f7b58cce36fed0303`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99164a65e1f060513df17430a291c788a5801cc0364c3cf0abaf9dd47e9d891c`  
		Last Modified: Thu, 05 Jun 2025 22:44:25 GMT  
		Size: 8.2 MB (8207469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a930b44823eb85c484514670f94fa0fadf7649aa34a692072e953b86cff998`  
		Last Modified: Thu, 05 Jun 2025 22:44:24 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89fad9bfb8f24abcb392b00c918762036dedf67787dc8a32b43aec570f3557f4`  
		Last Modified: Thu, 05 Jun 2025 22:44:28 GMT  
		Size: 20.1 MB (20083033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e993a5c36c8c13b622945142edd4bdf6b5d03775d8e91196856e50e0512650a`  
		Last Modified: Thu, 05 Jun 2025 22:44:27 GMT  
		Size: 21.3 MB (21290182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd58cf00359048abfc4f447feefe1373db7fd84dfe136fb751689b640844dd4b`  
		Last Modified: Thu, 05 Jun 2025 22:44:27 GMT  
		Size: 21.1 MB (21092192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bd9fc81ec33be8d5693955225a870888bf988fe35871af701d05810a7718b9`  
		Last Modified: Thu, 05 Jun 2025 22:44:26 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7dc70da6730815a90c517d43ed51312bc13932b65a288bbb8952f74df9d763a`  
		Last Modified: Thu, 05 Jun 2025 22:44:26 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2483cd3bb024143d65a844f930ffb5aa01cb0932a660abcaa0fcd68ddc0810`  
		Last Modified: Thu, 05 Jun 2025 22:44:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2.2-cli` - unknown; unknown

```console
$ docker pull docker@sha256:e3c92c354188244e1e651ab7c9384326a36594dbf3e27427328aa209be1c1e7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de64116684520fb5473d5fee53d9f710a283fa5926d23334bbeb9a13ece30127`

```dockerfile
```

-	Layers:
	-	`sha256:9f1baaf1f40a67141a0489af913841dd7e9427be207fe398702581c569cd1c20`  
		Last Modified: Thu, 05 Jun 2025 23:07:43 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.2.2-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:6f76795bf488400672b314ad95bc4add17d3871c369454a410a6072cd1f7fe6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69497654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4905167d30157f311983a0f0fbb87d96647db6c5478ae0071e5e9d717c22247`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
	-	`sha256:b18e44e663f768131c50d79640817a860ca8c20877f41bfc7e788ede7276f121`  
		Last Modified: Thu, 05 Jun 2025 22:44:12 GMT  
		Size: 19.8 MB (19834728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b7cf9bb5cb3a10f219b307b2ff9f67f54ab05208492bbe13e06a74ca78e54d`  
		Last Modified: Thu, 05 Jun 2025 22:44:13 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7393d30c6bcbe757d4919545933b9de1b6f48c9a46a3ed4a0ae9281792fbd51`  
		Last Modified: Thu, 05 Jun 2025 22:51:09 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe877f07f4d94074494db81efb5c5e890ab77b7ce09fa3952f972953a436545d`  
		Last Modified: Thu, 05 Jun 2025 22:51:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2.2-cli` - unknown; unknown

```console
$ docker pull docker@sha256:9c9ad38782ad3e5c053ed8c736f10e9589825748a8c4233619fb70a2ec23af36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86ca6472c159b81f34510b55fdadf12635ed814ad061552012b01cc7622021dd`

```dockerfile
```

-	Layers:
	-	`sha256:c58766a24b3303a1f1acf7a634a2134383f4aa8fc7b6223cb9497695c7739a5f`  
		Last Modified: Thu, 05 Jun 2025 23:07:47 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.2.2-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:1e48b83f7392bb14bec910d025f2b5ba1a759fff65845d925284236bc07d4fe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68494484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61de327c238ebb7ad778ea80f8124ffd3e79271ceb1c162b0fbdfb43ad4a56f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:28.2.2-cli` - unknown; unknown

```console
$ docker pull docker@sha256:c13cadb351384ad992f27483f70dba162d9c5b57e6643cec3c37598aebb9ff47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ef1b27ab22635d8c650664a7ff740383003126f39daab1972f0db14de9fe5af`

```dockerfile
```

-	Layers:
	-	`sha256:efca98ea4b9f81656feedd1b0eb5f97c37873667b5a92fa941594dad0570afc7`  
		Last Modified: Thu, 05 Jun 2025 23:07:51 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.2.2-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:050e38ffb61f1a397a300e2c027858126865eb5c53026a10a231ea8c71637cf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70083597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:049c11c099d31b1b16a8eec2d4744a8baa44341b7f6489e7c2a70a8c597e17d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38a584a1da307e1ac31b3fd852369ae8a8176a1baa2e783b7e72077d8318364`  
		Last Modified: Thu, 05 Jun 2025 23:07:15 GMT  
		Size: 8.2 MB (8229004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122792206f35c9e929c0c28c585fd195a84012e2d9bea1522c579660e013f3a5`  
		Last Modified: Thu, 05 Jun 2025 22:50:09 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e5a5c767d7cf27a922e7c99956942414d9e65453df45e3500e05adf80db19d`  
		Last Modified: Thu, 05 Jun 2025 23:07:16 GMT  
		Size: 18.9 MB (18902608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2fc5aa8a4cd07adf8f84bd323a5d415f9ca2c5c158b74f9382a0b369265fe2`  
		Last Modified: Thu, 05 Jun 2025 23:07:14 GMT  
		Size: 19.5 MB (19469838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba639502cad797b5554e57bbdc209e0c34366d2a40e0b51a2fa20dfce1a5b337`  
		Last Modified: Thu, 05 Jun 2025 23:07:13 GMT  
		Size: 19.3 MB (19344051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda0f9c86634c1a6b9059d179ed7e6ead432e9b8bcddfb0e980660053ccaef13`  
		Last Modified: Thu, 05 Jun 2025 22:50:11 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef143fe66bfdc5598981ca016d8e3884fde63a7858eb245932bb9745217e515a`  
		Last Modified: Thu, 05 Jun 2025 22:50:14 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69e2c1a5fdbb4dad365dd880c4621563cfe56068eb2e2541c0de0b1de1353676`  
		Last Modified: Thu, 05 Jun 2025 22:50:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2.2-cli` - unknown; unknown

```console
$ docker pull docker@sha256:3d9117cfb4076144f396a04008c8592792765eb725010db68b4fc6a3e9d07a3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8f618e6cdf0288b0248e4b6b48f1bd5324300dfd40ccfdcc2698737d569f539`

```dockerfile
```

-	Layers:
	-	`sha256:07a44b113f5c5d8eb65a6af4b53f0ae0869dcbfdd809ec06739500831432a0db`  
		Last Modified: Thu, 05 Jun 2025 23:07:55 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.2.2-cli-alpine3.22`

```console
$ docker pull docker@sha256:c2e49a065e45c462dda70b65b1a50a74c75804091fae15b7e4fbec6b114996d1
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
$ docker pull docker@sha256:29ac2aff504532e72efca1a58f229c0e05f928828e62156fb304d391e82f7f49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74471875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd02548899f2c001be05193b91d116511f57fb7e8f5cec5f7b58cce36fed0303`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99164a65e1f060513df17430a291c788a5801cc0364c3cf0abaf9dd47e9d891c`  
		Last Modified: Thu, 05 Jun 2025 22:44:25 GMT  
		Size: 8.2 MB (8207469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a930b44823eb85c484514670f94fa0fadf7649aa34a692072e953b86cff998`  
		Last Modified: Thu, 05 Jun 2025 22:44:24 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89fad9bfb8f24abcb392b00c918762036dedf67787dc8a32b43aec570f3557f4`  
		Last Modified: Thu, 05 Jun 2025 22:44:28 GMT  
		Size: 20.1 MB (20083033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e993a5c36c8c13b622945142edd4bdf6b5d03775d8e91196856e50e0512650a`  
		Last Modified: Thu, 05 Jun 2025 22:44:27 GMT  
		Size: 21.3 MB (21290182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd58cf00359048abfc4f447feefe1373db7fd84dfe136fb751689b640844dd4b`  
		Last Modified: Thu, 05 Jun 2025 22:44:27 GMT  
		Size: 21.1 MB (21092192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bd9fc81ec33be8d5693955225a870888bf988fe35871af701d05810a7718b9`  
		Last Modified: Thu, 05 Jun 2025 22:44:26 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7dc70da6730815a90c517d43ed51312bc13932b65a288bbb8952f74df9d763a`  
		Last Modified: Thu, 05 Jun 2025 22:44:26 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2483cd3bb024143d65a844f930ffb5aa01cb0932a660abcaa0fcd68ddc0810`  
		Last Modified: Thu, 05 Jun 2025 22:44:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2.2-cli-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:e3c92c354188244e1e651ab7c9384326a36594dbf3e27427328aa209be1c1e7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de64116684520fb5473d5fee53d9f710a283fa5926d23334bbeb9a13ece30127`

```dockerfile
```

-	Layers:
	-	`sha256:9f1baaf1f40a67141a0489af913841dd7e9427be207fe398702581c569cd1c20`  
		Last Modified: Thu, 05 Jun 2025 23:07:43 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.2.2-cli-alpine3.22` - linux; arm variant v6

```console
$ docker pull docker@sha256:6f76795bf488400672b314ad95bc4add17d3871c369454a410a6072cd1f7fe6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69497654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4905167d30157f311983a0f0fbb87d96647db6c5478ae0071e5e9d717c22247`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
	-	`sha256:b18e44e663f768131c50d79640817a860ca8c20877f41bfc7e788ede7276f121`  
		Last Modified: Thu, 05 Jun 2025 22:44:12 GMT  
		Size: 19.8 MB (19834728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b7cf9bb5cb3a10f219b307b2ff9f67f54ab05208492bbe13e06a74ca78e54d`  
		Last Modified: Thu, 05 Jun 2025 22:44:13 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7393d30c6bcbe757d4919545933b9de1b6f48c9a46a3ed4a0ae9281792fbd51`  
		Last Modified: Thu, 05 Jun 2025 22:51:09 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe877f07f4d94074494db81efb5c5e890ab77b7ce09fa3952f972953a436545d`  
		Last Modified: Thu, 05 Jun 2025 22:51:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2.2-cli-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:9c9ad38782ad3e5c053ed8c736f10e9589825748a8c4233619fb70a2ec23af36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86ca6472c159b81f34510b55fdadf12635ed814ad061552012b01cc7622021dd`

```dockerfile
```

-	Layers:
	-	`sha256:c58766a24b3303a1f1acf7a634a2134383f4aa8fc7b6223cb9497695c7739a5f`  
		Last Modified: Thu, 05 Jun 2025 23:07:47 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.2.2-cli-alpine3.22` - linux; arm variant v7

```console
$ docker pull docker@sha256:1e48b83f7392bb14bec910d025f2b5ba1a759fff65845d925284236bc07d4fe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68494484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61de327c238ebb7ad778ea80f8124ffd3e79271ceb1c162b0fbdfb43ad4a56f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:28.2.2-cli-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:c13cadb351384ad992f27483f70dba162d9c5b57e6643cec3c37598aebb9ff47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ef1b27ab22635d8c650664a7ff740383003126f39daab1972f0db14de9fe5af`

```dockerfile
```

-	Layers:
	-	`sha256:efca98ea4b9f81656feedd1b0eb5f97c37873667b5a92fa941594dad0570afc7`  
		Last Modified: Thu, 05 Jun 2025 23:07:51 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.2.2-cli-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:050e38ffb61f1a397a300e2c027858126865eb5c53026a10a231ea8c71637cf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70083597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:049c11c099d31b1b16a8eec2d4744a8baa44341b7f6489e7c2a70a8c597e17d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38a584a1da307e1ac31b3fd852369ae8a8176a1baa2e783b7e72077d8318364`  
		Last Modified: Thu, 05 Jun 2025 23:07:15 GMT  
		Size: 8.2 MB (8229004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122792206f35c9e929c0c28c585fd195a84012e2d9bea1522c579660e013f3a5`  
		Last Modified: Thu, 05 Jun 2025 22:50:09 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e5a5c767d7cf27a922e7c99956942414d9e65453df45e3500e05adf80db19d`  
		Last Modified: Thu, 05 Jun 2025 23:07:16 GMT  
		Size: 18.9 MB (18902608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2fc5aa8a4cd07adf8f84bd323a5d415f9ca2c5c158b74f9382a0b369265fe2`  
		Last Modified: Thu, 05 Jun 2025 23:07:14 GMT  
		Size: 19.5 MB (19469838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba639502cad797b5554e57bbdc209e0c34366d2a40e0b51a2fa20dfce1a5b337`  
		Last Modified: Thu, 05 Jun 2025 23:07:13 GMT  
		Size: 19.3 MB (19344051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda0f9c86634c1a6b9059d179ed7e6ead432e9b8bcddfb0e980660053ccaef13`  
		Last Modified: Thu, 05 Jun 2025 22:50:11 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef143fe66bfdc5598981ca016d8e3884fde63a7858eb245932bb9745217e515a`  
		Last Modified: Thu, 05 Jun 2025 22:50:14 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69e2c1a5fdbb4dad365dd880c4621563cfe56068eb2e2541c0de0b1de1353676`  
		Last Modified: Thu, 05 Jun 2025 22:50:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2.2-cli-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:3d9117cfb4076144f396a04008c8592792765eb725010db68b4fc6a3e9d07a3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8f618e6cdf0288b0248e4b6b48f1bd5324300dfd40ccfdcc2698737d569f539`

```dockerfile
```

-	Layers:
	-	`sha256:07a44b113f5c5d8eb65a6af4b53f0ae0869dcbfdd809ec06739500831432a0db`  
		Last Modified: Thu, 05 Jun 2025 23:07:55 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.2.2-dind`

```console
$ docker pull docker@sha256:d4668861cabc1691635d98e827a81cfa834a416f8fe0f4efc609f9f806d86d82
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
$ docker pull docker@sha256:8c9502da312e1595a696775bea7d4e6e7b18102d62c413b43f9d3f9d353eb323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.7 MB (143680550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e1cee4b3a3c0bfea53084cb7708d24f3314dd7ce46631888127d8037a4158d9`
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
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99164a65e1f060513df17430a291c788a5801cc0364c3cf0abaf9dd47e9d891c`  
		Last Modified: Thu, 05 Jun 2025 22:44:25 GMT  
		Size: 8.2 MB (8207469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a930b44823eb85c484514670f94fa0fadf7649aa34a692072e953b86cff998`  
		Last Modified: Thu, 05 Jun 2025 22:44:24 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89fad9bfb8f24abcb392b00c918762036dedf67787dc8a32b43aec570f3557f4`  
		Last Modified: Thu, 05 Jun 2025 22:44:28 GMT  
		Size: 20.1 MB (20083033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e993a5c36c8c13b622945142edd4bdf6b5d03775d8e91196856e50e0512650a`  
		Last Modified: Thu, 05 Jun 2025 22:44:27 GMT  
		Size: 21.3 MB (21290182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd58cf00359048abfc4f447feefe1373db7fd84dfe136fb751689b640844dd4b`  
		Last Modified: Thu, 05 Jun 2025 22:44:27 GMT  
		Size: 21.1 MB (21092192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bd9fc81ec33be8d5693955225a870888bf988fe35871af701d05810a7718b9`  
		Last Modified: Thu, 05 Jun 2025 22:44:26 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7dc70da6730815a90c517d43ed51312bc13932b65a288bbb8952f74df9d763a`  
		Last Modified: Thu, 05 Jun 2025 22:44:26 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2483cd3bb024143d65a844f930ffb5aa01cb0932a660abcaa0fcd68ddc0810`  
		Last Modified: Thu, 05 Jun 2025 22:44:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:232671b8d6c574d91a514e1073ddb00bd37e47ba17cfeefc0a4e078e392e4a00`  
		Last Modified: Thu, 05 Jun 2025 23:10:12 GMT  
		Size: 6.9 MB (6905563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8947c15ddd39c2ad279e9f5b5180a071aa948c04d248e2dcf4cb13585d9b47b8`  
		Last Modified: Thu, 05 Jun 2025 23:10:12 GMT  
		Size: 90.5 KB (90492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f7e4c6039fec8c4db67902febab1ae735352d758ffb76367f1e3e68a0b04b9d`  
		Last Modified: Thu, 05 Jun 2025 23:10:11 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:369f3cb80e373dbeee03da49ca69ce93f7c63f165704f929f0a040a4de56ed8e`  
		Last Modified: Thu, 05 Jun 2025 23:10:16 GMT  
		Size: 62.2 MB (62206624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7a0f373a71bb7b7e7a3be4baa2472d2850c4c9549c66b58e70a59a51b696ee`  
		Last Modified: Thu, 05 Jun 2025 23:10:11 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4dbe5b0725a180af25ab3d235ff1a32980b060cb2e263d0362d2baa5b73d858`  
		Last Modified: Thu, 05 Jun 2025 23:10:11 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2.2-dind` - unknown; unknown

```console
$ docker pull docker@sha256:227416a58467a90d61d00571bea5da05930524bab4cb82350e892b245e0d2e6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:125d3c52d0be767b8d0f76f67d0acd7adb2635cac747795240c64e1792d2f95e`

```dockerfile
```

-	Layers:
	-	`sha256:06c3e6cf1c5d56e7cb2fe109c0aa850bd00d57c61602118e103dbffd829369a6`  
		Last Modified: Fri, 06 Jun 2025 02:07:30 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.2.2-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:7920dd4fb3d5c69b32f5a8fdad7bc083113e1eb057daf9551d3bec928642d2d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134721385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f04c9bfb20a7623a34894618839c13fd1bf730153cc94bc61f9b9d60dbc8dc6`
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
	-	`sha256:b18e44e663f768131c50d79640817a860ca8c20877f41bfc7e788ede7276f121`  
		Last Modified: Thu, 05 Jun 2025 22:44:12 GMT  
		Size: 19.8 MB (19834728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b7cf9bb5cb3a10f219b307b2ff9f67f54ab05208492bbe13e06a74ca78e54d`  
		Last Modified: Thu, 05 Jun 2025 22:44:13 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7393d30c6bcbe757d4919545933b9de1b6f48c9a46a3ed4a0ae9281792fbd51`  
		Last Modified: Thu, 05 Jun 2025 22:51:09 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe877f07f4d94074494db81efb5c5e890ab77b7ce09fa3952f972953a436545d`  
		Last Modified: Thu, 05 Jun 2025 22:51:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9526e4c6fe05aa09bd1848ecd6d91b389e046a9da41b839528a0f104ba7e6b`  
		Last Modified: Fri, 06 Jun 2025 01:05:46 GMT  
		Size: 7.2 MB (7230299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7741447d38cadd971edc0ea8d19ec995a5929dad7df81e579060cf95a0a66e0e`  
		Last Modified: Thu, 05 Jun 2025 23:14:04 GMT  
		Size: 90.1 KB (90052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eabb360d9297b2af61c701c3a02f961b3210cdb6c3a4119c7a03d703fd26c6b`  
		Last Modified: Thu, 05 Jun 2025 23:14:08 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c250f611b5a5d3e13bac22e1a236ffb37d10345c511e869b539265c145ebc1`  
		Last Modified: Fri, 06 Jun 2025 01:05:49 GMT  
		Size: 57.9 MB (57897379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b907cd35da6b2acf22cf12c6849885f91becbd5836560543543e4df0b7e4ede`  
		Last Modified: Thu, 05 Jun 2025 23:14:11 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b319c010975a1f690900a80187653a3834b1a65ec15f73ccd7edf9c103bc8eb`  
		Last Modified: Thu, 05 Jun 2025 23:14:13 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2.2-dind` - unknown; unknown

```console
$ docker pull docker@sha256:918e10532d5d49ad3d988b0f42404e4e65b4ff96c9f47d1de4c3bb238edfaf26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc5e34ba8e1767c238c0ca97f2315e8d15bc7d875be15383aa1599e4d71188d2`

```dockerfile
```

-	Layers:
	-	`sha256:21bc1dae29bbc15eda321d47bbd61a416fa4a9175b7a84d90debd5063a161db7`  
		Last Modified: Fri, 06 Jun 2025 02:07:34 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.2.2-dind` - linux; arm variant v7

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

### `docker:28.2.2-dind` - unknown; unknown

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

### `docker:28.2.2-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:0de688aa942b05b1ca86e80e9e87a92cab8690ca4d00819b777253ca12fd05b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.5 MB (134498975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e07111220cfca840da6105d81020ea43df6b1c90921916a1cd65417e1101d6e`
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
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38a584a1da307e1ac31b3fd852369ae8a8176a1baa2e783b7e72077d8318364`  
		Last Modified: Thu, 05 Jun 2025 23:07:15 GMT  
		Size: 8.2 MB (8229004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122792206f35c9e929c0c28c585fd195a84012e2d9bea1522c579660e013f3a5`  
		Last Modified: Thu, 05 Jun 2025 22:50:09 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e5a5c767d7cf27a922e7c99956942414d9e65453df45e3500e05adf80db19d`  
		Last Modified: Thu, 05 Jun 2025 23:07:16 GMT  
		Size: 18.9 MB (18902608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2fc5aa8a4cd07adf8f84bd323a5d415f9ca2c5c158b74f9382a0b369265fe2`  
		Last Modified: Thu, 05 Jun 2025 23:07:14 GMT  
		Size: 19.5 MB (19469838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba639502cad797b5554e57bbdc209e0c34366d2a40e0b51a2fa20dfce1a5b337`  
		Last Modified: Thu, 05 Jun 2025 23:07:13 GMT  
		Size: 19.3 MB (19344051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda0f9c86634c1a6b9059d179ed7e6ead432e9b8bcddfb0e980660053ccaef13`  
		Last Modified: Thu, 05 Jun 2025 22:50:11 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef143fe66bfdc5598981ca016d8e3884fde63a7858eb245932bb9745217e515a`  
		Last Modified: Thu, 05 Jun 2025 22:50:14 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69e2c1a5fdbb4dad365dd880c4621563cfe56068eb2e2541c0de0b1de1353676`  
		Last Modified: Thu, 05 Jun 2025 22:50:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b81c7606e8dcfe2fd4ea847b572c410188a1a61c1b7b1cda6ba28a64e97f159`  
		Last Modified: Thu, 05 Jun 2025 23:08:03 GMT  
		Size: 7.1 MB (7141567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e3f3d3d88e3f3363a8a38c1a676767483806a513d0552d4772a08e36257b1c`  
		Last Modified: Thu, 05 Jun 2025 23:08:04 GMT  
		Size: 99.6 KB (99634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abefbbf9a5b4d4cca3ef794fb554ab4acac7277079ebf9e0403cc7bb13360683`  
		Last Modified: Thu, 05 Jun 2025 23:08:03 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15537da54888f9d1dd7c82127a2affc9eaa21eec06bc9938606f42434884b95d`  
		Last Modified: Thu, 05 Jun 2025 23:08:12 GMT  
		Size: 57.2 MB (57168179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b5eff1498a195bfe23aea7da2bcdf6de5f313f4140c8715a32acf14d62d62cd`  
		Last Modified: Thu, 05 Jun 2025 23:08:04 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b4cb7df5229fcce96acdc6de42d98aa670436a784a0e59417a1584407b6bb8`  
		Last Modified: Thu, 05 Jun 2025 23:08:05 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2.2-dind` - unknown; unknown

```console
$ docker pull docker@sha256:5cad50c6b3b442444f6651f5c8b4d33a9f66b976fd04acda0c3b54328ac14556
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeded159db72e188c1c71b241cf1c67644293d460aa0a7d23d1fd5424dc510de`

```dockerfile
```

-	Layers:
	-	`sha256:431922ef17f88491b0a295b18dd805f113ce40a500def3af5b4651f0b1b77da1`  
		Last Modified: Fri, 06 Jun 2025 02:07:41 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.2.2-dind-alpine3.22`

```console
$ docker pull docker@sha256:d4668861cabc1691635d98e827a81cfa834a416f8fe0f4efc609f9f806d86d82
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
$ docker pull docker@sha256:8c9502da312e1595a696775bea7d4e6e7b18102d62c413b43f9d3f9d353eb323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.7 MB (143680550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e1cee4b3a3c0bfea53084cb7708d24f3314dd7ce46631888127d8037a4158d9`
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
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99164a65e1f060513df17430a291c788a5801cc0364c3cf0abaf9dd47e9d891c`  
		Last Modified: Thu, 05 Jun 2025 22:44:25 GMT  
		Size: 8.2 MB (8207469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a930b44823eb85c484514670f94fa0fadf7649aa34a692072e953b86cff998`  
		Last Modified: Thu, 05 Jun 2025 22:44:24 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89fad9bfb8f24abcb392b00c918762036dedf67787dc8a32b43aec570f3557f4`  
		Last Modified: Thu, 05 Jun 2025 22:44:28 GMT  
		Size: 20.1 MB (20083033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e993a5c36c8c13b622945142edd4bdf6b5d03775d8e91196856e50e0512650a`  
		Last Modified: Thu, 05 Jun 2025 22:44:27 GMT  
		Size: 21.3 MB (21290182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd58cf00359048abfc4f447feefe1373db7fd84dfe136fb751689b640844dd4b`  
		Last Modified: Thu, 05 Jun 2025 22:44:27 GMT  
		Size: 21.1 MB (21092192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bd9fc81ec33be8d5693955225a870888bf988fe35871af701d05810a7718b9`  
		Last Modified: Thu, 05 Jun 2025 22:44:26 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7dc70da6730815a90c517d43ed51312bc13932b65a288bbb8952f74df9d763a`  
		Last Modified: Thu, 05 Jun 2025 22:44:26 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2483cd3bb024143d65a844f930ffb5aa01cb0932a660abcaa0fcd68ddc0810`  
		Last Modified: Thu, 05 Jun 2025 22:44:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:232671b8d6c574d91a514e1073ddb00bd37e47ba17cfeefc0a4e078e392e4a00`  
		Last Modified: Thu, 05 Jun 2025 23:10:12 GMT  
		Size: 6.9 MB (6905563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8947c15ddd39c2ad279e9f5b5180a071aa948c04d248e2dcf4cb13585d9b47b8`  
		Last Modified: Thu, 05 Jun 2025 23:10:12 GMT  
		Size: 90.5 KB (90492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f7e4c6039fec8c4db67902febab1ae735352d758ffb76367f1e3e68a0b04b9d`  
		Last Modified: Thu, 05 Jun 2025 23:10:11 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:369f3cb80e373dbeee03da49ca69ce93f7c63f165704f929f0a040a4de56ed8e`  
		Last Modified: Thu, 05 Jun 2025 23:10:16 GMT  
		Size: 62.2 MB (62206624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7a0f373a71bb7b7e7a3be4baa2472d2850c4c9549c66b58e70a59a51b696ee`  
		Last Modified: Thu, 05 Jun 2025 23:10:11 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4dbe5b0725a180af25ab3d235ff1a32980b060cb2e263d0362d2baa5b73d858`  
		Last Modified: Thu, 05 Jun 2025 23:10:11 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2.2-dind-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:227416a58467a90d61d00571bea5da05930524bab4cb82350e892b245e0d2e6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:125d3c52d0be767b8d0f76f67d0acd7adb2635cac747795240c64e1792d2f95e`

```dockerfile
```

-	Layers:
	-	`sha256:06c3e6cf1c5d56e7cb2fe109c0aa850bd00d57c61602118e103dbffd829369a6`  
		Last Modified: Fri, 06 Jun 2025 02:07:30 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.2.2-dind-alpine3.22` - linux; arm variant v6

```console
$ docker pull docker@sha256:7920dd4fb3d5c69b32f5a8fdad7bc083113e1eb057daf9551d3bec928642d2d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134721385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f04c9bfb20a7623a34894618839c13fd1bf730153cc94bc61f9b9d60dbc8dc6`
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
	-	`sha256:b18e44e663f768131c50d79640817a860ca8c20877f41bfc7e788ede7276f121`  
		Last Modified: Thu, 05 Jun 2025 22:44:12 GMT  
		Size: 19.8 MB (19834728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b7cf9bb5cb3a10f219b307b2ff9f67f54ab05208492bbe13e06a74ca78e54d`  
		Last Modified: Thu, 05 Jun 2025 22:44:13 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7393d30c6bcbe757d4919545933b9de1b6f48c9a46a3ed4a0ae9281792fbd51`  
		Last Modified: Thu, 05 Jun 2025 22:51:09 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe877f07f4d94074494db81efb5c5e890ab77b7ce09fa3952f972953a436545d`  
		Last Modified: Thu, 05 Jun 2025 22:51:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9526e4c6fe05aa09bd1848ecd6d91b389e046a9da41b839528a0f104ba7e6b`  
		Last Modified: Fri, 06 Jun 2025 01:05:46 GMT  
		Size: 7.2 MB (7230299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7741447d38cadd971edc0ea8d19ec995a5929dad7df81e579060cf95a0a66e0e`  
		Last Modified: Thu, 05 Jun 2025 23:14:04 GMT  
		Size: 90.1 KB (90052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eabb360d9297b2af61c701c3a02f961b3210cdb6c3a4119c7a03d703fd26c6b`  
		Last Modified: Thu, 05 Jun 2025 23:14:08 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c250f611b5a5d3e13bac22e1a236ffb37d10345c511e869b539265c145ebc1`  
		Last Modified: Fri, 06 Jun 2025 01:05:49 GMT  
		Size: 57.9 MB (57897379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b907cd35da6b2acf22cf12c6849885f91becbd5836560543543e4df0b7e4ede`  
		Last Modified: Thu, 05 Jun 2025 23:14:11 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b319c010975a1f690900a80187653a3834b1a65ec15f73ccd7edf9c103bc8eb`  
		Last Modified: Thu, 05 Jun 2025 23:14:13 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2.2-dind-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:918e10532d5d49ad3d988b0f42404e4e65b4ff96c9f47d1de4c3bb238edfaf26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc5e34ba8e1767c238c0ca97f2315e8d15bc7d875be15383aa1599e4d71188d2`

```dockerfile
```

-	Layers:
	-	`sha256:21bc1dae29bbc15eda321d47bbd61a416fa4a9175b7a84d90debd5063a161db7`  
		Last Modified: Fri, 06 Jun 2025 02:07:34 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.2.2-dind-alpine3.22` - linux; arm variant v7

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

### `docker:28.2.2-dind-alpine3.22` - unknown; unknown

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

### `docker:28.2.2-dind-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:0de688aa942b05b1ca86e80e9e87a92cab8690ca4d00819b777253ca12fd05b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.5 MB (134498975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e07111220cfca840da6105d81020ea43df6b1c90921916a1cd65417e1101d6e`
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
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38a584a1da307e1ac31b3fd852369ae8a8176a1baa2e783b7e72077d8318364`  
		Last Modified: Thu, 05 Jun 2025 23:07:15 GMT  
		Size: 8.2 MB (8229004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122792206f35c9e929c0c28c585fd195a84012e2d9bea1522c579660e013f3a5`  
		Last Modified: Thu, 05 Jun 2025 22:50:09 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e5a5c767d7cf27a922e7c99956942414d9e65453df45e3500e05adf80db19d`  
		Last Modified: Thu, 05 Jun 2025 23:07:16 GMT  
		Size: 18.9 MB (18902608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2fc5aa8a4cd07adf8f84bd323a5d415f9ca2c5c158b74f9382a0b369265fe2`  
		Last Modified: Thu, 05 Jun 2025 23:07:14 GMT  
		Size: 19.5 MB (19469838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba639502cad797b5554e57bbdc209e0c34366d2a40e0b51a2fa20dfce1a5b337`  
		Last Modified: Thu, 05 Jun 2025 23:07:13 GMT  
		Size: 19.3 MB (19344051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda0f9c86634c1a6b9059d179ed7e6ead432e9b8bcddfb0e980660053ccaef13`  
		Last Modified: Thu, 05 Jun 2025 22:50:11 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef143fe66bfdc5598981ca016d8e3884fde63a7858eb245932bb9745217e515a`  
		Last Modified: Thu, 05 Jun 2025 22:50:14 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69e2c1a5fdbb4dad365dd880c4621563cfe56068eb2e2541c0de0b1de1353676`  
		Last Modified: Thu, 05 Jun 2025 22:50:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b81c7606e8dcfe2fd4ea847b572c410188a1a61c1b7b1cda6ba28a64e97f159`  
		Last Modified: Thu, 05 Jun 2025 23:08:03 GMT  
		Size: 7.1 MB (7141567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e3f3d3d88e3f3363a8a38c1a676767483806a513d0552d4772a08e36257b1c`  
		Last Modified: Thu, 05 Jun 2025 23:08:04 GMT  
		Size: 99.6 KB (99634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abefbbf9a5b4d4cca3ef794fb554ab4acac7277079ebf9e0403cc7bb13360683`  
		Last Modified: Thu, 05 Jun 2025 23:08:03 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15537da54888f9d1dd7c82127a2affc9eaa21eec06bc9938606f42434884b95d`  
		Last Modified: Thu, 05 Jun 2025 23:08:12 GMT  
		Size: 57.2 MB (57168179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b5eff1498a195bfe23aea7da2bcdf6de5f313f4140c8715a32acf14d62d62cd`  
		Last Modified: Thu, 05 Jun 2025 23:08:04 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b4cb7df5229fcce96acdc6de42d98aa670436a784a0e59417a1584407b6bb8`  
		Last Modified: Thu, 05 Jun 2025 23:08:05 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2.2-dind-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:5cad50c6b3b442444f6651f5c8b4d33a9f66b976fd04acda0c3b54328ac14556
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeded159db72e188c1c71b241cf1c67644293d460aa0a7d23d1fd5424dc510de`

```dockerfile
```

-	Layers:
	-	`sha256:431922ef17f88491b0a295b18dd805f113ce40a500def3af5b4651f0b1b77da1`  
		Last Modified: Fri, 06 Jun 2025 02:07:41 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.2.2-dind-rootless`

```console
$ docker pull docker@sha256:8fc8c7e252d63e2280415a0520caf2a014c86b5c8fd25c910fe8adc77aeb94ca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:28.2.2-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:abd2dd1debd13881cb395d987a48ef2db49e904f9260e691cdd8fb3f40c8c810
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.3 MB (162261128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:515c53634a6d629377edd34a1fa5f3f6977b9ff51a6afb4aa84a220a5f27d5c4`
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
ENV DOCKER_COMPOSE_VERSION=2.37.0
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-x86_64'; 			sha256='e6e471b1e7bf0443592d3987dea6073f08db3e48ba0580199109aa7a44257e54'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-armv6'; 			sha256='f09294bd81119701f051733b45be487d55faa29d20fb9c54412975a6c7fd8696'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-armv7'; 			sha256='b1b592889f15f50ddc77685ed499c69599117e52240b196447cb82821da3f7f8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-aarch64'; 			sha256='664e8c532ac0dd54d14af4eb3fe4edce86ce27d970ec832a96b55bc2ef1dffdf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-ppc64le'; 			sha256='83c7cf5afffcc7944e23ba5c1c038aff4f2d760f08681d76b5271b66c9e2af5d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-riscv64'; 			sha256='0e6047d2b0f745f0bbb13d707cfb945295bf45e397e67ff756f8551043a1f5bc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-s390x'; 			sha256='381b5b77e6a91075e746167ac160062a1adf4d2a1121e433f1ca731ad08e2353'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:99164a65e1f060513df17430a291c788a5801cc0364c3cf0abaf9dd47e9d891c`  
		Last Modified: Thu, 05 Jun 2025 22:44:25 GMT  
		Size: 8.2 MB (8207469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a930b44823eb85c484514670f94fa0fadf7649aa34a692072e953b86cff998`  
		Last Modified: Thu, 05 Jun 2025 22:44:24 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89fad9bfb8f24abcb392b00c918762036dedf67787dc8a32b43aec570f3557f4`  
		Last Modified: Thu, 05 Jun 2025 22:44:28 GMT  
		Size: 20.1 MB (20083033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e993a5c36c8c13b622945142edd4bdf6b5d03775d8e91196856e50e0512650a`  
		Last Modified: Thu, 05 Jun 2025 22:44:27 GMT  
		Size: 21.3 MB (21290182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd58cf00359048abfc4f447feefe1373db7fd84dfe136fb751689b640844dd4b`  
		Last Modified: Thu, 05 Jun 2025 22:44:27 GMT  
		Size: 21.1 MB (21092192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bd9fc81ec33be8d5693955225a870888bf988fe35871af701d05810a7718b9`  
		Last Modified: Thu, 05 Jun 2025 22:44:26 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7dc70da6730815a90c517d43ed51312bc13932b65a288bbb8952f74df9d763a`  
		Last Modified: Thu, 05 Jun 2025 22:44:26 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2483cd3bb024143d65a844f930ffb5aa01cb0932a660abcaa0fcd68ddc0810`  
		Last Modified: Thu, 05 Jun 2025 22:44:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:232671b8d6c574d91a514e1073ddb00bd37e47ba17cfeefc0a4e078e392e4a00`  
		Last Modified: Thu, 05 Jun 2025 23:10:12 GMT  
		Size: 6.9 MB (6905563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8947c15ddd39c2ad279e9f5b5180a071aa948c04d248e2dcf4cb13585d9b47b8`  
		Last Modified: Thu, 05 Jun 2025 23:10:12 GMT  
		Size: 90.5 KB (90492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f7e4c6039fec8c4db67902febab1ae735352d758ffb76367f1e3e68a0b04b9d`  
		Last Modified: Thu, 05 Jun 2025 23:10:11 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:369f3cb80e373dbeee03da49ca69ce93f7c63f165704f929f0a040a4de56ed8e`  
		Last Modified: Thu, 05 Jun 2025 23:10:16 GMT  
		Size: 62.2 MB (62206624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7a0f373a71bb7b7e7a3be4baa2472d2850c4c9549c66b58e70a59a51b696ee`  
		Last Modified: Thu, 05 Jun 2025 23:10:11 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4dbe5b0725a180af25ab3d235ff1a32980b060cb2e263d0362d2baa5b73d858`  
		Last Modified: Thu, 05 Jun 2025 23:10:11 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f64aa3fd56b6d8303e9c2e032693fa69765ebe0ca402c8652e2e4be4bd9b8a2f`  
		Last Modified: Fri, 06 Jun 2025 00:13:41 GMT  
		Size: 993.3 KB (993270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9ac68c4bd4a09936531af4a567ee2065e73f798766ad456aef07aa86555af1`  
		Last Modified: Fri, 06 Jun 2025 00:13:48 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e79fe881b6f2ad1dc6bfdf95095a21b2a9400b5098d82da1be17d678d59226`  
		Last Modified: Fri, 06 Jun 2025 00:13:51 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91260bbdd96570e120d536ac928e3f77c4f858234e17f2ba9abb34a416109116`  
		Last Modified: Fri, 06 Jun 2025 02:08:01 GMT  
		Size: 17.6 MB (17585969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e31b397060352f80943b2c245dfb2b9014d8caaaefa979cba711e233412315`  
		Last Modified: Fri, 06 Jun 2025 00:13:54 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2.2-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:0c4804528defa4555b2fadbd0044e12d0585c45979692580e6f2793f2e1eea66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.4 KB (30450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f33f1746b3d799c576bbbfea37de0b6f65df618daea063dddc5c07da8dfdd129`

```dockerfile
```

-	Layers:
	-	`sha256:4faecdc253478ec516ca521def628c3524f48440edfd20522bf779744323317c`  
		Last Modified: Fri, 06 Jun 2025 02:07:42 GMT  
		Size: 30.4 KB (30450 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.2.2-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:8f8a0cd4395a6ab286a0630f776e920239e6a01f6de484c2c23292ef76381bec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.5 MB (153539458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63acc824e3021e35e0fbed5808986ced5616f6da68905d273709d210e4a8ade6`
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
ENV DOCKER_COMPOSE_VERSION=2.37.0
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-x86_64'; 			sha256='e6e471b1e7bf0443592d3987dea6073f08db3e48ba0580199109aa7a44257e54'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-armv6'; 			sha256='f09294bd81119701f051733b45be487d55faa29d20fb9c54412975a6c7fd8696'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-armv7'; 			sha256='b1b592889f15f50ddc77685ed499c69599117e52240b196447cb82821da3f7f8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-aarch64'; 			sha256='664e8c532ac0dd54d14af4eb3fe4edce86ce27d970ec832a96b55bc2ef1dffdf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-ppc64le'; 			sha256='83c7cf5afffcc7944e23ba5c1c038aff4f2d760f08681d76b5271b66c9e2af5d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-riscv64'; 			sha256='0e6047d2b0f745f0bbb13d707cfb945295bf45e397e67ff756f8551043a1f5bc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-s390x'; 			sha256='381b5b77e6a91075e746167ac160062a1adf4d2a1121e433f1ca731ad08e2353'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:d38a584a1da307e1ac31b3fd852369ae8a8176a1baa2e783b7e72077d8318364`  
		Last Modified: Thu, 05 Jun 2025 23:07:15 GMT  
		Size: 8.2 MB (8229004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122792206f35c9e929c0c28c585fd195a84012e2d9bea1522c579660e013f3a5`  
		Last Modified: Thu, 05 Jun 2025 22:50:09 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e5a5c767d7cf27a922e7c99956942414d9e65453df45e3500e05adf80db19d`  
		Last Modified: Thu, 05 Jun 2025 23:07:16 GMT  
		Size: 18.9 MB (18902608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2fc5aa8a4cd07adf8f84bd323a5d415f9ca2c5c158b74f9382a0b369265fe2`  
		Last Modified: Thu, 05 Jun 2025 23:07:14 GMT  
		Size: 19.5 MB (19469838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba639502cad797b5554e57bbdc209e0c34366d2a40e0b51a2fa20dfce1a5b337`  
		Last Modified: Thu, 05 Jun 2025 23:07:13 GMT  
		Size: 19.3 MB (19344051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda0f9c86634c1a6b9059d179ed7e6ead432e9b8bcddfb0e980660053ccaef13`  
		Last Modified: Thu, 05 Jun 2025 22:50:11 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef143fe66bfdc5598981ca016d8e3884fde63a7858eb245932bb9745217e515a`  
		Last Modified: Thu, 05 Jun 2025 22:50:14 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69e2c1a5fdbb4dad365dd880c4621563cfe56068eb2e2541c0de0b1de1353676`  
		Last Modified: Thu, 05 Jun 2025 22:50:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b81c7606e8dcfe2fd4ea847b572c410188a1a61c1b7b1cda6ba28a64e97f159`  
		Last Modified: Thu, 05 Jun 2025 23:08:03 GMT  
		Size: 7.1 MB (7141567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e3f3d3d88e3f3363a8a38c1a676767483806a513d0552d4772a08e36257b1c`  
		Last Modified: Thu, 05 Jun 2025 23:08:04 GMT  
		Size: 99.6 KB (99634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abefbbf9a5b4d4cca3ef794fb554ab4acac7277079ebf9e0403cc7bb13360683`  
		Last Modified: Thu, 05 Jun 2025 23:08:03 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15537da54888f9d1dd7c82127a2affc9eaa21eec06bc9938606f42434884b95d`  
		Last Modified: Thu, 05 Jun 2025 23:08:12 GMT  
		Size: 57.2 MB (57168179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b5eff1498a195bfe23aea7da2bcdf6de5f313f4140c8715a32acf14d62d62cd`  
		Last Modified: Thu, 05 Jun 2025 23:08:04 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b4cb7df5229fcce96acdc6de42d98aa670436a784a0e59417a1584407b6bb8`  
		Last Modified: Thu, 05 Jun 2025 23:08:05 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b640b4b96d1a9d3b71ca7172efbfc7644661ed859290a1ef70f6efb5ae8646b6`  
		Last Modified: Thu, 05 Jun 2025 23:10:53 GMT  
		Size: 1.0 MB (1022994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3954fdd9c5b6656129957c10bf87d54fb3f5abd93ddb09065d380cb210a5077`  
		Last Modified: Thu, 05 Jun 2025 23:10:53 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4258e800a40d5a0144bf5289d6469124b4dcd57aa4a07ebfe0b4d51a68c8176e`  
		Last Modified: Thu, 05 Jun 2025 23:10:54 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603a03c83db0af7bcffad6809d5df5087ed7fc636e484590aa7baf42f257b2f2`  
		Last Modified: Thu, 05 Jun 2025 23:10:56 GMT  
		Size: 18.0 MB (18016150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ced063cb74820e91a874efbb44b00db32b5453e8cf96c0082bfe9265f119ad2`  
		Last Modified: Thu, 05 Jun 2025 23:14:26 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.2.2-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:84c0fd5fb3a3c2479438611da949f104f724c986c93c76c12541d88382d56a73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2929db2e0b226bded3985c6262f564307858288cba598d29b2ed0fa3c11f193`

```dockerfile
```

-	Layers:
	-	`sha256:fb773e2f1f91681ce7adadf4bf3c53895f7c309689fbb9874a70b1ce0fc12347`  
		Last Modified: Fri, 06 Jun 2025 02:07:46 GMT  
		Size: 30.6 KB (30621 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.2.2-windowsservercore`

```console
$ docker pull docker@sha256:0869de84e82e8707faa2238d565cea70e111fd670a2699eb7ed746f424fac81f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4061; amd64
	-	windows version 10.0.20348.3692; amd64

### `docker:28.2.2-windowsservercore` - windows version 10.0.26100.4061; amd64

```console
$ docker pull docker@sha256:25b529d707052438ef4b12929192d89e568c602554eff61b838530e3ba0862d0
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3496004439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5af2557ed6bf90b5a556401cda31f5e80c741723bd7d8d8dd85f75c9edb2beee`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 10 May 2025 01:13:32 GMT
RUN Install update 10.0.26100.4061
# Thu, 05 Jun 2025 22:49:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 05 Jun 2025 22:49:27 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 05 Jun 2025 22:49:29 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 05 Jun 2025 22:49:31 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.2.2.zip
# Thu, 05 Jun 2025 22:49:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 05 Jun 2025 22:49:45 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 05 Jun 2025 22:49:46 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Thu, 05 Jun 2025 22:49:48 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Thu, 05 Jun 2025 22:50:00 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 05 Jun 2025 22:50:02 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.0
# Thu, 05 Jun 2025 22:50:03 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-windows-x86_64.exe
# Thu, 05 Jun 2025 22:50:04 GMT
ENV DOCKER_COMPOSE_SHA256=5ddd1ff588eb7251381cf6257b9be44fbb92c02d984ccfc94b4280e8c33d0f8f
# Thu, 05 Jun 2025 22:50:15 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc834e13e71633c2d66ec6513d57c31a3157fc5933859d492ecf45fc8a7476c3`  
		Last Modified: Thu, 15 May 2025 19:25:03 GMT  
		Size: 1.2 GB (1215458626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90e49ef0e985b81e99d8b31a019b88aee89866bfb5c61dca46c36db719f75f72`  
		Last Modified: Thu, 05 Jun 2025 22:54:09 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35e4e87c87497c1f6d87a7f50d5b5d0f1d0cc7d219c6ce8eafc2a68e833177e3`  
		Last Modified: Thu, 05 Jun 2025 22:54:10 GMT  
		Size: 389.0 KB (389032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc34a02ab083801559a9993b8b75ebf1889f6ee4406ace24d67068a1db6d394`  
		Last Modified: Thu, 05 Jun 2025 22:54:09 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460eb4eabe732c14d4ba4780e91bfae9ce2f88f06d471caa6eaec23d33259db7`  
		Last Modified: Thu, 05 Jun 2025 22:54:10 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48921f27b31821d44d89e3376996fbcef78628b7c234b417f58afb6186212ee6`  
		Last Modified: Thu, 05 Jun 2025 22:54:12 GMT  
		Size: 20.5 MB (20482824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3fa9bcfc9c100af95e701bc8db63daa6762e21200bcbcfeacf780ceff4ac0a5`  
		Last Modified: Thu, 05 Jun 2025 23:02:29 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f73ddc322ec88bd49ef2ed8da74c0a7037d94bb1649764c3a424b89b9ba72f5`  
		Last Modified: Thu, 05 Jun 2025 23:02:32 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bee619612444d3cd3f98593f7912090ea8ebeaa7537f88e6ef0df6381f43660`  
		Last Modified: Thu, 05 Jun 2025 23:08:02 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aab9f1404ae5f4d3919e9d9b3989dc637b5461c0d61a0a8914464ac3efef61c`  
		Last Modified: Thu, 05 Jun 2025 23:08:03 GMT  
		Size: 22.3 MB (22293165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ffe3877611fd0a573d09a62990e99adc779e2ecfb7a0a99352b6097f1aedfa`  
		Last Modified: Thu, 05 Jun 2025 23:02:39 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c74c3be6ed0d6a50023b6597b4c73f7c8a6edf1bf15689254c3030e49379b3b`  
		Last Modified: Thu, 05 Jun 2025 23:02:42 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4546e8211fc088c3925f2b673074dc5a6d27527caf92983c56600ac02ceec30`  
		Last Modified: Thu, 05 Jun 2025 23:02:45 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:281c5b22c80200de8cb5cd27b59777a1a0c02818b3d09d937cc6ff99e29f8305`  
		Last Modified: Thu, 05 Jun 2025 23:08:07 GMT  
		Size: 22.1 MB (22061869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28.2.2-windowsservercore` - windows version 10.0.20348.3692; amd64

```console
$ docker pull docker@sha256:213ffc624913105fa7ee59720002de6a40b9768db21a5d09ec3f292a45573596
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2338596324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af09b10c562d5ce89c47cb4db81986d086849844eb9ea5e334925da4e6e60501`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Thu, 05 Jun 2025 22:44:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 05 Jun 2025 22:46:25 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 05 Jun 2025 22:46:26 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 05 Jun 2025 22:46:27 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.2.2.zip
# Thu, 05 Jun 2025 22:46:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 05 Jun 2025 22:46:51 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 05 Jun 2025 22:46:52 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Thu, 05 Jun 2025 22:46:52 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Thu, 05 Jun 2025 22:47:01 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 05 Jun 2025 22:47:02 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.0
# Thu, 05 Jun 2025 22:47:02 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-windows-x86_64.exe
# Thu, 05 Jun 2025 22:47:03 GMT
ENV DOCKER_COMPOSE_SHA256=5ddd1ff588eb7251381cf6257b9be44fbb92c02d984ccfc94b4280e8c33d0f8f
# Thu, 05 Jun 2025 22:47:14 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Thu, 15 May 2025 19:25:06 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69792782d0247e3e22c67f6096a5c5ac4096e3039e9902b31095ada21a3a3992`  
		Last Modified: Thu, 05 Jun 2025 22:47:55 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1528406f9d6a747555a27165ae52a9ade5da9bafe09faedc813fc9978410ebb1`  
		Last Modified: Thu, 05 Jun 2025 22:47:57 GMT  
		Size: 347.0 KB (347048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44599b0e57d9512be310c8211fc1db3c2b2f26d186b1f4fa5f41cb3239e83e08`  
		Last Modified: Thu, 05 Jun 2025 22:47:57 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5946a2c5ebb15f702288c926ad33ec3e48dc514e959828483bf2515343b8164`  
		Last Modified: Thu, 05 Jun 2025 22:47:58 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5950ebf7245c1e012f8bedfc8e4f944900fbb4429057e997700cbfc430e71db`  
		Last Modified: Thu, 05 Jun 2025 23:08:02 GMT  
		Size: 20.4 MB (20407814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e4979217510eb7de8d35cf3a6a4ea0d48a38fccd55990459ede40e90555a91`  
		Last Modified: Thu, 05 Jun 2025 22:50:52 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bee3bf1d9c1e36c3c62244bbf0b25abd4d3848230da86f8eb7ab9e87bfcce25`  
		Last Modified: Thu, 05 Jun 2025 22:50:55 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dd6d131f13751da51b0a0640902b80152d4626d65b68249d48306530f6af710`  
		Last Modified: Thu, 05 Jun 2025 22:50:58 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809edd0f0043024cc3f263278554b9d43f0af10b1ff965b9e755e7f504cc9448`  
		Last Modified: Thu, 05 Jun 2025 23:08:01 GMT  
		Size: 22.2 MB (22218481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3644edf37145bf3243218f63e04734da0ee41b17a3db4580ac428852159a95b4`  
		Last Modified: Thu, 05 Jun 2025 22:51:01 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f3f405f8fc75b4dbb8e568437773842a367615ed3dbe41b6be647fdbcb3756e`  
		Last Modified: Thu, 05 Jun 2025 22:51:04 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4701c8fc8cca7fb8a5a1d7d575fa186deff56c45e248857b3ed475c698ed20c8`  
		Last Modified: Thu, 05 Jun 2025 22:51:08 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b4da056663f41259b84270c9d8dc6b48fb2b7d53922c07335a68a8dc178b488`  
		Last Modified: Thu, 05 Jun 2025 23:08:02 GMT  
		Size: 22.0 MB (21983289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.2.2-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:bc2b0152ecb9f33a768c3b3a7ba14c8206d2b7f60077c28a3546b40efb6dd9c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `docker:28.2.2-windowsservercore-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull docker@sha256:213ffc624913105fa7ee59720002de6a40b9768db21a5d09ec3f292a45573596
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2338596324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af09b10c562d5ce89c47cb4db81986d086849844eb9ea5e334925da4e6e60501`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Thu, 05 Jun 2025 22:44:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 05 Jun 2025 22:46:25 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 05 Jun 2025 22:46:26 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 05 Jun 2025 22:46:27 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.2.2.zip
# Thu, 05 Jun 2025 22:46:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 05 Jun 2025 22:46:51 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 05 Jun 2025 22:46:52 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Thu, 05 Jun 2025 22:46:52 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Thu, 05 Jun 2025 22:47:01 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 05 Jun 2025 22:47:02 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.0
# Thu, 05 Jun 2025 22:47:02 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-windows-x86_64.exe
# Thu, 05 Jun 2025 22:47:03 GMT
ENV DOCKER_COMPOSE_SHA256=5ddd1ff588eb7251381cf6257b9be44fbb92c02d984ccfc94b4280e8c33d0f8f
# Thu, 05 Jun 2025 22:47:14 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Thu, 15 May 2025 19:25:06 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69792782d0247e3e22c67f6096a5c5ac4096e3039e9902b31095ada21a3a3992`  
		Last Modified: Thu, 05 Jun 2025 22:47:55 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1528406f9d6a747555a27165ae52a9ade5da9bafe09faedc813fc9978410ebb1`  
		Last Modified: Thu, 05 Jun 2025 22:47:57 GMT  
		Size: 347.0 KB (347048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44599b0e57d9512be310c8211fc1db3c2b2f26d186b1f4fa5f41cb3239e83e08`  
		Last Modified: Thu, 05 Jun 2025 22:47:57 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5946a2c5ebb15f702288c926ad33ec3e48dc514e959828483bf2515343b8164`  
		Last Modified: Thu, 05 Jun 2025 22:47:58 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5950ebf7245c1e012f8bedfc8e4f944900fbb4429057e997700cbfc430e71db`  
		Last Modified: Thu, 05 Jun 2025 23:08:02 GMT  
		Size: 20.4 MB (20407814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e4979217510eb7de8d35cf3a6a4ea0d48a38fccd55990459ede40e90555a91`  
		Last Modified: Thu, 05 Jun 2025 22:50:52 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bee3bf1d9c1e36c3c62244bbf0b25abd4d3848230da86f8eb7ab9e87bfcce25`  
		Last Modified: Thu, 05 Jun 2025 22:50:55 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dd6d131f13751da51b0a0640902b80152d4626d65b68249d48306530f6af710`  
		Last Modified: Thu, 05 Jun 2025 22:50:58 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809edd0f0043024cc3f263278554b9d43f0af10b1ff965b9e755e7f504cc9448`  
		Last Modified: Thu, 05 Jun 2025 23:08:01 GMT  
		Size: 22.2 MB (22218481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3644edf37145bf3243218f63e04734da0ee41b17a3db4580ac428852159a95b4`  
		Last Modified: Thu, 05 Jun 2025 22:51:01 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f3f405f8fc75b4dbb8e568437773842a367615ed3dbe41b6be647fdbcb3756e`  
		Last Modified: Thu, 05 Jun 2025 22:51:04 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4701c8fc8cca7fb8a5a1d7d575fa186deff56c45e248857b3ed475c698ed20c8`  
		Last Modified: Thu, 05 Jun 2025 22:51:08 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b4da056663f41259b84270c9d8dc6b48fb2b7d53922c07335a68a8dc178b488`  
		Last Modified: Thu, 05 Jun 2025 23:08:02 GMT  
		Size: 22.0 MB (21983289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.2.2-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:5f0071c24f8a2426413b698206c5a415be20f1024483d31ea54cd904e41465df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4061; amd64

### `docker:28.2.2-windowsservercore-ltsc2025` - windows version 10.0.26100.4061; amd64

```console
$ docker pull docker@sha256:25b529d707052438ef4b12929192d89e568c602554eff61b838530e3ba0862d0
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3496004439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5af2557ed6bf90b5a556401cda31f5e80c741723bd7d8d8dd85f75c9edb2beee`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 10 May 2025 01:13:32 GMT
RUN Install update 10.0.26100.4061
# Thu, 05 Jun 2025 22:49:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 05 Jun 2025 22:49:27 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 05 Jun 2025 22:49:29 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 05 Jun 2025 22:49:31 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.2.2.zip
# Thu, 05 Jun 2025 22:49:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 05 Jun 2025 22:49:45 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 05 Jun 2025 22:49:46 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Thu, 05 Jun 2025 22:49:48 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Thu, 05 Jun 2025 22:50:00 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 05 Jun 2025 22:50:02 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.0
# Thu, 05 Jun 2025 22:50:03 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-windows-x86_64.exe
# Thu, 05 Jun 2025 22:50:04 GMT
ENV DOCKER_COMPOSE_SHA256=5ddd1ff588eb7251381cf6257b9be44fbb92c02d984ccfc94b4280e8c33d0f8f
# Thu, 05 Jun 2025 22:50:15 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc834e13e71633c2d66ec6513d57c31a3157fc5933859d492ecf45fc8a7476c3`  
		Last Modified: Thu, 15 May 2025 19:25:03 GMT  
		Size: 1.2 GB (1215458626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90e49ef0e985b81e99d8b31a019b88aee89866bfb5c61dca46c36db719f75f72`  
		Last Modified: Thu, 05 Jun 2025 22:54:09 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35e4e87c87497c1f6d87a7f50d5b5d0f1d0cc7d219c6ce8eafc2a68e833177e3`  
		Last Modified: Thu, 05 Jun 2025 22:54:10 GMT  
		Size: 389.0 KB (389032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc34a02ab083801559a9993b8b75ebf1889f6ee4406ace24d67068a1db6d394`  
		Last Modified: Thu, 05 Jun 2025 22:54:09 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460eb4eabe732c14d4ba4780e91bfae9ce2f88f06d471caa6eaec23d33259db7`  
		Last Modified: Thu, 05 Jun 2025 22:54:10 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48921f27b31821d44d89e3376996fbcef78628b7c234b417f58afb6186212ee6`  
		Last Modified: Thu, 05 Jun 2025 22:54:12 GMT  
		Size: 20.5 MB (20482824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3fa9bcfc9c100af95e701bc8db63daa6762e21200bcbcfeacf780ceff4ac0a5`  
		Last Modified: Thu, 05 Jun 2025 23:02:29 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f73ddc322ec88bd49ef2ed8da74c0a7037d94bb1649764c3a424b89b9ba72f5`  
		Last Modified: Thu, 05 Jun 2025 23:02:32 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bee619612444d3cd3f98593f7912090ea8ebeaa7537f88e6ef0df6381f43660`  
		Last Modified: Thu, 05 Jun 2025 23:08:02 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aab9f1404ae5f4d3919e9d9b3989dc637b5461c0d61a0a8914464ac3efef61c`  
		Last Modified: Thu, 05 Jun 2025 23:08:03 GMT  
		Size: 22.3 MB (22293165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ffe3877611fd0a573d09a62990e99adc779e2ecfb7a0a99352b6097f1aedfa`  
		Last Modified: Thu, 05 Jun 2025 23:02:39 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c74c3be6ed0d6a50023b6597b4c73f7c8a6edf1bf15689254c3030e49379b3b`  
		Last Modified: Thu, 05 Jun 2025 23:02:42 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4546e8211fc088c3925f2b673074dc5a6d27527caf92983c56600ac02ceec30`  
		Last Modified: Thu, 05 Jun 2025 23:02:45 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:281c5b22c80200de8cb5cd27b59777a1a0c02818b3d09d937cc6ff99e29f8305`  
		Last Modified: Thu, 05 Jun 2025 23:08:07 GMT  
		Size: 22.1 MB (22061869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:cli`

```console
$ docker pull docker@sha256:c2e49a065e45c462dda70b65b1a50a74c75804091fae15b7e4fbec6b114996d1
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
$ docker pull docker@sha256:29ac2aff504532e72efca1a58f229c0e05f928828e62156fb304d391e82f7f49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74471875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd02548899f2c001be05193b91d116511f57fb7e8f5cec5f7b58cce36fed0303`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99164a65e1f060513df17430a291c788a5801cc0364c3cf0abaf9dd47e9d891c`  
		Last Modified: Thu, 05 Jun 2025 22:44:25 GMT  
		Size: 8.2 MB (8207469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a930b44823eb85c484514670f94fa0fadf7649aa34a692072e953b86cff998`  
		Last Modified: Thu, 05 Jun 2025 22:44:24 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89fad9bfb8f24abcb392b00c918762036dedf67787dc8a32b43aec570f3557f4`  
		Last Modified: Thu, 05 Jun 2025 22:44:28 GMT  
		Size: 20.1 MB (20083033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e993a5c36c8c13b622945142edd4bdf6b5d03775d8e91196856e50e0512650a`  
		Last Modified: Thu, 05 Jun 2025 22:44:27 GMT  
		Size: 21.3 MB (21290182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd58cf00359048abfc4f447feefe1373db7fd84dfe136fb751689b640844dd4b`  
		Last Modified: Thu, 05 Jun 2025 22:44:27 GMT  
		Size: 21.1 MB (21092192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bd9fc81ec33be8d5693955225a870888bf988fe35871af701d05810a7718b9`  
		Last Modified: Thu, 05 Jun 2025 22:44:26 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7dc70da6730815a90c517d43ed51312bc13932b65a288bbb8952f74df9d763a`  
		Last Modified: Thu, 05 Jun 2025 22:44:26 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2483cd3bb024143d65a844f930ffb5aa01cb0932a660abcaa0fcd68ddc0810`  
		Last Modified: Thu, 05 Jun 2025 22:44:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:e3c92c354188244e1e651ab7c9384326a36594dbf3e27427328aa209be1c1e7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de64116684520fb5473d5fee53d9f710a283fa5926d23334bbeb9a13ece30127`

```dockerfile
```

-	Layers:
	-	`sha256:9f1baaf1f40a67141a0489af913841dd7e9427be207fe398702581c569cd1c20`  
		Last Modified: Thu, 05 Jun 2025 23:07:43 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:6f76795bf488400672b314ad95bc4add17d3871c369454a410a6072cd1f7fe6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69497654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4905167d30157f311983a0f0fbb87d96647db6c5478ae0071e5e9d717c22247`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
	-	`sha256:b18e44e663f768131c50d79640817a860ca8c20877f41bfc7e788ede7276f121`  
		Last Modified: Thu, 05 Jun 2025 22:44:12 GMT  
		Size: 19.8 MB (19834728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b7cf9bb5cb3a10f219b307b2ff9f67f54ab05208492bbe13e06a74ca78e54d`  
		Last Modified: Thu, 05 Jun 2025 22:44:13 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7393d30c6bcbe757d4919545933b9de1b6f48c9a46a3ed4a0ae9281792fbd51`  
		Last Modified: Thu, 05 Jun 2025 22:51:09 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe877f07f4d94074494db81efb5c5e890ab77b7ce09fa3952f972953a436545d`  
		Last Modified: Thu, 05 Jun 2025 22:51:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:9c9ad38782ad3e5c053ed8c736f10e9589825748a8c4233619fb70a2ec23af36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86ca6472c159b81f34510b55fdadf12635ed814ad061552012b01cc7622021dd`

```dockerfile
```

-	Layers:
	-	`sha256:c58766a24b3303a1f1acf7a634a2134383f4aa8fc7b6223cb9497695c7739a5f`  
		Last Modified: Thu, 05 Jun 2025 23:07:47 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:1e48b83f7392bb14bec910d025f2b5ba1a759fff65845d925284236bc07d4fe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68494484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61de327c238ebb7ad778ea80f8124ffd3e79271ceb1c162b0fbdfb43ad4a56f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:c13cadb351384ad992f27483f70dba162d9c5b57e6643cec3c37598aebb9ff47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ef1b27ab22635d8c650664a7ff740383003126f39daab1972f0db14de9fe5af`

```dockerfile
```

-	Layers:
	-	`sha256:efca98ea4b9f81656feedd1b0eb5f97c37873667b5a92fa941594dad0570afc7`  
		Last Modified: Thu, 05 Jun 2025 23:07:51 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:050e38ffb61f1a397a300e2c027858126865eb5c53026a10a231ea8c71637cf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70083597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:049c11c099d31b1b16a8eec2d4744a8baa44341b7f6489e7c2a70a8c597e17d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38a584a1da307e1ac31b3fd852369ae8a8176a1baa2e783b7e72077d8318364`  
		Last Modified: Thu, 05 Jun 2025 23:07:15 GMT  
		Size: 8.2 MB (8229004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122792206f35c9e929c0c28c585fd195a84012e2d9bea1522c579660e013f3a5`  
		Last Modified: Thu, 05 Jun 2025 22:50:09 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e5a5c767d7cf27a922e7c99956942414d9e65453df45e3500e05adf80db19d`  
		Last Modified: Thu, 05 Jun 2025 23:07:16 GMT  
		Size: 18.9 MB (18902608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2fc5aa8a4cd07adf8f84bd323a5d415f9ca2c5c158b74f9382a0b369265fe2`  
		Last Modified: Thu, 05 Jun 2025 23:07:14 GMT  
		Size: 19.5 MB (19469838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba639502cad797b5554e57bbdc209e0c34366d2a40e0b51a2fa20dfce1a5b337`  
		Last Modified: Thu, 05 Jun 2025 23:07:13 GMT  
		Size: 19.3 MB (19344051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda0f9c86634c1a6b9059d179ed7e6ead432e9b8bcddfb0e980660053ccaef13`  
		Last Modified: Thu, 05 Jun 2025 22:50:11 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef143fe66bfdc5598981ca016d8e3884fde63a7858eb245932bb9745217e515a`  
		Last Modified: Thu, 05 Jun 2025 22:50:14 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69e2c1a5fdbb4dad365dd880c4621563cfe56068eb2e2541c0de0b1de1353676`  
		Last Modified: Thu, 05 Jun 2025 22:50:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:3d9117cfb4076144f396a04008c8592792765eb725010db68b4fc6a3e9d07a3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8f618e6cdf0288b0248e4b6b48f1bd5324300dfd40ccfdcc2698737d569f539`

```dockerfile
```

-	Layers:
	-	`sha256:07a44b113f5c5d8eb65a6af4b53f0ae0869dcbfdd809ec06739500831432a0db`  
		Last Modified: Thu, 05 Jun 2025 23:07:55 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind`

```console
$ docker pull docker@sha256:d4668861cabc1691635d98e827a81cfa834a416f8fe0f4efc609f9f806d86d82
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
$ docker pull docker@sha256:8c9502da312e1595a696775bea7d4e6e7b18102d62c413b43f9d3f9d353eb323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.7 MB (143680550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e1cee4b3a3c0bfea53084cb7708d24f3314dd7ce46631888127d8037a4158d9`
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
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99164a65e1f060513df17430a291c788a5801cc0364c3cf0abaf9dd47e9d891c`  
		Last Modified: Thu, 05 Jun 2025 22:44:25 GMT  
		Size: 8.2 MB (8207469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a930b44823eb85c484514670f94fa0fadf7649aa34a692072e953b86cff998`  
		Last Modified: Thu, 05 Jun 2025 22:44:24 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89fad9bfb8f24abcb392b00c918762036dedf67787dc8a32b43aec570f3557f4`  
		Last Modified: Thu, 05 Jun 2025 22:44:28 GMT  
		Size: 20.1 MB (20083033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e993a5c36c8c13b622945142edd4bdf6b5d03775d8e91196856e50e0512650a`  
		Last Modified: Thu, 05 Jun 2025 22:44:27 GMT  
		Size: 21.3 MB (21290182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd58cf00359048abfc4f447feefe1373db7fd84dfe136fb751689b640844dd4b`  
		Last Modified: Thu, 05 Jun 2025 22:44:27 GMT  
		Size: 21.1 MB (21092192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bd9fc81ec33be8d5693955225a870888bf988fe35871af701d05810a7718b9`  
		Last Modified: Thu, 05 Jun 2025 22:44:26 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7dc70da6730815a90c517d43ed51312bc13932b65a288bbb8952f74df9d763a`  
		Last Modified: Thu, 05 Jun 2025 22:44:26 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2483cd3bb024143d65a844f930ffb5aa01cb0932a660abcaa0fcd68ddc0810`  
		Last Modified: Thu, 05 Jun 2025 22:44:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:232671b8d6c574d91a514e1073ddb00bd37e47ba17cfeefc0a4e078e392e4a00`  
		Last Modified: Thu, 05 Jun 2025 23:10:12 GMT  
		Size: 6.9 MB (6905563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8947c15ddd39c2ad279e9f5b5180a071aa948c04d248e2dcf4cb13585d9b47b8`  
		Last Modified: Thu, 05 Jun 2025 23:10:12 GMT  
		Size: 90.5 KB (90492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f7e4c6039fec8c4db67902febab1ae735352d758ffb76367f1e3e68a0b04b9d`  
		Last Modified: Thu, 05 Jun 2025 23:10:11 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:369f3cb80e373dbeee03da49ca69ce93f7c63f165704f929f0a040a4de56ed8e`  
		Last Modified: Thu, 05 Jun 2025 23:10:16 GMT  
		Size: 62.2 MB (62206624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7a0f373a71bb7b7e7a3be4baa2472d2850c4c9549c66b58e70a59a51b696ee`  
		Last Modified: Thu, 05 Jun 2025 23:10:11 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4dbe5b0725a180af25ab3d235ff1a32980b060cb2e263d0362d2baa5b73d858`  
		Last Modified: Thu, 05 Jun 2025 23:10:11 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:227416a58467a90d61d00571bea5da05930524bab4cb82350e892b245e0d2e6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:125d3c52d0be767b8d0f76f67d0acd7adb2635cac747795240c64e1792d2f95e`

```dockerfile
```

-	Layers:
	-	`sha256:06c3e6cf1c5d56e7cb2fe109c0aa850bd00d57c61602118e103dbffd829369a6`  
		Last Modified: Fri, 06 Jun 2025 02:07:30 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:7920dd4fb3d5c69b32f5a8fdad7bc083113e1eb057daf9551d3bec928642d2d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134721385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f04c9bfb20a7623a34894618839c13fd1bf730153cc94bc61f9b9d60dbc8dc6`
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
	-	`sha256:b18e44e663f768131c50d79640817a860ca8c20877f41bfc7e788ede7276f121`  
		Last Modified: Thu, 05 Jun 2025 22:44:12 GMT  
		Size: 19.8 MB (19834728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b7cf9bb5cb3a10f219b307b2ff9f67f54ab05208492bbe13e06a74ca78e54d`  
		Last Modified: Thu, 05 Jun 2025 22:44:13 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7393d30c6bcbe757d4919545933b9de1b6f48c9a46a3ed4a0ae9281792fbd51`  
		Last Modified: Thu, 05 Jun 2025 22:51:09 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe877f07f4d94074494db81efb5c5e890ab77b7ce09fa3952f972953a436545d`  
		Last Modified: Thu, 05 Jun 2025 22:51:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9526e4c6fe05aa09bd1848ecd6d91b389e046a9da41b839528a0f104ba7e6b`  
		Last Modified: Fri, 06 Jun 2025 01:05:46 GMT  
		Size: 7.2 MB (7230299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7741447d38cadd971edc0ea8d19ec995a5929dad7df81e579060cf95a0a66e0e`  
		Last Modified: Thu, 05 Jun 2025 23:14:04 GMT  
		Size: 90.1 KB (90052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eabb360d9297b2af61c701c3a02f961b3210cdb6c3a4119c7a03d703fd26c6b`  
		Last Modified: Thu, 05 Jun 2025 23:14:08 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c250f611b5a5d3e13bac22e1a236ffb37d10345c511e869b539265c145ebc1`  
		Last Modified: Fri, 06 Jun 2025 01:05:49 GMT  
		Size: 57.9 MB (57897379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b907cd35da6b2acf22cf12c6849885f91becbd5836560543543e4df0b7e4ede`  
		Last Modified: Thu, 05 Jun 2025 23:14:11 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b319c010975a1f690900a80187653a3834b1a65ec15f73ccd7edf9c103bc8eb`  
		Last Modified: Thu, 05 Jun 2025 23:14:13 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:918e10532d5d49ad3d988b0f42404e4e65b4ff96c9f47d1de4c3bb238edfaf26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc5e34ba8e1767c238c0ca97f2315e8d15bc7d875be15383aa1599e4d71188d2`

```dockerfile
```

-	Layers:
	-	`sha256:21bc1dae29bbc15eda321d47bbd61a416fa4a9175b7a84d90debd5063a161db7`  
		Last Modified: Fri, 06 Jun 2025 02:07:34 GMT  
		Size: 34.8 KB (34766 bytes)  
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
$ docker pull docker@sha256:0de688aa942b05b1ca86e80e9e87a92cab8690ca4d00819b777253ca12fd05b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.5 MB (134498975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e07111220cfca840da6105d81020ea43df6b1c90921916a1cd65417e1101d6e`
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
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38a584a1da307e1ac31b3fd852369ae8a8176a1baa2e783b7e72077d8318364`  
		Last Modified: Thu, 05 Jun 2025 23:07:15 GMT  
		Size: 8.2 MB (8229004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122792206f35c9e929c0c28c585fd195a84012e2d9bea1522c579660e013f3a5`  
		Last Modified: Thu, 05 Jun 2025 22:50:09 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e5a5c767d7cf27a922e7c99956942414d9e65453df45e3500e05adf80db19d`  
		Last Modified: Thu, 05 Jun 2025 23:07:16 GMT  
		Size: 18.9 MB (18902608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2fc5aa8a4cd07adf8f84bd323a5d415f9ca2c5c158b74f9382a0b369265fe2`  
		Last Modified: Thu, 05 Jun 2025 23:07:14 GMT  
		Size: 19.5 MB (19469838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba639502cad797b5554e57bbdc209e0c34366d2a40e0b51a2fa20dfce1a5b337`  
		Last Modified: Thu, 05 Jun 2025 23:07:13 GMT  
		Size: 19.3 MB (19344051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda0f9c86634c1a6b9059d179ed7e6ead432e9b8bcddfb0e980660053ccaef13`  
		Last Modified: Thu, 05 Jun 2025 22:50:11 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef143fe66bfdc5598981ca016d8e3884fde63a7858eb245932bb9745217e515a`  
		Last Modified: Thu, 05 Jun 2025 22:50:14 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69e2c1a5fdbb4dad365dd880c4621563cfe56068eb2e2541c0de0b1de1353676`  
		Last Modified: Thu, 05 Jun 2025 22:50:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b81c7606e8dcfe2fd4ea847b572c410188a1a61c1b7b1cda6ba28a64e97f159`  
		Last Modified: Thu, 05 Jun 2025 23:08:03 GMT  
		Size: 7.1 MB (7141567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e3f3d3d88e3f3363a8a38c1a676767483806a513d0552d4772a08e36257b1c`  
		Last Modified: Thu, 05 Jun 2025 23:08:04 GMT  
		Size: 99.6 KB (99634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abefbbf9a5b4d4cca3ef794fb554ab4acac7277079ebf9e0403cc7bb13360683`  
		Last Modified: Thu, 05 Jun 2025 23:08:03 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15537da54888f9d1dd7c82127a2affc9eaa21eec06bc9938606f42434884b95d`  
		Last Modified: Thu, 05 Jun 2025 23:08:12 GMT  
		Size: 57.2 MB (57168179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b5eff1498a195bfe23aea7da2bcdf6de5f313f4140c8715a32acf14d62d62cd`  
		Last Modified: Thu, 05 Jun 2025 23:08:04 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b4cb7df5229fcce96acdc6de42d98aa670436a784a0e59417a1584407b6bb8`  
		Last Modified: Thu, 05 Jun 2025 23:08:05 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:5cad50c6b3b442444f6651f5c8b4d33a9f66b976fd04acda0c3b54328ac14556
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeded159db72e188c1c71b241cf1c67644293d460aa0a7d23d1fd5424dc510de`

```dockerfile
```

-	Layers:
	-	`sha256:431922ef17f88491b0a295b18dd805f113ce40a500def3af5b4651f0b1b77da1`  
		Last Modified: Fri, 06 Jun 2025 02:07:41 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind-rootless`

```console
$ docker pull docker@sha256:8fc8c7e252d63e2280415a0520caf2a014c86b5c8fd25c910fe8adc77aeb94ca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:abd2dd1debd13881cb395d987a48ef2db49e904f9260e691cdd8fb3f40c8c810
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.3 MB (162261128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:515c53634a6d629377edd34a1fa5f3f6977b9ff51a6afb4aa84a220a5f27d5c4`
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
ENV DOCKER_COMPOSE_VERSION=2.37.0
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-x86_64'; 			sha256='e6e471b1e7bf0443592d3987dea6073f08db3e48ba0580199109aa7a44257e54'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-armv6'; 			sha256='f09294bd81119701f051733b45be487d55faa29d20fb9c54412975a6c7fd8696'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-armv7'; 			sha256='b1b592889f15f50ddc77685ed499c69599117e52240b196447cb82821da3f7f8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-aarch64'; 			sha256='664e8c532ac0dd54d14af4eb3fe4edce86ce27d970ec832a96b55bc2ef1dffdf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-ppc64le'; 			sha256='83c7cf5afffcc7944e23ba5c1c038aff4f2d760f08681d76b5271b66c9e2af5d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-riscv64'; 			sha256='0e6047d2b0f745f0bbb13d707cfb945295bf45e397e67ff756f8551043a1f5bc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-s390x'; 			sha256='381b5b77e6a91075e746167ac160062a1adf4d2a1121e433f1ca731ad08e2353'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:99164a65e1f060513df17430a291c788a5801cc0364c3cf0abaf9dd47e9d891c`  
		Last Modified: Thu, 05 Jun 2025 22:44:25 GMT  
		Size: 8.2 MB (8207469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a930b44823eb85c484514670f94fa0fadf7649aa34a692072e953b86cff998`  
		Last Modified: Thu, 05 Jun 2025 22:44:24 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89fad9bfb8f24abcb392b00c918762036dedf67787dc8a32b43aec570f3557f4`  
		Last Modified: Thu, 05 Jun 2025 22:44:28 GMT  
		Size: 20.1 MB (20083033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e993a5c36c8c13b622945142edd4bdf6b5d03775d8e91196856e50e0512650a`  
		Last Modified: Thu, 05 Jun 2025 22:44:27 GMT  
		Size: 21.3 MB (21290182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd58cf00359048abfc4f447feefe1373db7fd84dfe136fb751689b640844dd4b`  
		Last Modified: Thu, 05 Jun 2025 22:44:27 GMT  
		Size: 21.1 MB (21092192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bd9fc81ec33be8d5693955225a870888bf988fe35871af701d05810a7718b9`  
		Last Modified: Thu, 05 Jun 2025 22:44:26 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7dc70da6730815a90c517d43ed51312bc13932b65a288bbb8952f74df9d763a`  
		Last Modified: Thu, 05 Jun 2025 22:44:26 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2483cd3bb024143d65a844f930ffb5aa01cb0932a660abcaa0fcd68ddc0810`  
		Last Modified: Thu, 05 Jun 2025 22:44:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:232671b8d6c574d91a514e1073ddb00bd37e47ba17cfeefc0a4e078e392e4a00`  
		Last Modified: Thu, 05 Jun 2025 23:10:12 GMT  
		Size: 6.9 MB (6905563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8947c15ddd39c2ad279e9f5b5180a071aa948c04d248e2dcf4cb13585d9b47b8`  
		Last Modified: Thu, 05 Jun 2025 23:10:12 GMT  
		Size: 90.5 KB (90492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f7e4c6039fec8c4db67902febab1ae735352d758ffb76367f1e3e68a0b04b9d`  
		Last Modified: Thu, 05 Jun 2025 23:10:11 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:369f3cb80e373dbeee03da49ca69ce93f7c63f165704f929f0a040a4de56ed8e`  
		Last Modified: Thu, 05 Jun 2025 23:10:16 GMT  
		Size: 62.2 MB (62206624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7a0f373a71bb7b7e7a3be4baa2472d2850c4c9549c66b58e70a59a51b696ee`  
		Last Modified: Thu, 05 Jun 2025 23:10:11 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4dbe5b0725a180af25ab3d235ff1a32980b060cb2e263d0362d2baa5b73d858`  
		Last Modified: Thu, 05 Jun 2025 23:10:11 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f64aa3fd56b6d8303e9c2e032693fa69765ebe0ca402c8652e2e4be4bd9b8a2f`  
		Last Modified: Fri, 06 Jun 2025 00:13:41 GMT  
		Size: 993.3 KB (993270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9ac68c4bd4a09936531af4a567ee2065e73f798766ad456aef07aa86555af1`  
		Last Modified: Fri, 06 Jun 2025 00:13:48 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e79fe881b6f2ad1dc6bfdf95095a21b2a9400b5098d82da1be17d678d59226`  
		Last Modified: Fri, 06 Jun 2025 00:13:51 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91260bbdd96570e120d536ac928e3f77c4f858234e17f2ba9abb34a416109116`  
		Last Modified: Fri, 06 Jun 2025 02:08:01 GMT  
		Size: 17.6 MB (17585969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e31b397060352f80943b2c245dfb2b9014d8caaaefa979cba711e233412315`  
		Last Modified: Fri, 06 Jun 2025 00:13:54 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:0c4804528defa4555b2fadbd0044e12d0585c45979692580e6f2793f2e1eea66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.4 KB (30450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f33f1746b3d799c576bbbfea37de0b6f65df618daea063dddc5c07da8dfdd129`

```dockerfile
```

-	Layers:
	-	`sha256:4faecdc253478ec516ca521def628c3524f48440edfd20522bf779744323317c`  
		Last Modified: Fri, 06 Jun 2025 02:07:42 GMT  
		Size: 30.4 KB (30450 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:8f8a0cd4395a6ab286a0630f776e920239e6a01f6de484c2c23292ef76381bec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.5 MB (153539458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63acc824e3021e35e0fbed5808986ced5616f6da68905d273709d210e4a8ade6`
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
ENV DOCKER_COMPOSE_VERSION=2.37.0
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-x86_64'; 			sha256='e6e471b1e7bf0443592d3987dea6073f08db3e48ba0580199109aa7a44257e54'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-armv6'; 			sha256='f09294bd81119701f051733b45be487d55faa29d20fb9c54412975a6c7fd8696'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-armv7'; 			sha256='b1b592889f15f50ddc77685ed499c69599117e52240b196447cb82821da3f7f8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-aarch64'; 			sha256='664e8c532ac0dd54d14af4eb3fe4edce86ce27d970ec832a96b55bc2ef1dffdf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-ppc64le'; 			sha256='83c7cf5afffcc7944e23ba5c1c038aff4f2d760f08681d76b5271b66c9e2af5d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-riscv64'; 			sha256='0e6047d2b0f745f0bbb13d707cfb945295bf45e397e67ff756f8551043a1f5bc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-s390x'; 			sha256='381b5b77e6a91075e746167ac160062a1adf4d2a1121e433f1ca731ad08e2353'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:d38a584a1da307e1ac31b3fd852369ae8a8176a1baa2e783b7e72077d8318364`  
		Last Modified: Thu, 05 Jun 2025 23:07:15 GMT  
		Size: 8.2 MB (8229004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122792206f35c9e929c0c28c585fd195a84012e2d9bea1522c579660e013f3a5`  
		Last Modified: Thu, 05 Jun 2025 22:50:09 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e5a5c767d7cf27a922e7c99956942414d9e65453df45e3500e05adf80db19d`  
		Last Modified: Thu, 05 Jun 2025 23:07:16 GMT  
		Size: 18.9 MB (18902608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2fc5aa8a4cd07adf8f84bd323a5d415f9ca2c5c158b74f9382a0b369265fe2`  
		Last Modified: Thu, 05 Jun 2025 23:07:14 GMT  
		Size: 19.5 MB (19469838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba639502cad797b5554e57bbdc209e0c34366d2a40e0b51a2fa20dfce1a5b337`  
		Last Modified: Thu, 05 Jun 2025 23:07:13 GMT  
		Size: 19.3 MB (19344051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda0f9c86634c1a6b9059d179ed7e6ead432e9b8bcddfb0e980660053ccaef13`  
		Last Modified: Thu, 05 Jun 2025 22:50:11 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef143fe66bfdc5598981ca016d8e3884fde63a7858eb245932bb9745217e515a`  
		Last Modified: Thu, 05 Jun 2025 22:50:14 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69e2c1a5fdbb4dad365dd880c4621563cfe56068eb2e2541c0de0b1de1353676`  
		Last Modified: Thu, 05 Jun 2025 22:50:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b81c7606e8dcfe2fd4ea847b572c410188a1a61c1b7b1cda6ba28a64e97f159`  
		Last Modified: Thu, 05 Jun 2025 23:08:03 GMT  
		Size: 7.1 MB (7141567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e3f3d3d88e3f3363a8a38c1a676767483806a513d0552d4772a08e36257b1c`  
		Last Modified: Thu, 05 Jun 2025 23:08:04 GMT  
		Size: 99.6 KB (99634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abefbbf9a5b4d4cca3ef794fb554ab4acac7277079ebf9e0403cc7bb13360683`  
		Last Modified: Thu, 05 Jun 2025 23:08:03 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15537da54888f9d1dd7c82127a2affc9eaa21eec06bc9938606f42434884b95d`  
		Last Modified: Thu, 05 Jun 2025 23:08:12 GMT  
		Size: 57.2 MB (57168179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b5eff1498a195bfe23aea7da2bcdf6de5f313f4140c8715a32acf14d62d62cd`  
		Last Modified: Thu, 05 Jun 2025 23:08:04 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b4cb7df5229fcce96acdc6de42d98aa670436a784a0e59417a1584407b6bb8`  
		Last Modified: Thu, 05 Jun 2025 23:08:05 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b640b4b96d1a9d3b71ca7172efbfc7644661ed859290a1ef70f6efb5ae8646b6`  
		Last Modified: Thu, 05 Jun 2025 23:10:53 GMT  
		Size: 1.0 MB (1022994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3954fdd9c5b6656129957c10bf87d54fb3f5abd93ddb09065d380cb210a5077`  
		Last Modified: Thu, 05 Jun 2025 23:10:53 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4258e800a40d5a0144bf5289d6469124b4dcd57aa4a07ebfe0b4d51a68c8176e`  
		Last Modified: Thu, 05 Jun 2025 23:10:54 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603a03c83db0af7bcffad6809d5df5087ed7fc636e484590aa7baf42f257b2f2`  
		Last Modified: Thu, 05 Jun 2025 23:10:56 GMT  
		Size: 18.0 MB (18016150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ced063cb74820e91a874efbb44b00db32b5453e8cf96c0082bfe9265f119ad2`  
		Last Modified: Thu, 05 Jun 2025 23:14:26 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:84c0fd5fb3a3c2479438611da949f104f724c986c93c76c12541d88382d56a73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2929db2e0b226bded3985c6262f564307858288cba598d29b2ed0fa3c11f193`

```dockerfile
```

-	Layers:
	-	`sha256:fb773e2f1f91681ce7adadf4bf3c53895f7c309689fbb9874a70b1ce0fc12347`  
		Last Modified: Fri, 06 Jun 2025 02:07:46 GMT  
		Size: 30.6 KB (30621 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:latest`

```console
$ docker pull docker@sha256:d4668861cabc1691635d98e827a81cfa834a416f8fe0f4efc609f9f806d86d82
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
$ docker pull docker@sha256:8c9502da312e1595a696775bea7d4e6e7b18102d62c413b43f9d3f9d353eb323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.7 MB (143680550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e1cee4b3a3c0bfea53084cb7708d24f3314dd7ce46631888127d8037a4158d9`
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
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99164a65e1f060513df17430a291c788a5801cc0364c3cf0abaf9dd47e9d891c`  
		Last Modified: Thu, 05 Jun 2025 22:44:25 GMT  
		Size: 8.2 MB (8207469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a930b44823eb85c484514670f94fa0fadf7649aa34a692072e953b86cff998`  
		Last Modified: Thu, 05 Jun 2025 22:44:24 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89fad9bfb8f24abcb392b00c918762036dedf67787dc8a32b43aec570f3557f4`  
		Last Modified: Thu, 05 Jun 2025 22:44:28 GMT  
		Size: 20.1 MB (20083033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e993a5c36c8c13b622945142edd4bdf6b5d03775d8e91196856e50e0512650a`  
		Last Modified: Thu, 05 Jun 2025 22:44:27 GMT  
		Size: 21.3 MB (21290182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd58cf00359048abfc4f447feefe1373db7fd84dfe136fb751689b640844dd4b`  
		Last Modified: Thu, 05 Jun 2025 22:44:27 GMT  
		Size: 21.1 MB (21092192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bd9fc81ec33be8d5693955225a870888bf988fe35871af701d05810a7718b9`  
		Last Modified: Thu, 05 Jun 2025 22:44:26 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7dc70da6730815a90c517d43ed51312bc13932b65a288bbb8952f74df9d763a`  
		Last Modified: Thu, 05 Jun 2025 22:44:26 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2483cd3bb024143d65a844f930ffb5aa01cb0932a660abcaa0fcd68ddc0810`  
		Last Modified: Thu, 05 Jun 2025 22:44:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:232671b8d6c574d91a514e1073ddb00bd37e47ba17cfeefc0a4e078e392e4a00`  
		Last Modified: Thu, 05 Jun 2025 23:10:12 GMT  
		Size: 6.9 MB (6905563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8947c15ddd39c2ad279e9f5b5180a071aa948c04d248e2dcf4cb13585d9b47b8`  
		Last Modified: Thu, 05 Jun 2025 23:10:12 GMT  
		Size: 90.5 KB (90492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f7e4c6039fec8c4db67902febab1ae735352d758ffb76367f1e3e68a0b04b9d`  
		Last Modified: Thu, 05 Jun 2025 23:10:11 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:369f3cb80e373dbeee03da49ca69ce93f7c63f165704f929f0a040a4de56ed8e`  
		Last Modified: Thu, 05 Jun 2025 23:10:16 GMT  
		Size: 62.2 MB (62206624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7a0f373a71bb7b7e7a3be4baa2472d2850c4c9549c66b58e70a59a51b696ee`  
		Last Modified: Thu, 05 Jun 2025 23:10:11 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4dbe5b0725a180af25ab3d235ff1a32980b060cb2e263d0362d2baa5b73d858`  
		Last Modified: Thu, 05 Jun 2025 23:10:11 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:227416a58467a90d61d00571bea5da05930524bab4cb82350e892b245e0d2e6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:125d3c52d0be767b8d0f76f67d0acd7adb2635cac747795240c64e1792d2f95e`

```dockerfile
```

-	Layers:
	-	`sha256:06c3e6cf1c5d56e7cb2fe109c0aa850bd00d57c61602118e103dbffd829369a6`  
		Last Modified: Fri, 06 Jun 2025 02:07:30 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v6

```console
$ docker pull docker@sha256:7920dd4fb3d5c69b32f5a8fdad7bc083113e1eb057daf9551d3bec928642d2d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134721385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f04c9bfb20a7623a34894618839c13fd1bf730153cc94bc61f9b9d60dbc8dc6`
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
	-	`sha256:b18e44e663f768131c50d79640817a860ca8c20877f41bfc7e788ede7276f121`  
		Last Modified: Thu, 05 Jun 2025 22:44:12 GMT  
		Size: 19.8 MB (19834728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b7cf9bb5cb3a10f219b307b2ff9f67f54ab05208492bbe13e06a74ca78e54d`  
		Last Modified: Thu, 05 Jun 2025 22:44:13 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7393d30c6bcbe757d4919545933b9de1b6f48c9a46a3ed4a0ae9281792fbd51`  
		Last Modified: Thu, 05 Jun 2025 22:51:09 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe877f07f4d94074494db81efb5c5e890ab77b7ce09fa3952f972953a436545d`  
		Last Modified: Thu, 05 Jun 2025 22:51:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9526e4c6fe05aa09bd1848ecd6d91b389e046a9da41b839528a0f104ba7e6b`  
		Last Modified: Fri, 06 Jun 2025 01:05:46 GMT  
		Size: 7.2 MB (7230299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7741447d38cadd971edc0ea8d19ec995a5929dad7df81e579060cf95a0a66e0e`  
		Last Modified: Thu, 05 Jun 2025 23:14:04 GMT  
		Size: 90.1 KB (90052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eabb360d9297b2af61c701c3a02f961b3210cdb6c3a4119c7a03d703fd26c6b`  
		Last Modified: Thu, 05 Jun 2025 23:14:08 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c250f611b5a5d3e13bac22e1a236ffb37d10345c511e869b539265c145ebc1`  
		Last Modified: Fri, 06 Jun 2025 01:05:49 GMT  
		Size: 57.9 MB (57897379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b907cd35da6b2acf22cf12c6849885f91becbd5836560543543e4df0b7e4ede`  
		Last Modified: Thu, 05 Jun 2025 23:14:11 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b319c010975a1f690900a80187653a3834b1a65ec15f73ccd7edf9c103bc8eb`  
		Last Modified: Thu, 05 Jun 2025 23:14:13 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:918e10532d5d49ad3d988b0f42404e4e65b4ff96c9f47d1de4c3bb238edfaf26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc5e34ba8e1767c238c0ca97f2315e8d15bc7d875be15383aa1599e4d71188d2`

```dockerfile
```

-	Layers:
	-	`sha256:21bc1dae29bbc15eda321d47bbd61a416fa4a9175b7a84d90debd5063a161db7`  
		Last Modified: Fri, 06 Jun 2025 02:07:34 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v7

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

### `docker:latest` - unknown; unknown

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

### `docker:latest` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:0de688aa942b05b1ca86e80e9e87a92cab8690ca4d00819b777253ca12fd05b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.5 MB (134498975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e07111220cfca840da6105d81020ea43df6b1c90921916a1cd65417e1101d6e`
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
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38a584a1da307e1ac31b3fd852369ae8a8176a1baa2e783b7e72077d8318364`  
		Last Modified: Thu, 05 Jun 2025 23:07:15 GMT  
		Size: 8.2 MB (8229004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122792206f35c9e929c0c28c585fd195a84012e2d9bea1522c579660e013f3a5`  
		Last Modified: Thu, 05 Jun 2025 22:50:09 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e5a5c767d7cf27a922e7c99956942414d9e65453df45e3500e05adf80db19d`  
		Last Modified: Thu, 05 Jun 2025 23:07:16 GMT  
		Size: 18.9 MB (18902608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2fc5aa8a4cd07adf8f84bd323a5d415f9ca2c5c158b74f9382a0b369265fe2`  
		Last Modified: Thu, 05 Jun 2025 23:07:14 GMT  
		Size: 19.5 MB (19469838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba639502cad797b5554e57bbdc209e0c34366d2a40e0b51a2fa20dfce1a5b337`  
		Last Modified: Thu, 05 Jun 2025 23:07:13 GMT  
		Size: 19.3 MB (19344051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda0f9c86634c1a6b9059d179ed7e6ead432e9b8bcddfb0e980660053ccaef13`  
		Last Modified: Thu, 05 Jun 2025 22:50:11 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef143fe66bfdc5598981ca016d8e3884fde63a7858eb245932bb9745217e515a`  
		Last Modified: Thu, 05 Jun 2025 22:50:14 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69e2c1a5fdbb4dad365dd880c4621563cfe56068eb2e2541c0de0b1de1353676`  
		Last Modified: Thu, 05 Jun 2025 22:50:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b81c7606e8dcfe2fd4ea847b572c410188a1a61c1b7b1cda6ba28a64e97f159`  
		Last Modified: Thu, 05 Jun 2025 23:08:03 GMT  
		Size: 7.1 MB (7141567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e3f3d3d88e3f3363a8a38c1a676767483806a513d0552d4772a08e36257b1c`  
		Last Modified: Thu, 05 Jun 2025 23:08:04 GMT  
		Size: 99.6 KB (99634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abefbbf9a5b4d4cca3ef794fb554ab4acac7277079ebf9e0403cc7bb13360683`  
		Last Modified: Thu, 05 Jun 2025 23:08:03 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15537da54888f9d1dd7c82127a2affc9eaa21eec06bc9938606f42434884b95d`  
		Last Modified: Thu, 05 Jun 2025 23:08:12 GMT  
		Size: 57.2 MB (57168179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b5eff1498a195bfe23aea7da2bcdf6de5f313f4140c8715a32acf14d62d62cd`  
		Last Modified: Thu, 05 Jun 2025 23:08:04 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b4cb7df5229fcce96acdc6de42d98aa670436a784a0e59417a1584407b6bb8`  
		Last Modified: Thu, 05 Jun 2025 23:08:05 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:5cad50c6b3b442444f6651f5c8b4d33a9f66b976fd04acda0c3b54328ac14556
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeded159db72e188c1c71b241cf1c67644293d460aa0a7d23d1fd5424dc510de`

```dockerfile
```

-	Layers:
	-	`sha256:431922ef17f88491b0a295b18dd805f113ce40a500def3af5b4651f0b1b77da1`  
		Last Modified: Fri, 06 Jun 2025 02:07:41 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:windowsservercore`

```console
$ docker pull docker@sha256:0869de84e82e8707faa2238d565cea70e111fd670a2699eb7ed746f424fac81f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4061; amd64
	-	windows version 10.0.20348.3692; amd64

### `docker:windowsservercore` - windows version 10.0.26100.4061; amd64

```console
$ docker pull docker@sha256:25b529d707052438ef4b12929192d89e568c602554eff61b838530e3ba0862d0
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3496004439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5af2557ed6bf90b5a556401cda31f5e80c741723bd7d8d8dd85f75c9edb2beee`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 10 May 2025 01:13:32 GMT
RUN Install update 10.0.26100.4061
# Thu, 05 Jun 2025 22:49:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 05 Jun 2025 22:49:27 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 05 Jun 2025 22:49:29 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 05 Jun 2025 22:49:31 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.2.2.zip
# Thu, 05 Jun 2025 22:49:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 05 Jun 2025 22:49:45 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 05 Jun 2025 22:49:46 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Thu, 05 Jun 2025 22:49:48 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Thu, 05 Jun 2025 22:50:00 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 05 Jun 2025 22:50:02 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.0
# Thu, 05 Jun 2025 22:50:03 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-windows-x86_64.exe
# Thu, 05 Jun 2025 22:50:04 GMT
ENV DOCKER_COMPOSE_SHA256=5ddd1ff588eb7251381cf6257b9be44fbb92c02d984ccfc94b4280e8c33d0f8f
# Thu, 05 Jun 2025 22:50:15 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc834e13e71633c2d66ec6513d57c31a3157fc5933859d492ecf45fc8a7476c3`  
		Last Modified: Thu, 15 May 2025 19:25:03 GMT  
		Size: 1.2 GB (1215458626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90e49ef0e985b81e99d8b31a019b88aee89866bfb5c61dca46c36db719f75f72`  
		Last Modified: Thu, 05 Jun 2025 22:54:09 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35e4e87c87497c1f6d87a7f50d5b5d0f1d0cc7d219c6ce8eafc2a68e833177e3`  
		Last Modified: Thu, 05 Jun 2025 22:54:10 GMT  
		Size: 389.0 KB (389032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc34a02ab083801559a9993b8b75ebf1889f6ee4406ace24d67068a1db6d394`  
		Last Modified: Thu, 05 Jun 2025 22:54:09 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460eb4eabe732c14d4ba4780e91bfae9ce2f88f06d471caa6eaec23d33259db7`  
		Last Modified: Thu, 05 Jun 2025 22:54:10 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48921f27b31821d44d89e3376996fbcef78628b7c234b417f58afb6186212ee6`  
		Last Modified: Thu, 05 Jun 2025 22:54:12 GMT  
		Size: 20.5 MB (20482824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3fa9bcfc9c100af95e701bc8db63daa6762e21200bcbcfeacf780ceff4ac0a5`  
		Last Modified: Thu, 05 Jun 2025 23:02:29 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f73ddc322ec88bd49ef2ed8da74c0a7037d94bb1649764c3a424b89b9ba72f5`  
		Last Modified: Thu, 05 Jun 2025 23:02:32 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bee619612444d3cd3f98593f7912090ea8ebeaa7537f88e6ef0df6381f43660`  
		Last Modified: Thu, 05 Jun 2025 23:08:02 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aab9f1404ae5f4d3919e9d9b3989dc637b5461c0d61a0a8914464ac3efef61c`  
		Last Modified: Thu, 05 Jun 2025 23:08:03 GMT  
		Size: 22.3 MB (22293165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ffe3877611fd0a573d09a62990e99adc779e2ecfb7a0a99352b6097f1aedfa`  
		Last Modified: Thu, 05 Jun 2025 23:02:39 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c74c3be6ed0d6a50023b6597b4c73f7c8a6edf1bf15689254c3030e49379b3b`  
		Last Modified: Thu, 05 Jun 2025 23:02:42 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4546e8211fc088c3925f2b673074dc5a6d27527caf92983c56600ac02ceec30`  
		Last Modified: Thu, 05 Jun 2025 23:02:45 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:281c5b22c80200de8cb5cd27b59777a1a0c02818b3d09d937cc6ff99e29f8305`  
		Last Modified: Thu, 05 Jun 2025 23:08:07 GMT  
		Size: 22.1 MB (22061869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.20348.3692; amd64

```console
$ docker pull docker@sha256:213ffc624913105fa7ee59720002de6a40b9768db21a5d09ec3f292a45573596
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2338596324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af09b10c562d5ce89c47cb4db81986d086849844eb9ea5e334925da4e6e60501`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Thu, 05 Jun 2025 22:44:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 05 Jun 2025 22:46:25 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 05 Jun 2025 22:46:26 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 05 Jun 2025 22:46:27 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.2.2.zip
# Thu, 05 Jun 2025 22:46:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 05 Jun 2025 22:46:51 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 05 Jun 2025 22:46:52 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Thu, 05 Jun 2025 22:46:52 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Thu, 05 Jun 2025 22:47:01 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 05 Jun 2025 22:47:02 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.0
# Thu, 05 Jun 2025 22:47:02 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-windows-x86_64.exe
# Thu, 05 Jun 2025 22:47:03 GMT
ENV DOCKER_COMPOSE_SHA256=5ddd1ff588eb7251381cf6257b9be44fbb92c02d984ccfc94b4280e8c33d0f8f
# Thu, 05 Jun 2025 22:47:14 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Thu, 15 May 2025 19:25:06 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69792782d0247e3e22c67f6096a5c5ac4096e3039e9902b31095ada21a3a3992`  
		Last Modified: Thu, 05 Jun 2025 22:47:55 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1528406f9d6a747555a27165ae52a9ade5da9bafe09faedc813fc9978410ebb1`  
		Last Modified: Thu, 05 Jun 2025 22:47:57 GMT  
		Size: 347.0 KB (347048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44599b0e57d9512be310c8211fc1db3c2b2f26d186b1f4fa5f41cb3239e83e08`  
		Last Modified: Thu, 05 Jun 2025 22:47:57 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5946a2c5ebb15f702288c926ad33ec3e48dc514e959828483bf2515343b8164`  
		Last Modified: Thu, 05 Jun 2025 22:47:58 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5950ebf7245c1e012f8bedfc8e4f944900fbb4429057e997700cbfc430e71db`  
		Last Modified: Thu, 05 Jun 2025 23:08:02 GMT  
		Size: 20.4 MB (20407814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e4979217510eb7de8d35cf3a6a4ea0d48a38fccd55990459ede40e90555a91`  
		Last Modified: Thu, 05 Jun 2025 22:50:52 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bee3bf1d9c1e36c3c62244bbf0b25abd4d3848230da86f8eb7ab9e87bfcce25`  
		Last Modified: Thu, 05 Jun 2025 22:50:55 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dd6d131f13751da51b0a0640902b80152d4626d65b68249d48306530f6af710`  
		Last Modified: Thu, 05 Jun 2025 22:50:58 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809edd0f0043024cc3f263278554b9d43f0af10b1ff965b9e755e7f504cc9448`  
		Last Modified: Thu, 05 Jun 2025 23:08:01 GMT  
		Size: 22.2 MB (22218481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3644edf37145bf3243218f63e04734da0ee41b17a3db4580ac428852159a95b4`  
		Last Modified: Thu, 05 Jun 2025 22:51:01 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f3f405f8fc75b4dbb8e568437773842a367615ed3dbe41b6be647fdbcb3756e`  
		Last Modified: Thu, 05 Jun 2025 22:51:04 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4701c8fc8cca7fb8a5a1d7d575fa186deff56c45e248857b3ed475c698ed20c8`  
		Last Modified: Thu, 05 Jun 2025 22:51:08 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b4da056663f41259b84270c9d8dc6b48fb2b7d53922c07335a68a8dc178b488`  
		Last Modified: Thu, 05 Jun 2025 23:08:02 GMT  
		Size: 22.0 MB (21983289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:bc2b0152ecb9f33a768c3b3a7ba14c8206d2b7f60077c28a3546b40efb6dd9c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull docker@sha256:213ffc624913105fa7ee59720002de6a40b9768db21a5d09ec3f292a45573596
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2338596324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af09b10c562d5ce89c47cb4db81986d086849844eb9ea5e334925da4e6e60501`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Thu, 05 Jun 2025 22:44:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 05 Jun 2025 22:46:25 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 05 Jun 2025 22:46:26 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 05 Jun 2025 22:46:27 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.2.2.zip
# Thu, 05 Jun 2025 22:46:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 05 Jun 2025 22:46:51 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 05 Jun 2025 22:46:52 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Thu, 05 Jun 2025 22:46:52 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Thu, 05 Jun 2025 22:47:01 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 05 Jun 2025 22:47:02 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.0
# Thu, 05 Jun 2025 22:47:02 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-windows-x86_64.exe
# Thu, 05 Jun 2025 22:47:03 GMT
ENV DOCKER_COMPOSE_SHA256=5ddd1ff588eb7251381cf6257b9be44fbb92c02d984ccfc94b4280e8c33d0f8f
# Thu, 05 Jun 2025 22:47:14 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Thu, 15 May 2025 19:25:06 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69792782d0247e3e22c67f6096a5c5ac4096e3039e9902b31095ada21a3a3992`  
		Last Modified: Thu, 05 Jun 2025 22:47:55 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1528406f9d6a747555a27165ae52a9ade5da9bafe09faedc813fc9978410ebb1`  
		Last Modified: Thu, 05 Jun 2025 22:47:57 GMT  
		Size: 347.0 KB (347048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44599b0e57d9512be310c8211fc1db3c2b2f26d186b1f4fa5f41cb3239e83e08`  
		Last Modified: Thu, 05 Jun 2025 22:47:57 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5946a2c5ebb15f702288c926ad33ec3e48dc514e959828483bf2515343b8164`  
		Last Modified: Thu, 05 Jun 2025 22:47:58 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5950ebf7245c1e012f8bedfc8e4f944900fbb4429057e997700cbfc430e71db`  
		Last Modified: Thu, 05 Jun 2025 23:08:02 GMT  
		Size: 20.4 MB (20407814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e4979217510eb7de8d35cf3a6a4ea0d48a38fccd55990459ede40e90555a91`  
		Last Modified: Thu, 05 Jun 2025 22:50:52 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bee3bf1d9c1e36c3c62244bbf0b25abd4d3848230da86f8eb7ab9e87bfcce25`  
		Last Modified: Thu, 05 Jun 2025 22:50:55 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dd6d131f13751da51b0a0640902b80152d4626d65b68249d48306530f6af710`  
		Last Modified: Thu, 05 Jun 2025 22:50:58 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809edd0f0043024cc3f263278554b9d43f0af10b1ff965b9e755e7f504cc9448`  
		Last Modified: Thu, 05 Jun 2025 23:08:01 GMT  
		Size: 22.2 MB (22218481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3644edf37145bf3243218f63e04734da0ee41b17a3db4580ac428852159a95b4`  
		Last Modified: Thu, 05 Jun 2025 22:51:01 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f3f405f8fc75b4dbb8e568437773842a367615ed3dbe41b6be647fdbcb3756e`  
		Last Modified: Thu, 05 Jun 2025 22:51:04 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4701c8fc8cca7fb8a5a1d7d575fa186deff56c45e248857b3ed475c698ed20c8`  
		Last Modified: Thu, 05 Jun 2025 22:51:08 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b4da056663f41259b84270c9d8dc6b48fb2b7d53922c07335a68a8dc178b488`  
		Last Modified: Thu, 05 Jun 2025 23:08:02 GMT  
		Size: 22.0 MB (21983289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:5f0071c24f8a2426413b698206c5a415be20f1024483d31ea54cd904e41465df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4061; amd64

### `docker:windowsservercore-ltsc2025` - windows version 10.0.26100.4061; amd64

```console
$ docker pull docker@sha256:25b529d707052438ef4b12929192d89e568c602554eff61b838530e3ba0862d0
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3496004439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5af2557ed6bf90b5a556401cda31f5e80c741723bd7d8d8dd85f75c9edb2beee`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 10 May 2025 01:13:32 GMT
RUN Install update 10.0.26100.4061
# Thu, 05 Jun 2025 22:49:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 05 Jun 2025 22:49:27 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 05 Jun 2025 22:49:29 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 05 Jun 2025 22:49:31 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.2.2.zip
# Thu, 05 Jun 2025 22:49:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 05 Jun 2025 22:49:45 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 05 Jun 2025 22:49:46 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Thu, 05 Jun 2025 22:49:48 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Thu, 05 Jun 2025 22:50:00 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 05 Jun 2025 22:50:02 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.0
# Thu, 05 Jun 2025 22:50:03 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-windows-x86_64.exe
# Thu, 05 Jun 2025 22:50:04 GMT
ENV DOCKER_COMPOSE_SHA256=5ddd1ff588eb7251381cf6257b9be44fbb92c02d984ccfc94b4280e8c33d0f8f
# Thu, 05 Jun 2025 22:50:15 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc834e13e71633c2d66ec6513d57c31a3157fc5933859d492ecf45fc8a7476c3`  
		Last Modified: Thu, 15 May 2025 19:25:03 GMT  
		Size: 1.2 GB (1215458626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90e49ef0e985b81e99d8b31a019b88aee89866bfb5c61dca46c36db719f75f72`  
		Last Modified: Thu, 05 Jun 2025 22:54:09 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35e4e87c87497c1f6d87a7f50d5b5d0f1d0cc7d219c6ce8eafc2a68e833177e3`  
		Last Modified: Thu, 05 Jun 2025 22:54:10 GMT  
		Size: 389.0 KB (389032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc34a02ab083801559a9993b8b75ebf1889f6ee4406ace24d67068a1db6d394`  
		Last Modified: Thu, 05 Jun 2025 22:54:09 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460eb4eabe732c14d4ba4780e91bfae9ce2f88f06d471caa6eaec23d33259db7`  
		Last Modified: Thu, 05 Jun 2025 22:54:10 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48921f27b31821d44d89e3376996fbcef78628b7c234b417f58afb6186212ee6`  
		Last Modified: Thu, 05 Jun 2025 22:54:12 GMT  
		Size: 20.5 MB (20482824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3fa9bcfc9c100af95e701bc8db63daa6762e21200bcbcfeacf780ceff4ac0a5`  
		Last Modified: Thu, 05 Jun 2025 23:02:29 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f73ddc322ec88bd49ef2ed8da74c0a7037d94bb1649764c3a424b89b9ba72f5`  
		Last Modified: Thu, 05 Jun 2025 23:02:32 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bee619612444d3cd3f98593f7912090ea8ebeaa7537f88e6ef0df6381f43660`  
		Last Modified: Thu, 05 Jun 2025 23:08:02 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aab9f1404ae5f4d3919e9d9b3989dc637b5461c0d61a0a8914464ac3efef61c`  
		Last Modified: Thu, 05 Jun 2025 23:08:03 GMT  
		Size: 22.3 MB (22293165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ffe3877611fd0a573d09a62990e99adc779e2ecfb7a0a99352b6097f1aedfa`  
		Last Modified: Thu, 05 Jun 2025 23:02:39 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c74c3be6ed0d6a50023b6597b4c73f7c8a6edf1bf15689254c3030e49379b3b`  
		Last Modified: Thu, 05 Jun 2025 23:02:42 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4546e8211fc088c3925f2b673074dc5a6d27527caf92983c56600ac02ceec30`  
		Last Modified: Thu, 05 Jun 2025 23:02:45 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:281c5b22c80200de8cb5cd27b59777a1a0c02818b3d09d937cc6ff99e29f8305`  
		Last Modified: Thu, 05 Jun 2025 23:08:07 GMT  
		Size: 22.1 MB (22061869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
