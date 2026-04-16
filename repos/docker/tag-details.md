<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `docker`

-	[`docker:29`](#docker29)
-	[`docker:29-cli`](#docker29-cli)
-	[`docker:29-dind`](#docker29-dind)
-	[`docker:29-dind-rootless`](#docker29-dind-rootless)
-	[`docker:29-windowsservercore`](#docker29-windowsservercore)
-	[`docker:29-windowsservercore-ltsc2022`](#docker29-windowsservercore-ltsc2022)
-	[`docker:29-windowsservercore-ltsc2025`](#docker29-windowsservercore-ltsc2025)
-	[`docker:29.4`](#docker294)
-	[`docker:29.4-cli`](#docker294-cli)
-	[`docker:29.4-dind`](#docker294-dind)
-	[`docker:29.4-dind-rootless`](#docker294-dind-rootless)
-	[`docker:29.4-windowsservercore`](#docker294-windowsservercore)
-	[`docker:29.4-windowsservercore-ltsc2022`](#docker294-windowsservercore-ltsc2022)
-	[`docker:29.4-windowsservercore-ltsc2025`](#docker294-windowsservercore-ltsc2025)
-	[`docker:29.4.0`](#docker2940)
-	[`docker:29.4.0-alpine3.23`](#docker2940-alpine323)
-	[`docker:29.4.0-cli`](#docker2940-cli)
-	[`docker:29.4.0-cli-alpine3.23`](#docker2940-cli-alpine323)
-	[`docker:29.4.0-dind`](#docker2940-dind)
-	[`docker:29.4.0-dind-alpine3.23`](#docker2940-dind-alpine323)
-	[`docker:29.4.0-dind-rootless`](#docker2940-dind-rootless)
-	[`docker:29.4.0-windowsservercore`](#docker2940-windowsservercore)
-	[`docker:29.4.0-windowsservercore-ltsc2022`](#docker2940-windowsservercore-ltsc2022)
-	[`docker:29.4.0-windowsservercore-ltsc2025`](#docker2940-windowsservercore-ltsc2025)
-	[`docker:cli`](#dockercli)
-	[`docker:dind`](#dockerdind)
-	[`docker:dind-rootless`](#dockerdind-rootless)
-	[`docker:latest`](#dockerlatest)
-	[`docker:windowsservercore`](#dockerwindowsservercore)
-	[`docker:windowsservercore-ltsc2022`](#dockerwindowsservercore-ltsc2022)
-	[`docker:windowsservercore-ltsc2025`](#dockerwindowsservercore-ltsc2025)

## `docker:29`

```console
$ docker pull docker@sha256:a6dd5322747a95cd8e3207bd8d415a8fd20ec34e9c00f06dc019cbd912013489
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
$ docker pull docker@sha256:4d2c6e334de4b26d492c0a8cc5438e3dbf1a02eee899fc0d4d39b96202c943a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.5 MB (140522901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:304d326357dcfc523ea9ea01226e742f15d0d548d8eaec0e14c3b39387303000`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:16:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 15 Apr 2026 20:16:25 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 15 Apr 2026 20:16:25 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 15 Apr 2026 20:16:27 GMT
ENV DOCKER_VERSION=29.4.0
# Wed, 15 Apr 2026 20:16:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 15 Apr 2026 20:16:27 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Wed, 15 Apr 2026 20:16:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 15 Apr 2026 20:16:28 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 15 Apr 2026 20:16:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 15 Apr 2026 20:16:29 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 15 Apr 2026 20:16:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:16:29 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Apr 2026 20:16:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 15 Apr 2026 20:16:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:16:30 GMT
CMD ["sh"]
# Wed, 15 Apr 2026 21:19:01 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 15 Apr 2026 21:19:02 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 15 Apr 2026 21:19:02 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 15 Apr 2026 21:19:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 15 Apr 2026 21:19:05 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 15 Apr 2026 21:19:05 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 15 Apr 2026 21:19:05 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:19:05 GMT
VOLUME [/var/lib/docker]
# Wed, 15 Apr 2026 21:19:05 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 15 Apr 2026 21:19:05 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 15 Apr 2026 21:19:05 GMT
CMD []
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00fef3bc4d7adc06c42d060d3a4fad2da6d129c5d2dac575a0a34e5276837acc`  
		Last Modified: Wed, 15 Apr 2026 20:16:37 GMT  
		Size: 8.4 MB (8390330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f8bdd90a189e988440fcec9f3b420d55047950b5f7601ba0e57b351852d7ba`  
		Last Modified: Wed, 15 Apr 2026 20:16:36 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4985eb1bbbfe749a8493542e038307f004a28671974b2a082ae06f9391c4aa64`  
		Last Modified: Wed, 15 Apr 2026 20:16:37 GMT  
		Size: 19.5 MB (19464794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859abcc7688b1a7cc3cc9e144132fc9069de384c58f57dcdc67bb82efa576352`  
		Last Modified: Wed, 15 Apr 2026 20:16:37 GMT  
		Size: 22.5 MB (22539232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c99a167aeca4fe59d6c36fcd7dd693309a219446eca7bcdc04b392e4d69c2c4`  
		Last Modified: Wed, 15 Apr 2026 20:16:38 GMT  
		Size: 11.0 MB (10955103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e81a750c9b2d394bb0113dc9e2ac999fdb73fc198aee986c23671ccc8b782c`  
		Last Modified: Wed, 15 Apr 2026 20:16:38 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ba37c8df4e2fbeeea282fc985c366a9d438cb9ac52b521a1ba48cc214ddd6c`  
		Last Modified: Wed, 15 Apr 2026 20:16:39 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26929be3c972c7f0a15b08c4029aaa790ccc1d494702813df05e37cf6c95ece4`  
		Last Modified: Wed, 15 Apr 2026 20:16:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72409ebb253eee0d0ac41d3def31dd521fd7fbb44646380257fce88e92956e1b`  
		Last Modified: Wed, 15 Apr 2026 21:19:16 GMT  
		Size: 6.9 MB (6941794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61b7bb0bfe4127ecc181695a6617bce6875877794291f6f411f1503400774934`  
		Last Modified: Wed, 15 Apr 2026 21:19:15 GMT  
		Size: 92.4 KB (92386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f322cdda1c007efd5a7874085a0a278df1d8cba0c79c539cecdfd441528c5063`  
		Last Modified: Wed, 15 Apr 2026 21:19:16 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b195c7fa897ae20e300894f9c01ab27baa6d026f2966d14da47768c0504f7e0d`  
		Last Modified: Wed, 15 Apr 2026 21:19:18 GMT  
		Size: 68.3 MB (68266921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d71ba441d54fb7122eab57ffb2e5cc6805c4abe5aa1229a369d61713d35c4a`  
		Last Modified: Wed, 15 Apr 2026 21:19:17 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471eb30b983e8a0f853e3d3be9271df608fd2048cec340fa2eaef5e93dccfdd6`  
		Last Modified: Wed, 15 Apr 2026 21:19:17 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:1c8aa5173659195543e7f2199b877ec50c9f568416a96a31cd42b2fcd07923ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36f6b76c4e162e68e3741832b1fa66576d6705a81ed60bdeeded8cbffb74e2ff`

```dockerfile
```

-	Layers:
	-	`sha256:4c3c193ad694d685d8594f91321d9d1fe73498db66cfb3767583e03cba34f0eb`  
		Last Modified: Wed, 15 Apr 2026 21:19:15 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29` - linux; arm variant v6

```console
$ docker pull docker@sha256:b23cae1ff183bc4e75d88eaf9ba1c6549849f1d134d11fc442d0f885b1f58d4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 MB (132507536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c664d0b218f2b2a9a4e105a5162c0ba967e6162e60df351421a2b174c2b02b2f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:11:18 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 15 Apr 2026 20:11:18 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 15 Apr 2026 20:11:18 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 15 Apr 2026 20:11:22 GMT
ENV DOCKER_VERSION=29.4.0
# Wed, 15 Apr 2026 20:11:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 15 Apr 2026 20:11:22 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Wed, 15 Apr 2026 20:11:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 15 Apr 2026 20:11:25 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 15 Apr 2026 20:11:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 15 Apr 2026 20:11:27 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 15 Apr 2026 20:11:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:11:27 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Apr 2026 20:11:27 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 15 Apr 2026 20:11:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:11:27 GMT
CMD ["sh"]
# Wed, 15 Apr 2026 21:19:39 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 15 Apr 2026 21:19:40 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 15 Apr 2026 21:19:40 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 15 Apr 2026 21:19:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 15 Apr 2026 21:19:44 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 15 Apr 2026 21:19:44 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 15 Apr 2026 21:19:44 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:19:44 GMT
VOLUME [/var/lib/docker]
# Wed, 15 Apr 2026 21:19:44 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 15 Apr 2026 21:19:44 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 15 Apr 2026 21:19:44 GMT
CMD []
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e29b5a067225f28735c3f9c28db7a022b344731761dc5bd14d0b7a283cc13aa1`  
		Last Modified: Wed, 15 Apr 2026 20:11:34 GMT  
		Size: 8.3 MB (8297061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae71f1757016712f17b7c9321ecac9183912e0037f929b5050fa04410093a993`  
		Last Modified: Wed, 15 Apr 2026 20:11:33 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64a558c789f63340dd86a3d8d48163d7ca0b3475c2b5c1d8ca27e0afc43f81a`  
		Last Modified: Wed, 15 Apr 2026 20:11:35 GMT  
		Size: 18.1 MB (18109476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03bc6071f6b066b797f80197a5147fa49e7c18d34820ebbd67e8a05f503815a0`  
		Last Modified: Wed, 15 Apr 2026 20:11:35 GMT  
		Size: 21.2 MB (21151872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84372c97713792c82b059361309092a10362cb4b047854a0b862c3ebeb6f45a7`  
		Last Modified: Wed, 15 Apr 2026 20:11:35 GMT  
		Size: 10.4 MB (10388823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1411d774c190d6fe75a26c80337ed792c1219b393396b9dd4008440601b2e8bb`  
		Last Modified: Wed, 15 Apr 2026 20:11:36 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:213ded2f75d406b851e7f9d90ac09eacb9ecd070136e9e64a5e44a7b62246ab0`  
		Last Modified: Wed, 15 Apr 2026 20:11:36 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9546667a8b53db55a0c88114559b89b5a4c5288c765a0efd17abf18956634f`  
		Last Modified: Wed, 15 Apr 2026 20:11:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db0f2e08cd52770499a4a7b14b1d7035c2bed565f5d1658d36f77ba8cae62ad5`  
		Last Modified: Wed, 15 Apr 2026 21:19:55 GMT  
		Size: 7.3 MB (7278394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810c7f3c3226c75491d45b3028f6aa4e32c04edce7619e9c304e5c7054c6e3e8`  
		Last Modified: Wed, 15 Apr 2026 21:19:55 GMT  
		Size: 91.7 KB (91683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80b9397e0c604f4cffa37ef63fc68b0849fbe399433ee3b1b24e32ea5c1b6138`  
		Last Modified: Wed, 15 Apr 2026 21:19:55 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:578128484de3ef92c76816591ca072998f01b1381725e18fd1c7a4baa20bc9f8`  
		Last Modified: Wed, 15 Apr 2026 21:19:56 GMT  
		Size: 63.6 MB (63610209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2209085b94038497f0af62b68d75961a5b080cb35551dcc8d0eefab6b722484a`  
		Last Modified: Wed, 15 Apr 2026 21:19:56 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b27ed318c8e6661d6fa40585004daf813302e8af45e485fdf0173af3947bc2`  
		Last Modified: Wed, 15 Apr 2026 21:19:56 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:a01657f9a7e1e95bc00dd7bf0d40d8f4e73263519d316ff513e77cd827e24f6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48c770ff5e3d911a2d76c733a01cc1a9e96597d1aeb12c3470e57cf12936aa28`

```dockerfile
```

-	Layers:
	-	`sha256:147b649936864607c8d1c5530d9427c37768a5718de420c9941b6f3b6625b9d5`  
		Last Modified: Wed, 15 Apr 2026 21:19:54 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29` - linux; arm variant v7

```console
$ docker pull docker@sha256:20d1ab4a0712e057c1adc25f5703a97b31a7f387b43adc77bb7308d4397970e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130593641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ca74a271ab95685bc02e667fcb161e01b626e71e3d25886e49bfab8239d7ded`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:16:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 15 Apr 2026 20:16:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 15 Apr 2026 20:16:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 15 Apr 2026 20:16:18 GMT
ENV DOCKER_VERSION=29.4.0
# Wed, 15 Apr 2026 20:16:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 15 Apr 2026 20:16:18 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Wed, 15 Apr 2026 20:16:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 15 Apr 2026 20:16:20 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 15 Apr 2026 20:16:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 15 Apr 2026 20:16:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 15 Apr 2026 20:16:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:16:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Apr 2026 20:16:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 15 Apr 2026 20:16:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:16:22 GMT
CMD ["sh"]
# Wed, 15 Apr 2026 21:27:26 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 15 Apr 2026 21:27:28 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 15 Apr 2026 21:27:28 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 15 Apr 2026 21:27:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 15 Apr 2026 21:27:31 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 15 Apr 2026 21:27:31 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 15 Apr 2026 21:27:31 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:27:31 GMT
VOLUME [/var/lib/docker]
# Wed, 15 Apr 2026 21:27:31 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 15 Apr 2026 21:27:31 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 15 Apr 2026 21:27:31 GMT
CMD []
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88cb38943f0f0a95a9ef76158143c405f36bad50621b2fd56aa2fc4f3615fd5`  
		Last Modified: Wed, 15 Apr 2026 20:16:29 GMT  
		Size: 7.6 MB (7595768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaaca956ad170283b847286ec873bec980d796519baf3f39fe964aded5374f8e`  
		Last Modified: Wed, 15 Apr 2026 20:16:28 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cdf1c13c7d0f067c56c9771266f9895d1041ebf30f39ab27603e18afb0c9081`  
		Last Modified: Wed, 15 Apr 2026 20:16:29 GMT  
		Size: 18.1 MB (18096362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813eda9384408e479910e06a79744324e1dce0b63fd42e5bce661a6e735e2f32`  
		Last Modified: Wed, 15 Apr 2026 20:16:29 GMT  
		Size: 21.1 MB (21129758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f4b664cfcad12fa1a9762a191ac3534cf78c30dd9df6eff79f75e17bd604215`  
		Last Modified: Wed, 15 Apr 2026 20:16:30 GMT  
		Size: 10.4 MB (10371870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f3580f46ae276e11707530d3b18cc55414bcb1f7a672d3cef371193e0e0947`  
		Last Modified: Wed, 15 Apr 2026 20:16:30 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d214a288fe8f0a47169af907737952cefa9e61f078490a75828a439107530b2`  
		Last Modified: Wed, 15 Apr 2026 20:16:31 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf0d872d260394713b2443444bb53d508d83624734c0239dcda7ff1830303db8`  
		Last Modified: Wed, 15 Apr 2026 20:16:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89db5f2f3e615ce6454e5c1c42292805de5a924c4769cb726472a5f992eef448`  
		Last Modified: Wed, 15 Apr 2026 21:27:42 GMT  
		Size: 6.6 MB (6577217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a486198c8f3ba2ab5d5c0c2444157dbdb3a24ef48b6dcbe399e92e72a5e6c28`  
		Last Modified: Wed, 15 Apr 2026 21:27:42 GMT  
		Size: 88.0 KB (88036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba24e0fe682bf1faf33f78d5b19ecad454f21527c9a6c33cfb4c1d694b52779`  
		Last Modified: Wed, 15 Apr 2026 21:27:42 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ca224f3bf33d1172adfccf0c242f89893fde617bd5885ef7545ecd22e41ef4f`  
		Last Modified: Wed, 15 Apr 2026 21:27:44 GMT  
		Size: 63.4 MB (63443351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac3934cb427133bc539854b45e314e2dc44838a979414cf67dd89810b967f06`  
		Last Modified: Wed, 15 Apr 2026 21:27:43 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5e8455627c95fe22aa58fead7cbf2a0934fd4d57d760756577ec0b8c9bf4bc`  
		Last Modified: Wed, 15 Apr 2026 21:27:43 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:9376e04ebe10bd90bf0a7a85bddeb4c723ab3c8e9ae5290a6f522143cdbed03d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58ce25b3cedf687af0bcb158bb0a1d2a8523dfeadcddc68360fc3394f815f730`

```dockerfile
```

-	Layers:
	-	`sha256:ecdd6391528d66bfad436f41aef96daa292510a5ddd3f115f031dd1728b3dd36`  
		Last Modified: Wed, 15 Apr 2026 21:27:42 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:553d694bc3ae2a92b67b73072e3923a8d2256e609b568c60d08e4544e8f39ff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.1 MB (130126872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5c1c78f7262d1e00eef13317919dc25b6d65c96115e46f851ab09818f2ddf0b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:13:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 15 Apr 2026 20:13:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 15 Apr 2026 20:13:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 15 Apr 2026 20:14:02 GMT
ENV DOCKER_VERSION=29.4.0
# Wed, 15 Apr 2026 20:14:02 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 15 Apr 2026 20:14:02 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Wed, 15 Apr 2026 20:14:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 15 Apr 2026 20:14:03 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 15 Apr 2026 20:14:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 15 Apr 2026 20:14:04 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 15 Apr 2026 20:14:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:14:04 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Apr 2026 20:14:04 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 15 Apr 2026 20:14:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:14:04 GMT
CMD ["sh"]
# Wed, 15 Apr 2026 21:33:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 15 Apr 2026 21:33:18 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 15 Apr 2026 21:33:18 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 15 Apr 2026 21:33:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 15 Apr 2026 21:33:21 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 15 Apr 2026 21:33:21 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 15 Apr 2026 21:33:21 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:33:21 GMT
VOLUME [/var/lib/docker]
# Wed, 15 Apr 2026 21:33:21 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 15 Apr 2026 21:33:21 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 15 Apr 2026 21:33:21 GMT
CMD []
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1f08e8ea565813fe5c533f3bf89a6fcb79b8ef2eb46e2872f132234aa070cf`  
		Last Modified: Wed, 15 Apr 2026 20:14:10 GMT  
		Size: 8.5 MB (8450092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ff0f79f131dfea84e2ad6ee3723888525425bfc628525e86c3cc1b288bace3`  
		Last Modified: Wed, 15 Apr 2026 20:14:10 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35bf88d1a58dc1d9ced6e216552eef44b2392e515454985dcd3f25372d12693`  
		Last Modified: Wed, 15 Apr 2026 20:14:11 GMT  
		Size: 17.9 MB (17921079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0aa9505e9a0f5469b8905ecd253d1fd12569434350a1c94898126c02a4a9c57`  
		Last Modified: Wed, 15 Apr 2026 20:14:11 GMT  
		Size: 20.5 MB (20453111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ff9179479c44e683ee3838185f58e7d707974096437fdccedcb7b1f316aa35`  
		Last Modified: Wed, 15 Apr 2026 20:14:11 GMT  
		Size: 10.0 MB (9982600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0771ed595b2bb7d830d904c0ed7f259d39bb70d0da784d731a39f7a1ceeacb04`  
		Last Modified: Wed, 15 Apr 2026 20:14:12 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627cec3b548e33f50bcd1682915056d5dfd8e5b28476d6c4842c0eb790b1f954`  
		Last Modified: Wed, 15 Apr 2026 20:14:12 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c67b1b44bc81549ba5caf988b00dabcb0c2ca6cee73ef7d756e26b08b1028e`  
		Last Modified: Wed, 15 Apr 2026 20:14:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c169b754493e049763aeab1727fe430cecafcd9032c4389b3053958aebc360c9`  
		Last Modified: Wed, 15 Apr 2026 21:33:31 GMT  
		Size: 7.2 MB (7219816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbba1f41e162f643c431dbb55a4cfb94284235c55c0c226f2f85fdc2797d7d3`  
		Last Modified: Wed, 15 Apr 2026 21:33:30 GMT  
		Size: 101.2 KB (101171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc3e20cde46cbbd2b898524e10c8ed94082175c8c21daf98b34e7a6006aafee`  
		Last Modified: Wed, 15 Apr 2026 21:33:30 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ae4baf5361489e96a43c6d29d47fdd4eb63dd088b10e8bf91df746925678ea`  
		Last Modified: Wed, 15 Apr 2026 21:33:32 GMT  
		Size: 61.8 MB (61790985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7fa8aac1af219d886ca4026da0a5a043fde1dae9d3e8534dd78f23360b8763`  
		Last Modified: Wed, 15 Apr 2026 21:33:32 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f667dde4f795a12a4a9d7129f07e71678ffec2ae9a15d680f09fd672a64ab154`  
		Last Modified: Wed, 15 Apr 2026 21:33:32 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:71c18f631e3205680e2fcd0ea55f0f373c7fb19de8336794fe07f3d4793786b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48d9407668f8511b7b181ffcfea6ce22705df56aaf20a9dd84a0930f31f6ecf7`

```dockerfile
```

-	Layers:
	-	`sha256:623b2bc83b8d25632b5e152b95570ef2a7af85709fedfa2ae3ed9d312b61c77c`  
		Last Modified: Wed, 15 Apr 2026 21:33:30 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-cli`

```console
$ docker pull docker@sha256:2efe7c8e806b35050def6ba1ba0ddad67b521a0a6d37f4910b3d88f11b495d03
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
$ docker pull docker@sha256:bb21349a52c00b206ad8b5c03fa52023c741c4cf11f269d40d40b9ebaac73d96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65215798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b7281830dcb31636378f562663cd54df1ce82f631d1cd037968aae8c1034bc2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:16:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 15 Apr 2026 20:16:25 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 15 Apr 2026 20:16:25 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 15 Apr 2026 20:16:27 GMT
ENV DOCKER_VERSION=29.4.0
# Wed, 15 Apr 2026 20:16:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 15 Apr 2026 20:16:27 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Wed, 15 Apr 2026 20:16:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 15 Apr 2026 20:16:28 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 15 Apr 2026 20:16:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 15 Apr 2026 20:16:29 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 15 Apr 2026 20:16:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:16:29 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Apr 2026 20:16:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 15 Apr 2026 20:16:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:16:30 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00fef3bc4d7adc06c42d060d3a4fad2da6d129c5d2dac575a0a34e5276837acc`  
		Last Modified: Wed, 15 Apr 2026 20:16:37 GMT  
		Size: 8.4 MB (8390330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f8bdd90a189e988440fcec9f3b420d55047950b5f7601ba0e57b351852d7ba`  
		Last Modified: Wed, 15 Apr 2026 20:16:36 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4985eb1bbbfe749a8493542e038307f004a28671974b2a082ae06f9391c4aa64`  
		Last Modified: Wed, 15 Apr 2026 20:16:37 GMT  
		Size: 19.5 MB (19464794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859abcc7688b1a7cc3cc9e144132fc9069de384c58f57dcdc67bb82efa576352`  
		Last Modified: Wed, 15 Apr 2026 20:16:37 GMT  
		Size: 22.5 MB (22539232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c99a167aeca4fe59d6c36fcd7dd693309a219446eca7bcdc04b392e4d69c2c4`  
		Last Modified: Wed, 15 Apr 2026 20:16:38 GMT  
		Size: 11.0 MB (10955103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e81a750c9b2d394bb0113dc9e2ac999fdb73fc198aee986c23671ccc8b782c`  
		Last Modified: Wed, 15 Apr 2026 20:16:38 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ba37c8df4e2fbeeea282fc985c366a9d438cb9ac52b521a1ba48cc214ddd6c`  
		Last Modified: Wed, 15 Apr 2026 20:16:39 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26929be3c972c7f0a15b08c4029aaa790ccc1d494702813df05e37cf6c95ece4`  
		Last Modified: Wed, 15 Apr 2026 20:16:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:5c727440eaffe25d1a2f89a448a8aeef8118f192ce752f5f55b0e7dcf3bee15d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d4150275339c1686c0b7eab0e338d57f441efecf63ffadf5cfa59dfe3a3e9a0`

```dockerfile
```

-	Layers:
	-	`sha256:083400d83f577b87f30bc974ae857508bdaeb3c56dafaa2a3985dbc6a2be5c32`  
		Last Modified: Wed, 15 Apr 2026 20:16:36 GMT  
		Size: 38.1 KB (38056 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:b0448a7e451eb2df18d117260c232b9064f3b11bd751ac2e603c18bef0289a37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61521248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ab4c337f9a3ba981939d8eb77b75c53cbc28458c647ccce32e93d0f7a99ee4e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:11:18 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 15 Apr 2026 20:11:18 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 15 Apr 2026 20:11:18 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 15 Apr 2026 20:11:22 GMT
ENV DOCKER_VERSION=29.4.0
# Wed, 15 Apr 2026 20:11:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 15 Apr 2026 20:11:22 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Wed, 15 Apr 2026 20:11:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 15 Apr 2026 20:11:25 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 15 Apr 2026 20:11:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 15 Apr 2026 20:11:27 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 15 Apr 2026 20:11:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:11:27 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Apr 2026 20:11:27 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 15 Apr 2026 20:11:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:11:27 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e29b5a067225f28735c3f9c28db7a022b344731761dc5bd14d0b7a283cc13aa1`  
		Last Modified: Wed, 15 Apr 2026 20:11:34 GMT  
		Size: 8.3 MB (8297061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae71f1757016712f17b7c9321ecac9183912e0037f929b5050fa04410093a993`  
		Last Modified: Wed, 15 Apr 2026 20:11:33 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64a558c789f63340dd86a3d8d48163d7ca0b3475c2b5c1d8ca27e0afc43f81a`  
		Last Modified: Wed, 15 Apr 2026 20:11:35 GMT  
		Size: 18.1 MB (18109476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03bc6071f6b066b797f80197a5147fa49e7c18d34820ebbd67e8a05f503815a0`  
		Last Modified: Wed, 15 Apr 2026 20:11:35 GMT  
		Size: 21.2 MB (21151872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84372c97713792c82b059361309092a10362cb4b047854a0b862c3ebeb6f45a7`  
		Last Modified: Wed, 15 Apr 2026 20:11:35 GMT  
		Size: 10.4 MB (10388823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1411d774c190d6fe75a26c80337ed792c1219b393396b9dd4008440601b2e8bb`  
		Last Modified: Wed, 15 Apr 2026 20:11:36 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:213ded2f75d406b851e7f9d90ac09eacb9ecd070136e9e64a5e44a7b62246ab0`  
		Last Modified: Wed, 15 Apr 2026 20:11:36 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9546667a8b53db55a0c88114559b89b5a4c5288c765a0efd17abf18956634f`  
		Last Modified: Wed, 15 Apr 2026 20:11:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:bbcdf7618a730942664487ce478f3a269e4859185ac161e3578319a0f54ff6d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8a566184814fc34593f5137a7bba3c2c3aae7de569de008b69e5efb6fd4f2b8`

```dockerfile
```

-	Layers:
	-	`sha256:34582c23f82fc6f533690de02a4263c869ac6e2e06850e19652639cbf36d4f4c`  
		Last Modified: Wed, 15 Apr 2026 20:11:33 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:75b479961472cf73f0407e0b3c7576c45be650ab0f523fc539f33fde7777f22f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60479031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:254b0d5926521e59075cd4b154a10ba99b2e222f9e1b682d6ef3bda0b94beaef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:16:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 15 Apr 2026 20:16:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 15 Apr 2026 20:16:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 15 Apr 2026 20:16:18 GMT
ENV DOCKER_VERSION=29.4.0
# Wed, 15 Apr 2026 20:16:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 15 Apr 2026 20:16:18 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Wed, 15 Apr 2026 20:16:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 15 Apr 2026 20:16:20 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 15 Apr 2026 20:16:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 15 Apr 2026 20:16:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 15 Apr 2026 20:16:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:16:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Apr 2026 20:16:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 15 Apr 2026 20:16:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:16:22 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88cb38943f0f0a95a9ef76158143c405f36bad50621b2fd56aa2fc4f3615fd5`  
		Last Modified: Wed, 15 Apr 2026 20:16:29 GMT  
		Size: 7.6 MB (7595768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaaca956ad170283b847286ec873bec980d796519baf3f39fe964aded5374f8e`  
		Last Modified: Wed, 15 Apr 2026 20:16:28 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cdf1c13c7d0f067c56c9771266f9895d1041ebf30f39ab27603e18afb0c9081`  
		Last Modified: Wed, 15 Apr 2026 20:16:29 GMT  
		Size: 18.1 MB (18096362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813eda9384408e479910e06a79744324e1dce0b63fd42e5bce661a6e735e2f32`  
		Last Modified: Wed, 15 Apr 2026 20:16:29 GMT  
		Size: 21.1 MB (21129758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f4b664cfcad12fa1a9762a191ac3534cf78c30dd9df6eff79f75e17bd604215`  
		Last Modified: Wed, 15 Apr 2026 20:16:30 GMT  
		Size: 10.4 MB (10371870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f3580f46ae276e11707530d3b18cc55414bcb1f7a672d3cef371193e0e0947`  
		Last Modified: Wed, 15 Apr 2026 20:16:30 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d214a288fe8f0a47169af907737952cefa9e61f078490a75828a439107530b2`  
		Last Modified: Wed, 15 Apr 2026 20:16:31 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf0d872d260394713b2443444bb53d508d83624734c0239dcda7ff1830303db8`  
		Last Modified: Wed, 15 Apr 2026 20:16:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:70f0601152bac7df07b2933f0e46a2774591dbebc7e87523cc02d222b56c86b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e085d1943182e6d53f4b66b7d1654479506a41c31da6cbd8241cba54df3ce900`

```dockerfile
```

-	Layers:
	-	`sha256:368fab9b9711e124e80b9dedf4aa9bea5ba28ad952bacb0003647ef444f12135`  
		Last Modified: Wed, 15 Apr 2026 20:16:28 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:9d3f67fe1f4cf51c084744dec419b466b7075f5b365ef4b9b791187d9c2d4127
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.0 MB (61008901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dea3a61a70d2ba11898616b2f246eaeef9d1c75b7041f2e45826da60d2e47276`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:13:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 15 Apr 2026 20:13:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 15 Apr 2026 20:13:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 15 Apr 2026 20:14:02 GMT
ENV DOCKER_VERSION=29.4.0
# Wed, 15 Apr 2026 20:14:02 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 15 Apr 2026 20:14:02 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Wed, 15 Apr 2026 20:14:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 15 Apr 2026 20:14:03 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 15 Apr 2026 20:14:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 15 Apr 2026 20:14:04 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 15 Apr 2026 20:14:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:14:04 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Apr 2026 20:14:04 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 15 Apr 2026 20:14:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:14:04 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1f08e8ea565813fe5c533f3bf89a6fcb79b8ef2eb46e2872f132234aa070cf`  
		Last Modified: Wed, 15 Apr 2026 20:14:10 GMT  
		Size: 8.5 MB (8450092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ff0f79f131dfea84e2ad6ee3723888525425bfc628525e86c3cc1b288bace3`  
		Last Modified: Wed, 15 Apr 2026 20:14:10 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35bf88d1a58dc1d9ced6e216552eef44b2392e515454985dcd3f25372d12693`  
		Last Modified: Wed, 15 Apr 2026 20:14:11 GMT  
		Size: 17.9 MB (17921079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0aa9505e9a0f5469b8905ecd253d1fd12569434350a1c94898126c02a4a9c57`  
		Last Modified: Wed, 15 Apr 2026 20:14:11 GMT  
		Size: 20.5 MB (20453111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ff9179479c44e683ee3838185f58e7d707974096437fdccedcb7b1f316aa35`  
		Last Modified: Wed, 15 Apr 2026 20:14:11 GMT  
		Size: 10.0 MB (9982600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0771ed595b2bb7d830d904c0ed7f259d39bb70d0da784d731a39f7a1ceeacb04`  
		Last Modified: Wed, 15 Apr 2026 20:14:12 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627cec3b548e33f50bcd1682915056d5dfd8e5b28476d6c4842c0eb790b1f954`  
		Last Modified: Wed, 15 Apr 2026 20:14:12 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c67b1b44bc81549ba5caf988b00dabcb0c2ca6cee73ef7d756e26b08b1028e`  
		Last Modified: Wed, 15 Apr 2026 20:14:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:e021182c1f750cfc367850ea8b786139b8a3c428c84711dcaf82dad470636664
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a194ccda70da01232600045e81eff9a9985e4f5f2d0762a6d6f356e6cff9fe0`

```dockerfile
```

-	Layers:
	-	`sha256:c94d9b9821f47c73547b7085c1041bda87c05335abab499b01c9fcc9f12a80bf`  
		Last Modified: Wed, 15 Apr 2026 20:14:10 GMT  
		Size: 38.3 KB (38258 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-dind`

```console
$ docker pull docker@sha256:a6dd5322747a95cd8e3207bd8d415a8fd20ec34e9c00f06dc019cbd912013489
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
$ docker pull docker@sha256:4d2c6e334de4b26d492c0a8cc5438e3dbf1a02eee899fc0d4d39b96202c943a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.5 MB (140522901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:304d326357dcfc523ea9ea01226e742f15d0d548d8eaec0e14c3b39387303000`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:16:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 15 Apr 2026 20:16:25 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 15 Apr 2026 20:16:25 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 15 Apr 2026 20:16:27 GMT
ENV DOCKER_VERSION=29.4.0
# Wed, 15 Apr 2026 20:16:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 15 Apr 2026 20:16:27 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Wed, 15 Apr 2026 20:16:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 15 Apr 2026 20:16:28 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 15 Apr 2026 20:16:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 15 Apr 2026 20:16:29 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 15 Apr 2026 20:16:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:16:29 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Apr 2026 20:16:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 15 Apr 2026 20:16:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:16:30 GMT
CMD ["sh"]
# Wed, 15 Apr 2026 21:19:01 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 15 Apr 2026 21:19:02 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 15 Apr 2026 21:19:02 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 15 Apr 2026 21:19:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 15 Apr 2026 21:19:05 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 15 Apr 2026 21:19:05 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 15 Apr 2026 21:19:05 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:19:05 GMT
VOLUME [/var/lib/docker]
# Wed, 15 Apr 2026 21:19:05 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 15 Apr 2026 21:19:05 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 15 Apr 2026 21:19:05 GMT
CMD []
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00fef3bc4d7adc06c42d060d3a4fad2da6d129c5d2dac575a0a34e5276837acc`  
		Last Modified: Wed, 15 Apr 2026 20:16:37 GMT  
		Size: 8.4 MB (8390330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f8bdd90a189e988440fcec9f3b420d55047950b5f7601ba0e57b351852d7ba`  
		Last Modified: Wed, 15 Apr 2026 20:16:36 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4985eb1bbbfe749a8493542e038307f004a28671974b2a082ae06f9391c4aa64`  
		Last Modified: Wed, 15 Apr 2026 20:16:37 GMT  
		Size: 19.5 MB (19464794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859abcc7688b1a7cc3cc9e144132fc9069de384c58f57dcdc67bb82efa576352`  
		Last Modified: Wed, 15 Apr 2026 20:16:37 GMT  
		Size: 22.5 MB (22539232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c99a167aeca4fe59d6c36fcd7dd693309a219446eca7bcdc04b392e4d69c2c4`  
		Last Modified: Wed, 15 Apr 2026 20:16:38 GMT  
		Size: 11.0 MB (10955103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e81a750c9b2d394bb0113dc9e2ac999fdb73fc198aee986c23671ccc8b782c`  
		Last Modified: Wed, 15 Apr 2026 20:16:38 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ba37c8df4e2fbeeea282fc985c366a9d438cb9ac52b521a1ba48cc214ddd6c`  
		Last Modified: Wed, 15 Apr 2026 20:16:39 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26929be3c972c7f0a15b08c4029aaa790ccc1d494702813df05e37cf6c95ece4`  
		Last Modified: Wed, 15 Apr 2026 20:16:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72409ebb253eee0d0ac41d3def31dd521fd7fbb44646380257fce88e92956e1b`  
		Last Modified: Wed, 15 Apr 2026 21:19:16 GMT  
		Size: 6.9 MB (6941794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61b7bb0bfe4127ecc181695a6617bce6875877794291f6f411f1503400774934`  
		Last Modified: Wed, 15 Apr 2026 21:19:15 GMT  
		Size: 92.4 KB (92386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f322cdda1c007efd5a7874085a0a278df1d8cba0c79c539cecdfd441528c5063`  
		Last Modified: Wed, 15 Apr 2026 21:19:16 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b195c7fa897ae20e300894f9c01ab27baa6d026f2966d14da47768c0504f7e0d`  
		Last Modified: Wed, 15 Apr 2026 21:19:18 GMT  
		Size: 68.3 MB (68266921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d71ba441d54fb7122eab57ffb2e5cc6805c4abe5aa1229a369d61713d35c4a`  
		Last Modified: Wed, 15 Apr 2026 21:19:17 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471eb30b983e8a0f853e3d3be9271df608fd2048cec340fa2eaef5e93dccfdd6`  
		Last Modified: Wed, 15 Apr 2026 21:19:17 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:1c8aa5173659195543e7f2199b877ec50c9f568416a96a31cd42b2fcd07923ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36f6b76c4e162e68e3741832b1fa66576d6705a81ed60bdeeded8cbffb74e2ff`

```dockerfile
```

-	Layers:
	-	`sha256:4c3c193ad694d685d8594f91321d9d1fe73498db66cfb3767583e03cba34f0eb`  
		Last Modified: Wed, 15 Apr 2026 21:19:15 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:b23cae1ff183bc4e75d88eaf9ba1c6549849f1d134d11fc442d0f885b1f58d4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 MB (132507536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c664d0b218f2b2a9a4e105a5162c0ba967e6162e60df351421a2b174c2b02b2f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:11:18 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 15 Apr 2026 20:11:18 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 15 Apr 2026 20:11:18 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 15 Apr 2026 20:11:22 GMT
ENV DOCKER_VERSION=29.4.0
# Wed, 15 Apr 2026 20:11:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 15 Apr 2026 20:11:22 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Wed, 15 Apr 2026 20:11:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 15 Apr 2026 20:11:25 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 15 Apr 2026 20:11:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 15 Apr 2026 20:11:27 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 15 Apr 2026 20:11:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:11:27 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Apr 2026 20:11:27 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 15 Apr 2026 20:11:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:11:27 GMT
CMD ["sh"]
# Wed, 15 Apr 2026 21:19:39 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 15 Apr 2026 21:19:40 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 15 Apr 2026 21:19:40 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 15 Apr 2026 21:19:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 15 Apr 2026 21:19:44 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 15 Apr 2026 21:19:44 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 15 Apr 2026 21:19:44 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:19:44 GMT
VOLUME [/var/lib/docker]
# Wed, 15 Apr 2026 21:19:44 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 15 Apr 2026 21:19:44 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 15 Apr 2026 21:19:44 GMT
CMD []
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e29b5a067225f28735c3f9c28db7a022b344731761dc5bd14d0b7a283cc13aa1`  
		Last Modified: Wed, 15 Apr 2026 20:11:34 GMT  
		Size: 8.3 MB (8297061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae71f1757016712f17b7c9321ecac9183912e0037f929b5050fa04410093a993`  
		Last Modified: Wed, 15 Apr 2026 20:11:33 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64a558c789f63340dd86a3d8d48163d7ca0b3475c2b5c1d8ca27e0afc43f81a`  
		Last Modified: Wed, 15 Apr 2026 20:11:35 GMT  
		Size: 18.1 MB (18109476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03bc6071f6b066b797f80197a5147fa49e7c18d34820ebbd67e8a05f503815a0`  
		Last Modified: Wed, 15 Apr 2026 20:11:35 GMT  
		Size: 21.2 MB (21151872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84372c97713792c82b059361309092a10362cb4b047854a0b862c3ebeb6f45a7`  
		Last Modified: Wed, 15 Apr 2026 20:11:35 GMT  
		Size: 10.4 MB (10388823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1411d774c190d6fe75a26c80337ed792c1219b393396b9dd4008440601b2e8bb`  
		Last Modified: Wed, 15 Apr 2026 20:11:36 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:213ded2f75d406b851e7f9d90ac09eacb9ecd070136e9e64a5e44a7b62246ab0`  
		Last Modified: Wed, 15 Apr 2026 20:11:36 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9546667a8b53db55a0c88114559b89b5a4c5288c765a0efd17abf18956634f`  
		Last Modified: Wed, 15 Apr 2026 20:11:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db0f2e08cd52770499a4a7b14b1d7035c2bed565f5d1658d36f77ba8cae62ad5`  
		Last Modified: Wed, 15 Apr 2026 21:19:55 GMT  
		Size: 7.3 MB (7278394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810c7f3c3226c75491d45b3028f6aa4e32c04edce7619e9c304e5c7054c6e3e8`  
		Last Modified: Wed, 15 Apr 2026 21:19:55 GMT  
		Size: 91.7 KB (91683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80b9397e0c604f4cffa37ef63fc68b0849fbe399433ee3b1b24e32ea5c1b6138`  
		Last Modified: Wed, 15 Apr 2026 21:19:55 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:578128484de3ef92c76816591ca072998f01b1381725e18fd1c7a4baa20bc9f8`  
		Last Modified: Wed, 15 Apr 2026 21:19:56 GMT  
		Size: 63.6 MB (63610209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2209085b94038497f0af62b68d75961a5b080cb35551dcc8d0eefab6b722484a`  
		Last Modified: Wed, 15 Apr 2026 21:19:56 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b27ed318c8e6661d6fa40585004daf813302e8af45e485fdf0173af3947bc2`  
		Last Modified: Wed, 15 Apr 2026 21:19:56 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:a01657f9a7e1e95bc00dd7bf0d40d8f4e73263519d316ff513e77cd827e24f6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48c770ff5e3d911a2d76c733a01cc1a9e96597d1aeb12c3470e57cf12936aa28`

```dockerfile
```

-	Layers:
	-	`sha256:147b649936864607c8d1c5530d9427c37768a5718de420c9941b6f3b6625b9d5`  
		Last Modified: Wed, 15 Apr 2026 21:19:54 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:20d1ab4a0712e057c1adc25f5703a97b31a7f387b43adc77bb7308d4397970e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130593641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ca74a271ab95685bc02e667fcb161e01b626e71e3d25886e49bfab8239d7ded`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:16:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 15 Apr 2026 20:16:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 15 Apr 2026 20:16:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 15 Apr 2026 20:16:18 GMT
ENV DOCKER_VERSION=29.4.0
# Wed, 15 Apr 2026 20:16:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 15 Apr 2026 20:16:18 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Wed, 15 Apr 2026 20:16:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 15 Apr 2026 20:16:20 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 15 Apr 2026 20:16:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 15 Apr 2026 20:16:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 15 Apr 2026 20:16:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:16:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Apr 2026 20:16:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 15 Apr 2026 20:16:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:16:22 GMT
CMD ["sh"]
# Wed, 15 Apr 2026 21:27:26 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 15 Apr 2026 21:27:28 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 15 Apr 2026 21:27:28 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 15 Apr 2026 21:27:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 15 Apr 2026 21:27:31 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 15 Apr 2026 21:27:31 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 15 Apr 2026 21:27:31 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:27:31 GMT
VOLUME [/var/lib/docker]
# Wed, 15 Apr 2026 21:27:31 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 15 Apr 2026 21:27:31 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 15 Apr 2026 21:27:31 GMT
CMD []
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88cb38943f0f0a95a9ef76158143c405f36bad50621b2fd56aa2fc4f3615fd5`  
		Last Modified: Wed, 15 Apr 2026 20:16:29 GMT  
		Size: 7.6 MB (7595768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaaca956ad170283b847286ec873bec980d796519baf3f39fe964aded5374f8e`  
		Last Modified: Wed, 15 Apr 2026 20:16:28 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cdf1c13c7d0f067c56c9771266f9895d1041ebf30f39ab27603e18afb0c9081`  
		Last Modified: Wed, 15 Apr 2026 20:16:29 GMT  
		Size: 18.1 MB (18096362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813eda9384408e479910e06a79744324e1dce0b63fd42e5bce661a6e735e2f32`  
		Last Modified: Wed, 15 Apr 2026 20:16:29 GMT  
		Size: 21.1 MB (21129758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f4b664cfcad12fa1a9762a191ac3534cf78c30dd9df6eff79f75e17bd604215`  
		Last Modified: Wed, 15 Apr 2026 20:16:30 GMT  
		Size: 10.4 MB (10371870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f3580f46ae276e11707530d3b18cc55414bcb1f7a672d3cef371193e0e0947`  
		Last Modified: Wed, 15 Apr 2026 20:16:30 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d214a288fe8f0a47169af907737952cefa9e61f078490a75828a439107530b2`  
		Last Modified: Wed, 15 Apr 2026 20:16:31 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf0d872d260394713b2443444bb53d508d83624734c0239dcda7ff1830303db8`  
		Last Modified: Wed, 15 Apr 2026 20:16:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89db5f2f3e615ce6454e5c1c42292805de5a924c4769cb726472a5f992eef448`  
		Last Modified: Wed, 15 Apr 2026 21:27:42 GMT  
		Size: 6.6 MB (6577217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a486198c8f3ba2ab5d5c0c2444157dbdb3a24ef48b6dcbe399e92e72a5e6c28`  
		Last Modified: Wed, 15 Apr 2026 21:27:42 GMT  
		Size: 88.0 KB (88036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba24e0fe682bf1faf33f78d5b19ecad454f21527c9a6c33cfb4c1d694b52779`  
		Last Modified: Wed, 15 Apr 2026 21:27:42 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ca224f3bf33d1172adfccf0c242f89893fde617bd5885ef7545ecd22e41ef4f`  
		Last Modified: Wed, 15 Apr 2026 21:27:44 GMT  
		Size: 63.4 MB (63443351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac3934cb427133bc539854b45e314e2dc44838a979414cf67dd89810b967f06`  
		Last Modified: Wed, 15 Apr 2026 21:27:43 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5e8455627c95fe22aa58fead7cbf2a0934fd4d57d760756577ec0b8c9bf4bc`  
		Last Modified: Wed, 15 Apr 2026 21:27:43 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:9376e04ebe10bd90bf0a7a85bddeb4c723ab3c8e9ae5290a6f522143cdbed03d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58ce25b3cedf687af0bcb158bb0a1d2a8523dfeadcddc68360fc3394f815f730`

```dockerfile
```

-	Layers:
	-	`sha256:ecdd6391528d66bfad436f41aef96daa292510a5ddd3f115f031dd1728b3dd36`  
		Last Modified: Wed, 15 Apr 2026 21:27:42 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:553d694bc3ae2a92b67b73072e3923a8d2256e609b568c60d08e4544e8f39ff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.1 MB (130126872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5c1c78f7262d1e00eef13317919dc25b6d65c96115e46f851ab09818f2ddf0b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:13:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 15 Apr 2026 20:13:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 15 Apr 2026 20:13:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 15 Apr 2026 20:14:02 GMT
ENV DOCKER_VERSION=29.4.0
# Wed, 15 Apr 2026 20:14:02 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 15 Apr 2026 20:14:02 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Wed, 15 Apr 2026 20:14:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 15 Apr 2026 20:14:03 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 15 Apr 2026 20:14:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 15 Apr 2026 20:14:04 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 15 Apr 2026 20:14:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:14:04 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Apr 2026 20:14:04 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 15 Apr 2026 20:14:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:14:04 GMT
CMD ["sh"]
# Wed, 15 Apr 2026 21:33:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 15 Apr 2026 21:33:18 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 15 Apr 2026 21:33:18 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 15 Apr 2026 21:33:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 15 Apr 2026 21:33:21 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 15 Apr 2026 21:33:21 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 15 Apr 2026 21:33:21 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:33:21 GMT
VOLUME [/var/lib/docker]
# Wed, 15 Apr 2026 21:33:21 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 15 Apr 2026 21:33:21 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 15 Apr 2026 21:33:21 GMT
CMD []
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1f08e8ea565813fe5c533f3bf89a6fcb79b8ef2eb46e2872f132234aa070cf`  
		Last Modified: Wed, 15 Apr 2026 20:14:10 GMT  
		Size: 8.5 MB (8450092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ff0f79f131dfea84e2ad6ee3723888525425bfc628525e86c3cc1b288bace3`  
		Last Modified: Wed, 15 Apr 2026 20:14:10 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35bf88d1a58dc1d9ced6e216552eef44b2392e515454985dcd3f25372d12693`  
		Last Modified: Wed, 15 Apr 2026 20:14:11 GMT  
		Size: 17.9 MB (17921079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0aa9505e9a0f5469b8905ecd253d1fd12569434350a1c94898126c02a4a9c57`  
		Last Modified: Wed, 15 Apr 2026 20:14:11 GMT  
		Size: 20.5 MB (20453111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ff9179479c44e683ee3838185f58e7d707974096437fdccedcb7b1f316aa35`  
		Last Modified: Wed, 15 Apr 2026 20:14:11 GMT  
		Size: 10.0 MB (9982600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0771ed595b2bb7d830d904c0ed7f259d39bb70d0da784d731a39f7a1ceeacb04`  
		Last Modified: Wed, 15 Apr 2026 20:14:12 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627cec3b548e33f50bcd1682915056d5dfd8e5b28476d6c4842c0eb790b1f954`  
		Last Modified: Wed, 15 Apr 2026 20:14:12 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c67b1b44bc81549ba5caf988b00dabcb0c2ca6cee73ef7d756e26b08b1028e`  
		Last Modified: Wed, 15 Apr 2026 20:14:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c169b754493e049763aeab1727fe430cecafcd9032c4389b3053958aebc360c9`  
		Last Modified: Wed, 15 Apr 2026 21:33:31 GMT  
		Size: 7.2 MB (7219816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbba1f41e162f643c431dbb55a4cfb94284235c55c0c226f2f85fdc2797d7d3`  
		Last Modified: Wed, 15 Apr 2026 21:33:30 GMT  
		Size: 101.2 KB (101171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc3e20cde46cbbd2b898524e10c8ed94082175c8c21daf98b34e7a6006aafee`  
		Last Modified: Wed, 15 Apr 2026 21:33:30 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ae4baf5361489e96a43c6d29d47fdd4eb63dd088b10e8bf91df746925678ea`  
		Last Modified: Wed, 15 Apr 2026 21:33:32 GMT  
		Size: 61.8 MB (61790985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7fa8aac1af219d886ca4026da0a5a043fde1dae9d3e8534dd78f23360b8763`  
		Last Modified: Wed, 15 Apr 2026 21:33:32 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f667dde4f795a12a4a9d7129f07e71678ffec2ae9a15d680f09fd672a64ab154`  
		Last Modified: Wed, 15 Apr 2026 21:33:32 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:71c18f631e3205680e2fcd0ea55f0f373c7fb19de8336794fe07f3d4793786b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48d9407668f8511b7b181ffcfea6ce22705df56aaf20a9dd84a0930f31f6ecf7`

```dockerfile
```

-	Layers:
	-	`sha256:623b2bc83b8d25632b5e152b95570ef2a7af85709fedfa2ae3ed9d312b61c77c`  
		Last Modified: Wed, 15 Apr 2026 21:33:30 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-dind-rootless`

```console
$ docker pull docker@sha256:76944d96ec8f4d759b5c8d9bf5f0787813f278e46aa078ae65338216739cb0fd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:29-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:e89e2c0f44ba58a65f9f9dc8b04aea6ee7f31c76a7ff8048465f2576746fadb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.5 MB (161524750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ceb46e5e927ba19a62569af7c8eb32cbcef000cd7379578db1e3a3e4fe943aa`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:16:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 15 Apr 2026 20:16:25 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 15 Apr 2026 20:16:25 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 15 Apr 2026 20:16:27 GMT
ENV DOCKER_VERSION=29.4.0
# Wed, 15 Apr 2026 20:16:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 15 Apr 2026 20:16:27 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Wed, 15 Apr 2026 20:16:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 15 Apr 2026 20:16:28 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 15 Apr 2026 20:16:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 15 Apr 2026 20:16:29 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 15 Apr 2026 20:16:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:16:29 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Apr 2026 20:16:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 15 Apr 2026 20:16:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:16:30 GMT
CMD ["sh"]
# Wed, 15 Apr 2026 21:19:01 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 15 Apr 2026 21:19:02 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 15 Apr 2026 21:19:02 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 15 Apr 2026 21:19:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 15 Apr 2026 21:19:05 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 15 Apr 2026 21:19:05 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 15 Apr 2026 21:19:05 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:19:05 GMT
VOLUME [/var/lib/docker]
# Wed, 15 Apr 2026 21:19:05 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 15 Apr 2026 21:19:05 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 15 Apr 2026 21:19:05 GMT
CMD []
# Wed, 15 Apr 2026 22:12:18 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Wed, 15 Apr 2026 22:12:18 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 15 Apr 2026 22:12:18 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 15 Apr 2026 22:12:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 15 Apr 2026 22:12:19 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 15 Apr 2026 22:12:19 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 15 Apr 2026 22:12:19 GMT
USER rootless
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00fef3bc4d7adc06c42d060d3a4fad2da6d129c5d2dac575a0a34e5276837acc`  
		Last Modified: Wed, 15 Apr 2026 20:16:37 GMT  
		Size: 8.4 MB (8390330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f8bdd90a189e988440fcec9f3b420d55047950b5f7601ba0e57b351852d7ba`  
		Last Modified: Wed, 15 Apr 2026 20:16:36 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4985eb1bbbfe749a8493542e038307f004a28671974b2a082ae06f9391c4aa64`  
		Last Modified: Wed, 15 Apr 2026 20:16:37 GMT  
		Size: 19.5 MB (19464794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859abcc7688b1a7cc3cc9e144132fc9069de384c58f57dcdc67bb82efa576352`  
		Last Modified: Wed, 15 Apr 2026 20:16:37 GMT  
		Size: 22.5 MB (22539232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c99a167aeca4fe59d6c36fcd7dd693309a219446eca7bcdc04b392e4d69c2c4`  
		Last Modified: Wed, 15 Apr 2026 20:16:38 GMT  
		Size: 11.0 MB (10955103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e81a750c9b2d394bb0113dc9e2ac999fdb73fc198aee986c23671ccc8b782c`  
		Last Modified: Wed, 15 Apr 2026 20:16:38 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ba37c8df4e2fbeeea282fc985c366a9d438cb9ac52b521a1ba48cc214ddd6c`  
		Last Modified: Wed, 15 Apr 2026 20:16:39 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26929be3c972c7f0a15b08c4029aaa790ccc1d494702813df05e37cf6c95ece4`  
		Last Modified: Wed, 15 Apr 2026 20:16:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72409ebb253eee0d0ac41d3def31dd521fd7fbb44646380257fce88e92956e1b`  
		Last Modified: Wed, 15 Apr 2026 21:19:16 GMT  
		Size: 6.9 MB (6941794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61b7bb0bfe4127ecc181695a6617bce6875877794291f6f411f1503400774934`  
		Last Modified: Wed, 15 Apr 2026 21:19:15 GMT  
		Size: 92.4 KB (92386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f322cdda1c007efd5a7874085a0a278df1d8cba0c79c539cecdfd441528c5063`  
		Last Modified: Wed, 15 Apr 2026 21:19:16 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b195c7fa897ae20e300894f9c01ab27baa6d026f2966d14da47768c0504f7e0d`  
		Last Modified: Wed, 15 Apr 2026 21:19:18 GMT  
		Size: 68.3 MB (68266921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d71ba441d54fb7122eab57ffb2e5cc6805c4abe5aa1229a369d61713d35c4a`  
		Last Modified: Wed, 15 Apr 2026 21:19:17 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471eb30b983e8a0f853e3d3be9271df608fd2048cec340fa2eaef5e93dccfdd6`  
		Last Modified: Wed, 15 Apr 2026 21:19:17 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d603a61ab9bf085d4c5ed544ebdc6930cedac60c151b8c3d844ec4a5e1907a3f`  
		Last Modified: Wed, 15 Apr 2026 22:12:32 GMT  
		Size: 3.4 MB (3420096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f6cf84eabf10318aff4902301c0a7eb0d5e3a1fbedc2457d5a03e48ec176798`  
		Last Modified: Wed, 15 Apr 2026 22:12:26 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c7e42a9e418d966d88e75d7076fb61e32f5f036331ad87079c2af72fee32a29`  
		Last Modified: Wed, 15 Apr 2026 22:12:28 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:707634342cc50aaa8f17842865d9fe9c4d140289067e551027f32d44235c5e64`  
		Last Modified: Wed, 15 Apr 2026 22:12:36 GMT  
		Size: 17.6 MB (17580415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5efa74639426aef15709b77e6fe19278595bf047f2e03f5a8449cc234b9df8c2`  
		Last Modified: Wed, 15 Apr 2026 22:12:32 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:16263b4914888c6b7270d1a2b9da8845365aacaafbf2ae86d9c3e093373eb29c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9072388f94ef26c4fd86a7769ed365d8a261d4df812abb3ef6950a2400d130af`

```dockerfile
```

-	Layers:
	-	`sha256:f9339be88cc342b92f34d4da76922c287e26b230e4ebab8ba0b5ce74a00df08b`  
		Last Modified: Wed, 15 Apr 2026 22:12:24 GMT  
		Size: 30.6 KB (30589 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:b4fad2141f6e11611acfc843f2434ba2a41e6915639963b943fa2ba4b51e87d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.4 MB (151405559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95e9af8ffe8cf19d9949f80c4fe0f01db4518273f5f1e3f6470799d230530909`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:13:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 15 Apr 2026 20:13:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 15 Apr 2026 20:13:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 15 Apr 2026 20:14:02 GMT
ENV DOCKER_VERSION=29.4.0
# Wed, 15 Apr 2026 20:14:02 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 15 Apr 2026 20:14:02 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Wed, 15 Apr 2026 20:14:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 15 Apr 2026 20:14:03 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 15 Apr 2026 20:14:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 15 Apr 2026 20:14:04 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 15 Apr 2026 20:14:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:14:04 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Apr 2026 20:14:04 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 15 Apr 2026 20:14:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:14:04 GMT
CMD ["sh"]
# Wed, 15 Apr 2026 21:33:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 15 Apr 2026 21:33:18 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 15 Apr 2026 21:33:18 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 15 Apr 2026 21:33:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 15 Apr 2026 21:33:21 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 15 Apr 2026 21:33:21 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 15 Apr 2026 21:33:21 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:33:21 GMT
VOLUME [/var/lib/docker]
# Wed, 15 Apr 2026 21:33:21 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 15 Apr 2026 21:33:21 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 15 Apr 2026 21:33:21 GMT
CMD []
# Wed, 15 Apr 2026 22:24:13 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Wed, 15 Apr 2026 22:24:13 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 15 Apr 2026 22:24:13 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 15 Apr 2026 22:24:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 15 Apr 2026 22:24:14 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 15 Apr 2026 22:24:14 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 15 Apr 2026 22:24:14 GMT
USER rootless
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1f08e8ea565813fe5c533f3bf89a6fcb79b8ef2eb46e2872f132234aa070cf`  
		Last Modified: Wed, 15 Apr 2026 20:14:10 GMT  
		Size: 8.5 MB (8450092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ff0f79f131dfea84e2ad6ee3723888525425bfc628525e86c3cc1b288bace3`  
		Last Modified: Wed, 15 Apr 2026 20:14:10 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35bf88d1a58dc1d9ced6e216552eef44b2392e515454985dcd3f25372d12693`  
		Last Modified: Wed, 15 Apr 2026 20:14:11 GMT  
		Size: 17.9 MB (17921079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0aa9505e9a0f5469b8905ecd253d1fd12569434350a1c94898126c02a4a9c57`  
		Last Modified: Wed, 15 Apr 2026 20:14:11 GMT  
		Size: 20.5 MB (20453111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ff9179479c44e683ee3838185f58e7d707974096437fdccedcb7b1f316aa35`  
		Last Modified: Wed, 15 Apr 2026 20:14:11 GMT  
		Size: 10.0 MB (9982600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0771ed595b2bb7d830d904c0ed7f259d39bb70d0da784d731a39f7a1ceeacb04`  
		Last Modified: Wed, 15 Apr 2026 20:14:12 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627cec3b548e33f50bcd1682915056d5dfd8e5b28476d6c4842c0eb790b1f954`  
		Last Modified: Wed, 15 Apr 2026 20:14:12 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c67b1b44bc81549ba5caf988b00dabcb0c2ca6cee73ef7d756e26b08b1028e`  
		Last Modified: Wed, 15 Apr 2026 20:14:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c169b754493e049763aeab1727fe430cecafcd9032c4389b3053958aebc360c9`  
		Last Modified: Wed, 15 Apr 2026 21:33:31 GMT  
		Size: 7.2 MB (7219816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbba1f41e162f643c431dbb55a4cfb94284235c55c0c226f2f85fdc2797d7d3`  
		Last Modified: Wed, 15 Apr 2026 21:33:30 GMT  
		Size: 101.2 KB (101171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc3e20cde46cbbd2b898524e10c8ed94082175c8c21daf98b34e7a6006aafee`  
		Last Modified: Wed, 15 Apr 2026 21:33:30 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ae4baf5361489e96a43c6d29d47fdd4eb63dd088b10e8bf91df746925678ea`  
		Last Modified: Wed, 15 Apr 2026 21:33:32 GMT  
		Size: 61.8 MB (61790985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7fa8aac1af219d886ca4026da0a5a043fde1dae9d3e8534dd78f23360b8763`  
		Last Modified: Wed, 15 Apr 2026 21:33:32 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f667dde4f795a12a4a9d7129f07e71678ffec2ae9a15d680f09fd672a64ab154`  
		Last Modified: Wed, 15 Apr 2026 21:33:32 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9012b0d6da5801eab238bb387dbb36b8d6a39d5aa7039815d1c9e2a24833a04`  
		Last Modified: Wed, 15 Apr 2026 22:24:20 GMT  
		Size: 3.4 MB (3394534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:960aa9d16806e38df09387de191ea1c727cc5093bc76be222ed5d2a7ca369379`  
		Last Modified: Wed, 15 Apr 2026 22:24:20 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78adb818d73519733cf9dc2e2f2fdf7f7b19abf1d6a5f6050937e7df4fca78d3`  
		Last Modified: Wed, 15 Apr 2026 22:24:20 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f755f683e7f98d710321e727c122d4fd09ba183d051ff46907c74d640b25fcc8`  
		Last Modified: Wed, 15 Apr 2026 22:24:21 GMT  
		Size: 17.9 MB (17882814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d3922b05d8ff64a19ec81b180d6950d39f6867f3dee697b2c3495cb2625bcc`  
		Last Modified: Wed, 15 Apr 2026 22:24:21 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:bb4750590667d42b5f476e8c84bbfb8c1157d5e39d0a4d73884792417165644b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6910dd353dfd57bed56f7465cd51c75e8b8d0c0213fe745a77273d1d7a3f43c4`

```dockerfile
```

-	Layers:
	-	`sha256:4bfbb83e76361cdb9defcea46dc5c48423a4c288e606987803e7f5ee3edc2883`  
		Last Modified: Wed, 15 Apr 2026 22:24:20 GMT  
		Size: 30.8 KB (30752 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-windowsservercore`

```console
$ docker pull docker@sha256:d74502081e87e340ae439759f8ec2ea8904f7c6d482c2e01ef2d63e4eab78fce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32690; amd64
	-	windows version 10.0.20348.5020; amd64

### `docker:29-windowsservercore` - windows version 10.0.26100.32690; amd64

```console
$ docker pull docker@sha256:d46ee739eeb7f2f3919de6950a0c17a20bb1d22971380a4bb658f91004b6e533
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2185608492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:451cb635e20acafc0c39412eaf4ae9baa78105ff334cffab02ee607ff7e6d625`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Mon, 13 Apr 2026 07:00:46 GMT
RUN Install update 10.0.26100.32690
# Tue, 14 Apr 2026 21:01:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Apr 2026 21:02:06 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Apr 2026 21:02:07 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 14 Apr 2026 21:02:08 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.4.0.zip
# Tue, 14 Apr 2026 21:02:20 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 14 Apr 2026 21:02:20 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 14 Apr 2026 21:02:21 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.windows-amd64.exe
# Tue, 14 Apr 2026 21:02:21 GMT
ENV DOCKER_BUILDX_SHA256=832ddf42373203ee3836a7cb3b16fe5080231491e7edb32019ac0f6fe03b99ed
# Tue, 14 Apr 2026 21:02:35 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 14 Apr 2026 21:02:35 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 14 Apr 2026 21:02:36 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-windows-x86_64.exe
# Tue, 14 Apr 2026 21:02:37 GMT
ENV DOCKER_COMPOSE_SHA256=f7ad2f6965c88153e4902019ec86e95414f0025cba0b6440f328f935a1f8b12b
# Tue, 14 Apr 2026 21:02:43 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3642e4b8bb65ad3768f9f74a0dc48bb2e3294779b5d51573a234bfbe4f65324e`  
		Last Modified: Tue, 14 Apr 2026 18:48:19 GMT  
		Size: 606.9 MB (606926634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68ac02bb5872fbad22e76d99d54ab9b35a1e35759bbddff4f282081ba61100d5`  
		Last Modified: Tue, 14 Apr 2026 21:02:53 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774f3049f1ff5e124ea4f250ee1167ecf42896b3e9bcd067e2f4926ab7a0602d`  
		Last Modified: Tue, 14 Apr 2026 21:02:52 GMT  
		Size: 369.0 KB (368971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae8c2209515b42fd04e40e13a7bca32c3f1f16411393fc4cee562ca8f641bb7`  
		Last Modified: Tue, 14 Apr 2026 21:02:52 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3790546541b36e26bd73f9dfdaf940ebe9fe8013ff0a1cf891fba5e7701b36f`  
		Last Modified: Tue, 14 Apr 2026 21:02:51 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:445fc7e4e770e7d61fdf3492872b7e8bca998a26fffc4515e6344d6952d41f0f`  
		Last Modified: Tue, 14 Apr 2026 21:02:53 GMT  
		Size: 20.2 MB (20155911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b10e1a8a2bc350119623c441e4e0d952f69a7c50a192f764cb4e772b2359ea46`  
		Last Modified: Tue, 14 Apr 2026 21:02:50 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e015ae5429fcbb9151f7c03f83907b5d7d7e627e93ac5666dd54c102cf6f9909`  
		Last Modified: Tue, 14 Apr 2026 21:02:50 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ccf5f62308e0033a83afd116f4287e8951801b466ac66e960370bbd100b0c2b`  
		Last Modified: Tue, 14 Apr 2026 21:02:50 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:308fbcfb831872272d007db361ab5130df2705896b45ad22706bc3ed69a4208b`  
		Last Modified: Tue, 14 Apr 2026 21:02:52 GMT  
		Size: 23.4 MB (23435945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b688d291c4ee097cfa7d6bd989a5730f385d7ed44f7e307e89f8243f044db00a`  
		Last Modified: Tue, 14 Apr 2026 21:02:48 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:391e7d1ca3eae4c8c6acd6553f00297119056613a326ddae9eecb91f055806f4`  
		Last Modified: Tue, 14 Apr 2026 21:02:48 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebbf7aced575c80864697740f99f4f025250da7e7180003679632024cb1987f3`  
		Last Modified: Tue, 14 Apr 2026 21:02:48 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91a6dca9753cc712a25b48c9dbe9e9556c8e7bedfc0f97baf1d62b4cc5503798`  
		Last Modified: Tue, 14 Apr 2026 21:02:50 GMT  
		Size: 11.6 MB (11649820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:29-windowsservercore` - windows version 10.0.20348.5020; amd64

```console
$ docker pull docker@sha256:dfeb15b1635155bf333f2033fd733a796d52ede5fa96f898b11e57c12e2412a0
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2125867669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17085df04e58942536df91898016031a94b7bdce5841470b1904db146ee78bca`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Tue, 14 Apr 2026 20:56:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Apr 2026 20:56:45 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Apr 2026 20:56:47 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 14 Apr 2026 20:56:48 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.4.0.zip
# Tue, 14 Apr 2026 20:57:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 14 Apr 2026 20:57:06 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 14 Apr 2026 20:57:07 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.windows-amd64.exe
# Tue, 14 Apr 2026 20:57:08 GMT
ENV DOCKER_BUILDX_SHA256=832ddf42373203ee3836a7cb3b16fe5080231491e7edb32019ac0f6fe03b99ed
# Tue, 14 Apr 2026 20:57:26 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 14 Apr 2026 20:57:27 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 14 Apr 2026 20:57:27 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-windows-x86_64.exe
# Tue, 14 Apr 2026 20:57:28 GMT
ENV DOCKER_COMPOSE_SHA256=f7ad2f6965c88153e4902019ec86e95414f0025cba0b6440f328f935a1f8b12b
# Tue, 14 Apr 2026 20:57:41 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7111ae68f8961455d230dc12d44c2193d29b7c981e35417323613a0c1aa06384`  
		Last Modified: Tue, 14 Apr 2026 17:31:38 GMT  
		Size: 581.2 MB (581192160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4911c7412282b7f1d93fad64ba92d82b42d1ac47c62c4ff886b516f02ea28a55`  
		Last Modified: Tue, 14 Apr 2026 20:57:50 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:151b1d340c8ca7ccd1a0024ff46837779a87b23f90be4512b66ca317e849176b`  
		Last Modified: Tue, 14 Apr 2026 20:57:49 GMT  
		Size: 468.6 KB (468589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c05f9fed2a2861e1aad93076abf9515f202306cf4c6e381ac7b874a9c1d1196`  
		Last Modified: Tue, 14 Apr 2026 20:57:48 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c7405e2df63bc9fec89f85fb677309b86bf973025d8f6b08da62e988f2a629`  
		Last Modified: Tue, 14 Apr 2026 20:57:48 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7f5562b59f5d6e8946261211a66a4f3d8e26a59a704ca4ac6c6405a3ec5f055`  
		Last Modified: Tue, 14 Apr 2026 20:57:50 GMT  
		Size: 20.1 MB (20130256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6f3b1f33de25d313624bac12844dba1d78714061572c4a74d1fe93ad71ce9ad`  
		Last Modified: Tue, 14 Apr 2026 20:57:46 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b55352e1cad29fb0adf25f61e251a05aa1b8ddefb796d15d4793e871bfbaad`  
		Last Modified: Tue, 14 Apr 2026 20:57:47 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a54c516e756ba1351d4ab57988ca90f91af80ca4cce2b27e45eb8dd2ab1ac579`  
		Last Modified: Tue, 14 Apr 2026 20:57:46 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:935fbf8b04da4242e47da7bfee8df2b984a65ed241ffa13f675e09c528cabf8c`  
		Last Modified: Tue, 14 Apr 2026 20:57:54 GMT  
		Size: 23.4 MB (23419466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c62827bb4e356ec246f0a9426681e101860c87ca41a8081887faa7a911a04b19`  
		Last Modified: Tue, 14 Apr 2026 20:57:45 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:830e8d77d7ec0a09f8111f5d4fbe1b1bc385938ec59812da38a864323c7e4963`  
		Last Modified: Tue, 14 Apr 2026 20:57:45 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2405085b41ebd2fbc5a8f4683c3debadbd731eb6e54352fab4de5f2f74bc187d`  
		Last Modified: Tue, 14 Apr 2026 20:57:45 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5d8306d6e8e4e9eb43d89651b670cda922a16548c151c2bdbb51db4656787e6`  
		Last Modified: Tue, 14 Apr 2026 20:57:47 GMT  
		Size: 11.6 MB (11626371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:bba4a40903cac7bbfad1686d3aef377f0f7294e2311b9da2e962d1cf4526c500
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `docker:29-windowsservercore-ltsc2022` - windows version 10.0.20348.5020; amd64

```console
$ docker pull docker@sha256:dfeb15b1635155bf333f2033fd733a796d52ede5fa96f898b11e57c12e2412a0
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2125867669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17085df04e58942536df91898016031a94b7bdce5841470b1904db146ee78bca`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Tue, 14 Apr 2026 20:56:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Apr 2026 20:56:45 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Apr 2026 20:56:47 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 14 Apr 2026 20:56:48 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.4.0.zip
# Tue, 14 Apr 2026 20:57:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 14 Apr 2026 20:57:06 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 14 Apr 2026 20:57:07 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.windows-amd64.exe
# Tue, 14 Apr 2026 20:57:08 GMT
ENV DOCKER_BUILDX_SHA256=832ddf42373203ee3836a7cb3b16fe5080231491e7edb32019ac0f6fe03b99ed
# Tue, 14 Apr 2026 20:57:26 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 14 Apr 2026 20:57:27 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 14 Apr 2026 20:57:27 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-windows-x86_64.exe
# Tue, 14 Apr 2026 20:57:28 GMT
ENV DOCKER_COMPOSE_SHA256=f7ad2f6965c88153e4902019ec86e95414f0025cba0b6440f328f935a1f8b12b
# Tue, 14 Apr 2026 20:57:41 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7111ae68f8961455d230dc12d44c2193d29b7c981e35417323613a0c1aa06384`  
		Last Modified: Tue, 14 Apr 2026 17:31:38 GMT  
		Size: 581.2 MB (581192160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4911c7412282b7f1d93fad64ba92d82b42d1ac47c62c4ff886b516f02ea28a55`  
		Last Modified: Tue, 14 Apr 2026 20:57:50 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:151b1d340c8ca7ccd1a0024ff46837779a87b23f90be4512b66ca317e849176b`  
		Last Modified: Tue, 14 Apr 2026 20:57:49 GMT  
		Size: 468.6 KB (468589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c05f9fed2a2861e1aad93076abf9515f202306cf4c6e381ac7b874a9c1d1196`  
		Last Modified: Tue, 14 Apr 2026 20:57:48 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c7405e2df63bc9fec89f85fb677309b86bf973025d8f6b08da62e988f2a629`  
		Last Modified: Tue, 14 Apr 2026 20:57:48 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7f5562b59f5d6e8946261211a66a4f3d8e26a59a704ca4ac6c6405a3ec5f055`  
		Last Modified: Tue, 14 Apr 2026 20:57:50 GMT  
		Size: 20.1 MB (20130256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6f3b1f33de25d313624bac12844dba1d78714061572c4a74d1fe93ad71ce9ad`  
		Last Modified: Tue, 14 Apr 2026 20:57:46 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b55352e1cad29fb0adf25f61e251a05aa1b8ddefb796d15d4793e871bfbaad`  
		Last Modified: Tue, 14 Apr 2026 20:57:47 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a54c516e756ba1351d4ab57988ca90f91af80ca4cce2b27e45eb8dd2ab1ac579`  
		Last Modified: Tue, 14 Apr 2026 20:57:46 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:935fbf8b04da4242e47da7bfee8df2b984a65ed241ffa13f675e09c528cabf8c`  
		Last Modified: Tue, 14 Apr 2026 20:57:54 GMT  
		Size: 23.4 MB (23419466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c62827bb4e356ec246f0a9426681e101860c87ca41a8081887faa7a911a04b19`  
		Last Modified: Tue, 14 Apr 2026 20:57:45 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:830e8d77d7ec0a09f8111f5d4fbe1b1bc385938ec59812da38a864323c7e4963`  
		Last Modified: Tue, 14 Apr 2026 20:57:45 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2405085b41ebd2fbc5a8f4683c3debadbd731eb6e54352fab4de5f2f74bc187d`  
		Last Modified: Tue, 14 Apr 2026 20:57:45 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5d8306d6e8e4e9eb43d89651b670cda922a16548c151c2bdbb51db4656787e6`  
		Last Modified: Tue, 14 Apr 2026 20:57:47 GMT  
		Size: 11.6 MB (11626371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:7453a45c03a9501b7dfb80e7846d848c74853c4eed947a7ea01ce577f840a92e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32690; amd64

### `docker:29-windowsservercore-ltsc2025` - windows version 10.0.26100.32690; amd64

```console
$ docker pull docker@sha256:d46ee739eeb7f2f3919de6950a0c17a20bb1d22971380a4bb658f91004b6e533
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2185608492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:451cb635e20acafc0c39412eaf4ae9baa78105ff334cffab02ee607ff7e6d625`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Mon, 13 Apr 2026 07:00:46 GMT
RUN Install update 10.0.26100.32690
# Tue, 14 Apr 2026 21:01:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Apr 2026 21:02:06 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Apr 2026 21:02:07 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 14 Apr 2026 21:02:08 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.4.0.zip
# Tue, 14 Apr 2026 21:02:20 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 14 Apr 2026 21:02:20 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 14 Apr 2026 21:02:21 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.windows-amd64.exe
# Tue, 14 Apr 2026 21:02:21 GMT
ENV DOCKER_BUILDX_SHA256=832ddf42373203ee3836a7cb3b16fe5080231491e7edb32019ac0f6fe03b99ed
# Tue, 14 Apr 2026 21:02:35 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 14 Apr 2026 21:02:35 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 14 Apr 2026 21:02:36 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-windows-x86_64.exe
# Tue, 14 Apr 2026 21:02:37 GMT
ENV DOCKER_COMPOSE_SHA256=f7ad2f6965c88153e4902019ec86e95414f0025cba0b6440f328f935a1f8b12b
# Tue, 14 Apr 2026 21:02:43 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3642e4b8bb65ad3768f9f74a0dc48bb2e3294779b5d51573a234bfbe4f65324e`  
		Last Modified: Tue, 14 Apr 2026 18:48:19 GMT  
		Size: 606.9 MB (606926634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68ac02bb5872fbad22e76d99d54ab9b35a1e35759bbddff4f282081ba61100d5`  
		Last Modified: Tue, 14 Apr 2026 21:02:53 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774f3049f1ff5e124ea4f250ee1167ecf42896b3e9bcd067e2f4926ab7a0602d`  
		Last Modified: Tue, 14 Apr 2026 21:02:52 GMT  
		Size: 369.0 KB (368971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae8c2209515b42fd04e40e13a7bca32c3f1f16411393fc4cee562ca8f641bb7`  
		Last Modified: Tue, 14 Apr 2026 21:02:52 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3790546541b36e26bd73f9dfdaf940ebe9fe8013ff0a1cf891fba5e7701b36f`  
		Last Modified: Tue, 14 Apr 2026 21:02:51 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:445fc7e4e770e7d61fdf3492872b7e8bca998a26fffc4515e6344d6952d41f0f`  
		Last Modified: Tue, 14 Apr 2026 21:02:53 GMT  
		Size: 20.2 MB (20155911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b10e1a8a2bc350119623c441e4e0d952f69a7c50a192f764cb4e772b2359ea46`  
		Last Modified: Tue, 14 Apr 2026 21:02:50 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e015ae5429fcbb9151f7c03f83907b5d7d7e627e93ac5666dd54c102cf6f9909`  
		Last Modified: Tue, 14 Apr 2026 21:02:50 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ccf5f62308e0033a83afd116f4287e8951801b466ac66e960370bbd100b0c2b`  
		Last Modified: Tue, 14 Apr 2026 21:02:50 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:308fbcfb831872272d007db361ab5130df2705896b45ad22706bc3ed69a4208b`  
		Last Modified: Tue, 14 Apr 2026 21:02:52 GMT  
		Size: 23.4 MB (23435945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b688d291c4ee097cfa7d6bd989a5730f385d7ed44f7e307e89f8243f044db00a`  
		Last Modified: Tue, 14 Apr 2026 21:02:48 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:391e7d1ca3eae4c8c6acd6553f00297119056613a326ddae9eecb91f055806f4`  
		Last Modified: Tue, 14 Apr 2026 21:02:48 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebbf7aced575c80864697740f99f4f025250da7e7180003679632024cb1987f3`  
		Last Modified: Tue, 14 Apr 2026 21:02:48 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91a6dca9753cc712a25b48c9dbe9e9556c8e7bedfc0f97baf1d62b4cc5503798`  
		Last Modified: Tue, 14 Apr 2026 21:02:50 GMT  
		Size: 11.6 MB (11649820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.4`

```console
$ docker pull docker@sha256:a6dd5322747a95cd8e3207bd8d415a8fd20ec34e9c00f06dc019cbd912013489
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

### `docker:29.4` - linux; amd64

```console
$ docker pull docker@sha256:4d2c6e334de4b26d492c0a8cc5438e3dbf1a02eee899fc0d4d39b96202c943a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.5 MB (140522901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:304d326357dcfc523ea9ea01226e742f15d0d548d8eaec0e14c3b39387303000`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:16:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 15 Apr 2026 20:16:25 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 15 Apr 2026 20:16:25 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 15 Apr 2026 20:16:27 GMT
ENV DOCKER_VERSION=29.4.0
# Wed, 15 Apr 2026 20:16:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 15 Apr 2026 20:16:27 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Wed, 15 Apr 2026 20:16:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 15 Apr 2026 20:16:28 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 15 Apr 2026 20:16:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 15 Apr 2026 20:16:29 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 15 Apr 2026 20:16:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:16:29 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Apr 2026 20:16:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 15 Apr 2026 20:16:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:16:30 GMT
CMD ["sh"]
# Wed, 15 Apr 2026 21:19:01 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 15 Apr 2026 21:19:02 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 15 Apr 2026 21:19:02 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 15 Apr 2026 21:19:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 15 Apr 2026 21:19:05 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 15 Apr 2026 21:19:05 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 15 Apr 2026 21:19:05 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:19:05 GMT
VOLUME [/var/lib/docker]
# Wed, 15 Apr 2026 21:19:05 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 15 Apr 2026 21:19:05 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 15 Apr 2026 21:19:05 GMT
CMD []
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00fef3bc4d7adc06c42d060d3a4fad2da6d129c5d2dac575a0a34e5276837acc`  
		Last Modified: Wed, 15 Apr 2026 20:16:37 GMT  
		Size: 8.4 MB (8390330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f8bdd90a189e988440fcec9f3b420d55047950b5f7601ba0e57b351852d7ba`  
		Last Modified: Wed, 15 Apr 2026 20:16:36 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4985eb1bbbfe749a8493542e038307f004a28671974b2a082ae06f9391c4aa64`  
		Last Modified: Wed, 15 Apr 2026 20:16:37 GMT  
		Size: 19.5 MB (19464794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859abcc7688b1a7cc3cc9e144132fc9069de384c58f57dcdc67bb82efa576352`  
		Last Modified: Wed, 15 Apr 2026 20:16:37 GMT  
		Size: 22.5 MB (22539232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c99a167aeca4fe59d6c36fcd7dd693309a219446eca7bcdc04b392e4d69c2c4`  
		Last Modified: Wed, 15 Apr 2026 20:16:38 GMT  
		Size: 11.0 MB (10955103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e81a750c9b2d394bb0113dc9e2ac999fdb73fc198aee986c23671ccc8b782c`  
		Last Modified: Wed, 15 Apr 2026 20:16:38 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ba37c8df4e2fbeeea282fc985c366a9d438cb9ac52b521a1ba48cc214ddd6c`  
		Last Modified: Wed, 15 Apr 2026 20:16:39 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26929be3c972c7f0a15b08c4029aaa790ccc1d494702813df05e37cf6c95ece4`  
		Last Modified: Wed, 15 Apr 2026 20:16:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72409ebb253eee0d0ac41d3def31dd521fd7fbb44646380257fce88e92956e1b`  
		Last Modified: Wed, 15 Apr 2026 21:19:16 GMT  
		Size: 6.9 MB (6941794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61b7bb0bfe4127ecc181695a6617bce6875877794291f6f411f1503400774934`  
		Last Modified: Wed, 15 Apr 2026 21:19:15 GMT  
		Size: 92.4 KB (92386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f322cdda1c007efd5a7874085a0a278df1d8cba0c79c539cecdfd441528c5063`  
		Last Modified: Wed, 15 Apr 2026 21:19:16 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b195c7fa897ae20e300894f9c01ab27baa6d026f2966d14da47768c0504f7e0d`  
		Last Modified: Wed, 15 Apr 2026 21:19:18 GMT  
		Size: 68.3 MB (68266921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d71ba441d54fb7122eab57ffb2e5cc6805c4abe5aa1229a369d61713d35c4a`  
		Last Modified: Wed, 15 Apr 2026 21:19:17 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471eb30b983e8a0f853e3d3be9271df608fd2048cec340fa2eaef5e93dccfdd6`  
		Last Modified: Wed, 15 Apr 2026 21:19:17 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4` - unknown; unknown

```console
$ docker pull docker@sha256:1c8aa5173659195543e7f2199b877ec50c9f568416a96a31cd42b2fcd07923ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36f6b76c4e162e68e3741832b1fa66576d6705a81ed60bdeeded8cbffb74e2ff`

```dockerfile
```

-	Layers:
	-	`sha256:4c3c193ad694d685d8594f91321d9d1fe73498db66cfb3767583e03cba34f0eb`  
		Last Modified: Wed, 15 Apr 2026 21:19:15 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.4` - linux; arm variant v6

```console
$ docker pull docker@sha256:b23cae1ff183bc4e75d88eaf9ba1c6549849f1d134d11fc442d0f885b1f58d4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 MB (132507536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c664d0b218f2b2a9a4e105a5162c0ba967e6162e60df351421a2b174c2b02b2f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:11:18 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 15 Apr 2026 20:11:18 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 15 Apr 2026 20:11:18 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 15 Apr 2026 20:11:22 GMT
ENV DOCKER_VERSION=29.4.0
# Wed, 15 Apr 2026 20:11:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 15 Apr 2026 20:11:22 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Wed, 15 Apr 2026 20:11:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 15 Apr 2026 20:11:25 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 15 Apr 2026 20:11:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 15 Apr 2026 20:11:27 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 15 Apr 2026 20:11:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:11:27 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Apr 2026 20:11:27 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 15 Apr 2026 20:11:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:11:27 GMT
CMD ["sh"]
# Wed, 15 Apr 2026 21:19:39 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 15 Apr 2026 21:19:40 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 15 Apr 2026 21:19:40 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 15 Apr 2026 21:19:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 15 Apr 2026 21:19:44 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 15 Apr 2026 21:19:44 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 15 Apr 2026 21:19:44 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:19:44 GMT
VOLUME [/var/lib/docker]
# Wed, 15 Apr 2026 21:19:44 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 15 Apr 2026 21:19:44 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 15 Apr 2026 21:19:44 GMT
CMD []
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e29b5a067225f28735c3f9c28db7a022b344731761dc5bd14d0b7a283cc13aa1`  
		Last Modified: Wed, 15 Apr 2026 20:11:34 GMT  
		Size: 8.3 MB (8297061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae71f1757016712f17b7c9321ecac9183912e0037f929b5050fa04410093a993`  
		Last Modified: Wed, 15 Apr 2026 20:11:33 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64a558c789f63340dd86a3d8d48163d7ca0b3475c2b5c1d8ca27e0afc43f81a`  
		Last Modified: Wed, 15 Apr 2026 20:11:35 GMT  
		Size: 18.1 MB (18109476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03bc6071f6b066b797f80197a5147fa49e7c18d34820ebbd67e8a05f503815a0`  
		Last Modified: Wed, 15 Apr 2026 20:11:35 GMT  
		Size: 21.2 MB (21151872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84372c97713792c82b059361309092a10362cb4b047854a0b862c3ebeb6f45a7`  
		Last Modified: Wed, 15 Apr 2026 20:11:35 GMT  
		Size: 10.4 MB (10388823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1411d774c190d6fe75a26c80337ed792c1219b393396b9dd4008440601b2e8bb`  
		Last Modified: Wed, 15 Apr 2026 20:11:36 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:213ded2f75d406b851e7f9d90ac09eacb9ecd070136e9e64a5e44a7b62246ab0`  
		Last Modified: Wed, 15 Apr 2026 20:11:36 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9546667a8b53db55a0c88114559b89b5a4c5288c765a0efd17abf18956634f`  
		Last Modified: Wed, 15 Apr 2026 20:11:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db0f2e08cd52770499a4a7b14b1d7035c2bed565f5d1658d36f77ba8cae62ad5`  
		Last Modified: Wed, 15 Apr 2026 21:19:55 GMT  
		Size: 7.3 MB (7278394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810c7f3c3226c75491d45b3028f6aa4e32c04edce7619e9c304e5c7054c6e3e8`  
		Last Modified: Wed, 15 Apr 2026 21:19:55 GMT  
		Size: 91.7 KB (91683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80b9397e0c604f4cffa37ef63fc68b0849fbe399433ee3b1b24e32ea5c1b6138`  
		Last Modified: Wed, 15 Apr 2026 21:19:55 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:578128484de3ef92c76816591ca072998f01b1381725e18fd1c7a4baa20bc9f8`  
		Last Modified: Wed, 15 Apr 2026 21:19:56 GMT  
		Size: 63.6 MB (63610209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2209085b94038497f0af62b68d75961a5b080cb35551dcc8d0eefab6b722484a`  
		Last Modified: Wed, 15 Apr 2026 21:19:56 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b27ed318c8e6661d6fa40585004daf813302e8af45e485fdf0173af3947bc2`  
		Last Modified: Wed, 15 Apr 2026 21:19:56 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4` - unknown; unknown

```console
$ docker pull docker@sha256:a01657f9a7e1e95bc00dd7bf0d40d8f4e73263519d316ff513e77cd827e24f6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48c770ff5e3d911a2d76c733a01cc1a9e96597d1aeb12c3470e57cf12936aa28`

```dockerfile
```

-	Layers:
	-	`sha256:147b649936864607c8d1c5530d9427c37768a5718de420c9941b6f3b6625b9d5`  
		Last Modified: Wed, 15 Apr 2026 21:19:54 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.4` - linux; arm variant v7

```console
$ docker pull docker@sha256:20d1ab4a0712e057c1adc25f5703a97b31a7f387b43adc77bb7308d4397970e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130593641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ca74a271ab95685bc02e667fcb161e01b626e71e3d25886e49bfab8239d7ded`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:16:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 15 Apr 2026 20:16:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 15 Apr 2026 20:16:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 15 Apr 2026 20:16:18 GMT
ENV DOCKER_VERSION=29.4.0
# Wed, 15 Apr 2026 20:16:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 15 Apr 2026 20:16:18 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Wed, 15 Apr 2026 20:16:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 15 Apr 2026 20:16:20 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 15 Apr 2026 20:16:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 15 Apr 2026 20:16:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 15 Apr 2026 20:16:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:16:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Apr 2026 20:16:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 15 Apr 2026 20:16:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:16:22 GMT
CMD ["sh"]
# Wed, 15 Apr 2026 21:27:26 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 15 Apr 2026 21:27:28 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 15 Apr 2026 21:27:28 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 15 Apr 2026 21:27:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 15 Apr 2026 21:27:31 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 15 Apr 2026 21:27:31 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 15 Apr 2026 21:27:31 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:27:31 GMT
VOLUME [/var/lib/docker]
# Wed, 15 Apr 2026 21:27:31 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 15 Apr 2026 21:27:31 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 15 Apr 2026 21:27:31 GMT
CMD []
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88cb38943f0f0a95a9ef76158143c405f36bad50621b2fd56aa2fc4f3615fd5`  
		Last Modified: Wed, 15 Apr 2026 20:16:29 GMT  
		Size: 7.6 MB (7595768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaaca956ad170283b847286ec873bec980d796519baf3f39fe964aded5374f8e`  
		Last Modified: Wed, 15 Apr 2026 20:16:28 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cdf1c13c7d0f067c56c9771266f9895d1041ebf30f39ab27603e18afb0c9081`  
		Last Modified: Wed, 15 Apr 2026 20:16:29 GMT  
		Size: 18.1 MB (18096362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813eda9384408e479910e06a79744324e1dce0b63fd42e5bce661a6e735e2f32`  
		Last Modified: Wed, 15 Apr 2026 20:16:29 GMT  
		Size: 21.1 MB (21129758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f4b664cfcad12fa1a9762a191ac3534cf78c30dd9df6eff79f75e17bd604215`  
		Last Modified: Wed, 15 Apr 2026 20:16:30 GMT  
		Size: 10.4 MB (10371870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f3580f46ae276e11707530d3b18cc55414bcb1f7a672d3cef371193e0e0947`  
		Last Modified: Wed, 15 Apr 2026 20:16:30 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d214a288fe8f0a47169af907737952cefa9e61f078490a75828a439107530b2`  
		Last Modified: Wed, 15 Apr 2026 20:16:31 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf0d872d260394713b2443444bb53d508d83624734c0239dcda7ff1830303db8`  
		Last Modified: Wed, 15 Apr 2026 20:16:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89db5f2f3e615ce6454e5c1c42292805de5a924c4769cb726472a5f992eef448`  
		Last Modified: Wed, 15 Apr 2026 21:27:42 GMT  
		Size: 6.6 MB (6577217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a486198c8f3ba2ab5d5c0c2444157dbdb3a24ef48b6dcbe399e92e72a5e6c28`  
		Last Modified: Wed, 15 Apr 2026 21:27:42 GMT  
		Size: 88.0 KB (88036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba24e0fe682bf1faf33f78d5b19ecad454f21527c9a6c33cfb4c1d694b52779`  
		Last Modified: Wed, 15 Apr 2026 21:27:42 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ca224f3bf33d1172adfccf0c242f89893fde617bd5885ef7545ecd22e41ef4f`  
		Last Modified: Wed, 15 Apr 2026 21:27:44 GMT  
		Size: 63.4 MB (63443351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac3934cb427133bc539854b45e314e2dc44838a979414cf67dd89810b967f06`  
		Last Modified: Wed, 15 Apr 2026 21:27:43 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5e8455627c95fe22aa58fead7cbf2a0934fd4d57d760756577ec0b8c9bf4bc`  
		Last Modified: Wed, 15 Apr 2026 21:27:43 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4` - unknown; unknown

```console
$ docker pull docker@sha256:9376e04ebe10bd90bf0a7a85bddeb4c723ab3c8e9ae5290a6f522143cdbed03d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58ce25b3cedf687af0bcb158bb0a1d2a8523dfeadcddc68360fc3394f815f730`

```dockerfile
```

-	Layers:
	-	`sha256:ecdd6391528d66bfad436f41aef96daa292510a5ddd3f115f031dd1728b3dd36`  
		Last Modified: Wed, 15 Apr 2026 21:27:42 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.4` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:553d694bc3ae2a92b67b73072e3923a8d2256e609b568c60d08e4544e8f39ff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.1 MB (130126872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5c1c78f7262d1e00eef13317919dc25b6d65c96115e46f851ab09818f2ddf0b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:13:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 15 Apr 2026 20:13:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 15 Apr 2026 20:13:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 15 Apr 2026 20:14:02 GMT
ENV DOCKER_VERSION=29.4.0
# Wed, 15 Apr 2026 20:14:02 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 15 Apr 2026 20:14:02 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Wed, 15 Apr 2026 20:14:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 15 Apr 2026 20:14:03 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 15 Apr 2026 20:14:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 15 Apr 2026 20:14:04 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 15 Apr 2026 20:14:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:14:04 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Apr 2026 20:14:04 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 15 Apr 2026 20:14:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:14:04 GMT
CMD ["sh"]
# Wed, 15 Apr 2026 21:33:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 15 Apr 2026 21:33:18 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 15 Apr 2026 21:33:18 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 15 Apr 2026 21:33:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 15 Apr 2026 21:33:21 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 15 Apr 2026 21:33:21 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 15 Apr 2026 21:33:21 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:33:21 GMT
VOLUME [/var/lib/docker]
# Wed, 15 Apr 2026 21:33:21 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 15 Apr 2026 21:33:21 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 15 Apr 2026 21:33:21 GMT
CMD []
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1f08e8ea565813fe5c533f3bf89a6fcb79b8ef2eb46e2872f132234aa070cf`  
		Last Modified: Wed, 15 Apr 2026 20:14:10 GMT  
		Size: 8.5 MB (8450092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ff0f79f131dfea84e2ad6ee3723888525425bfc628525e86c3cc1b288bace3`  
		Last Modified: Wed, 15 Apr 2026 20:14:10 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35bf88d1a58dc1d9ced6e216552eef44b2392e515454985dcd3f25372d12693`  
		Last Modified: Wed, 15 Apr 2026 20:14:11 GMT  
		Size: 17.9 MB (17921079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0aa9505e9a0f5469b8905ecd253d1fd12569434350a1c94898126c02a4a9c57`  
		Last Modified: Wed, 15 Apr 2026 20:14:11 GMT  
		Size: 20.5 MB (20453111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ff9179479c44e683ee3838185f58e7d707974096437fdccedcb7b1f316aa35`  
		Last Modified: Wed, 15 Apr 2026 20:14:11 GMT  
		Size: 10.0 MB (9982600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0771ed595b2bb7d830d904c0ed7f259d39bb70d0da784d731a39f7a1ceeacb04`  
		Last Modified: Wed, 15 Apr 2026 20:14:12 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627cec3b548e33f50bcd1682915056d5dfd8e5b28476d6c4842c0eb790b1f954`  
		Last Modified: Wed, 15 Apr 2026 20:14:12 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c67b1b44bc81549ba5caf988b00dabcb0c2ca6cee73ef7d756e26b08b1028e`  
		Last Modified: Wed, 15 Apr 2026 20:14:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c169b754493e049763aeab1727fe430cecafcd9032c4389b3053958aebc360c9`  
		Last Modified: Wed, 15 Apr 2026 21:33:31 GMT  
		Size: 7.2 MB (7219816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbba1f41e162f643c431dbb55a4cfb94284235c55c0c226f2f85fdc2797d7d3`  
		Last Modified: Wed, 15 Apr 2026 21:33:30 GMT  
		Size: 101.2 KB (101171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc3e20cde46cbbd2b898524e10c8ed94082175c8c21daf98b34e7a6006aafee`  
		Last Modified: Wed, 15 Apr 2026 21:33:30 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ae4baf5361489e96a43c6d29d47fdd4eb63dd088b10e8bf91df746925678ea`  
		Last Modified: Wed, 15 Apr 2026 21:33:32 GMT  
		Size: 61.8 MB (61790985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7fa8aac1af219d886ca4026da0a5a043fde1dae9d3e8534dd78f23360b8763`  
		Last Modified: Wed, 15 Apr 2026 21:33:32 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f667dde4f795a12a4a9d7129f07e71678ffec2ae9a15d680f09fd672a64ab154`  
		Last Modified: Wed, 15 Apr 2026 21:33:32 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4` - unknown; unknown

```console
$ docker pull docker@sha256:71c18f631e3205680e2fcd0ea55f0f373c7fb19de8336794fe07f3d4793786b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48d9407668f8511b7b181ffcfea6ce22705df56aaf20a9dd84a0930f31f6ecf7`

```dockerfile
```

-	Layers:
	-	`sha256:623b2bc83b8d25632b5e152b95570ef2a7af85709fedfa2ae3ed9d312b61c77c`  
		Last Modified: Wed, 15 Apr 2026 21:33:30 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.4-cli`

```console
$ docker pull docker@sha256:2efe7c8e806b35050def6ba1ba0ddad67b521a0a6d37f4910b3d88f11b495d03
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

### `docker:29.4-cli` - linux; amd64

```console
$ docker pull docker@sha256:bb21349a52c00b206ad8b5c03fa52023c741c4cf11f269d40d40b9ebaac73d96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65215798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b7281830dcb31636378f562663cd54df1ce82f631d1cd037968aae8c1034bc2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:16:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 15 Apr 2026 20:16:25 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 15 Apr 2026 20:16:25 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 15 Apr 2026 20:16:27 GMT
ENV DOCKER_VERSION=29.4.0
# Wed, 15 Apr 2026 20:16:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 15 Apr 2026 20:16:27 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Wed, 15 Apr 2026 20:16:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 15 Apr 2026 20:16:28 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 15 Apr 2026 20:16:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 15 Apr 2026 20:16:29 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 15 Apr 2026 20:16:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:16:29 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Apr 2026 20:16:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 15 Apr 2026 20:16:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:16:30 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00fef3bc4d7adc06c42d060d3a4fad2da6d129c5d2dac575a0a34e5276837acc`  
		Last Modified: Wed, 15 Apr 2026 20:16:37 GMT  
		Size: 8.4 MB (8390330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f8bdd90a189e988440fcec9f3b420d55047950b5f7601ba0e57b351852d7ba`  
		Last Modified: Wed, 15 Apr 2026 20:16:36 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4985eb1bbbfe749a8493542e038307f004a28671974b2a082ae06f9391c4aa64`  
		Last Modified: Wed, 15 Apr 2026 20:16:37 GMT  
		Size: 19.5 MB (19464794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859abcc7688b1a7cc3cc9e144132fc9069de384c58f57dcdc67bb82efa576352`  
		Last Modified: Wed, 15 Apr 2026 20:16:37 GMT  
		Size: 22.5 MB (22539232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c99a167aeca4fe59d6c36fcd7dd693309a219446eca7bcdc04b392e4d69c2c4`  
		Last Modified: Wed, 15 Apr 2026 20:16:38 GMT  
		Size: 11.0 MB (10955103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e81a750c9b2d394bb0113dc9e2ac999fdb73fc198aee986c23671ccc8b782c`  
		Last Modified: Wed, 15 Apr 2026 20:16:38 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ba37c8df4e2fbeeea282fc985c366a9d438cb9ac52b521a1ba48cc214ddd6c`  
		Last Modified: Wed, 15 Apr 2026 20:16:39 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26929be3c972c7f0a15b08c4029aaa790ccc1d494702813df05e37cf6c95ece4`  
		Last Modified: Wed, 15 Apr 2026 20:16:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4-cli` - unknown; unknown

```console
$ docker pull docker@sha256:5c727440eaffe25d1a2f89a448a8aeef8118f192ce752f5f55b0e7dcf3bee15d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d4150275339c1686c0b7eab0e338d57f441efecf63ffadf5cfa59dfe3a3e9a0`

```dockerfile
```

-	Layers:
	-	`sha256:083400d83f577b87f30bc974ae857508bdaeb3c56dafaa2a3985dbc6a2be5c32`  
		Last Modified: Wed, 15 Apr 2026 20:16:36 GMT  
		Size: 38.1 KB (38056 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.4-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:b0448a7e451eb2df18d117260c232b9064f3b11bd751ac2e603c18bef0289a37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61521248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ab4c337f9a3ba981939d8eb77b75c53cbc28458c647ccce32e93d0f7a99ee4e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:11:18 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 15 Apr 2026 20:11:18 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 15 Apr 2026 20:11:18 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 15 Apr 2026 20:11:22 GMT
ENV DOCKER_VERSION=29.4.0
# Wed, 15 Apr 2026 20:11:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 15 Apr 2026 20:11:22 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Wed, 15 Apr 2026 20:11:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 15 Apr 2026 20:11:25 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 15 Apr 2026 20:11:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 15 Apr 2026 20:11:27 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 15 Apr 2026 20:11:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:11:27 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Apr 2026 20:11:27 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 15 Apr 2026 20:11:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:11:27 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e29b5a067225f28735c3f9c28db7a022b344731761dc5bd14d0b7a283cc13aa1`  
		Last Modified: Wed, 15 Apr 2026 20:11:34 GMT  
		Size: 8.3 MB (8297061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae71f1757016712f17b7c9321ecac9183912e0037f929b5050fa04410093a993`  
		Last Modified: Wed, 15 Apr 2026 20:11:33 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64a558c789f63340dd86a3d8d48163d7ca0b3475c2b5c1d8ca27e0afc43f81a`  
		Last Modified: Wed, 15 Apr 2026 20:11:35 GMT  
		Size: 18.1 MB (18109476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03bc6071f6b066b797f80197a5147fa49e7c18d34820ebbd67e8a05f503815a0`  
		Last Modified: Wed, 15 Apr 2026 20:11:35 GMT  
		Size: 21.2 MB (21151872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84372c97713792c82b059361309092a10362cb4b047854a0b862c3ebeb6f45a7`  
		Last Modified: Wed, 15 Apr 2026 20:11:35 GMT  
		Size: 10.4 MB (10388823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1411d774c190d6fe75a26c80337ed792c1219b393396b9dd4008440601b2e8bb`  
		Last Modified: Wed, 15 Apr 2026 20:11:36 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:213ded2f75d406b851e7f9d90ac09eacb9ecd070136e9e64a5e44a7b62246ab0`  
		Last Modified: Wed, 15 Apr 2026 20:11:36 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9546667a8b53db55a0c88114559b89b5a4c5288c765a0efd17abf18956634f`  
		Last Modified: Wed, 15 Apr 2026 20:11:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4-cli` - unknown; unknown

```console
$ docker pull docker@sha256:bbcdf7618a730942664487ce478f3a269e4859185ac161e3578319a0f54ff6d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8a566184814fc34593f5137a7bba3c2c3aae7de569de008b69e5efb6fd4f2b8`

```dockerfile
```

-	Layers:
	-	`sha256:34582c23f82fc6f533690de02a4263c869ac6e2e06850e19652639cbf36d4f4c`  
		Last Modified: Wed, 15 Apr 2026 20:11:33 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.4-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:75b479961472cf73f0407e0b3c7576c45be650ab0f523fc539f33fde7777f22f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60479031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:254b0d5926521e59075cd4b154a10ba99b2e222f9e1b682d6ef3bda0b94beaef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:16:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 15 Apr 2026 20:16:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 15 Apr 2026 20:16:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 15 Apr 2026 20:16:18 GMT
ENV DOCKER_VERSION=29.4.0
# Wed, 15 Apr 2026 20:16:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 15 Apr 2026 20:16:18 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Wed, 15 Apr 2026 20:16:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 15 Apr 2026 20:16:20 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 15 Apr 2026 20:16:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 15 Apr 2026 20:16:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 15 Apr 2026 20:16:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:16:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Apr 2026 20:16:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 15 Apr 2026 20:16:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:16:22 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88cb38943f0f0a95a9ef76158143c405f36bad50621b2fd56aa2fc4f3615fd5`  
		Last Modified: Wed, 15 Apr 2026 20:16:29 GMT  
		Size: 7.6 MB (7595768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaaca956ad170283b847286ec873bec980d796519baf3f39fe964aded5374f8e`  
		Last Modified: Wed, 15 Apr 2026 20:16:28 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cdf1c13c7d0f067c56c9771266f9895d1041ebf30f39ab27603e18afb0c9081`  
		Last Modified: Wed, 15 Apr 2026 20:16:29 GMT  
		Size: 18.1 MB (18096362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813eda9384408e479910e06a79744324e1dce0b63fd42e5bce661a6e735e2f32`  
		Last Modified: Wed, 15 Apr 2026 20:16:29 GMT  
		Size: 21.1 MB (21129758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f4b664cfcad12fa1a9762a191ac3534cf78c30dd9df6eff79f75e17bd604215`  
		Last Modified: Wed, 15 Apr 2026 20:16:30 GMT  
		Size: 10.4 MB (10371870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f3580f46ae276e11707530d3b18cc55414bcb1f7a672d3cef371193e0e0947`  
		Last Modified: Wed, 15 Apr 2026 20:16:30 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d214a288fe8f0a47169af907737952cefa9e61f078490a75828a439107530b2`  
		Last Modified: Wed, 15 Apr 2026 20:16:31 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf0d872d260394713b2443444bb53d508d83624734c0239dcda7ff1830303db8`  
		Last Modified: Wed, 15 Apr 2026 20:16:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4-cli` - unknown; unknown

```console
$ docker pull docker@sha256:70f0601152bac7df07b2933f0e46a2774591dbebc7e87523cc02d222b56c86b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e085d1943182e6d53f4b66b7d1654479506a41c31da6cbd8241cba54df3ce900`

```dockerfile
```

-	Layers:
	-	`sha256:368fab9b9711e124e80b9dedf4aa9bea5ba28ad952bacb0003647ef444f12135`  
		Last Modified: Wed, 15 Apr 2026 20:16:28 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.4-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:9d3f67fe1f4cf51c084744dec419b466b7075f5b365ef4b9b791187d9c2d4127
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.0 MB (61008901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dea3a61a70d2ba11898616b2f246eaeef9d1c75b7041f2e45826da60d2e47276`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:13:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 15 Apr 2026 20:13:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 15 Apr 2026 20:13:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 15 Apr 2026 20:14:02 GMT
ENV DOCKER_VERSION=29.4.0
# Wed, 15 Apr 2026 20:14:02 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 15 Apr 2026 20:14:02 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Wed, 15 Apr 2026 20:14:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 15 Apr 2026 20:14:03 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 15 Apr 2026 20:14:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 15 Apr 2026 20:14:04 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 15 Apr 2026 20:14:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:14:04 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Apr 2026 20:14:04 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 15 Apr 2026 20:14:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:14:04 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1f08e8ea565813fe5c533f3bf89a6fcb79b8ef2eb46e2872f132234aa070cf`  
		Last Modified: Wed, 15 Apr 2026 20:14:10 GMT  
		Size: 8.5 MB (8450092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ff0f79f131dfea84e2ad6ee3723888525425bfc628525e86c3cc1b288bace3`  
		Last Modified: Wed, 15 Apr 2026 20:14:10 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35bf88d1a58dc1d9ced6e216552eef44b2392e515454985dcd3f25372d12693`  
		Last Modified: Wed, 15 Apr 2026 20:14:11 GMT  
		Size: 17.9 MB (17921079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0aa9505e9a0f5469b8905ecd253d1fd12569434350a1c94898126c02a4a9c57`  
		Last Modified: Wed, 15 Apr 2026 20:14:11 GMT  
		Size: 20.5 MB (20453111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ff9179479c44e683ee3838185f58e7d707974096437fdccedcb7b1f316aa35`  
		Last Modified: Wed, 15 Apr 2026 20:14:11 GMT  
		Size: 10.0 MB (9982600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0771ed595b2bb7d830d904c0ed7f259d39bb70d0da784d731a39f7a1ceeacb04`  
		Last Modified: Wed, 15 Apr 2026 20:14:12 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627cec3b548e33f50bcd1682915056d5dfd8e5b28476d6c4842c0eb790b1f954`  
		Last Modified: Wed, 15 Apr 2026 20:14:12 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c67b1b44bc81549ba5caf988b00dabcb0c2ca6cee73ef7d756e26b08b1028e`  
		Last Modified: Wed, 15 Apr 2026 20:14:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4-cli` - unknown; unknown

```console
$ docker pull docker@sha256:e021182c1f750cfc367850ea8b786139b8a3c428c84711dcaf82dad470636664
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a194ccda70da01232600045e81eff9a9985e4f5f2d0762a6d6f356e6cff9fe0`

```dockerfile
```

-	Layers:
	-	`sha256:c94d9b9821f47c73547b7085c1041bda87c05335abab499b01c9fcc9f12a80bf`  
		Last Modified: Wed, 15 Apr 2026 20:14:10 GMT  
		Size: 38.3 KB (38258 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.4-dind`

```console
$ docker pull docker@sha256:a6dd5322747a95cd8e3207bd8d415a8fd20ec34e9c00f06dc019cbd912013489
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

### `docker:29.4-dind` - linux; amd64

```console
$ docker pull docker@sha256:4d2c6e334de4b26d492c0a8cc5438e3dbf1a02eee899fc0d4d39b96202c943a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.5 MB (140522901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:304d326357dcfc523ea9ea01226e742f15d0d548d8eaec0e14c3b39387303000`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:16:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 15 Apr 2026 20:16:25 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 15 Apr 2026 20:16:25 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 15 Apr 2026 20:16:27 GMT
ENV DOCKER_VERSION=29.4.0
# Wed, 15 Apr 2026 20:16:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 15 Apr 2026 20:16:27 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Wed, 15 Apr 2026 20:16:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 15 Apr 2026 20:16:28 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 15 Apr 2026 20:16:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 15 Apr 2026 20:16:29 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 15 Apr 2026 20:16:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:16:29 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Apr 2026 20:16:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 15 Apr 2026 20:16:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:16:30 GMT
CMD ["sh"]
# Wed, 15 Apr 2026 21:19:01 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 15 Apr 2026 21:19:02 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 15 Apr 2026 21:19:02 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 15 Apr 2026 21:19:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 15 Apr 2026 21:19:05 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 15 Apr 2026 21:19:05 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 15 Apr 2026 21:19:05 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:19:05 GMT
VOLUME [/var/lib/docker]
# Wed, 15 Apr 2026 21:19:05 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 15 Apr 2026 21:19:05 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 15 Apr 2026 21:19:05 GMT
CMD []
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00fef3bc4d7adc06c42d060d3a4fad2da6d129c5d2dac575a0a34e5276837acc`  
		Last Modified: Wed, 15 Apr 2026 20:16:37 GMT  
		Size: 8.4 MB (8390330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f8bdd90a189e988440fcec9f3b420d55047950b5f7601ba0e57b351852d7ba`  
		Last Modified: Wed, 15 Apr 2026 20:16:36 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4985eb1bbbfe749a8493542e038307f004a28671974b2a082ae06f9391c4aa64`  
		Last Modified: Wed, 15 Apr 2026 20:16:37 GMT  
		Size: 19.5 MB (19464794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859abcc7688b1a7cc3cc9e144132fc9069de384c58f57dcdc67bb82efa576352`  
		Last Modified: Wed, 15 Apr 2026 20:16:37 GMT  
		Size: 22.5 MB (22539232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c99a167aeca4fe59d6c36fcd7dd693309a219446eca7bcdc04b392e4d69c2c4`  
		Last Modified: Wed, 15 Apr 2026 20:16:38 GMT  
		Size: 11.0 MB (10955103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e81a750c9b2d394bb0113dc9e2ac999fdb73fc198aee986c23671ccc8b782c`  
		Last Modified: Wed, 15 Apr 2026 20:16:38 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ba37c8df4e2fbeeea282fc985c366a9d438cb9ac52b521a1ba48cc214ddd6c`  
		Last Modified: Wed, 15 Apr 2026 20:16:39 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26929be3c972c7f0a15b08c4029aaa790ccc1d494702813df05e37cf6c95ece4`  
		Last Modified: Wed, 15 Apr 2026 20:16:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72409ebb253eee0d0ac41d3def31dd521fd7fbb44646380257fce88e92956e1b`  
		Last Modified: Wed, 15 Apr 2026 21:19:16 GMT  
		Size: 6.9 MB (6941794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61b7bb0bfe4127ecc181695a6617bce6875877794291f6f411f1503400774934`  
		Last Modified: Wed, 15 Apr 2026 21:19:15 GMT  
		Size: 92.4 KB (92386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f322cdda1c007efd5a7874085a0a278df1d8cba0c79c539cecdfd441528c5063`  
		Last Modified: Wed, 15 Apr 2026 21:19:16 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b195c7fa897ae20e300894f9c01ab27baa6d026f2966d14da47768c0504f7e0d`  
		Last Modified: Wed, 15 Apr 2026 21:19:18 GMT  
		Size: 68.3 MB (68266921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d71ba441d54fb7122eab57ffb2e5cc6805c4abe5aa1229a369d61713d35c4a`  
		Last Modified: Wed, 15 Apr 2026 21:19:17 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471eb30b983e8a0f853e3d3be9271df608fd2048cec340fa2eaef5e93dccfdd6`  
		Last Modified: Wed, 15 Apr 2026 21:19:17 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4-dind` - unknown; unknown

```console
$ docker pull docker@sha256:1c8aa5173659195543e7f2199b877ec50c9f568416a96a31cd42b2fcd07923ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36f6b76c4e162e68e3741832b1fa66576d6705a81ed60bdeeded8cbffb74e2ff`

```dockerfile
```

-	Layers:
	-	`sha256:4c3c193ad694d685d8594f91321d9d1fe73498db66cfb3767583e03cba34f0eb`  
		Last Modified: Wed, 15 Apr 2026 21:19:15 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.4-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:b23cae1ff183bc4e75d88eaf9ba1c6549849f1d134d11fc442d0f885b1f58d4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 MB (132507536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c664d0b218f2b2a9a4e105a5162c0ba967e6162e60df351421a2b174c2b02b2f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:11:18 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 15 Apr 2026 20:11:18 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 15 Apr 2026 20:11:18 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 15 Apr 2026 20:11:22 GMT
ENV DOCKER_VERSION=29.4.0
# Wed, 15 Apr 2026 20:11:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 15 Apr 2026 20:11:22 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Wed, 15 Apr 2026 20:11:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 15 Apr 2026 20:11:25 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 15 Apr 2026 20:11:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 15 Apr 2026 20:11:27 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 15 Apr 2026 20:11:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:11:27 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Apr 2026 20:11:27 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 15 Apr 2026 20:11:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:11:27 GMT
CMD ["sh"]
# Wed, 15 Apr 2026 21:19:39 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 15 Apr 2026 21:19:40 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 15 Apr 2026 21:19:40 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 15 Apr 2026 21:19:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 15 Apr 2026 21:19:44 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 15 Apr 2026 21:19:44 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 15 Apr 2026 21:19:44 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:19:44 GMT
VOLUME [/var/lib/docker]
# Wed, 15 Apr 2026 21:19:44 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 15 Apr 2026 21:19:44 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 15 Apr 2026 21:19:44 GMT
CMD []
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e29b5a067225f28735c3f9c28db7a022b344731761dc5bd14d0b7a283cc13aa1`  
		Last Modified: Wed, 15 Apr 2026 20:11:34 GMT  
		Size: 8.3 MB (8297061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae71f1757016712f17b7c9321ecac9183912e0037f929b5050fa04410093a993`  
		Last Modified: Wed, 15 Apr 2026 20:11:33 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64a558c789f63340dd86a3d8d48163d7ca0b3475c2b5c1d8ca27e0afc43f81a`  
		Last Modified: Wed, 15 Apr 2026 20:11:35 GMT  
		Size: 18.1 MB (18109476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03bc6071f6b066b797f80197a5147fa49e7c18d34820ebbd67e8a05f503815a0`  
		Last Modified: Wed, 15 Apr 2026 20:11:35 GMT  
		Size: 21.2 MB (21151872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84372c97713792c82b059361309092a10362cb4b047854a0b862c3ebeb6f45a7`  
		Last Modified: Wed, 15 Apr 2026 20:11:35 GMT  
		Size: 10.4 MB (10388823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1411d774c190d6fe75a26c80337ed792c1219b393396b9dd4008440601b2e8bb`  
		Last Modified: Wed, 15 Apr 2026 20:11:36 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:213ded2f75d406b851e7f9d90ac09eacb9ecd070136e9e64a5e44a7b62246ab0`  
		Last Modified: Wed, 15 Apr 2026 20:11:36 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9546667a8b53db55a0c88114559b89b5a4c5288c765a0efd17abf18956634f`  
		Last Modified: Wed, 15 Apr 2026 20:11:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db0f2e08cd52770499a4a7b14b1d7035c2bed565f5d1658d36f77ba8cae62ad5`  
		Last Modified: Wed, 15 Apr 2026 21:19:55 GMT  
		Size: 7.3 MB (7278394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810c7f3c3226c75491d45b3028f6aa4e32c04edce7619e9c304e5c7054c6e3e8`  
		Last Modified: Wed, 15 Apr 2026 21:19:55 GMT  
		Size: 91.7 KB (91683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80b9397e0c604f4cffa37ef63fc68b0849fbe399433ee3b1b24e32ea5c1b6138`  
		Last Modified: Wed, 15 Apr 2026 21:19:55 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:578128484de3ef92c76816591ca072998f01b1381725e18fd1c7a4baa20bc9f8`  
		Last Modified: Wed, 15 Apr 2026 21:19:56 GMT  
		Size: 63.6 MB (63610209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2209085b94038497f0af62b68d75961a5b080cb35551dcc8d0eefab6b722484a`  
		Last Modified: Wed, 15 Apr 2026 21:19:56 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b27ed318c8e6661d6fa40585004daf813302e8af45e485fdf0173af3947bc2`  
		Last Modified: Wed, 15 Apr 2026 21:19:56 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4-dind` - unknown; unknown

```console
$ docker pull docker@sha256:a01657f9a7e1e95bc00dd7bf0d40d8f4e73263519d316ff513e77cd827e24f6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48c770ff5e3d911a2d76c733a01cc1a9e96597d1aeb12c3470e57cf12936aa28`

```dockerfile
```

-	Layers:
	-	`sha256:147b649936864607c8d1c5530d9427c37768a5718de420c9941b6f3b6625b9d5`  
		Last Modified: Wed, 15 Apr 2026 21:19:54 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.4-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:20d1ab4a0712e057c1adc25f5703a97b31a7f387b43adc77bb7308d4397970e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130593641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ca74a271ab95685bc02e667fcb161e01b626e71e3d25886e49bfab8239d7ded`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:16:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 15 Apr 2026 20:16:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 15 Apr 2026 20:16:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 15 Apr 2026 20:16:18 GMT
ENV DOCKER_VERSION=29.4.0
# Wed, 15 Apr 2026 20:16:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 15 Apr 2026 20:16:18 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Wed, 15 Apr 2026 20:16:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 15 Apr 2026 20:16:20 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 15 Apr 2026 20:16:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 15 Apr 2026 20:16:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 15 Apr 2026 20:16:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:16:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Apr 2026 20:16:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 15 Apr 2026 20:16:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:16:22 GMT
CMD ["sh"]
# Wed, 15 Apr 2026 21:27:26 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 15 Apr 2026 21:27:28 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 15 Apr 2026 21:27:28 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 15 Apr 2026 21:27:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 15 Apr 2026 21:27:31 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 15 Apr 2026 21:27:31 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 15 Apr 2026 21:27:31 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:27:31 GMT
VOLUME [/var/lib/docker]
# Wed, 15 Apr 2026 21:27:31 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 15 Apr 2026 21:27:31 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 15 Apr 2026 21:27:31 GMT
CMD []
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88cb38943f0f0a95a9ef76158143c405f36bad50621b2fd56aa2fc4f3615fd5`  
		Last Modified: Wed, 15 Apr 2026 20:16:29 GMT  
		Size: 7.6 MB (7595768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaaca956ad170283b847286ec873bec980d796519baf3f39fe964aded5374f8e`  
		Last Modified: Wed, 15 Apr 2026 20:16:28 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cdf1c13c7d0f067c56c9771266f9895d1041ebf30f39ab27603e18afb0c9081`  
		Last Modified: Wed, 15 Apr 2026 20:16:29 GMT  
		Size: 18.1 MB (18096362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813eda9384408e479910e06a79744324e1dce0b63fd42e5bce661a6e735e2f32`  
		Last Modified: Wed, 15 Apr 2026 20:16:29 GMT  
		Size: 21.1 MB (21129758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f4b664cfcad12fa1a9762a191ac3534cf78c30dd9df6eff79f75e17bd604215`  
		Last Modified: Wed, 15 Apr 2026 20:16:30 GMT  
		Size: 10.4 MB (10371870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f3580f46ae276e11707530d3b18cc55414bcb1f7a672d3cef371193e0e0947`  
		Last Modified: Wed, 15 Apr 2026 20:16:30 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d214a288fe8f0a47169af907737952cefa9e61f078490a75828a439107530b2`  
		Last Modified: Wed, 15 Apr 2026 20:16:31 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf0d872d260394713b2443444bb53d508d83624734c0239dcda7ff1830303db8`  
		Last Modified: Wed, 15 Apr 2026 20:16:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89db5f2f3e615ce6454e5c1c42292805de5a924c4769cb726472a5f992eef448`  
		Last Modified: Wed, 15 Apr 2026 21:27:42 GMT  
		Size: 6.6 MB (6577217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a486198c8f3ba2ab5d5c0c2444157dbdb3a24ef48b6dcbe399e92e72a5e6c28`  
		Last Modified: Wed, 15 Apr 2026 21:27:42 GMT  
		Size: 88.0 KB (88036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba24e0fe682bf1faf33f78d5b19ecad454f21527c9a6c33cfb4c1d694b52779`  
		Last Modified: Wed, 15 Apr 2026 21:27:42 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ca224f3bf33d1172adfccf0c242f89893fde617bd5885ef7545ecd22e41ef4f`  
		Last Modified: Wed, 15 Apr 2026 21:27:44 GMT  
		Size: 63.4 MB (63443351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac3934cb427133bc539854b45e314e2dc44838a979414cf67dd89810b967f06`  
		Last Modified: Wed, 15 Apr 2026 21:27:43 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5e8455627c95fe22aa58fead7cbf2a0934fd4d57d760756577ec0b8c9bf4bc`  
		Last Modified: Wed, 15 Apr 2026 21:27:43 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4-dind` - unknown; unknown

```console
$ docker pull docker@sha256:9376e04ebe10bd90bf0a7a85bddeb4c723ab3c8e9ae5290a6f522143cdbed03d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58ce25b3cedf687af0bcb158bb0a1d2a8523dfeadcddc68360fc3394f815f730`

```dockerfile
```

-	Layers:
	-	`sha256:ecdd6391528d66bfad436f41aef96daa292510a5ddd3f115f031dd1728b3dd36`  
		Last Modified: Wed, 15 Apr 2026 21:27:42 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.4-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:553d694bc3ae2a92b67b73072e3923a8d2256e609b568c60d08e4544e8f39ff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.1 MB (130126872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5c1c78f7262d1e00eef13317919dc25b6d65c96115e46f851ab09818f2ddf0b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:13:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 15 Apr 2026 20:13:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 15 Apr 2026 20:13:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 15 Apr 2026 20:14:02 GMT
ENV DOCKER_VERSION=29.4.0
# Wed, 15 Apr 2026 20:14:02 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 15 Apr 2026 20:14:02 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Wed, 15 Apr 2026 20:14:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 15 Apr 2026 20:14:03 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 15 Apr 2026 20:14:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 15 Apr 2026 20:14:04 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 15 Apr 2026 20:14:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:14:04 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Apr 2026 20:14:04 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 15 Apr 2026 20:14:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:14:04 GMT
CMD ["sh"]
# Wed, 15 Apr 2026 21:33:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 15 Apr 2026 21:33:18 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 15 Apr 2026 21:33:18 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 15 Apr 2026 21:33:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 15 Apr 2026 21:33:21 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 15 Apr 2026 21:33:21 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 15 Apr 2026 21:33:21 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:33:21 GMT
VOLUME [/var/lib/docker]
# Wed, 15 Apr 2026 21:33:21 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 15 Apr 2026 21:33:21 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 15 Apr 2026 21:33:21 GMT
CMD []
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1f08e8ea565813fe5c533f3bf89a6fcb79b8ef2eb46e2872f132234aa070cf`  
		Last Modified: Wed, 15 Apr 2026 20:14:10 GMT  
		Size: 8.5 MB (8450092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ff0f79f131dfea84e2ad6ee3723888525425bfc628525e86c3cc1b288bace3`  
		Last Modified: Wed, 15 Apr 2026 20:14:10 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35bf88d1a58dc1d9ced6e216552eef44b2392e515454985dcd3f25372d12693`  
		Last Modified: Wed, 15 Apr 2026 20:14:11 GMT  
		Size: 17.9 MB (17921079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0aa9505e9a0f5469b8905ecd253d1fd12569434350a1c94898126c02a4a9c57`  
		Last Modified: Wed, 15 Apr 2026 20:14:11 GMT  
		Size: 20.5 MB (20453111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ff9179479c44e683ee3838185f58e7d707974096437fdccedcb7b1f316aa35`  
		Last Modified: Wed, 15 Apr 2026 20:14:11 GMT  
		Size: 10.0 MB (9982600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0771ed595b2bb7d830d904c0ed7f259d39bb70d0da784d731a39f7a1ceeacb04`  
		Last Modified: Wed, 15 Apr 2026 20:14:12 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627cec3b548e33f50bcd1682915056d5dfd8e5b28476d6c4842c0eb790b1f954`  
		Last Modified: Wed, 15 Apr 2026 20:14:12 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c67b1b44bc81549ba5caf988b00dabcb0c2ca6cee73ef7d756e26b08b1028e`  
		Last Modified: Wed, 15 Apr 2026 20:14:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c169b754493e049763aeab1727fe430cecafcd9032c4389b3053958aebc360c9`  
		Last Modified: Wed, 15 Apr 2026 21:33:31 GMT  
		Size: 7.2 MB (7219816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbba1f41e162f643c431dbb55a4cfb94284235c55c0c226f2f85fdc2797d7d3`  
		Last Modified: Wed, 15 Apr 2026 21:33:30 GMT  
		Size: 101.2 KB (101171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc3e20cde46cbbd2b898524e10c8ed94082175c8c21daf98b34e7a6006aafee`  
		Last Modified: Wed, 15 Apr 2026 21:33:30 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ae4baf5361489e96a43c6d29d47fdd4eb63dd088b10e8bf91df746925678ea`  
		Last Modified: Wed, 15 Apr 2026 21:33:32 GMT  
		Size: 61.8 MB (61790985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7fa8aac1af219d886ca4026da0a5a043fde1dae9d3e8534dd78f23360b8763`  
		Last Modified: Wed, 15 Apr 2026 21:33:32 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f667dde4f795a12a4a9d7129f07e71678ffec2ae9a15d680f09fd672a64ab154`  
		Last Modified: Wed, 15 Apr 2026 21:33:32 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4-dind` - unknown; unknown

```console
$ docker pull docker@sha256:71c18f631e3205680e2fcd0ea55f0f373c7fb19de8336794fe07f3d4793786b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48d9407668f8511b7b181ffcfea6ce22705df56aaf20a9dd84a0930f31f6ecf7`

```dockerfile
```

-	Layers:
	-	`sha256:623b2bc83b8d25632b5e152b95570ef2a7af85709fedfa2ae3ed9d312b61c77c`  
		Last Modified: Wed, 15 Apr 2026 21:33:30 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.4-dind-rootless`

```console
$ docker pull docker@sha256:76944d96ec8f4d759b5c8d9bf5f0787813f278e46aa078ae65338216739cb0fd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:29.4-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:e89e2c0f44ba58a65f9f9dc8b04aea6ee7f31c76a7ff8048465f2576746fadb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.5 MB (161524750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ceb46e5e927ba19a62569af7c8eb32cbcef000cd7379578db1e3a3e4fe943aa`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:16:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 15 Apr 2026 20:16:25 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 15 Apr 2026 20:16:25 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 15 Apr 2026 20:16:27 GMT
ENV DOCKER_VERSION=29.4.0
# Wed, 15 Apr 2026 20:16:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 15 Apr 2026 20:16:27 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Wed, 15 Apr 2026 20:16:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 15 Apr 2026 20:16:28 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 15 Apr 2026 20:16:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 15 Apr 2026 20:16:29 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 15 Apr 2026 20:16:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:16:29 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Apr 2026 20:16:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 15 Apr 2026 20:16:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:16:30 GMT
CMD ["sh"]
# Wed, 15 Apr 2026 21:19:01 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 15 Apr 2026 21:19:02 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 15 Apr 2026 21:19:02 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 15 Apr 2026 21:19:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 15 Apr 2026 21:19:05 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 15 Apr 2026 21:19:05 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 15 Apr 2026 21:19:05 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:19:05 GMT
VOLUME [/var/lib/docker]
# Wed, 15 Apr 2026 21:19:05 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 15 Apr 2026 21:19:05 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 15 Apr 2026 21:19:05 GMT
CMD []
# Wed, 15 Apr 2026 22:12:18 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Wed, 15 Apr 2026 22:12:18 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 15 Apr 2026 22:12:18 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 15 Apr 2026 22:12:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 15 Apr 2026 22:12:19 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 15 Apr 2026 22:12:19 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 15 Apr 2026 22:12:19 GMT
USER rootless
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00fef3bc4d7adc06c42d060d3a4fad2da6d129c5d2dac575a0a34e5276837acc`  
		Last Modified: Wed, 15 Apr 2026 20:16:37 GMT  
		Size: 8.4 MB (8390330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f8bdd90a189e988440fcec9f3b420d55047950b5f7601ba0e57b351852d7ba`  
		Last Modified: Wed, 15 Apr 2026 20:16:36 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4985eb1bbbfe749a8493542e038307f004a28671974b2a082ae06f9391c4aa64`  
		Last Modified: Wed, 15 Apr 2026 20:16:37 GMT  
		Size: 19.5 MB (19464794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859abcc7688b1a7cc3cc9e144132fc9069de384c58f57dcdc67bb82efa576352`  
		Last Modified: Wed, 15 Apr 2026 20:16:37 GMT  
		Size: 22.5 MB (22539232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c99a167aeca4fe59d6c36fcd7dd693309a219446eca7bcdc04b392e4d69c2c4`  
		Last Modified: Wed, 15 Apr 2026 20:16:38 GMT  
		Size: 11.0 MB (10955103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e81a750c9b2d394bb0113dc9e2ac999fdb73fc198aee986c23671ccc8b782c`  
		Last Modified: Wed, 15 Apr 2026 20:16:38 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ba37c8df4e2fbeeea282fc985c366a9d438cb9ac52b521a1ba48cc214ddd6c`  
		Last Modified: Wed, 15 Apr 2026 20:16:39 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26929be3c972c7f0a15b08c4029aaa790ccc1d494702813df05e37cf6c95ece4`  
		Last Modified: Wed, 15 Apr 2026 20:16:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72409ebb253eee0d0ac41d3def31dd521fd7fbb44646380257fce88e92956e1b`  
		Last Modified: Wed, 15 Apr 2026 21:19:16 GMT  
		Size: 6.9 MB (6941794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61b7bb0bfe4127ecc181695a6617bce6875877794291f6f411f1503400774934`  
		Last Modified: Wed, 15 Apr 2026 21:19:15 GMT  
		Size: 92.4 KB (92386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f322cdda1c007efd5a7874085a0a278df1d8cba0c79c539cecdfd441528c5063`  
		Last Modified: Wed, 15 Apr 2026 21:19:16 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b195c7fa897ae20e300894f9c01ab27baa6d026f2966d14da47768c0504f7e0d`  
		Last Modified: Wed, 15 Apr 2026 21:19:18 GMT  
		Size: 68.3 MB (68266921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d71ba441d54fb7122eab57ffb2e5cc6805c4abe5aa1229a369d61713d35c4a`  
		Last Modified: Wed, 15 Apr 2026 21:19:17 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471eb30b983e8a0f853e3d3be9271df608fd2048cec340fa2eaef5e93dccfdd6`  
		Last Modified: Wed, 15 Apr 2026 21:19:17 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d603a61ab9bf085d4c5ed544ebdc6930cedac60c151b8c3d844ec4a5e1907a3f`  
		Last Modified: Wed, 15 Apr 2026 22:12:32 GMT  
		Size: 3.4 MB (3420096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f6cf84eabf10318aff4902301c0a7eb0d5e3a1fbedc2457d5a03e48ec176798`  
		Last Modified: Wed, 15 Apr 2026 22:12:26 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c7e42a9e418d966d88e75d7076fb61e32f5f036331ad87079c2af72fee32a29`  
		Last Modified: Wed, 15 Apr 2026 22:12:28 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:707634342cc50aaa8f17842865d9fe9c4d140289067e551027f32d44235c5e64`  
		Last Modified: Wed, 15 Apr 2026 22:12:36 GMT  
		Size: 17.6 MB (17580415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5efa74639426aef15709b77e6fe19278595bf047f2e03f5a8449cc234b9df8c2`  
		Last Modified: Wed, 15 Apr 2026 22:12:32 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:16263b4914888c6b7270d1a2b9da8845365aacaafbf2ae86d9c3e093373eb29c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9072388f94ef26c4fd86a7769ed365d8a261d4df812abb3ef6950a2400d130af`

```dockerfile
```

-	Layers:
	-	`sha256:f9339be88cc342b92f34d4da76922c287e26b230e4ebab8ba0b5ce74a00df08b`  
		Last Modified: Wed, 15 Apr 2026 22:12:24 GMT  
		Size: 30.6 KB (30589 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.4-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:b4fad2141f6e11611acfc843f2434ba2a41e6915639963b943fa2ba4b51e87d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.4 MB (151405559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95e9af8ffe8cf19d9949f80c4fe0f01db4518273f5f1e3f6470799d230530909`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:13:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 15 Apr 2026 20:13:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 15 Apr 2026 20:13:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 15 Apr 2026 20:14:02 GMT
ENV DOCKER_VERSION=29.4.0
# Wed, 15 Apr 2026 20:14:02 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 15 Apr 2026 20:14:02 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Wed, 15 Apr 2026 20:14:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 15 Apr 2026 20:14:03 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 15 Apr 2026 20:14:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 15 Apr 2026 20:14:04 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 15 Apr 2026 20:14:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:14:04 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Apr 2026 20:14:04 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 15 Apr 2026 20:14:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:14:04 GMT
CMD ["sh"]
# Wed, 15 Apr 2026 21:33:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 15 Apr 2026 21:33:18 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 15 Apr 2026 21:33:18 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 15 Apr 2026 21:33:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 15 Apr 2026 21:33:21 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 15 Apr 2026 21:33:21 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 15 Apr 2026 21:33:21 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:33:21 GMT
VOLUME [/var/lib/docker]
# Wed, 15 Apr 2026 21:33:21 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 15 Apr 2026 21:33:21 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 15 Apr 2026 21:33:21 GMT
CMD []
# Wed, 15 Apr 2026 22:24:13 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Wed, 15 Apr 2026 22:24:13 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 15 Apr 2026 22:24:13 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 15 Apr 2026 22:24:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 15 Apr 2026 22:24:14 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 15 Apr 2026 22:24:14 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 15 Apr 2026 22:24:14 GMT
USER rootless
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1f08e8ea565813fe5c533f3bf89a6fcb79b8ef2eb46e2872f132234aa070cf`  
		Last Modified: Wed, 15 Apr 2026 20:14:10 GMT  
		Size: 8.5 MB (8450092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ff0f79f131dfea84e2ad6ee3723888525425bfc628525e86c3cc1b288bace3`  
		Last Modified: Wed, 15 Apr 2026 20:14:10 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35bf88d1a58dc1d9ced6e216552eef44b2392e515454985dcd3f25372d12693`  
		Last Modified: Wed, 15 Apr 2026 20:14:11 GMT  
		Size: 17.9 MB (17921079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0aa9505e9a0f5469b8905ecd253d1fd12569434350a1c94898126c02a4a9c57`  
		Last Modified: Wed, 15 Apr 2026 20:14:11 GMT  
		Size: 20.5 MB (20453111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ff9179479c44e683ee3838185f58e7d707974096437fdccedcb7b1f316aa35`  
		Last Modified: Wed, 15 Apr 2026 20:14:11 GMT  
		Size: 10.0 MB (9982600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0771ed595b2bb7d830d904c0ed7f259d39bb70d0da784d731a39f7a1ceeacb04`  
		Last Modified: Wed, 15 Apr 2026 20:14:12 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627cec3b548e33f50bcd1682915056d5dfd8e5b28476d6c4842c0eb790b1f954`  
		Last Modified: Wed, 15 Apr 2026 20:14:12 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c67b1b44bc81549ba5caf988b00dabcb0c2ca6cee73ef7d756e26b08b1028e`  
		Last Modified: Wed, 15 Apr 2026 20:14:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c169b754493e049763aeab1727fe430cecafcd9032c4389b3053958aebc360c9`  
		Last Modified: Wed, 15 Apr 2026 21:33:31 GMT  
		Size: 7.2 MB (7219816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbba1f41e162f643c431dbb55a4cfb94284235c55c0c226f2f85fdc2797d7d3`  
		Last Modified: Wed, 15 Apr 2026 21:33:30 GMT  
		Size: 101.2 KB (101171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc3e20cde46cbbd2b898524e10c8ed94082175c8c21daf98b34e7a6006aafee`  
		Last Modified: Wed, 15 Apr 2026 21:33:30 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ae4baf5361489e96a43c6d29d47fdd4eb63dd088b10e8bf91df746925678ea`  
		Last Modified: Wed, 15 Apr 2026 21:33:32 GMT  
		Size: 61.8 MB (61790985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7fa8aac1af219d886ca4026da0a5a043fde1dae9d3e8534dd78f23360b8763`  
		Last Modified: Wed, 15 Apr 2026 21:33:32 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f667dde4f795a12a4a9d7129f07e71678ffec2ae9a15d680f09fd672a64ab154`  
		Last Modified: Wed, 15 Apr 2026 21:33:32 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9012b0d6da5801eab238bb387dbb36b8d6a39d5aa7039815d1c9e2a24833a04`  
		Last Modified: Wed, 15 Apr 2026 22:24:20 GMT  
		Size: 3.4 MB (3394534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:960aa9d16806e38df09387de191ea1c727cc5093bc76be222ed5d2a7ca369379`  
		Last Modified: Wed, 15 Apr 2026 22:24:20 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78adb818d73519733cf9dc2e2f2fdf7f7b19abf1d6a5f6050937e7df4fca78d3`  
		Last Modified: Wed, 15 Apr 2026 22:24:20 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f755f683e7f98d710321e727c122d4fd09ba183d051ff46907c74d640b25fcc8`  
		Last Modified: Wed, 15 Apr 2026 22:24:21 GMT  
		Size: 17.9 MB (17882814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d3922b05d8ff64a19ec81b180d6950d39f6867f3dee697b2c3495cb2625bcc`  
		Last Modified: Wed, 15 Apr 2026 22:24:21 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:bb4750590667d42b5f476e8c84bbfb8c1157d5e39d0a4d73884792417165644b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6910dd353dfd57bed56f7465cd51c75e8b8d0c0213fe745a77273d1d7a3f43c4`

```dockerfile
```

-	Layers:
	-	`sha256:4bfbb83e76361cdb9defcea46dc5c48423a4c288e606987803e7f5ee3edc2883`  
		Last Modified: Wed, 15 Apr 2026 22:24:20 GMT  
		Size: 30.8 KB (30752 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.4-windowsservercore`

```console
$ docker pull docker@sha256:d74502081e87e340ae439759f8ec2ea8904f7c6d482c2e01ef2d63e4eab78fce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32690; amd64
	-	windows version 10.0.20348.5020; amd64

### `docker:29.4-windowsservercore` - windows version 10.0.26100.32690; amd64

```console
$ docker pull docker@sha256:d46ee739eeb7f2f3919de6950a0c17a20bb1d22971380a4bb658f91004b6e533
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2185608492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:451cb635e20acafc0c39412eaf4ae9baa78105ff334cffab02ee607ff7e6d625`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Mon, 13 Apr 2026 07:00:46 GMT
RUN Install update 10.0.26100.32690
# Tue, 14 Apr 2026 21:01:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Apr 2026 21:02:06 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Apr 2026 21:02:07 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 14 Apr 2026 21:02:08 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.4.0.zip
# Tue, 14 Apr 2026 21:02:20 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 14 Apr 2026 21:02:20 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 14 Apr 2026 21:02:21 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.windows-amd64.exe
# Tue, 14 Apr 2026 21:02:21 GMT
ENV DOCKER_BUILDX_SHA256=832ddf42373203ee3836a7cb3b16fe5080231491e7edb32019ac0f6fe03b99ed
# Tue, 14 Apr 2026 21:02:35 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 14 Apr 2026 21:02:35 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 14 Apr 2026 21:02:36 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-windows-x86_64.exe
# Tue, 14 Apr 2026 21:02:37 GMT
ENV DOCKER_COMPOSE_SHA256=f7ad2f6965c88153e4902019ec86e95414f0025cba0b6440f328f935a1f8b12b
# Tue, 14 Apr 2026 21:02:43 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3642e4b8bb65ad3768f9f74a0dc48bb2e3294779b5d51573a234bfbe4f65324e`  
		Last Modified: Tue, 14 Apr 2026 18:48:19 GMT  
		Size: 606.9 MB (606926634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68ac02bb5872fbad22e76d99d54ab9b35a1e35759bbddff4f282081ba61100d5`  
		Last Modified: Tue, 14 Apr 2026 21:02:53 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774f3049f1ff5e124ea4f250ee1167ecf42896b3e9bcd067e2f4926ab7a0602d`  
		Last Modified: Tue, 14 Apr 2026 21:02:52 GMT  
		Size: 369.0 KB (368971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae8c2209515b42fd04e40e13a7bca32c3f1f16411393fc4cee562ca8f641bb7`  
		Last Modified: Tue, 14 Apr 2026 21:02:52 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3790546541b36e26bd73f9dfdaf940ebe9fe8013ff0a1cf891fba5e7701b36f`  
		Last Modified: Tue, 14 Apr 2026 21:02:51 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:445fc7e4e770e7d61fdf3492872b7e8bca998a26fffc4515e6344d6952d41f0f`  
		Last Modified: Tue, 14 Apr 2026 21:02:53 GMT  
		Size: 20.2 MB (20155911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b10e1a8a2bc350119623c441e4e0d952f69a7c50a192f764cb4e772b2359ea46`  
		Last Modified: Tue, 14 Apr 2026 21:02:50 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e015ae5429fcbb9151f7c03f83907b5d7d7e627e93ac5666dd54c102cf6f9909`  
		Last Modified: Tue, 14 Apr 2026 21:02:50 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ccf5f62308e0033a83afd116f4287e8951801b466ac66e960370bbd100b0c2b`  
		Last Modified: Tue, 14 Apr 2026 21:02:50 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:308fbcfb831872272d007db361ab5130df2705896b45ad22706bc3ed69a4208b`  
		Last Modified: Tue, 14 Apr 2026 21:02:52 GMT  
		Size: 23.4 MB (23435945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b688d291c4ee097cfa7d6bd989a5730f385d7ed44f7e307e89f8243f044db00a`  
		Last Modified: Tue, 14 Apr 2026 21:02:48 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:391e7d1ca3eae4c8c6acd6553f00297119056613a326ddae9eecb91f055806f4`  
		Last Modified: Tue, 14 Apr 2026 21:02:48 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebbf7aced575c80864697740f99f4f025250da7e7180003679632024cb1987f3`  
		Last Modified: Tue, 14 Apr 2026 21:02:48 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91a6dca9753cc712a25b48c9dbe9e9556c8e7bedfc0f97baf1d62b4cc5503798`  
		Last Modified: Tue, 14 Apr 2026 21:02:50 GMT  
		Size: 11.6 MB (11649820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:29.4-windowsservercore` - windows version 10.0.20348.5020; amd64

```console
$ docker pull docker@sha256:dfeb15b1635155bf333f2033fd733a796d52ede5fa96f898b11e57c12e2412a0
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2125867669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17085df04e58942536df91898016031a94b7bdce5841470b1904db146ee78bca`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Tue, 14 Apr 2026 20:56:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Apr 2026 20:56:45 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Apr 2026 20:56:47 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 14 Apr 2026 20:56:48 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.4.0.zip
# Tue, 14 Apr 2026 20:57:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 14 Apr 2026 20:57:06 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 14 Apr 2026 20:57:07 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.windows-amd64.exe
# Tue, 14 Apr 2026 20:57:08 GMT
ENV DOCKER_BUILDX_SHA256=832ddf42373203ee3836a7cb3b16fe5080231491e7edb32019ac0f6fe03b99ed
# Tue, 14 Apr 2026 20:57:26 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 14 Apr 2026 20:57:27 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 14 Apr 2026 20:57:27 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-windows-x86_64.exe
# Tue, 14 Apr 2026 20:57:28 GMT
ENV DOCKER_COMPOSE_SHA256=f7ad2f6965c88153e4902019ec86e95414f0025cba0b6440f328f935a1f8b12b
# Tue, 14 Apr 2026 20:57:41 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7111ae68f8961455d230dc12d44c2193d29b7c981e35417323613a0c1aa06384`  
		Last Modified: Tue, 14 Apr 2026 17:31:38 GMT  
		Size: 581.2 MB (581192160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4911c7412282b7f1d93fad64ba92d82b42d1ac47c62c4ff886b516f02ea28a55`  
		Last Modified: Tue, 14 Apr 2026 20:57:50 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:151b1d340c8ca7ccd1a0024ff46837779a87b23f90be4512b66ca317e849176b`  
		Last Modified: Tue, 14 Apr 2026 20:57:49 GMT  
		Size: 468.6 KB (468589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c05f9fed2a2861e1aad93076abf9515f202306cf4c6e381ac7b874a9c1d1196`  
		Last Modified: Tue, 14 Apr 2026 20:57:48 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c7405e2df63bc9fec89f85fb677309b86bf973025d8f6b08da62e988f2a629`  
		Last Modified: Tue, 14 Apr 2026 20:57:48 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7f5562b59f5d6e8946261211a66a4f3d8e26a59a704ca4ac6c6405a3ec5f055`  
		Last Modified: Tue, 14 Apr 2026 20:57:50 GMT  
		Size: 20.1 MB (20130256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6f3b1f33de25d313624bac12844dba1d78714061572c4a74d1fe93ad71ce9ad`  
		Last Modified: Tue, 14 Apr 2026 20:57:46 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b55352e1cad29fb0adf25f61e251a05aa1b8ddefb796d15d4793e871bfbaad`  
		Last Modified: Tue, 14 Apr 2026 20:57:47 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a54c516e756ba1351d4ab57988ca90f91af80ca4cce2b27e45eb8dd2ab1ac579`  
		Last Modified: Tue, 14 Apr 2026 20:57:46 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:935fbf8b04da4242e47da7bfee8df2b984a65ed241ffa13f675e09c528cabf8c`  
		Last Modified: Tue, 14 Apr 2026 20:57:54 GMT  
		Size: 23.4 MB (23419466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c62827bb4e356ec246f0a9426681e101860c87ca41a8081887faa7a911a04b19`  
		Last Modified: Tue, 14 Apr 2026 20:57:45 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:830e8d77d7ec0a09f8111f5d4fbe1b1bc385938ec59812da38a864323c7e4963`  
		Last Modified: Tue, 14 Apr 2026 20:57:45 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2405085b41ebd2fbc5a8f4683c3debadbd731eb6e54352fab4de5f2f74bc187d`  
		Last Modified: Tue, 14 Apr 2026 20:57:45 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5d8306d6e8e4e9eb43d89651b670cda922a16548c151c2bdbb51db4656787e6`  
		Last Modified: Tue, 14 Apr 2026 20:57:47 GMT  
		Size: 11.6 MB (11626371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.4-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:bba4a40903cac7bbfad1686d3aef377f0f7294e2311b9da2e962d1cf4526c500
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `docker:29.4-windowsservercore-ltsc2022` - windows version 10.0.20348.5020; amd64

```console
$ docker pull docker@sha256:dfeb15b1635155bf333f2033fd733a796d52ede5fa96f898b11e57c12e2412a0
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2125867669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17085df04e58942536df91898016031a94b7bdce5841470b1904db146ee78bca`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Tue, 14 Apr 2026 20:56:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Apr 2026 20:56:45 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Apr 2026 20:56:47 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 14 Apr 2026 20:56:48 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.4.0.zip
# Tue, 14 Apr 2026 20:57:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 14 Apr 2026 20:57:06 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 14 Apr 2026 20:57:07 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.windows-amd64.exe
# Tue, 14 Apr 2026 20:57:08 GMT
ENV DOCKER_BUILDX_SHA256=832ddf42373203ee3836a7cb3b16fe5080231491e7edb32019ac0f6fe03b99ed
# Tue, 14 Apr 2026 20:57:26 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 14 Apr 2026 20:57:27 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 14 Apr 2026 20:57:27 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-windows-x86_64.exe
# Tue, 14 Apr 2026 20:57:28 GMT
ENV DOCKER_COMPOSE_SHA256=f7ad2f6965c88153e4902019ec86e95414f0025cba0b6440f328f935a1f8b12b
# Tue, 14 Apr 2026 20:57:41 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7111ae68f8961455d230dc12d44c2193d29b7c981e35417323613a0c1aa06384`  
		Last Modified: Tue, 14 Apr 2026 17:31:38 GMT  
		Size: 581.2 MB (581192160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4911c7412282b7f1d93fad64ba92d82b42d1ac47c62c4ff886b516f02ea28a55`  
		Last Modified: Tue, 14 Apr 2026 20:57:50 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:151b1d340c8ca7ccd1a0024ff46837779a87b23f90be4512b66ca317e849176b`  
		Last Modified: Tue, 14 Apr 2026 20:57:49 GMT  
		Size: 468.6 KB (468589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c05f9fed2a2861e1aad93076abf9515f202306cf4c6e381ac7b874a9c1d1196`  
		Last Modified: Tue, 14 Apr 2026 20:57:48 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c7405e2df63bc9fec89f85fb677309b86bf973025d8f6b08da62e988f2a629`  
		Last Modified: Tue, 14 Apr 2026 20:57:48 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7f5562b59f5d6e8946261211a66a4f3d8e26a59a704ca4ac6c6405a3ec5f055`  
		Last Modified: Tue, 14 Apr 2026 20:57:50 GMT  
		Size: 20.1 MB (20130256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6f3b1f33de25d313624bac12844dba1d78714061572c4a74d1fe93ad71ce9ad`  
		Last Modified: Tue, 14 Apr 2026 20:57:46 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b55352e1cad29fb0adf25f61e251a05aa1b8ddefb796d15d4793e871bfbaad`  
		Last Modified: Tue, 14 Apr 2026 20:57:47 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a54c516e756ba1351d4ab57988ca90f91af80ca4cce2b27e45eb8dd2ab1ac579`  
		Last Modified: Tue, 14 Apr 2026 20:57:46 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:935fbf8b04da4242e47da7bfee8df2b984a65ed241ffa13f675e09c528cabf8c`  
		Last Modified: Tue, 14 Apr 2026 20:57:54 GMT  
		Size: 23.4 MB (23419466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c62827bb4e356ec246f0a9426681e101860c87ca41a8081887faa7a911a04b19`  
		Last Modified: Tue, 14 Apr 2026 20:57:45 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:830e8d77d7ec0a09f8111f5d4fbe1b1bc385938ec59812da38a864323c7e4963`  
		Last Modified: Tue, 14 Apr 2026 20:57:45 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2405085b41ebd2fbc5a8f4683c3debadbd731eb6e54352fab4de5f2f74bc187d`  
		Last Modified: Tue, 14 Apr 2026 20:57:45 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5d8306d6e8e4e9eb43d89651b670cda922a16548c151c2bdbb51db4656787e6`  
		Last Modified: Tue, 14 Apr 2026 20:57:47 GMT  
		Size: 11.6 MB (11626371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.4-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:7453a45c03a9501b7dfb80e7846d848c74853c4eed947a7ea01ce577f840a92e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32690; amd64

### `docker:29.4-windowsservercore-ltsc2025` - windows version 10.0.26100.32690; amd64

```console
$ docker pull docker@sha256:d46ee739eeb7f2f3919de6950a0c17a20bb1d22971380a4bb658f91004b6e533
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2185608492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:451cb635e20acafc0c39412eaf4ae9baa78105ff334cffab02ee607ff7e6d625`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Mon, 13 Apr 2026 07:00:46 GMT
RUN Install update 10.0.26100.32690
# Tue, 14 Apr 2026 21:01:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Apr 2026 21:02:06 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Apr 2026 21:02:07 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 14 Apr 2026 21:02:08 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.4.0.zip
# Tue, 14 Apr 2026 21:02:20 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 14 Apr 2026 21:02:20 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 14 Apr 2026 21:02:21 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.windows-amd64.exe
# Tue, 14 Apr 2026 21:02:21 GMT
ENV DOCKER_BUILDX_SHA256=832ddf42373203ee3836a7cb3b16fe5080231491e7edb32019ac0f6fe03b99ed
# Tue, 14 Apr 2026 21:02:35 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 14 Apr 2026 21:02:35 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 14 Apr 2026 21:02:36 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-windows-x86_64.exe
# Tue, 14 Apr 2026 21:02:37 GMT
ENV DOCKER_COMPOSE_SHA256=f7ad2f6965c88153e4902019ec86e95414f0025cba0b6440f328f935a1f8b12b
# Tue, 14 Apr 2026 21:02:43 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3642e4b8bb65ad3768f9f74a0dc48bb2e3294779b5d51573a234bfbe4f65324e`  
		Last Modified: Tue, 14 Apr 2026 18:48:19 GMT  
		Size: 606.9 MB (606926634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68ac02bb5872fbad22e76d99d54ab9b35a1e35759bbddff4f282081ba61100d5`  
		Last Modified: Tue, 14 Apr 2026 21:02:53 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774f3049f1ff5e124ea4f250ee1167ecf42896b3e9bcd067e2f4926ab7a0602d`  
		Last Modified: Tue, 14 Apr 2026 21:02:52 GMT  
		Size: 369.0 KB (368971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae8c2209515b42fd04e40e13a7bca32c3f1f16411393fc4cee562ca8f641bb7`  
		Last Modified: Tue, 14 Apr 2026 21:02:52 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3790546541b36e26bd73f9dfdaf940ebe9fe8013ff0a1cf891fba5e7701b36f`  
		Last Modified: Tue, 14 Apr 2026 21:02:51 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:445fc7e4e770e7d61fdf3492872b7e8bca998a26fffc4515e6344d6952d41f0f`  
		Last Modified: Tue, 14 Apr 2026 21:02:53 GMT  
		Size: 20.2 MB (20155911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b10e1a8a2bc350119623c441e4e0d952f69a7c50a192f764cb4e772b2359ea46`  
		Last Modified: Tue, 14 Apr 2026 21:02:50 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e015ae5429fcbb9151f7c03f83907b5d7d7e627e93ac5666dd54c102cf6f9909`  
		Last Modified: Tue, 14 Apr 2026 21:02:50 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ccf5f62308e0033a83afd116f4287e8951801b466ac66e960370bbd100b0c2b`  
		Last Modified: Tue, 14 Apr 2026 21:02:50 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:308fbcfb831872272d007db361ab5130df2705896b45ad22706bc3ed69a4208b`  
		Last Modified: Tue, 14 Apr 2026 21:02:52 GMT  
		Size: 23.4 MB (23435945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b688d291c4ee097cfa7d6bd989a5730f385d7ed44f7e307e89f8243f044db00a`  
		Last Modified: Tue, 14 Apr 2026 21:02:48 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:391e7d1ca3eae4c8c6acd6553f00297119056613a326ddae9eecb91f055806f4`  
		Last Modified: Tue, 14 Apr 2026 21:02:48 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebbf7aced575c80864697740f99f4f025250da7e7180003679632024cb1987f3`  
		Last Modified: Tue, 14 Apr 2026 21:02:48 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91a6dca9753cc712a25b48c9dbe9e9556c8e7bedfc0f97baf1d62b4cc5503798`  
		Last Modified: Tue, 14 Apr 2026 21:02:50 GMT  
		Size: 11.6 MB (11649820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.4.0`

```console
$ docker pull docker@sha256:a6dd5322747a95cd8e3207bd8d415a8fd20ec34e9c00f06dc019cbd912013489
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

### `docker:29.4.0` - linux; amd64

```console
$ docker pull docker@sha256:4d2c6e334de4b26d492c0a8cc5438e3dbf1a02eee899fc0d4d39b96202c943a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.5 MB (140522901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:304d326357dcfc523ea9ea01226e742f15d0d548d8eaec0e14c3b39387303000`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:16:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 15 Apr 2026 20:16:25 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 15 Apr 2026 20:16:25 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 15 Apr 2026 20:16:27 GMT
ENV DOCKER_VERSION=29.4.0
# Wed, 15 Apr 2026 20:16:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 15 Apr 2026 20:16:27 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Wed, 15 Apr 2026 20:16:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 15 Apr 2026 20:16:28 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 15 Apr 2026 20:16:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 15 Apr 2026 20:16:29 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 15 Apr 2026 20:16:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:16:29 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Apr 2026 20:16:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 15 Apr 2026 20:16:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:16:30 GMT
CMD ["sh"]
# Wed, 15 Apr 2026 21:19:01 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 15 Apr 2026 21:19:02 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 15 Apr 2026 21:19:02 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 15 Apr 2026 21:19:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 15 Apr 2026 21:19:05 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 15 Apr 2026 21:19:05 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 15 Apr 2026 21:19:05 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:19:05 GMT
VOLUME [/var/lib/docker]
# Wed, 15 Apr 2026 21:19:05 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 15 Apr 2026 21:19:05 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 15 Apr 2026 21:19:05 GMT
CMD []
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00fef3bc4d7adc06c42d060d3a4fad2da6d129c5d2dac575a0a34e5276837acc`  
		Last Modified: Wed, 15 Apr 2026 20:16:37 GMT  
		Size: 8.4 MB (8390330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f8bdd90a189e988440fcec9f3b420d55047950b5f7601ba0e57b351852d7ba`  
		Last Modified: Wed, 15 Apr 2026 20:16:36 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4985eb1bbbfe749a8493542e038307f004a28671974b2a082ae06f9391c4aa64`  
		Last Modified: Wed, 15 Apr 2026 20:16:37 GMT  
		Size: 19.5 MB (19464794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859abcc7688b1a7cc3cc9e144132fc9069de384c58f57dcdc67bb82efa576352`  
		Last Modified: Wed, 15 Apr 2026 20:16:37 GMT  
		Size: 22.5 MB (22539232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c99a167aeca4fe59d6c36fcd7dd693309a219446eca7bcdc04b392e4d69c2c4`  
		Last Modified: Wed, 15 Apr 2026 20:16:38 GMT  
		Size: 11.0 MB (10955103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e81a750c9b2d394bb0113dc9e2ac999fdb73fc198aee986c23671ccc8b782c`  
		Last Modified: Wed, 15 Apr 2026 20:16:38 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ba37c8df4e2fbeeea282fc985c366a9d438cb9ac52b521a1ba48cc214ddd6c`  
		Last Modified: Wed, 15 Apr 2026 20:16:39 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26929be3c972c7f0a15b08c4029aaa790ccc1d494702813df05e37cf6c95ece4`  
		Last Modified: Wed, 15 Apr 2026 20:16:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72409ebb253eee0d0ac41d3def31dd521fd7fbb44646380257fce88e92956e1b`  
		Last Modified: Wed, 15 Apr 2026 21:19:16 GMT  
		Size: 6.9 MB (6941794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61b7bb0bfe4127ecc181695a6617bce6875877794291f6f411f1503400774934`  
		Last Modified: Wed, 15 Apr 2026 21:19:15 GMT  
		Size: 92.4 KB (92386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f322cdda1c007efd5a7874085a0a278df1d8cba0c79c539cecdfd441528c5063`  
		Last Modified: Wed, 15 Apr 2026 21:19:16 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b195c7fa897ae20e300894f9c01ab27baa6d026f2966d14da47768c0504f7e0d`  
		Last Modified: Wed, 15 Apr 2026 21:19:18 GMT  
		Size: 68.3 MB (68266921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d71ba441d54fb7122eab57ffb2e5cc6805c4abe5aa1229a369d61713d35c4a`  
		Last Modified: Wed, 15 Apr 2026 21:19:17 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471eb30b983e8a0f853e3d3be9271df608fd2048cec340fa2eaef5e93dccfdd6`  
		Last Modified: Wed, 15 Apr 2026 21:19:17 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4.0` - unknown; unknown

```console
$ docker pull docker@sha256:1c8aa5173659195543e7f2199b877ec50c9f568416a96a31cd42b2fcd07923ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36f6b76c4e162e68e3741832b1fa66576d6705a81ed60bdeeded8cbffb74e2ff`

```dockerfile
```

-	Layers:
	-	`sha256:4c3c193ad694d685d8594f91321d9d1fe73498db66cfb3767583e03cba34f0eb`  
		Last Modified: Wed, 15 Apr 2026 21:19:15 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.4.0` - linux; arm variant v6

```console
$ docker pull docker@sha256:b23cae1ff183bc4e75d88eaf9ba1c6549849f1d134d11fc442d0f885b1f58d4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 MB (132507536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c664d0b218f2b2a9a4e105a5162c0ba967e6162e60df351421a2b174c2b02b2f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:11:18 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 15 Apr 2026 20:11:18 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 15 Apr 2026 20:11:18 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 15 Apr 2026 20:11:22 GMT
ENV DOCKER_VERSION=29.4.0
# Wed, 15 Apr 2026 20:11:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 15 Apr 2026 20:11:22 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Wed, 15 Apr 2026 20:11:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 15 Apr 2026 20:11:25 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 15 Apr 2026 20:11:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 15 Apr 2026 20:11:27 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 15 Apr 2026 20:11:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:11:27 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Apr 2026 20:11:27 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 15 Apr 2026 20:11:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:11:27 GMT
CMD ["sh"]
# Wed, 15 Apr 2026 21:19:39 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 15 Apr 2026 21:19:40 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 15 Apr 2026 21:19:40 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 15 Apr 2026 21:19:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 15 Apr 2026 21:19:44 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 15 Apr 2026 21:19:44 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 15 Apr 2026 21:19:44 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:19:44 GMT
VOLUME [/var/lib/docker]
# Wed, 15 Apr 2026 21:19:44 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 15 Apr 2026 21:19:44 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 15 Apr 2026 21:19:44 GMT
CMD []
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e29b5a067225f28735c3f9c28db7a022b344731761dc5bd14d0b7a283cc13aa1`  
		Last Modified: Wed, 15 Apr 2026 20:11:34 GMT  
		Size: 8.3 MB (8297061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae71f1757016712f17b7c9321ecac9183912e0037f929b5050fa04410093a993`  
		Last Modified: Wed, 15 Apr 2026 20:11:33 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64a558c789f63340dd86a3d8d48163d7ca0b3475c2b5c1d8ca27e0afc43f81a`  
		Last Modified: Wed, 15 Apr 2026 20:11:35 GMT  
		Size: 18.1 MB (18109476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03bc6071f6b066b797f80197a5147fa49e7c18d34820ebbd67e8a05f503815a0`  
		Last Modified: Wed, 15 Apr 2026 20:11:35 GMT  
		Size: 21.2 MB (21151872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84372c97713792c82b059361309092a10362cb4b047854a0b862c3ebeb6f45a7`  
		Last Modified: Wed, 15 Apr 2026 20:11:35 GMT  
		Size: 10.4 MB (10388823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1411d774c190d6fe75a26c80337ed792c1219b393396b9dd4008440601b2e8bb`  
		Last Modified: Wed, 15 Apr 2026 20:11:36 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:213ded2f75d406b851e7f9d90ac09eacb9ecd070136e9e64a5e44a7b62246ab0`  
		Last Modified: Wed, 15 Apr 2026 20:11:36 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9546667a8b53db55a0c88114559b89b5a4c5288c765a0efd17abf18956634f`  
		Last Modified: Wed, 15 Apr 2026 20:11:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db0f2e08cd52770499a4a7b14b1d7035c2bed565f5d1658d36f77ba8cae62ad5`  
		Last Modified: Wed, 15 Apr 2026 21:19:55 GMT  
		Size: 7.3 MB (7278394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810c7f3c3226c75491d45b3028f6aa4e32c04edce7619e9c304e5c7054c6e3e8`  
		Last Modified: Wed, 15 Apr 2026 21:19:55 GMT  
		Size: 91.7 KB (91683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80b9397e0c604f4cffa37ef63fc68b0849fbe399433ee3b1b24e32ea5c1b6138`  
		Last Modified: Wed, 15 Apr 2026 21:19:55 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:578128484de3ef92c76816591ca072998f01b1381725e18fd1c7a4baa20bc9f8`  
		Last Modified: Wed, 15 Apr 2026 21:19:56 GMT  
		Size: 63.6 MB (63610209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2209085b94038497f0af62b68d75961a5b080cb35551dcc8d0eefab6b722484a`  
		Last Modified: Wed, 15 Apr 2026 21:19:56 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b27ed318c8e6661d6fa40585004daf813302e8af45e485fdf0173af3947bc2`  
		Last Modified: Wed, 15 Apr 2026 21:19:56 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4.0` - unknown; unknown

```console
$ docker pull docker@sha256:a01657f9a7e1e95bc00dd7bf0d40d8f4e73263519d316ff513e77cd827e24f6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48c770ff5e3d911a2d76c733a01cc1a9e96597d1aeb12c3470e57cf12936aa28`

```dockerfile
```

-	Layers:
	-	`sha256:147b649936864607c8d1c5530d9427c37768a5718de420c9941b6f3b6625b9d5`  
		Last Modified: Wed, 15 Apr 2026 21:19:54 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.4.0` - linux; arm variant v7

```console
$ docker pull docker@sha256:20d1ab4a0712e057c1adc25f5703a97b31a7f387b43adc77bb7308d4397970e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130593641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ca74a271ab95685bc02e667fcb161e01b626e71e3d25886e49bfab8239d7ded`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:16:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 15 Apr 2026 20:16:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 15 Apr 2026 20:16:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 15 Apr 2026 20:16:18 GMT
ENV DOCKER_VERSION=29.4.0
# Wed, 15 Apr 2026 20:16:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 15 Apr 2026 20:16:18 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Wed, 15 Apr 2026 20:16:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 15 Apr 2026 20:16:20 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 15 Apr 2026 20:16:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 15 Apr 2026 20:16:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 15 Apr 2026 20:16:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:16:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Apr 2026 20:16:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 15 Apr 2026 20:16:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:16:22 GMT
CMD ["sh"]
# Wed, 15 Apr 2026 21:27:26 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 15 Apr 2026 21:27:28 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 15 Apr 2026 21:27:28 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 15 Apr 2026 21:27:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 15 Apr 2026 21:27:31 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 15 Apr 2026 21:27:31 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 15 Apr 2026 21:27:31 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:27:31 GMT
VOLUME [/var/lib/docker]
# Wed, 15 Apr 2026 21:27:31 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 15 Apr 2026 21:27:31 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 15 Apr 2026 21:27:31 GMT
CMD []
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88cb38943f0f0a95a9ef76158143c405f36bad50621b2fd56aa2fc4f3615fd5`  
		Last Modified: Wed, 15 Apr 2026 20:16:29 GMT  
		Size: 7.6 MB (7595768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaaca956ad170283b847286ec873bec980d796519baf3f39fe964aded5374f8e`  
		Last Modified: Wed, 15 Apr 2026 20:16:28 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cdf1c13c7d0f067c56c9771266f9895d1041ebf30f39ab27603e18afb0c9081`  
		Last Modified: Wed, 15 Apr 2026 20:16:29 GMT  
		Size: 18.1 MB (18096362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813eda9384408e479910e06a79744324e1dce0b63fd42e5bce661a6e735e2f32`  
		Last Modified: Wed, 15 Apr 2026 20:16:29 GMT  
		Size: 21.1 MB (21129758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f4b664cfcad12fa1a9762a191ac3534cf78c30dd9df6eff79f75e17bd604215`  
		Last Modified: Wed, 15 Apr 2026 20:16:30 GMT  
		Size: 10.4 MB (10371870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f3580f46ae276e11707530d3b18cc55414bcb1f7a672d3cef371193e0e0947`  
		Last Modified: Wed, 15 Apr 2026 20:16:30 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d214a288fe8f0a47169af907737952cefa9e61f078490a75828a439107530b2`  
		Last Modified: Wed, 15 Apr 2026 20:16:31 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf0d872d260394713b2443444bb53d508d83624734c0239dcda7ff1830303db8`  
		Last Modified: Wed, 15 Apr 2026 20:16:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89db5f2f3e615ce6454e5c1c42292805de5a924c4769cb726472a5f992eef448`  
		Last Modified: Wed, 15 Apr 2026 21:27:42 GMT  
		Size: 6.6 MB (6577217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a486198c8f3ba2ab5d5c0c2444157dbdb3a24ef48b6dcbe399e92e72a5e6c28`  
		Last Modified: Wed, 15 Apr 2026 21:27:42 GMT  
		Size: 88.0 KB (88036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba24e0fe682bf1faf33f78d5b19ecad454f21527c9a6c33cfb4c1d694b52779`  
		Last Modified: Wed, 15 Apr 2026 21:27:42 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ca224f3bf33d1172adfccf0c242f89893fde617bd5885ef7545ecd22e41ef4f`  
		Last Modified: Wed, 15 Apr 2026 21:27:44 GMT  
		Size: 63.4 MB (63443351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac3934cb427133bc539854b45e314e2dc44838a979414cf67dd89810b967f06`  
		Last Modified: Wed, 15 Apr 2026 21:27:43 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5e8455627c95fe22aa58fead7cbf2a0934fd4d57d760756577ec0b8c9bf4bc`  
		Last Modified: Wed, 15 Apr 2026 21:27:43 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4.0` - unknown; unknown

```console
$ docker pull docker@sha256:9376e04ebe10bd90bf0a7a85bddeb4c723ab3c8e9ae5290a6f522143cdbed03d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58ce25b3cedf687af0bcb158bb0a1d2a8523dfeadcddc68360fc3394f815f730`

```dockerfile
```

-	Layers:
	-	`sha256:ecdd6391528d66bfad436f41aef96daa292510a5ddd3f115f031dd1728b3dd36`  
		Last Modified: Wed, 15 Apr 2026 21:27:42 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.4.0` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:553d694bc3ae2a92b67b73072e3923a8d2256e609b568c60d08e4544e8f39ff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.1 MB (130126872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5c1c78f7262d1e00eef13317919dc25b6d65c96115e46f851ab09818f2ddf0b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:13:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 15 Apr 2026 20:13:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 15 Apr 2026 20:13:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 15 Apr 2026 20:14:02 GMT
ENV DOCKER_VERSION=29.4.0
# Wed, 15 Apr 2026 20:14:02 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 15 Apr 2026 20:14:02 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Wed, 15 Apr 2026 20:14:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 15 Apr 2026 20:14:03 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 15 Apr 2026 20:14:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 15 Apr 2026 20:14:04 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 15 Apr 2026 20:14:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:14:04 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Apr 2026 20:14:04 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 15 Apr 2026 20:14:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:14:04 GMT
CMD ["sh"]
# Wed, 15 Apr 2026 21:33:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 15 Apr 2026 21:33:18 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 15 Apr 2026 21:33:18 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 15 Apr 2026 21:33:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 15 Apr 2026 21:33:21 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 15 Apr 2026 21:33:21 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 15 Apr 2026 21:33:21 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:33:21 GMT
VOLUME [/var/lib/docker]
# Wed, 15 Apr 2026 21:33:21 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 15 Apr 2026 21:33:21 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 15 Apr 2026 21:33:21 GMT
CMD []
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1f08e8ea565813fe5c533f3bf89a6fcb79b8ef2eb46e2872f132234aa070cf`  
		Last Modified: Wed, 15 Apr 2026 20:14:10 GMT  
		Size: 8.5 MB (8450092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ff0f79f131dfea84e2ad6ee3723888525425bfc628525e86c3cc1b288bace3`  
		Last Modified: Wed, 15 Apr 2026 20:14:10 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35bf88d1a58dc1d9ced6e216552eef44b2392e515454985dcd3f25372d12693`  
		Last Modified: Wed, 15 Apr 2026 20:14:11 GMT  
		Size: 17.9 MB (17921079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0aa9505e9a0f5469b8905ecd253d1fd12569434350a1c94898126c02a4a9c57`  
		Last Modified: Wed, 15 Apr 2026 20:14:11 GMT  
		Size: 20.5 MB (20453111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ff9179479c44e683ee3838185f58e7d707974096437fdccedcb7b1f316aa35`  
		Last Modified: Wed, 15 Apr 2026 20:14:11 GMT  
		Size: 10.0 MB (9982600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0771ed595b2bb7d830d904c0ed7f259d39bb70d0da784d731a39f7a1ceeacb04`  
		Last Modified: Wed, 15 Apr 2026 20:14:12 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627cec3b548e33f50bcd1682915056d5dfd8e5b28476d6c4842c0eb790b1f954`  
		Last Modified: Wed, 15 Apr 2026 20:14:12 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c67b1b44bc81549ba5caf988b00dabcb0c2ca6cee73ef7d756e26b08b1028e`  
		Last Modified: Wed, 15 Apr 2026 20:14:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c169b754493e049763aeab1727fe430cecafcd9032c4389b3053958aebc360c9`  
		Last Modified: Wed, 15 Apr 2026 21:33:31 GMT  
		Size: 7.2 MB (7219816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbba1f41e162f643c431dbb55a4cfb94284235c55c0c226f2f85fdc2797d7d3`  
		Last Modified: Wed, 15 Apr 2026 21:33:30 GMT  
		Size: 101.2 KB (101171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc3e20cde46cbbd2b898524e10c8ed94082175c8c21daf98b34e7a6006aafee`  
		Last Modified: Wed, 15 Apr 2026 21:33:30 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ae4baf5361489e96a43c6d29d47fdd4eb63dd088b10e8bf91df746925678ea`  
		Last Modified: Wed, 15 Apr 2026 21:33:32 GMT  
		Size: 61.8 MB (61790985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7fa8aac1af219d886ca4026da0a5a043fde1dae9d3e8534dd78f23360b8763`  
		Last Modified: Wed, 15 Apr 2026 21:33:32 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f667dde4f795a12a4a9d7129f07e71678ffec2ae9a15d680f09fd672a64ab154`  
		Last Modified: Wed, 15 Apr 2026 21:33:32 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4.0` - unknown; unknown

```console
$ docker pull docker@sha256:71c18f631e3205680e2fcd0ea55f0f373c7fb19de8336794fe07f3d4793786b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48d9407668f8511b7b181ffcfea6ce22705df56aaf20a9dd84a0930f31f6ecf7`

```dockerfile
```

-	Layers:
	-	`sha256:623b2bc83b8d25632b5e152b95570ef2a7af85709fedfa2ae3ed9d312b61c77c`  
		Last Modified: Wed, 15 Apr 2026 21:33:30 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.4.0-alpine3.23`

```console
$ docker pull docker@sha256:a6dd5322747a95cd8e3207bd8d415a8fd20ec34e9c00f06dc019cbd912013489
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

### `docker:29.4.0-alpine3.23` - linux; amd64

```console
$ docker pull docker@sha256:4d2c6e334de4b26d492c0a8cc5438e3dbf1a02eee899fc0d4d39b96202c943a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.5 MB (140522901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:304d326357dcfc523ea9ea01226e742f15d0d548d8eaec0e14c3b39387303000`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:16:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 15 Apr 2026 20:16:25 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 15 Apr 2026 20:16:25 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 15 Apr 2026 20:16:27 GMT
ENV DOCKER_VERSION=29.4.0
# Wed, 15 Apr 2026 20:16:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 15 Apr 2026 20:16:27 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Wed, 15 Apr 2026 20:16:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 15 Apr 2026 20:16:28 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 15 Apr 2026 20:16:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 15 Apr 2026 20:16:29 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 15 Apr 2026 20:16:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:16:29 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Apr 2026 20:16:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 15 Apr 2026 20:16:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:16:30 GMT
CMD ["sh"]
# Wed, 15 Apr 2026 21:19:01 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 15 Apr 2026 21:19:02 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 15 Apr 2026 21:19:02 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 15 Apr 2026 21:19:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 15 Apr 2026 21:19:05 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 15 Apr 2026 21:19:05 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 15 Apr 2026 21:19:05 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:19:05 GMT
VOLUME [/var/lib/docker]
# Wed, 15 Apr 2026 21:19:05 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 15 Apr 2026 21:19:05 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 15 Apr 2026 21:19:05 GMT
CMD []
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00fef3bc4d7adc06c42d060d3a4fad2da6d129c5d2dac575a0a34e5276837acc`  
		Last Modified: Wed, 15 Apr 2026 20:16:37 GMT  
		Size: 8.4 MB (8390330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f8bdd90a189e988440fcec9f3b420d55047950b5f7601ba0e57b351852d7ba`  
		Last Modified: Wed, 15 Apr 2026 20:16:36 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4985eb1bbbfe749a8493542e038307f004a28671974b2a082ae06f9391c4aa64`  
		Last Modified: Wed, 15 Apr 2026 20:16:37 GMT  
		Size: 19.5 MB (19464794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859abcc7688b1a7cc3cc9e144132fc9069de384c58f57dcdc67bb82efa576352`  
		Last Modified: Wed, 15 Apr 2026 20:16:37 GMT  
		Size: 22.5 MB (22539232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c99a167aeca4fe59d6c36fcd7dd693309a219446eca7bcdc04b392e4d69c2c4`  
		Last Modified: Wed, 15 Apr 2026 20:16:38 GMT  
		Size: 11.0 MB (10955103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e81a750c9b2d394bb0113dc9e2ac999fdb73fc198aee986c23671ccc8b782c`  
		Last Modified: Wed, 15 Apr 2026 20:16:38 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ba37c8df4e2fbeeea282fc985c366a9d438cb9ac52b521a1ba48cc214ddd6c`  
		Last Modified: Wed, 15 Apr 2026 20:16:39 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26929be3c972c7f0a15b08c4029aaa790ccc1d494702813df05e37cf6c95ece4`  
		Last Modified: Wed, 15 Apr 2026 20:16:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72409ebb253eee0d0ac41d3def31dd521fd7fbb44646380257fce88e92956e1b`  
		Last Modified: Wed, 15 Apr 2026 21:19:16 GMT  
		Size: 6.9 MB (6941794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61b7bb0bfe4127ecc181695a6617bce6875877794291f6f411f1503400774934`  
		Last Modified: Wed, 15 Apr 2026 21:19:15 GMT  
		Size: 92.4 KB (92386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f322cdda1c007efd5a7874085a0a278df1d8cba0c79c539cecdfd441528c5063`  
		Last Modified: Wed, 15 Apr 2026 21:19:16 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b195c7fa897ae20e300894f9c01ab27baa6d026f2966d14da47768c0504f7e0d`  
		Last Modified: Wed, 15 Apr 2026 21:19:18 GMT  
		Size: 68.3 MB (68266921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d71ba441d54fb7122eab57ffb2e5cc6805c4abe5aa1229a369d61713d35c4a`  
		Last Modified: Wed, 15 Apr 2026 21:19:17 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471eb30b983e8a0f853e3d3be9271df608fd2048cec340fa2eaef5e93dccfdd6`  
		Last Modified: Wed, 15 Apr 2026 21:19:17 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4.0-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:1c8aa5173659195543e7f2199b877ec50c9f568416a96a31cd42b2fcd07923ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36f6b76c4e162e68e3741832b1fa66576d6705a81ed60bdeeded8cbffb74e2ff`

```dockerfile
```

-	Layers:
	-	`sha256:4c3c193ad694d685d8594f91321d9d1fe73498db66cfb3767583e03cba34f0eb`  
		Last Modified: Wed, 15 Apr 2026 21:19:15 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.4.0-alpine3.23` - linux; arm variant v6

```console
$ docker pull docker@sha256:b23cae1ff183bc4e75d88eaf9ba1c6549849f1d134d11fc442d0f885b1f58d4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 MB (132507536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c664d0b218f2b2a9a4e105a5162c0ba967e6162e60df351421a2b174c2b02b2f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:11:18 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 15 Apr 2026 20:11:18 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 15 Apr 2026 20:11:18 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 15 Apr 2026 20:11:22 GMT
ENV DOCKER_VERSION=29.4.0
# Wed, 15 Apr 2026 20:11:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 15 Apr 2026 20:11:22 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Wed, 15 Apr 2026 20:11:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 15 Apr 2026 20:11:25 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 15 Apr 2026 20:11:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 15 Apr 2026 20:11:27 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 15 Apr 2026 20:11:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:11:27 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Apr 2026 20:11:27 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 15 Apr 2026 20:11:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:11:27 GMT
CMD ["sh"]
# Wed, 15 Apr 2026 21:19:39 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 15 Apr 2026 21:19:40 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 15 Apr 2026 21:19:40 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 15 Apr 2026 21:19:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 15 Apr 2026 21:19:44 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 15 Apr 2026 21:19:44 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 15 Apr 2026 21:19:44 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:19:44 GMT
VOLUME [/var/lib/docker]
# Wed, 15 Apr 2026 21:19:44 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 15 Apr 2026 21:19:44 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 15 Apr 2026 21:19:44 GMT
CMD []
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e29b5a067225f28735c3f9c28db7a022b344731761dc5bd14d0b7a283cc13aa1`  
		Last Modified: Wed, 15 Apr 2026 20:11:34 GMT  
		Size: 8.3 MB (8297061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae71f1757016712f17b7c9321ecac9183912e0037f929b5050fa04410093a993`  
		Last Modified: Wed, 15 Apr 2026 20:11:33 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64a558c789f63340dd86a3d8d48163d7ca0b3475c2b5c1d8ca27e0afc43f81a`  
		Last Modified: Wed, 15 Apr 2026 20:11:35 GMT  
		Size: 18.1 MB (18109476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03bc6071f6b066b797f80197a5147fa49e7c18d34820ebbd67e8a05f503815a0`  
		Last Modified: Wed, 15 Apr 2026 20:11:35 GMT  
		Size: 21.2 MB (21151872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84372c97713792c82b059361309092a10362cb4b047854a0b862c3ebeb6f45a7`  
		Last Modified: Wed, 15 Apr 2026 20:11:35 GMT  
		Size: 10.4 MB (10388823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1411d774c190d6fe75a26c80337ed792c1219b393396b9dd4008440601b2e8bb`  
		Last Modified: Wed, 15 Apr 2026 20:11:36 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:213ded2f75d406b851e7f9d90ac09eacb9ecd070136e9e64a5e44a7b62246ab0`  
		Last Modified: Wed, 15 Apr 2026 20:11:36 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9546667a8b53db55a0c88114559b89b5a4c5288c765a0efd17abf18956634f`  
		Last Modified: Wed, 15 Apr 2026 20:11:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db0f2e08cd52770499a4a7b14b1d7035c2bed565f5d1658d36f77ba8cae62ad5`  
		Last Modified: Wed, 15 Apr 2026 21:19:55 GMT  
		Size: 7.3 MB (7278394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810c7f3c3226c75491d45b3028f6aa4e32c04edce7619e9c304e5c7054c6e3e8`  
		Last Modified: Wed, 15 Apr 2026 21:19:55 GMT  
		Size: 91.7 KB (91683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80b9397e0c604f4cffa37ef63fc68b0849fbe399433ee3b1b24e32ea5c1b6138`  
		Last Modified: Wed, 15 Apr 2026 21:19:55 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:578128484de3ef92c76816591ca072998f01b1381725e18fd1c7a4baa20bc9f8`  
		Last Modified: Wed, 15 Apr 2026 21:19:56 GMT  
		Size: 63.6 MB (63610209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2209085b94038497f0af62b68d75961a5b080cb35551dcc8d0eefab6b722484a`  
		Last Modified: Wed, 15 Apr 2026 21:19:56 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b27ed318c8e6661d6fa40585004daf813302e8af45e485fdf0173af3947bc2`  
		Last Modified: Wed, 15 Apr 2026 21:19:56 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4.0-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:a01657f9a7e1e95bc00dd7bf0d40d8f4e73263519d316ff513e77cd827e24f6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48c770ff5e3d911a2d76c733a01cc1a9e96597d1aeb12c3470e57cf12936aa28`

```dockerfile
```

-	Layers:
	-	`sha256:147b649936864607c8d1c5530d9427c37768a5718de420c9941b6f3b6625b9d5`  
		Last Modified: Wed, 15 Apr 2026 21:19:54 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.4.0-alpine3.23` - linux; arm variant v7

```console
$ docker pull docker@sha256:20d1ab4a0712e057c1adc25f5703a97b31a7f387b43adc77bb7308d4397970e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130593641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ca74a271ab95685bc02e667fcb161e01b626e71e3d25886e49bfab8239d7ded`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:16:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 15 Apr 2026 20:16:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 15 Apr 2026 20:16:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 15 Apr 2026 20:16:18 GMT
ENV DOCKER_VERSION=29.4.0
# Wed, 15 Apr 2026 20:16:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 15 Apr 2026 20:16:18 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Wed, 15 Apr 2026 20:16:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 15 Apr 2026 20:16:20 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 15 Apr 2026 20:16:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 15 Apr 2026 20:16:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 15 Apr 2026 20:16:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:16:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Apr 2026 20:16:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 15 Apr 2026 20:16:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:16:22 GMT
CMD ["sh"]
# Wed, 15 Apr 2026 21:27:26 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 15 Apr 2026 21:27:28 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 15 Apr 2026 21:27:28 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 15 Apr 2026 21:27:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 15 Apr 2026 21:27:31 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 15 Apr 2026 21:27:31 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 15 Apr 2026 21:27:31 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:27:31 GMT
VOLUME [/var/lib/docker]
# Wed, 15 Apr 2026 21:27:31 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 15 Apr 2026 21:27:31 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 15 Apr 2026 21:27:31 GMT
CMD []
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88cb38943f0f0a95a9ef76158143c405f36bad50621b2fd56aa2fc4f3615fd5`  
		Last Modified: Wed, 15 Apr 2026 20:16:29 GMT  
		Size: 7.6 MB (7595768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaaca956ad170283b847286ec873bec980d796519baf3f39fe964aded5374f8e`  
		Last Modified: Wed, 15 Apr 2026 20:16:28 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cdf1c13c7d0f067c56c9771266f9895d1041ebf30f39ab27603e18afb0c9081`  
		Last Modified: Wed, 15 Apr 2026 20:16:29 GMT  
		Size: 18.1 MB (18096362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813eda9384408e479910e06a79744324e1dce0b63fd42e5bce661a6e735e2f32`  
		Last Modified: Wed, 15 Apr 2026 20:16:29 GMT  
		Size: 21.1 MB (21129758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f4b664cfcad12fa1a9762a191ac3534cf78c30dd9df6eff79f75e17bd604215`  
		Last Modified: Wed, 15 Apr 2026 20:16:30 GMT  
		Size: 10.4 MB (10371870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f3580f46ae276e11707530d3b18cc55414bcb1f7a672d3cef371193e0e0947`  
		Last Modified: Wed, 15 Apr 2026 20:16:30 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d214a288fe8f0a47169af907737952cefa9e61f078490a75828a439107530b2`  
		Last Modified: Wed, 15 Apr 2026 20:16:31 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf0d872d260394713b2443444bb53d508d83624734c0239dcda7ff1830303db8`  
		Last Modified: Wed, 15 Apr 2026 20:16:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89db5f2f3e615ce6454e5c1c42292805de5a924c4769cb726472a5f992eef448`  
		Last Modified: Wed, 15 Apr 2026 21:27:42 GMT  
		Size: 6.6 MB (6577217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a486198c8f3ba2ab5d5c0c2444157dbdb3a24ef48b6dcbe399e92e72a5e6c28`  
		Last Modified: Wed, 15 Apr 2026 21:27:42 GMT  
		Size: 88.0 KB (88036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba24e0fe682bf1faf33f78d5b19ecad454f21527c9a6c33cfb4c1d694b52779`  
		Last Modified: Wed, 15 Apr 2026 21:27:42 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ca224f3bf33d1172adfccf0c242f89893fde617bd5885ef7545ecd22e41ef4f`  
		Last Modified: Wed, 15 Apr 2026 21:27:44 GMT  
		Size: 63.4 MB (63443351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac3934cb427133bc539854b45e314e2dc44838a979414cf67dd89810b967f06`  
		Last Modified: Wed, 15 Apr 2026 21:27:43 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5e8455627c95fe22aa58fead7cbf2a0934fd4d57d760756577ec0b8c9bf4bc`  
		Last Modified: Wed, 15 Apr 2026 21:27:43 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4.0-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:9376e04ebe10bd90bf0a7a85bddeb4c723ab3c8e9ae5290a6f522143cdbed03d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58ce25b3cedf687af0bcb158bb0a1d2a8523dfeadcddc68360fc3394f815f730`

```dockerfile
```

-	Layers:
	-	`sha256:ecdd6391528d66bfad436f41aef96daa292510a5ddd3f115f031dd1728b3dd36`  
		Last Modified: Wed, 15 Apr 2026 21:27:42 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.4.0-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:553d694bc3ae2a92b67b73072e3923a8d2256e609b568c60d08e4544e8f39ff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.1 MB (130126872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5c1c78f7262d1e00eef13317919dc25b6d65c96115e46f851ab09818f2ddf0b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:13:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 15 Apr 2026 20:13:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 15 Apr 2026 20:13:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 15 Apr 2026 20:14:02 GMT
ENV DOCKER_VERSION=29.4.0
# Wed, 15 Apr 2026 20:14:02 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 15 Apr 2026 20:14:02 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Wed, 15 Apr 2026 20:14:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 15 Apr 2026 20:14:03 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 15 Apr 2026 20:14:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 15 Apr 2026 20:14:04 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 15 Apr 2026 20:14:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:14:04 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Apr 2026 20:14:04 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 15 Apr 2026 20:14:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:14:04 GMT
CMD ["sh"]
# Wed, 15 Apr 2026 21:33:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 15 Apr 2026 21:33:18 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 15 Apr 2026 21:33:18 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 15 Apr 2026 21:33:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 15 Apr 2026 21:33:21 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 15 Apr 2026 21:33:21 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 15 Apr 2026 21:33:21 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:33:21 GMT
VOLUME [/var/lib/docker]
# Wed, 15 Apr 2026 21:33:21 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 15 Apr 2026 21:33:21 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 15 Apr 2026 21:33:21 GMT
CMD []
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1f08e8ea565813fe5c533f3bf89a6fcb79b8ef2eb46e2872f132234aa070cf`  
		Last Modified: Wed, 15 Apr 2026 20:14:10 GMT  
		Size: 8.5 MB (8450092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ff0f79f131dfea84e2ad6ee3723888525425bfc628525e86c3cc1b288bace3`  
		Last Modified: Wed, 15 Apr 2026 20:14:10 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35bf88d1a58dc1d9ced6e216552eef44b2392e515454985dcd3f25372d12693`  
		Last Modified: Wed, 15 Apr 2026 20:14:11 GMT  
		Size: 17.9 MB (17921079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0aa9505e9a0f5469b8905ecd253d1fd12569434350a1c94898126c02a4a9c57`  
		Last Modified: Wed, 15 Apr 2026 20:14:11 GMT  
		Size: 20.5 MB (20453111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ff9179479c44e683ee3838185f58e7d707974096437fdccedcb7b1f316aa35`  
		Last Modified: Wed, 15 Apr 2026 20:14:11 GMT  
		Size: 10.0 MB (9982600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0771ed595b2bb7d830d904c0ed7f259d39bb70d0da784d731a39f7a1ceeacb04`  
		Last Modified: Wed, 15 Apr 2026 20:14:12 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627cec3b548e33f50bcd1682915056d5dfd8e5b28476d6c4842c0eb790b1f954`  
		Last Modified: Wed, 15 Apr 2026 20:14:12 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c67b1b44bc81549ba5caf988b00dabcb0c2ca6cee73ef7d756e26b08b1028e`  
		Last Modified: Wed, 15 Apr 2026 20:14:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c169b754493e049763aeab1727fe430cecafcd9032c4389b3053958aebc360c9`  
		Last Modified: Wed, 15 Apr 2026 21:33:31 GMT  
		Size: 7.2 MB (7219816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbba1f41e162f643c431dbb55a4cfb94284235c55c0c226f2f85fdc2797d7d3`  
		Last Modified: Wed, 15 Apr 2026 21:33:30 GMT  
		Size: 101.2 KB (101171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc3e20cde46cbbd2b898524e10c8ed94082175c8c21daf98b34e7a6006aafee`  
		Last Modified: Wed, 15 Apr 2026 21:33:30 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ae4baf5361489e96a43c6d29d47fdd4eb63dd088b10e8bf91df746925678ea`  
		Last Modified: Wed, 15 Apr 2026 21:33:32 GMT  
		Size: 61.8 MB (61790985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7fa8aac1af219d886ca4026da0a5a043fde1dae9d3e8534dd78f23360b8763`  
		Last Modified: Wed, 15 Apr 2026 21:33:32 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f667dde4f795a12a4a9d7129f07e71678ffec2ae9a15d680f09fd672a64ab154`  
		Last Modified: Wed, 15 Apr 2026 21:33:32 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4.0-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:71c18f631e3205680e2fcd0ea55f0f373c7fb19de8336794fe07f3d4793786b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48d9407668f8511b7b181ffcfea6ce22705df56aaf20a9dd84a0930f31f6ecf7`

```dockerfile
```

-	Layers:
	-	`sha256:623b2bc83b8d25632b5e152b95570ef2a7af85709fedfa2ae3ed9d312b61c77c`  
		Last Modified: Wed, 15 Apr 2026 21:33:30 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.4.0-cli`

```console
$ docker pull docker@sha256:2efe7c8e806b35050def6ba1ba0ddad67b521a0a6d37f4910b3d88f11b495d03
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

### `docker:29.4.0-cli` - linux; amd64

```console
$ docker pull docker@sha256:bb21349a52c00b206ad8b5c03fa52023c741c4cf11f269d40d40b9ebaac73d96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65215798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b7281830dcb31636378f562663cd54df1ce82f631d1cd037968aae8c1034bc2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:16:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 15 Apr 2026 20:16:25 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 15 Apr 2026 20:16:25 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 15 Apr 2026 20:16:27 GMT
ENV DOCKER_VERSION=29.4.0
# Wed, 15 Apr 2026 20:16:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 15 Apr 2026 20:16:27 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Wed, 15 Apr 2026 20:16:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 15 Apr 2026 20:16:28 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 15 Apr 2026 20:16:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 15 Apr 2026 20:16:29 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 15 Apr 2026 20:16:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:16:29 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Apr 2026 20:16:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 15 Apr 2026 20:16:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:16:30 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00fef3bc4d7adc06c42d060d3a4fad2da6d129c5d2dac575a0a34e5276837acc`  
		Last Modified: Wed, 15 Apr 2026 20:16:37 GMT  
		Size: 8.4 MB (8390330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f8bdd90a189e988440fcec9f3b420d55047950b5f7601ba0e57b351852d7ba`  
		Last Modified: Wed, 15 Apr 2026 20:16:36 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4985eb1bbbfe749a8493542e038307f004a28671974b2a082ae06f9391c4aa64`  
		Last Modified: Wed, 15 Apr 2026 20:16:37 GMT  
		Size: 19.5 MB (19464794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859abcc7688b1a7cc3cc9e144132fc9069de384c58f57dcdc67bb82efa576352`  
		Last Modified: Wed, 15 Apr 2026 20:16:37 GMT  
		Size: 22.5 MB (22539232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c99a167aeca4fe59d6c36fcd7dd693309a219446eca7bcdc04b392e4d69c2c4`  
		Last Modified: Wed, 15 Apr 2026 20:16:38 GMT  
		Size: 11.0 MB (10955103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e81a750c9b2d394bb0113dc9e2ac999fdb73fc198aee986c23671ccc8b782c`  
		Last Modified: Wed, 15 Apr 2026 20:16:38 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ba37c8df4e2fbeeea282fc985c366a9d438cb9ac52b521a1ba48cc214ddd6c`  
		Last Modified: Wed, 15 Apr 2026 20:16:39 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26929be3c972c7f0a15b08c4029aaa790ccc1d494702813df05e37cf6c95ece4`  
		Last Modified: Wed, 15 Apr 2026 20:16:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:5c727440eaffe25d1a2f89a448a8aeef8118f192ce752f5f55b0e7dcf3bee15d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d4150275339c1686c0b7eab0e338d57f441efecf63ffadf5cfa59dfe3a3e9a0`

```dockerfile
```

-	Layers:
	-	`sha256:083400d83f577b87f30bc974ae857508bdaeb3c56dafaa2a3985dbc6a2be5c32`  
		Last Modified: Wed, 15 Apr 2026 20:16:36 GMT  
		Size: 38.1 KB (38056 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.4.0-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:b0448a7e451eb2df18d117260c232b9064f3b11bd751ac2e603c18bef0289a37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61521248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ab4c337f9a3ba981939d8eb77b75c53cbc28458c647ccce32e93d0f7a99ee4e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:11:18 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 15 Apr 2026 20:11:18 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 15 Apr 2026 20:11:18 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 15 Apr 2026 20:11:22 GMT
ENV DOCKER_VERSION=29.4.0
# Wed, 15 Apr 2026 20:11:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 15 Apr 2026 20:11:22 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Wed, 15 Apr 2026 20:11:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 15 Apr 2026 20:11:25 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 15 Apr 2026 20:11:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 15 Apr 2026 20:11:27 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 15 Apr 2026 20:11:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:11:27 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Apr 2026 20:11:27 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 15 Apr 2026 20:11:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:11:27 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e29b5a067225f28735c3f9c28db7a022b344731761dc5bd14d0b7a283cc13aa1`  
		Last Modified: Wed, 15 Apr 2026 20:11:34 GMT  
		Size: 8.3 MB (8297061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae71f1757016712f17b7c9321ecac9183912e0037f929b5050fa04410093a993`  
		Last Modified: Wed, 15 Apr 2026 20:11:33 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64a558c789f63340dd86a3d8d48163d7ca0b3475c2b5c1d8ca27e0afc43f81a`  
		Last Modified: Wed, 15 Apr 2026 20:11:35 GMT  
		Size: 18.1 MB (18109476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03bc6071f6b066b797f80197a5147fa49e7c18d34820ebbd67e8a05f503815a0`  
		Last Modified: Wed, 15 Apr 2026 20:11:35 GMT  
		Size: 21.2 MB (21151872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84372c97713792c82b059361309092a10362cb4b047854a0b862c3ebeb6f45a7`  
		Last Modified: Wed, 15 Apr 2026 20:11:35 GMT  
		Size: 10.4 MB (10388823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1411d774c190d6fe75a26c80337ed792c1219b393396b9dd4008440601b2e8bb`  
		Last Modified: Wed, 15 Apr 2026 20:11:36 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:213ded2f75d406b851e7f9d90ac09eacb9ecd070136e9e64a5e44a7b62246ab0`  
		Last Modified: Wed, 15 Apr 2026 20:11:36 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9546667a8b53db55a0c88114559b89b5a4c5288c765a0efd17abf18956634f`  
		Last Modified: Wed, 15 Apr 2026 20:11:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:bbcdf7618a730942664487ce478f3a269e4859185ac161e3578319a0f54ff6d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8a566184814fc34593f5137a7bba3c2c3aae7de569de008b69e5efb6fd4f2b8`

```dockerfile
```

-	Layers:
	-	`sha256:34582c23f82fc6f533690de02a4263c869ac6e2e06850e19652639cbf36d4f4c`  
		Last Modified: Wed, 15 Apr 2026 20:11:33 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.4.0-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:75b479961472cf73f0407e0b3c7576c45be650ab0f523fc539f33fde7777f22f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60479031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:254b0d5926521e59075cd4b154a10ba99b2e222f9e1b682d6ef3bda0b94beaef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:16:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 15 Apr 2026 20:16:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 15 Apr 2026 20:16:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 15 Apr 2026 20:16:18 GMT
ENV DOCKER_VERSION=29.4.0
# Wed, 15 Apr 2026 20:16:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 15 Apr 2026 20:16:18 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Wed, 15 Apr 2026 20:16:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 15 Apr 2026 20:16:20 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 15 Apr 2026 20:16:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 15 Apr 2026 20:16:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 15 Apr 2026 20:16:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:16:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Apr 2026 20:16:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 15 Apr 2026 20:16:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:16:22 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88cb38943f0f0a95a9ef76158143c405f36bad50621b2fd56aa2fc4f3615fd5`  
		Last Modified: Wed, 15 Apr 2026 20:16:29 GMT  
		Size: 7.6 MB (7595768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaaca956ad170283b847286ec873bec980d796519baf3f39fe964aded5374f8e`  
		Last Modified: Wed, 15 Apr 2026 20:16:28 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cdf1c13c7d0f067c56c9771266f9895d1041ebf30f39ab27603e18afb0c9081`  
		Last Modified: Wed, 15 Apr 2026 20:16:29 GMT  
		Size: 18.1 MB (18096362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813eda9384408e479910e06a79744324e1dce0b63fd42e5bce661a6e735e2f32`  
		Last Modified: Wed, 15 Apr 2026 20:16:29 GMT  
		Size: 21.1 MB (21129758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f4b664cfcad12fa1a9762a191ac3534cf78c30dd9df6eff79f75e17bd604215`  
		Last Modified: Wed, 15 Apr 2026 20:16:30 GMT  
		Size: 10.4 MB (10371870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f3580f46ae276e11707530d3b18cc55414bcb1f7a672d3cef371193e0e0947`  
		Last Modified: Wed, 15 Apr 2026 20:16:30 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d214a288fe8f0a47169af907737952cefa9e61f078490a75828a439107530b2`  
		Last Modified: Wed, 15 Apr 2026 20:16:31 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf0d872d260394713b2443444bb53d508d83624734c0239dcda7ff1830303db8`  
		Last Modified: Wed, 15 Apr 2026 20:16:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:70f0601152bac7df07b2933f0e46a2774591dbebc7e87523cc02d222b56c86b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e085d1943182e6d53f4b66b7d1654479506a41c31da6cbd8241cba54df3ce900`

```dockerfile
```

-	Layers:
	-	`sha256:368fab9b9711e124e80b9dedf4aa9bea5ba28ad952bacb0003647ef444f12135`  
		Last Modified: Wed, 15 Apr 2026 20:16:28 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.4.0-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:9d3f67fe1f4cf51c084744dec419b466b7075f5b365ef4b9b791187d9c2d4127
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.0 MB (61008901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dea3a61a70d2ba11898616b2f246eaeef9d1c75b7041f2e45826da60d2e47276`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:13:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 15 Apr 2026 20:13:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 15 Apr 2026 20:13:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 15 Apr 2026 20:14:02 GMT
ENV DOCKER_VERSION=29.4.0
# Wed, 15 Apr 2026 20:14:02 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 15 Apr 2026 20:14:02 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Wed, 15 Apr 2026 20:14:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 15 Apr 2026 20:14:03 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 15 Apr 2026 20:14:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 15 Apr 2026 20:14:04 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 15 Apr 2026 20:14:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:14:04 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Apr 2026 20:14:04 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 15 Apr 2026 20:14:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:14:04 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1f08e8ea565813fe5c533f3bf89a6fcb79b8ef2eb46e2872f132234aa070cf`  
		Last Modified: Wed, 15 Apr 2026 20:14:10 GMT  
		Size: 8.5 MB (8450092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ff0f79f131dfea84e2ad6ee3723888525425bfc628525e86c3cc1b288bace3`  
		Last Modified: Wed, 15 Apr 2026 20:14:10 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35bf88d1a58dc1d9ced6e216552eef44b2392e515454985dcd3f25372d12693`  
		Last Modified: Wed, 15 Apr 2026 20:14:11 GMT  
		Size: 17.9 MB (17921079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0aa9505e9a0f5469b8905ecd253d1fd12569434350a1c94898126c02a4a9c57`  
		Last Modified: Wed, 15 Apr 2026 20:14:11 GMT  
		Size: 20.5 MB (20453111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ff9179479c44e683ee3838185f58e7d707974096437fdccedcb7b1f316aa35`  
		Last Modified: Wed, 15 Apr 2026 20:14:11 GMT  
		Size: 10.0 MB (9982600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0771ed595b2bb7d830d904c0ed7f259d39bb70d0da784d731a39f7a1ceeacb04`  
		Last Modified: Wed, 15 Apr 2026 20:14:12 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627cec3b548e33f50bcd1682915056d5dfd8e5b28476d6c4842c0eb790b1f954`  
		Last Modified: Wed, 15 Apr 2026 20:14:12 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c67b1b44bc81549ba5caf988b00dabcb0c2ca6cee73ef7d756e26b08b1028e`  
		Last Modified: Wed, 15 Apr 2026 20:14:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:e021182c1f750cfc367850ea8b786139b8a3c428c84711dcaf82dad470636664
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a194ccda70da01232600045e81eff9a9985e4f5f2d0762a6d6f356e6cff9fe0`

```dockerfile
```

-	Layers:
	-	`sha256:c94d9b9821f47c73547b7085c1041bda87c05335abab499b01c9fcc9f12a80bf`  
		Last Modified: Wed, 15 Apr 2026 20:14:10 GMT  
		Size: 38.3 KB (38258 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.4.0-cli-alpine3.23`

```console
$ docker pull docker@sha256:2efe7c8e806b35050def6ba1ba0ddad67b521a0a6d37f4910b3d88f11b495d03
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

### `docker:29.4.0-cli-alpine3.23` - linux; amd64

```console
$ docker pull docker@sha256:bb21349a52c00b206ad8b5c03fa52023c741c4cf11f269d40d40b9ebaac73d96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65215798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b7281830dcb31636378f562663cd54df1ce82f631d1cd037968aae8c1034bc2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:16:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 15 Apr 2026 20:16:25 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 15 Apr 2026 20:16:25 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 15 Apr 2026 20:16:27 GMT
ENV DOCKER_VERSION=29.4.0
# Wed, 15 Apr 2026 20:16:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 15 Apr 2026 20:16:27 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Wed, 15 Apr 2026 20:16:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 15 Apr 2026 20:16:28 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 15 Apr 2026 20:16:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 15 Apr 2026 20:16:29 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 15 Apr 2026 20:16:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:16:29 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Apr 2026 20:16:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 15 Apr 2026 20:16:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:16:30 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00fef3bc4d7adc06c42d060d3a4fad2da6d129c5d2dac575a0a34e5276837acc`  
		Last Modified: Wed, 15 Apr 2026 20:16:37 GMT  
		Size: 8.4 MB (8390330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f8bdd90a189e988440fcec9f3b420d55047950b5f7601ba0e57b351852d7ba`  
		Last Modified: Wed, 15 Apr 2026 20:16:36 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4985eb1bbbfe749a8493542e038307f004a28671974b2a082ae06f9391c4aa64`  
		Last Modified: Wed, 15 Apr 2026 20:16:37 GMT  
		Size: 19.5 MB (19464794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859abcc7688b1a7cc3cc9e144132fc9069de384c58f57dcdc67bb82efa576352`  
		Last Modified: Wed, 15 Apr 2026 20:16:37 GMT  
		Size: 22.5 MB (22539232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c99a167aeca4fe59d6c36fcd7dd693309a219446eca7bcdc04b392e4d69c2c4`  
		Last Modified: Wed, 15 Apr 2026 20:16:38 GMT  
		Size: 11.0 MB (10955103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e81a750c9b2d394bb0113dc9e2ac999fdb73fc198aee986c23671ccc8b782c`  
		Last Modified: Wed, 15 Apr 2026 20:16:38 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ba37c8df4e2fbeeea282fc985c366a9d438cb9ac52b521a1ba48cc214ddd6c`  
		Last Modified: Wed, 15 Apr 2026 20:16:39 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26929be3c972c7f0a15b08c4029aaa790ccc1d494702813df05e37cf6c95ece4`  
		Last Modified: Wed, 15 Apr 2026 20:16:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4.0-cli-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:5c727440eaffe25d1a2f89a448a8aeef8118f192ce752f5f55b0e7dcf3bee15d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d4150275339c1686c0b7eab0e338d57f441efecf63ffadf5cfa59dfe3a3e9a0`

```dockerfile
```

-	Layers:
	-	`sha256:083400d83f577b87f30bc974ae857508bdaeb3c56dafaa2a3985dbc6a2be5c32`  
		Last Modified: Wed, 15 Apr 2026 20:16:36 GMT  
		Size: 38.1 KB (38056 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.4.0-cli-alpine3.23` - linux; arm variant v6

```console
$ docker pull docker@sha256:b0448a7e451eb2df18d117260c232b9064f3b11bd751ac2e603c18bef0289a37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61521248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ab4c337f9a3ba981939d8eb77b75c53cbc28458c647ccce32e93d0f7a99ee4e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:11:18 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 15 Apr 2026 20:11:18 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 15 Apr 2026 20:11:18 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 15 Apr 2026 20:11:22 GMT
ENV DOCKER_VERSION=29.4.0
# Wed, 15 Apr 2026 20:11:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 15 Apr 2026 20:11:22 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Wed, 15 Apr 2026 20:11:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 15 Apr 2026 20:11:25 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 15 Apr 2026 20:11:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 15 Apr 2026 20:11:27 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 15 Apr 2026 20:11:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:11:27 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Apr 2026 20:11:27 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 15 Apr 2026 20:11:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:11:27 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e29b5a067225f28735c3f9c28db7a022b344731761dc5bd14d0b7a283cc13aa1`  
		Last Modified: Wed, 15 Apr 2026 20:11:34 GMT  
		Size: 8.3 MB (8297061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae71f1757016712f17b7c9321ecac9183912e0037f929b5050fa04410093a993`  
		Last Modified: Wed, 15 Apr 2026 20:11:33 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64a558c789f63340dd86a3d8d48163d7ca0b3475c2b5c1d8ca27e0afc43f81a`  
		Last Modified: Wed, 15 Apr 2026 20:11:35 GMT  
		Size: 18.1 MB (18109476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03bc6071f6b066b797f80197a5147fa49e7c18d34820ebbd67e8a05f503815a0`  
		Last Modified: Wed, 15 Apr 2026 20:11:35 GMT  
		Size: 21.2 MB (21151872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84372c97713792c82b059361309092a10362cb4b047854a0b862c3ebeb6f45a7`  
		Last Modified: Wed, 15 Apr 2026 20:11:35 GMT  
		Size: 10.4 MB (10388823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1411d774c190d6fe75a26c80337ed792c1219b393396b9dd4008440601b2e8bb`  
		Last Modified: Wed, 15 Apr 2026 20:11:36 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:213ded2f75d406b851e7f9d90ac09eacb9ecd070136e9e64a5e44a7b62246ab0`  
		Last Modified: Wed, 15 Apr 2026 20:11:36 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9546667a8b53db55a0c88114559b89b5a4c5288c765a0efd17abf18956634f`  
		Last Modified: Wed, 15 Apr 2026 20:11:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4.0-cli-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:bbcdf7618a730942664487ce478f3a269e4859185ac161e3578319a0f54ff6d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8a566184814fc34593f5137a7bba3c2c3aae7de569de008b69e5efb6fd4f2b8`

```dockerfile
```

-	Layers:
	-	`sha256:34582c23f82fc6f533690de02a4263c869ac6e2e06850e19652639cbf36d4f4c`  
		Last Modified: Wed, 15 Apr 2026 20:11:33 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.4.0-cli-alpine3.23` - linux; arm variant v7

```console
$ docker pull docker@sha256:75b479961472cf73f0407e0b3c7576c45be650ab0f523fc539f33fde7777f22f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60479031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:254b0d5926521e59075cd4b154a10ba99b2e222f9e1b682d6ef3bda0b94beaef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:16:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 15 Apr 2026 20:16:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 15 Apr 2026 20:16:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 15 Apr 2026 20:16:18 GMT
ENV DOCKER_VERSION=29.4.0
# Wed, 15 Apr 2026 20:16:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 15 Apr 2026 20:16:18 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Wed, 15 Apr 2026 20:16:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 15 Apr 2026 20:16:20 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 15 Apr 2026 20:16:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 15 Apr 2026 20:16:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 15 Apr 2026 20:16:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:16:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Apr 2026 20:16:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 15 Apr 2026 20:16:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:16:22 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88cb38943f0f0a95a9ef76158143c405f36bad50621b2fd56aa2fc4f3615fd5`  
		Last Modified: Wed, 15 Apr 2026 20:16:29 GMT  
		Size: 7.6 MB (7595768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaaca956ad170283b847286ec873bec980d796519baf3f39fe964aded5374f8e`  
		Last Modified: Wed, 15 Apr 2026 20:16:28 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cdf1c13c7d0f067c56c9771266f9895d1041ebf30f39ab27603e18afb0c9081`  
		Last Modified: Wed, 15 Apr 2026 20:16:29 GMT  
		Size: 18.1 MB (18096362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813eda9384408e479910e06a79744324e1dce0b63fd42e5bce661a6e735e2f32`  
		Last Modified: Wed, 15 Apr 2026 20:16:29 GMT  
		Size: 21.1 MB (21129758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f4b664cfcad12fa1a9762a191ac3534cf78c30dd9df6eff79f75e17bd604215`  
		Last Modified: Wed, 15 Apr 2026 20:16:30 GMT  
		Size: 10.4 MB (10371870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f3580f46ae276e11707530d3b18cc55414bcb1f7a672d3cef371193e0e0947`  
		Last Modified: Wed, 15 Apr 2026 20:16:30 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d214a288fe8f0a47169af907737952cefa9e61f078490a75828a439107530b2`  
		Last Modified: Wed, 15 Apr 2026 20:16:31 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf0d872d260394713b2443444bb53d508d83624734c0239dcda7ff1830303db8`  
		Last Modified: Wed, 15 Apr 2026 20:16:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4.0-cli-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:70f0601152bac7df07b2933f0e46a2774591dbebc7e87523cc02d222b56c86b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e085d1943182e6d53f4b66b7d1654479506a41c31da6cbd8241cba54df3ce900`

```dockerfile
```

-	Layers:
	-	`sha256:368fab9b9711e124e80b9dedf4aa9bea5ba28ad952bacb0003647ef444f12135`  
		Last Modified: Wed, 15 Apr 2026 20:16:28 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.4.0-cli-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:9d3f67fe1f4cf51c084744dec419b466b7075f5b365ef4b9b791187d9c2d4127
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.0 MB (61008901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dea3a61a70d2ba11898616b2f246eaeef9d1c75b7041f2e45826da60d2e47276`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:13:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 15 Apr 2026 20:13:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 15 Apr 2026 20:13:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 15 Apr 2026 20:14:02 GMT
ENV DOCKER_VERSION=29.4.0
# Wed, 15 Apr 2026 20:14:02 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 15 Apr 2026 20:14:02 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Wed, 15 Apr 2026 20:14:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 15 Apr 2026 20:14:03 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 15 Apr 2026 20:14:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 15 Apr 2026 20:14:04 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 15 Apr 2026 20:14:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:14:04 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Apr 2026 20:14:04 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 15 Apr 2026 20:14:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:14:04 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1f08e8ea565813fe5c533f3bf89a6fcb79b8ef2eb46e2872f132234aa070cf`  
		Last Modified: Wed, 15 Apr 2026 20:14:10 GMT  
		Size: 8.5 MB (8450092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ff0f79f131dfea84e2ad6ee3723888525425bfc628525e86c3cc1b288bace3`  
		Last Modified: Wed, 15 Apr 2026 20:14:10 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35bf88d1a58dc1d9ced6e216552eef44b2392e515454985dcd3f25372d12693`  
		Last Modified: Wed, 15 Apr 2026 20:14:11 GMT  
		Size: 17.9 MB (17921079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0aa9505e9a0f5469b8905ecd253d1fd12569434350a1c94898126c02a4a9c57`  
		Last Modified: Wed, 15 Apr 2026 20:14:11 GMT  
		Size: 20.5 MB (20453111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ff9179479c44e683ee3838185f58e7d707974096437fdccedcb7b1f316aa35`  
		Last Modified: Wed, 15 Apr 2026 20:14:11 GMT  
		Size: 10.0 MB (9982600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0771ed595b2bb7d830d904c0ed7f259d39bb70d0da784d731a39f7a1ceeacb04`  
		Last Modified: Wed, 15 Apr 2026 20:14:12 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627cec3b548e33f50bcd1682915056d5dfd8e5b28476d6c4842c0eb790b1f954`  
		Last Modified: Wed, 15 Apr 2026 20:14:12 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c67b1b44bc81549ba5caf988b00dabcb0c2ca6cee73ef7d756e26b08b1028e`  
		Last Modified: Wed, 15 Apr 2026 20:14:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4.0-cli-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:e021182c1f750cfc367850ea8b786139b8a3c428c84711dcaf82dad470636664
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a194ccda70da01232600045e81eff9a9985e4f5f2d0762a6d6f356e6cff9fe0`

```dockerfile
```

-	Layers:
	-	`sha256:c94d9b9821f47c73547b7085c1041bda87c05335abab499b01c9fcc9f12a80bf`  
		Last Modified: Wed, 15 Apr 2026 20:14:10 GMT  
		Size: 38.3 KB (38258 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.4.0-dind`

```console
$ docker pull docker@sha256:a6dd5322747a95cd8e3207bd8d415a8fd20ec34e9c00f06dc019cbd912013489
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

### `docker:29.4.0-dind` - linux; amd64

```console
$ docker pull docker@sha256:4d2c6e334de4b26d492c0a8cc5438e3dbf1a02eee899fc0d4d39b96202c943a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.5 MB (140522901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:304d326357dcfc523ea9ea01226e742f15d0d548d8eaec0e14c3b39387303000`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:16:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 15 Apr 2026 20:16:25 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 15 Apr 2026 20:16:25 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 15 Apr 2026 20:16:27 GMT
ENV DOCKER_VERSION=29.4.0
# Wed, 15 Apr 2026 20:16:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 15 Apr 2026 20:16:27 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Wed, 15 Apr 2026 20:16:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 15 Apr 2026 20:16:28 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 15 Apr 2026 20:16:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 15 Apr 2026 20:16:29 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 15 Apr 2026 20:16:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:16:29 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Apr 2026 20:16:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 15 Apr 2026 20:16:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:16:30 GMT
CMD ["sh"]
# Wed, 15 Apr 2026 21:19:01 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 15 Apr 2026 21:19:02 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 15 Apr 2026 21:19:02 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 15 Apr 2026 21:19:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 15 Apr 2026 21:19:05 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 15 Apr 2026 21:19:05 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 15 Apr 2026 21:19:05 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:19:05 GMT
VOLUME [/var/lib/docker]
# Wed, 15 Apr 2026 21:19:05 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 15 Apr 2026 21:19:05 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 15 Apr 2026 21:19:05 GMT
CMD []
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00fef3bc4d7adc06c42d060d3a4fad2da6d129c5d2dac575a0a34e5276837acc`  
		Last Modified: Wed, 15 Apr 2026 20:16:37 GMT  
		Size: 8.4 MB (8390330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f8bdd90a189e988440fcec9f3b420d55047950b5f7601ba0e57b351852d7ba`  
		Last Modified: Wed, 15 Apr 2026 20:16:36 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4985eb1bbbfe749a8493542e038307f004a28671974b2a082ae06f9391c4aa64`  
		Last Modified: Wed, 15 Apr 2026 20:16:37 GMT  
		Size: 19.5 MB (19464794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859abcc7688b1a7cc3cc9e144132fc9069de384c58f57dcdc67bb82efa576352`  
		Last Modified: Wed, 15 Apr 2026 20:16:37 GMT  
		Size: 22.5 MB (22539232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c99a167aeca4fe59d6c36fcd7dd693309a219446eca7bcdc04b392e4d69c2c4`  
		Last Modified: Wed, 15 Apr 2026 20:16:38 GMT  
		Size: 11.0 MB (10955103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e81a750c9b2d394bb0113dc9e2ac999fdb73fc198aee986c23671ccc8b782c`  
		Last Modified: Wed, 15 Apr 2026 20:16:38 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ba37c8df4e2fbeeea282fc985c366a9d438cb9ac52b521a1ba48cc214ddd6c`  
		Last Modified: Wed, 15 Apr 2026 20:16:39 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26929be3c972c7f0a15b08c4029aaa790ccc1d494702813df05e37cf6c95ece4`  
		Last Modified: Wed, 15 Apr 2026 20:16:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72409ebb253eee0d0ac41d3def31dd521fd7fbb44646380257fce88e92956e1b`  
		Last Modified: Wed, 15 Apr 2026 21:19:16 GMT  
		Size: 6.9 MB (6941794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61b7bb0bfe4127ecc181695a6617bce6875877794291f6f411f1503400774934`  
		Last Modified: Wed, 15 Apr 2026 21:19:15 GMT  
		Size: 92.4 KB (92386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f322cdda1c007efd5a7874085a0a278df1d8cba0c79c539cecdfd441528c5063`  
		Last Modified: Wed, 15 Apr 2026 21:19:16 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b195c7fa897ae20e300894f9c01ab27baa6d026f2966d14da47768c0504f7e0d`  
		Last Modified: Wed, 15 Apr 2026 21:19:18 GMT  
		Size: 68.3 MB (68266921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d71ba441d54fb7122eab57ffb2e5cc6805c4abe5aa1229a369d61713d35c4a`  
		Last Modified: Wed, 15 Apr 2026 21:19:17 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471eb30b983e8a0f853e3d3be9271df608fd2048cec340fa2eaef5e93dccfdd6`  
		Last Modified: Wed, 15 Apr 2026 21:19:17 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4.0-dind` - unknown; unknown

```console
$ docker pull docker@sha256:1c8aa5173659195543e7f2199b877ec50c9f568416a96a31cd42b2fcd07923ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36f6b76c4e162e68e3741832b1fa66576d6705a81ed60bdeeded8cbffb74e2ff`

```dockerfile
```

-	Layers:
	-	`sha256:4c3c193ad694d685d8594f91321d9d1fe73498db66cfb3767583e03cba34f0eb`  
		Last Modified: Wed, 15 Apr 2026 21:19:15 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.4.0-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:b23cae1ff183bc4e75d88eaf9ba1c6549849f1d134d11fc442d0f885b1f58d4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 MB (132507536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c664d0b218f2b2a9a4e105a5162c0ba967e6162e60df351421a2b174c2b02b2f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:11:18 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 15 Apr 2026 20:11:18 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 15 Apr 2026 20:11:18 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 15 Apr 2026 20:11:22 GMT
ENV DOCKER_VERSION=29.4.0
# Wed, 15 Apr 2026 20:11:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 15 Apr 2026 20:11:22 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Wed, 15 Apr 2026 20:11:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 15 Apr 2026 20:11:25 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 15 Apr 2026 20:11:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 15 Apr 2026 20:11:27 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 15 Apr 2026 20:11:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:11:27 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Apr 2026 20:11:27 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 15 Apr 2026 20:11:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:11:27 GMT
CMD ["sh"]
# Wed, 15 Apr 2026 21:19:39 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 15 Apr 2026 21:19:40 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 15 Apr 2026 21:19:40 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 15 Apr 2026 21:19:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 15 Apr 2026 21:19:44 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 15 Apr 2026 21:19:44 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 15 Apr 2026 21:19:44 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:19:44 GMT
VOLUME [/var/lib/docker]
# Wed, 15 Apr 2026 21:19:44 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 15 Apr 2026 21:19:44 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 15 Apr 2026 21:19:44 GMT
CMD []
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e29b5a067225f28735c3f9c28db7a022b344731761dc5bd14d0b7a283cc13aa1`  
		Last Modified: Wed, 15 Apr 2026 20:11:34 GMT  
		Size: 8.3 MB (8297061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae71f1757016712f17b7c9321ecac9183912e0037f929b5050fa04410093a993`  
		Last Modified: Wed, 15 Apr 2026 20:11:33 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64a558c789f63340dd86a3d8d48163d7ca0b3475c2b5c1d8ca27e0afc43f81a`  
		Last Modified: Wed, 15 Apr 2026 20:11:35 GMT  
		Size: 18.1 MB (18109476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03bc6071f6b066b797f80197a5147fa49e7c18d34820ebbd67e8a05f503815a0`  
		Last Modified: Wed, 15 Apr 2026 20:11:35 GMT  
		Size: 21.2 MB (21151872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84372c97713792c82b059361309092a10362cb4b047854a0b862c3ebeb6f45a7`  
		Last Modified: Wed, 15 Apr 2026 20:11:35 GMT  
		Size: 10.4 MB (10388823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1411d774c190d6fe75a26c80337ed792c1219b393396b9dd4008440601b2e8bb`  
		Last Modified: Wed, 15 Apr 2026 20:11:36 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:213ded2f75d406b851e7f9d90ac09eacb9ecd070136e9e64a5e44a7b62246ab0`  
		Last Modified: Wed, 15 Apr 2026 20:11:36 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9546667a8b53db55a0c88114559b89b5a4c5288c765a0efd17abf18956634f`  
		Last Modified: Wed, 15 Apr 2026 20:11:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db0f2e08cd52770499a4a7b14b1d7035c2bed565f5d1658d36f77ba8cae62ad5`  
		Last Modified: Wed, 15 Apr 2026 21:19:55 GMT  
		Size: 7.3 MB (7278394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810c7f3c3226c75491d45b3028f6aa4e32c04edce7619e9c304e5c7054c6e3e8`  
		Last Modified: Wed, 15 Apr 2026 21:19:55 GMT  
		Size: 91.7 KB (91683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80b9397e0c604f4cffa37ef63fc68b0849fbe399433ee3b1b24e32ea5c1b6138`  
		Last Modified: Wed, 15 Apr 2026 21:19:55 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:578128484de3ef92c76816591ca072998f01b1381725e18fd1c7a4baa20bc9f8`  
		Last Modified: Wed, 15 Apr 2026 21:19:56 GMT  
		Size: 63.6 MB (63610209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2209085b94038497f0af62b68d75961a5b080cb35551dcc8d0eefab6b722484a`  
		Last Modified: Wed, 15 Apr 2026 21:19:56 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b27ed318c8e6661d6fa40585004daf813302e8af45e485fdf0173af3947bc2`  
		Last Modified: Wed, 15 Apr 2026 21:19:56 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4.0-dind` - unknown; unknown

```console
$ docker pull docker@sha256:a01657f9a7e1e95bc00dd7bf0d40d8f4e73263519d316ff513e77cd827e24f6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48c770ff5e3d911a2d76c733a01cc1a9e96597d1aeb12c3470e57cf12936aa28`

```dockerfile
```

-	Layers:
	-	`sha256:147b649936864607c8d1c5530d9427c37768a5718de420c9941b6f3b6625b9d5`  
		Last Modified: Wed, 15 Apr 2026 21:19:54 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.4.0-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:20d1ab4a0712e057c1adc25f5703a97b31a7f387b43adc77bb7308d4397970e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130593641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ca74a271ab95685bc02e667fcb161e01b626e71e3d25886e49bfab8239d7ded`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:16:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 15 Apr 2026 20:16:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 15 Apr 2026 20:16:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 15 Apr 2026 20:16:18 GMT
ENV DOCKER_VERSION=29.4.0
# Wed, 15 Apr 2026 20:16:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 15 Apr 2026 20:16:18 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Wed, 15 Apr 2026 20:16:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 15 Apr 2026 20:16:20 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 15 Apr 2026 20:16:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 15 Apr 2026 20:16:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 15 Apr 2026 20:16:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:16:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Apr 2026 20:16:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 15 Apr 2026 20:16:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:16:22 GMT
CMD ["sh"]
# Wed, 15 Apr 2026 21:27:26 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 15 Apr 2026 21:27:28 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 15 Apr 2026 21:27:28 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 15 Apr 2026 21:27:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 15 Apr 2026 21:27:31 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 15 Apr 2026 21:27:31 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 15 Apr 2026 21:27:31 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:27:31 GMT
VOLUME [/var/lib/docker]
# Wed, 15 Apr 2026 21:27:31 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 15 Apr 2026 21:27:31 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 15 Apr 2026 21:27:31 GMT
CMD []
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88cb38943f0f0a95a9ef76158143c405f36bad50621b2fd56aa2fc4f3615fd5`  
		Last Modified: Wed, 15 Apr 2026 20:16:29 GMT  
		Size: 7.6 MB (7595768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaaca956ad170283b847286ec873bec980d796519baf3f39fe964aded5374f8e`  
		Last Modified: Wed, 15 Apr 2026 20:16:28 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cdf1c13c7d0f067c56c9771266f9895d1041ebf30f39ab27603e18afb0c9081`  
		Last Modified: Wed, 15 Apr 2026 20:16:29 GMT  
		Size: 18.1 MB (18096362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813eda9384408e479910e06a79744324e1dce0b63fd42e5bce661a6e735e2f32`  
		Last Modified: Wed, 15 Apr 2026 20:16:29 GMT  
		Size: 21.1 MB (21129758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f4b664cfcad12fa1a9762a191ac3534cf78c30dd9df6eff79f75e17bd604215`  
		Last Modified: Wed, 15 Apr 2026 20:16:30 GMT  
		Size: 10.4 MB (10371870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f3580f46ae276e11707530d3b18cc55414bcb1f7a672d3cef371193e0e0947`  
		Last Modified: Wed, 15 Apr 2026 20:16:30 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d214a288fe8f0a47169af907737952cefa9e61f078490a75828a439107530b2`  
		Last Modified: Wed, 15 Apr 2026 20:16:31 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf0d872d260394713b2443444bb53d508d83624734c0239dcda7ff1830303db8`  
		Last Modified: Wed, 15 Apr 2026 20:16:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89db5f2f3e615ce6454e5c1c42292805de5a924c4769cb726472a5f992eef448`  
		Last Modified: Wed, 15 Apr 2026 21:27:42 GMT  
		Size: 6.6 MB (6577217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a486198c8f3ba2ab5d5c0c2444157dbdb3a24ef48b6dcbe399e92e72a5e6c28`  
		Last Modified: Wed, 15 Apr 2026 21:27:42 GMT  
		Size: 88.0 KB (88036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba24e0fe682bf1faf33f78d5b19ecad454f21527c9a6c33cfb4c1d694b52779`  
		Last Modified: Wed, 15 Apr 2026 21:27:42 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ca224f3bf33d1172adfccf0c242f89893fde617bd5885ef7545ecd22e41ef4f`  
		Last Modified: Wed, 15 Apr 2026 21:27:44 GMT  
		Size: 63.4 MB (63443351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac3934cb427133bc539854b45e314e2dc44838a979414cf67dd89810b967f06`  
		Last Modified: Wed, 15 Apr 2026 21:27:43 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5e8455627c95fe22aa58fead7cbf2a0934fd4d57d760756577ec0b8c9bf4bc`  
		Last Modified: Wed, 15 Apr 2026 21:27:43 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4.0-dind` - unknown; unknown

```console
$ docker pull docker@sha256:9376e04ebe10bd90bf0a7a85bddeb4c723ab3c8e9ae5290a6f522143cdbed03d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58ce25b3cedf687af0bcb158bb0a1d2a8523dfeadcddc68360fc3394f815f730`

```dockerfile
```

-	Layers:
	-	`sha256:ecdd6391528d66bfad436f41aef96daa292510a5ddd3f115f031dd1728b3dd36`  
		Last Modified: Wed, 15 Apr 2026 21:27:42 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.4.0-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:553d694bc3ae2a92b67b73072e3923a8d2256e609b568c60d08e4544e8f39ff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.1 MB (130126872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5c1c78f7262d1e00eef13317919dc25b6d65c96115e46f851ab09818f2ddf0b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:13:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 15 Apr 2026 20:13:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 15 Apr 2026 20:13:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 15 Apr 2026 20:14:02 GMT
ENV DOCKER_VERSION=29.4.0
# Wed, 15 Apr 2026 20:14:02 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 15 Apr 2026 20:14:02 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Wed, 15 Apr 2026 20:14:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 15 Apr 2026 20:14:03 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 15 Apr 2026 20:14:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 15 Apr 2026 20:14:04 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 15 Apr 2026 20:14:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:14:04 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Apr 2026 20:14:04 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 15 Apr 2026 20:14:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:14:04 GMT
CMD ["sh"]
# Wed, 15 Apr 2026 21:33:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 15 Apr 2026 21:33:18 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 15 Apr 2026 21:33:18 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 15 Apr 2026 21:33:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 15 Apr 2026 21:33:21 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 15 Apr 2026 21:33:21 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 15 Apr 2026 21:33:21 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:33:21 GMT
VOLUME [/var/lib/docker]
# Wed, 15 Apr 2026 21:33:21 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 15 Apr 2026 21:33:21 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 15 Apr 2026 21:33:21 GMT
CMD []
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1f08e8ea565813fe5c533f3bf89a6fcb79b8ef2eb46e2872f132234aa070cf`  
		Last Modified: Wed, 15 Apr 2026 20:14:10 GMT  
		Size: 8.5 MB (8450092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ff0f79f131dfea84e2ad6ee3723888525425bfc628525e86c3cc1b288bace3`  
		Last Modified: Wed, 15 Apr 2026 20:14:10 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35bf88d1a58dc1d9ced6e216552eef44b2392e515454985dcd3f25372d12693`  
		Last Modified: Wed, 15 Apr 2026 20:14:11 GMT  
		Size: 17.9 MB (17921079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0aa9505e9a0f5469b8905ecd253d1fd12569434350a1c94898126c02a4a9c57`  
		Last Modified: Wed, 15 Apr 2026 20:14:11 GMT  
		Size: 20.5 MB (20453111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ff9179479c44e683ee3838185f58e7d707974096437fdccedcb7b1f316aa35`  
		Last Modified: Wed, 15 Apr 2026 20:14:11 GMT  
		Size: 10.0 MB (9982600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0771ed595b2bb7d830d904c0ed7f259d39bb70d0da784d731a39f7a1ceeacb04`  
		Last Modified: Wed, 15 Apr 2026 20:14:12 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627cec3b548e33f50bcd1682915056d5dfd8e5b28476d6c4842c0eb790b1f954`  
		Last Modified: Wed, 15 Apr 2026 20:14:12 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c67b1b44bc81549ba5caf988b00dabcb0c2ca6cee73ef7d756e26b08b1028e`  
		Last Modified: Wed, 15 Apr 2026 20:14:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c169b754493e049763aeab1727fe430cecafcd9032c4389b3053958aebc360c9`  
		Last Modified: Wed, 15 Apr 2026 21:33:31 GMT  
		Size: 7.2 MB (7219816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbba1f41e162f643c431dbb55a4cfb94284235c55c0c226f2f85fdc2797d7d3`  
		Last Modified: Wed, 15 Apr 2026 21:33:30 GMT  
		Size: 101.2 KB (101171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc3e20cde46cbbd2b898524e10c8ed94082175c8c21daf98b34e7a6006aafee`  
		Last Modified: Wed, 15 Apr 2026 21:33:30 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ae4baf5361489e96a43c6d29d47fdd4eb63dd088b10e8bf91df746925678ea`  
		Last Modified: Wed, 15 Apr 2026 21:33:32 GMT  
		Size: 61.8 MB (61790985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7fa8aac1af219d886ca4026da0a5a043fde1dae9d3e8534dd78f23360b8763`  
		Last Modified: Wed, 15 Apr 2026 21:33:32 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f667dde4f795a12a4a9d7129f07e71678ffec2ae9a15d680f09fd672a64ab154`  
		Last Modified: Wed, 15 Apr 2026 21:33:32 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4.0-dind` - unknown; unknown

```console
$ docker pull docker@sha256:71c18f631e3205680e2fcd0ea55f0f373c7fb19de8336794fe07f3d4793786b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48d9407668f8511b7b181ffcfea6ce22705df56aaf20a9dd84a0930f31f6ecf7`

```dockerfile
```

-	Layers:
	-	`sha256:623b2bc83b8d25632b5e152b95570ef2a7af85709fedfa2ae3ed9d312b61c77c`  
		Last Modified: Wed, 15 Apr 2026 21:33:30 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.4.0-dind-alpine3.23`

```console
$ docker pull docker@sha256:a6dd5322747a95cd8e3207bd8d415a8fd20ec34e9c00f06dc019cbd912013489
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

### `docker:29.4.0-dind-alpine3.23` - linux; amd64

```console
$ docker pull docker@sha256:4d2c6e334de4b26d492c0a8cc5438e3dbf1a02eee899fc0d4d39b96202c943a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.5 MB (140522901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:304d326357dcfc523ea9ea01226e742f15d0d548d8eaec0e14c3b39387303000`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:16:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 15 Apr 2026 20:16:25 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 15 Apr 2026 20:16:25 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 15 Apr 2026 20:16:27 GMT
ENV DOCKER_VERSION=29.4.0
# Wed, 15 Apr 2026 20:16:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 15 Apr 2026 20:16:27 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Wed, 15 Apr 2026 20:16:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 15 Apr 2026 20:16:28 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 15 Apr 2026 20:16:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 15 Apr 2026 20:16:29 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 15 Apr 2026 20:16:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:16:29 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Apr 2026 20:16:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 15 Apr 2026 20:16:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:16:30 GMT
CMD ["sh"]
# Wed, 15 Apr 2026 21:19:01 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 15 Apr 2026 21:19:02 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 15 Apr 2026 21:19:02 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 15 Apr 2026 21:19:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 15 Apr 2026 21:19:05 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 15 Apr 2026 21:19:05 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 15 Apr 2026 21:19:05 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:19:05 GMT
VOLUME [/var/lib/docker]
# Wed, 15 Apr 2026 21:19:05 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 15 Apr 2026 21:19:05 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 15 Apr 2026 21:19:05 GMT
CMD []
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00fef3bc4d7adc06c42d060d3a4fad2da6d129c5d2dac575a0a34e5276837acc`  
		Last Modified: Wed, 15 Apr 2026 20:16:37 GMT  
		Size: 8.4 MB (8390330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f8bdd90a189e988440fcec9f3b420d55047950b5f7601ba0e57b351852d7ba`  
		Last Modified: Wed, 15 Apr 2026 20:16:36 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4985eb1bbbfe749a8493542e038307f004a28671974b2a082ae06f9391c4aa64`  
		Last Modified: Wed, 15 Apr 2026 20:16:37 GMT  
		Size: 19.5 MB (19464794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859abcc7688b1a7cc3cc9e144132fc9069de384c58f57dcdc67bb82efa576352`  
		Last Modified: Wed, 15 Apr 2026 20:16:37 GMT  
		Size: 22.5 MB (22539232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c99a167aeca4fe59d6c36fcd7dd693309a219446eca7bcdc04b392e4d69c2c4`  
		Last Modified: Wed, 15 Apr 2026 20:16:38 GMT  
		Size: 11.0 MB (10955103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e81a750c9b2d394bb0113dc9e2ac999fdb73fc198aee986c23671ccc8b782c`  
		Last Modified: Wed, 15 Apr 2026 20:16:38 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ba37c8df4e2fbeeea282fc985c366a9d438cb9ac52b521a1ba48cc214ddd6c`  
		Last Modified: Wed, 15 Apr 2026 20:16:39 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26929be3c972c7f0a15b08c4029aaa790ccc1d494702813df05e37cf6c95ece4`  
		Last Modified: Wed, 15 Apr 2026 20:16:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72409ebb253eee0d0ac41d3def31dd521fd7fbb44646380257fce88e92956e1b`  
		Last Modified: Wed, 15 Apr 2026 21:19:16 GMT  
		Size: 6.9 MB (6941794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61b7bb0bfe4127ecc181695a6617bce6875877794291f6f411f1503400774934`  
		Last Modified: Wed, 15 Apr 2026 21:19:15 GMT  
		Size: 92.4 KB (92386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f322cdda1c007efd5a7874085a0a278df1d8cba0c79c539cecdfd441528c5063`  
		Last Modified: Wed, 15 Apr 2026 21:19:16 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b195c7fa897ae20e300894f9c01ab27baa6d026f2966d14da47768c0504f7e0d`  
		Last Modified: Wed, 15 Apr 2026 21:19:18 GMT  
		Size: 68.3 MB (68266921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d71ba441d54fb7122eab57ffb2e5cc6805c4abe5aa1229a369d61713d35c4a`  
		Last Modified: Wed, 15 Apr 2026 21:19:17 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471eb30b983e8a0f853e3d3be9271df608fd2048cec340fa2eaef5e93dccfdd6`  
		Last Modified: Wed, 15 Apr 2026 21:19:17 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4.0-dind-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:1c8aa5173659195543e7f2199b877ec50c9f568416a96a31cd42b2fcd07923ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36f6b76c4e162e68e3741832b1fa66576d6705a81ed60bdeeded8cbffb74e2ff`

```dockerfile
```

-	Layers:
	-	`sha256:4c3c193ad694d685d8594f91321d9d1fe73498db66cfb3767583e03cba34f0eb`  
		Last Modified: Wed, 15 Apr 2026 21:19:15 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.4.0-dind-alpine3.23` - linux; arm variant v6

```console
$ docker pull docker@sha256:b23cae1ff183bc4e75d88eaf9ba1c6549849f1d134d11fc442d0f885b1f58d4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 MB (132507536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c664d0b218f2b2a9a4e105a5162c0ba967e6162e60df351421a2b174c2b02b2f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:11:18 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 15 Apr 2026 20:11:18 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 15 Apr 2026 20:11:18 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 15 Apr 2026 20:11:22 GMT
ENV DOCKER_VERSION=29.4.0
# Wed, 15 Apr 2026 20:11:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 15 Apr 2026 20:11:22 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Wed, 15 Apr 2026 20:11:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 15 Apr 2026 20:11:25 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 15 Apr 2026 20:11:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 15 Apr 2026 20:11:27 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 15 Apr 2026 20:11:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:11:27 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Apr 2026 20:11:27 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 15 Apr 2026 20:11:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:11:27 GMT
CMD ["sh"]
# Wed, 15 Apr 2026 21:19:39 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 15 Apr 2026 21:19:40 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 15 Apr 2026 21:19:40 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 15 Apr 2026 21:19:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 15 Apr 2026 21:19:44 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 15 Apr 2026 21:19:44 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 15 Apr 2026 21:19:44 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:19:44 GMT
VOLUME [/var/lib/docker]
# Wed, 15 Apr 2026 21:19:44 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 15 Apr 2026 21:19:44 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 15 Apr 2026 21:19:44 GMT
CMD []
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e29b5a067225f28735c3f9c28db7a022b344731761dc5bd14d0b7a283cc13aa1`  
		Last Modified: Wed, 15 Apr 2026 20:11:34 GMT  
		Size: 8.3 MB (8297061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae71f1757016712f17b7c9321ecac9183912e0037f929b5050fa04410093a993`  
		Last Modified: Wed, 15 Apr 2026 20:11:33 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64a558c789f63340dd86a3d8d48163d7ca0b3475c2b5c1d8ca27e0afc43f81a`  
		Last Modified: Wed, 15 Apr 2026 20:11:35 GMT  
		Size: 18.1 MB (18109476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03bc6071f6b066b797f80197a5147fa49e7c18d34820ebbd67e8a05f503815a0`  
		Last Modified: Wed, 15 Apr 2026 20:11:35 GMT  
		Size: 21.2 MB (21151872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84372c97713792c82b059361309092a10362cb4b047854a0b862c3ebeb6f45a7`  
		Last Modified: Wed, 15 Apr 2026 20:11:35 GMT  
		Size: 10.4 MB (10388823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1411d774c190d6fe75a26c80337ed792c1219b393396b9dd4008440601b2e8bb`  
		Last Modified: Wed, 15 Apr 2026 20:11:36 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:213ded2f75d406b851e7f9d90ac09eacb9ecd070136e9e64a5e44a7b62246ab0`  
		Last Modified: Wed, 15 Apr 2026 20:11:36 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9546667a8b53db55a0c88114559b89b5a4c5288c765a0efd17abf18956634f`  
		Last Modified: Wed, 15 Apr 2026 20:11:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db0f2e08cd52770499a4a7b14b1d7035c2bed565f5d1658d36f77ba8cae62ad5`  
		Last Modified: Wed, 15 Apr 2026 21:19:55 GMT  
		Size: 7.3 MB (7278394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810c7f3c3226c75491d45b3028f6aa4e32c04edce7619e9c304e5c7054c6e3e8`  
		Last Modified: Wed, 15 Apr 2026 21:19:55 GMT  
		Size: 91.7 KB (91683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80b9397e0c604f4cffa37ef63fc68b0849fbe399433ee3b1b24e32ea5c1b6138`  
		Last Modified: Wed, 15 Apr 2026 21:19:55 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:578128484de3ef92c76816591ca072998f01b1381725e18fd1c7a4baa20bc9f8`  
		Last Modified: Wed, 15 Apr 2026 21:19:56 GMT  
		Size: 63.6 MB (63610209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2209085b94038497f0af62b68d75961a5b080cb35551dcc8d0eefab6b722484a`  
		Last Modified: Wed, 15 Apr 2026 21:19:56 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b27ed318c8e6661d6fa40585004daf813302e8af45e485fdf0173af3947bc2`  
		Last Modified: Wed, 15 Apr 2026 21:19:56 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4.0-dind-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:a01657f9a7e1e95bc00dd7bf0d40d8f4e73263519d316ff513e77cd827e24f6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48c770ff5e3d911a2d76c733a01cc1a9e96597d1aeb12c3470e57cf12936aa28`

```dockerfile
```

-	Layers:
	-	`sha256:147b649936864607c8d1c5530d9427c37768a5718de420c9941b6f3b6625b9d5`  
		Last Modified: Wed, 15 Apr 2026 21:19:54 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.4.0-dind-alpine3.23` - linux; arm variant v7

```console
$ docker pull docker@sha256:20d1ab4a0712e057c1adc25f5703a97b31a7f387b43adc77bb7308d4397970e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130593641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ca74a271ab95685bc02e667fcb161e01b626e71e3d25886e49bfab8239d7ded`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:16:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 15 Apr 2026 20:16:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 15 Apr 2026 20:16:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 15 Apr 2026 20:16:18 GMT
ENV DOCKER_VERSION=29.4.0
# Wed, 15 Apr 2026 20:16:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 15 Apr 2026 20:16:18 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Wed, 15 Apr 2026 20:16:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 15 Apr 2026 20:16:20 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 15 Apr 2026 20:16:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 15 Apr 2026 20:16:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 15 Apr 2026 20:16:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:16:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Apr 2026 20:16:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 15 Apr 2026 20:16:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:16:22 GMT
CMD ["sh"]
# Wed, 15 Apr 2026 21:27:26 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 15 Apr 2026 21:27:28 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 15 Apr 2026 21:27:28 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 15 Apr 2026 21:27:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 15 Apr 2026 21:27:31 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 15 Apr 2026 21:27:31 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 15 Apr 2026 21:27:31 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:27:31 GMT
VOLUME [/var/lib/docker]
# Wed, 15 Apr 2026 21:27:31 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 15 Apr 2026 21:27:31 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 15 Apr 2026 21:27:31 GMT
CMD []
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88cb38943f0f0a95a9ef76158143c405f36bad50621b2fd56aa2fc4f3615fd5`  
		Last Modified: Wed, 15 Apr 2026 20:16:29 GMT  
		Size: 7.6 MB (7595768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaaca956ad170283b847286ec873bec980d796519baf3f39fe964aded5374f8e`  
		Last Modified: Wed, 15 Apr 2026 20:16:28 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cdf1c13c7d0f067c56c9771266f9895d1041ebf30f39ab27603e18afb0c9081`  
		Last Modified: Wed, 15 Apr 2026 20:16:29 GMT  
		Size: 18.1 MB (18096362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813eda9384408e479910e06a79744324e1dce0b63fd42e5bce661a6e735e2f32`  
		Last Modified: Wed, 15 Apr 2026 20:16:29 GMT  
		Size: 21.1 MB (21129758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f4b664cfcad12fa1a9762a191ac3534cf78c30dd9df6eff79f75e17bd604215`  
		Last Modified: Wed, 15 Apr 2026 20:16:30 GMT  
		Size: 10.4 MB (10371870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f3580f46ae276e11707530d3b18cc55414bcb1f7a672d3cef371193e0e0947`  
		Last Modified: Wed, 15 Apr 2026 20:16:30 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d214a288fe8f0a47169af907737952cefa9e61f078490a75828a439107530b2`  
		Last Modified: Wed, 15 Apr 2026 20:16:31 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf0d872d260394713b2443444bb53d508d83624734c0239dcda7ff1830303db8`  
		Last Modified: Wed, 15 Apr 2026 20:16:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89db5f2f3e615ce6454e5c1c42292805de5a924c4769cb726472a5f992eef448`  
		Last Modified: Wed, 15 Apr 2026 21:27:42 GMT  
		Size: 6.6 MB (6577217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a486198c8f3ba2ab5d5c0c2444157dbdb3a24ef48b6dcbe399e92e72a5e6c28`  
		Last Modified: Wed, 15 Apr 2026 21:27:42 GMT  
		Size: 88.0 KB (88036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba24e0fe682bf1faf33f78d5b19ecad454f21527c9a6c33cfb4c1d694b52779`  
		Last Modified: Wed, 15 Apr 2026 21:27:42 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ca224f3bf33d1172adfccf0c242f89893fde617bd5885ef7545ecd22e41ef4f`  
		Last Modified: Wed, 15 Apr 2026 21:27:44 GMT  
		Size: 63.4 MB (63443351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac3934cb427133bc539854b45e314e2dc44838a979414cf67dd89810b967f06`  
		Last Modified: Wed, 15 Apr 2026 21:27:43 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5e8455627c95fe22aa58fead7cbf2a0934fd4d57d760756577ec0b8c9bf4bc`  
		Last Modified: Wed, 15 Apr 2026 21:27:43 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4.0-dind-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:9376e04ebe10bd90bf0a7a85bddeb4c723ab3c8e9ae5290a6f522143cdbed03d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58ce25b3cedf687af0bcb158bb0a1d2a8523dfeadcddc68360fc3394f815f730`

```dockerfile
```

-	Layers:
	-	`sha256:ecdd6391528d66bfad436f41aef96daa292510a5ddd3f115f031dd1728b3dd36`  
		Last Modified: Wed, 15 Apr 2026 21:27:42 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.4.0-dind-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:553d694bc3ae2a92b67b73072e3923a8d2256e609b568c60d08e4544e8f39ff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.1 MB (130126872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5c1c78f7262d1e00eef13317919dc25b6d65c96115e46f851ab09818f2ddf0b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:13:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 15 Apr 2026 20:13:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 15 Apr 2026 20:13:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 15 Apr 2026 20:14:02 GMT
ENV DOCKER_VERSION=29.4.0
# Wed, 15 Apr 2026 20:14:02 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 15 Apr 2026 20:14:02 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Wed, 15 Apr 2026 20:14:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 15 Apr 2026 20:14:03 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 15 Apr 2026 20:14:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 15 Apr 2026 20:14:04 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 15 Apr 2026 20:14:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:14:04 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Apr 2026 20:14:04 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 15 Apr 2026 20:14:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:14:04 GMT
CMD ["sh"]
# Wed, 15 Apr 2026 21:33:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 15 Apr 2026 21:33:18 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 15 Apr 2026 21:33:18 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 15 Apr 2026 21:33:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 15 Apr 2026 21:33:21 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 15 Apr 2026 21:33:21 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 15 Apr 2026 21:33:21 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:33:21 GMT
VOLUME [/var/lib/docker]
# Wed, 15 Apr 2026 21:33:21 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 15 Apr 2026 21:33:21 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 15 Apr 2026 21:33:21 GMT
CMD []
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1f08e8ea565813fe5c533f3bf89a6fcb79b8ef2eb46e2872f132234aa070cf`  
		Last Modified: Wed, 15 Apr 2026 20:14:10 GMT  
		Size: 8.5 MB (8450092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ff0f79f131dfea84e2ad6ee3723888525425bfc628525e86c3cc1b288bace3`  
		Last Modified: Wed, 15 Apr 2026 20:14:10 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35bf88d1a58dc1d9ced6e216552eef44b2392e515454985dcd3f25372d12693`  
		Last Modified: Wed, 15 Apr 2026 20:14:11 GMT  
		Size: 17.9 MB (17921079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0aa9505e9a0f5469b8905ecd253d1fd12569434350a1c94898126c02a4a9c57`  
		Last Modified: Wed, 15 Apr 2026 20:14:11 GMT  
		Size: 20.5 MB (20453111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ff9179479c44e683ee3838185f58e7d707974096437fdccedcb7b1f316aa35`  
		Last Modified: Wed, 15 Apr 2026 20:14:11 GMT  
		Size: 10.0 MB (9982600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0771ed595b2bb7d830d904c0ed7f259d39bb70d0da784d731a39f7a1ceeacb04`  
		Last Modified: Wed, 15 Apr 2026 20:14:12 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627cec3b548e33f50bcd1682915056d5dfd8e5b28476d6c4842c0eb790b1f954`  
		Last Modified: Wed, 15 Apr 2026 20:14:12 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c67b1b44bc81549ba5caf988b00dabcb0c2ca6cee73ef7d756e26b08b1028e`  
		Last Modified: Wed, 15 Apr 2026 20:14:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c169b754493e049763aeab1727fe430cecafcd9032c4389b3053958aebc360c9`  
		Last Modified: Wed, 15 Apr 2026 21:33:31 GMT  
		Size: 7.2 MB (7219816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbba1f41e162f643c431dbb55a4cfb94284235c55c0c226f2f85fdc2797d7d3`  
		Last Modified: Wed, 15 Apr 2026 21:33:30 GMT  
		Size: 101.2 KB (101171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc3e20cde46cbbd2b898524e10c8ed94082175c8c21daf98b34e7a6006aafee`  
		Last Modified: Wed, 15 Apr 2026 21:33:30 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ae4baf5361489e96a43c6d29d47fdd4eb63dd088b10e8bf91df746925678ea`  
		Last Modified: Wed, 15 Apr 2026 21:33:32 GMT  
		Size: 61.8 MB (61790985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7fa8aac1af219d886ca4026da0a5a043fde1dae9d3e8534dd78f23360b8763`  
		Last Modified: Wed, 15 Apr 2026 21:33:32 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f667dde4f795a12a4a9d7129f07e71678ffec2ae9a15d680f09fd672a64ab154`  
		Last Modified: Wed, 15 Apr 2026 21:33:32 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4.0-dind-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:71c18f631e3205680e2fcd0ea55f0f373c7fb19de8336794fe07f3d4793786b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48d9407668f8511b7b181ffcfea6ce22705df56aaf20a9dd84a0930f31f6ecf7`

```dockerfile
```

-	Layers:
	-	`sha256:623b2bc83b8d25632b5e152b95570ef2a7af85709fedfa2ae3ed9d312b61c77c`  
		Last Modified: Wed, 15 Apr 2026 21:33:30 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.4.0-dind-rootless`

```console
$ docker pull docker@sha256:76944d96ec8f4d759b5c8d9bf5f0787813f278e46aa078ae65338216739cb0fd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:29.4.0-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:e89e2c0f44ba58a65f9f9dc8b04aea6ee7f31c76a7ff8048465f2576746fadb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.5 MB (161524750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ceb46e5e927ba19a62569af7c8eb32cbcef000cd7379578db1e3a3e4fe943aa`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:16:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 15 Apr 2026 20:16:25 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 15 Apr 2026 20:16:25 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 15 Apr 2026 20:16:27 GMT
ENV DOCKER_VERSION=29.4.0
# Wed, 15 Apr 2026 20:16:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 15 Apr 2026 20:16:27 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Wed, 15 Apr 2026 20:16:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 15 Apr 2026 20:16:28 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 15 Apr 2026 20:16:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 15 Apr 2026 20:16:29 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 15 Apr 2026 20:16:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:16:29 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Apr 2026 20:16:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 15 Apr 2026 20:16:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:16:30 GMT
CMD ["sh"]
# Wed, 15 Apr 2026 21:19:01 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 15 Apr 2026 21:19:02 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 15 Apr 2026 21:19:02 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 15 Apr 2026 21:19:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 15 Apr 2026 21:19:05 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 15 Apr 2026 21:19:05 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 15 Apr 2026 21:19:05 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:19:05 GMT
VOLUME [/var/lib/docker]
# Wed, 15 Apr 2026 21:19:05 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 15 Apr 2026 21:19:05 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 15 Apr 2026 21:19:05 GMT
CMD []
# Wed, 15 Apr 2026 22:12:18 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Wed, 15 Apr 2026 22:12:18 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 15 Apr 2026 22:12:18 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 15 Apr 2026 22:12:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 15 Apr 2026 22:12:19 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 15 Apr 2026 22:12:19 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 15 Apr 2026 22:12:19 GMT
USER rootless
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00fef3bc4d7adc06c42d060d3a4fad2da6d129c5d2dac575a0a34e5276837acc`  
		Last Modified: Wed, 15 Apr 2026 20:16:37 GMT  
		Size: 8.4 MB (8390330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f8bdd90a189e988440fcec9f3b420d55047950b5f7601ba0e57b351852d7ba`  
		Last Modified: Wed, 15 Apr 2026 20:16:36 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4985eb1bbbfe749a8493542e038307f004a28671974b2a082ae06f9391c4aa64`  
		Last Modified: Wed, 15 Apr 2026 20:16:37 GMT  
		Size: 19.5 MB (19464794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859abcc7688b1a7cc3cc9e144132fc9069de384c58f57dcdc67bb82efa576352`  
		Last Modified: Wed, 15 Apr 2026 20:16:37 GMT  
		Size: 22.5 MB (22539232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c99a167aeca4fe59d6c36fcd7dd693309a219446eca7bcdc04b392e4d69c2c4`  
		Last Modified: Wed, 15 Apr 2026 20:16:38 GMT  
		Size: 11.0 MB (10955103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e81a750c9b2d394bb0113dc9e2ac999fdb73fc198aee986c23671ccc8b782c`  
		Last Modified: Wed, 15 Apr 2026 20:16:38 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ba37c8df4e2fbeeea282fc985c366a9d438cb9ac52b521a1ba48cc214ddd6c`  
		Last Modified: Wed, 15 Apr 2026 20:16:39 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26929be3c972c7f0a15b08c4029aaa790ccc1d494702813df05e37cf6c95ece4`  
		Last Modified: Wed, 15 Apr 2026 20:16:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72409ebb253eee0d0ac41d3def31dd521fd7fbb44646380257fce88e92956e1b`  
		Last Modified: Wed, 15 Apr 2026 21:19:16 GMT  
		Size: 6.9 MB (6941794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61b7bb0bfe4127ecc181695a6617bce6875877794291f6f411f1503400774934`  
		Last Modified: Wed, 15 Apr 2026 21:19:15 GMT  
		Size: 92.4 KB (92386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f322cdda1c007efd5a7874085a0a278df1d8cba0c79c539cecdfd441528c5063`  
		Last Modified: Wed, 15 Apr 2026 21:19:16 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b195c7fa897ae20e300894f9c01ab27baa6d026f2966d14da47768c0504f7e0d`  
		Last Modified: Wed, 15 Apr 2026 21:19:18 GMT  
		Size: 68.3 MB (68266921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d71ba441d54fb7122eab57ffb2e5cc6805c4abe5aa1229a369d61713d35c4a`  
		Last Modified: Wed, 15 Apr 2026 21:19:17 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471eb30b983e8a0f853e3d3be9271df608fd2048cec340fa2eaef5e93dccfdd6`  
		Last Modified: Wed, 15 Apr 2026 21:19:17 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d603a61ab9bf085d4c5ed544ebdc6930cedac60c151b8c3d844ec4a5e1907a3f`  
		Last Modified: Wed, 15 Apr 2026 22:12:32 GMT  
		Size: 3.4 MB (3420096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f6cf84eabf10318aff4902301c0a7eb0d5e3a1fbedc2457d5a03e48ec176798`  
		Last Modified: Wed, 15 Apr 2026 22:12:26 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c7e42a9e418d966d88e75d7076fb61e32f5f036331ad87079c2af72fee32a29`  
		Last Modified: Wed, 15 Apr 2026 22:12:28 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:707634342cc50aaa8f17842865d9fe9c4d140289067e551027f32d44235c5e64`  
		Last Modified: Wed, 15 Apr 2026 22:12:36 GMT  
		Size: 17.6 MB (17580415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5efa74639426aef15709b77e6fe19278595bf047f2e03f5a8449cc234b9df8c2`  
		Last Modified: Wed, 15 Apr 2026 22:12:32 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4.0-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:16263b4914888c6b7270d1a2b9da8845365aacaafbf2ae86d9c3e093373eb29c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9072388f94ef26c4fd86a7769ed365d8a261d4df812abb3ef6950a2400d130af`

```dockerfile
```

-	Layers:
	-	`sha256:f9339be88cc342b92f34d4da76922c287e26b230e4ebab8ba0b5ce74a00df08b`  
		Last Modified: Wed, 15 Apr 2026 22:12:24 GMT  
		Size: 30.6 KB (30589 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.4.0-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:b4fad2141f6e11611acfc843f2434ba2a41e6915639963b943fa2ba4b51e87d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.4 MB (151405559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95e9af8ffe8cf19d9949f80c4fe0f01db4518273f5f1e3f6470799d230530909`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:13:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 15 Apr 2026 20:13:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 15 Apr 2026 20:13:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 15 Apr 2026 20:14:02 GMT
ENV DOCKER_VERSION=29.4.0
# Wed, 15 Apr 2026 20:14:02 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 15 Apr 2026 20:14:02 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Wed, 15 Apr 2026 20:14:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 15 Apr 2026 20:14:03 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 15 Apr 2026 20:14:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 15 Apr 2026 20:14:04 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 15 Apr 2026 20:14:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:14:04 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Apr 2026 20:14:04 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 15 Apr 2026 20:14:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:14:04 GMT
CMD ["sh"]
# Wed, 15 Apr 2026 21:33:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 15 Apr 2026 21:33:18 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 15 Apr 2026 21:33:18 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 15 Apr 2026 21:33:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 15 Apr 2026 21:33:21 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 15 Apr 2026 21:33:21 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 15 Apr 2026 21:33:21 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:33:21 GMT
VOLUME [/var/lib/docker]
# Wed, 15 Apr 2026 21:33:21 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 15 Apr 2026 21:33:21 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 15 Apr 2026 21:33:21 GMT
CMD []
# Wed, 15 Apr 2026 22:24:13 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Wed, 15 Apr 2026 22:24:13 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 15 Apr 2026 22:24:13 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 15 Apr 2026 22:24:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 15 Apr 2026 22:24:14 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 15 Apr 2026 22:24:14 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 15 Apr 2026 22:24:14 GMT
USER rootless
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1f08e8ea565813fe5c533f3bf89a6fcb79b8ef2eb46e2872f132234aa070cf`  
		Last Modified: Wed, 15 Apr 2026 20:14:10 GMT  
		Size: 8.5 MB (8450092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ff0f79f131dfea84e2ad6ee3723888525425bfc628525e86c3cc1b288bace3`  
		Last Modified: Wed, 15 Apr 2026 20:14:10 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35bf88d1a58dc1d9ced6e216552eef44b2392e515454985dcd3f25372d12693`  
		Last Modified: Wed, 15 Apr 2026 20:14:11 GMT  
		Size: 17.9 MB (17921079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0aa9505e9a0f5469b8905ecd253d1fd12569434350a1c94898126c02a4a9c57`  
		Last Modified: Wed, 15 Apr 2026 20:14:11 GMT  
		Size: 20.5 MB (20453111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ff9179479c44e683ee3838185f58e7d707974096437fdccedcb7b1f316aa35`  
		Last Modified: Wed, 15 Apr 2026 20:14:11 GMT  
		Size: 10.0 MB (9982600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0771ed595b2bb7d830d904c0ed7f259d39bb70d0da784d731a39f7a1ceeacb04`  
		Last Modified: Wed, 15 Apr 2026 20:14:12 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627cec3b548e33f50bcd1682915056d5dfd8e5b28476d6c4842c0eb790b1f954`  
		Last Modified: Wed, 15 Apr 2026 20:14:12 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c67b1b44bc81549ba5caf988b00dabcb0c2ca6cee73ef7d756e26b08b1028e`  
		Last Modified: Wed, 15 Apr 2026 20:14:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c169b754493e049763aeab1727fe430cecafcd9032c4389b3053958aebc360c9`  
		Last Modified: Wed, 15 Apr 2026 21:33:31 GMT  
		Size: 7.2 MB (7219816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbba1f41e162f643c431dbb55a4cfb94284235c55c0c226f2f85fdc2797d7d3`  
		Last Modified: Wed, 15 Apr 2026 21:33:30 GMT  
		Size: 101.2 KB (101171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc3e20cde46cbbd2b898524e10c8ed94082175c8c21daf98b34e7a6006aafee`  
		Last Modified: Wed, 15 Apr 2026 21:33:30 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ae4baf5361489e96a43c6d29d47fdd4eb63dd088b10e8bf91df746925678ea`  
		Last Modified: Wed, 15 Apr 2026 21:33:32 GMT  
		Size: 61.8 MB (61790985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7fa8aac1af219d886ca4026da0a5a043fde1dae9d3e8534dd78f23360b8763`  
		Last Modified: Wed, 15 Apr 2026 21:33:32 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f667dde4f795a12a4a9d7129f07e71678ffec2ae9a15d680f09fd672a64ab154`  
		Last Modified: Wed, 15 Apr 2026 21:33:32 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9012b0d6da5801eab238bb387dbb36b8d6a39d5aa7039815d1c9e2a24833a04`  
		Last Modified: Wed, 15 Apr 2026 22:24:20 GMT  
		Size: 3.4 MB (3394534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:960aa9d16806e38df09387de191ea1c727cc5093bc76be222ed5d2a7ca369379`  
		Last Modified: Wed, 15 Apr 2026 22:24:20 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78adb818d73519733cf9dc2e2f2fdf7f7b19abf1d6a5f6050937e7df4fca78d3`  
		Last Modified: Wed, 15 Apr 2026 22:24:20 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f755f683e7f98d710321e727c122d4fd09ba183d051ff46907c74d640b25fcc8`  
		Last Modified: Wed, 15 Apr 2026 22:24:21 GMT  
		Size: 17.9 MB (17882814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d3922b05d8ff64a19ec81b180d6950d39f6867f3dee697b2c3495cb2625bcc`  
		Last Modified: Wed, 15 Apr 2026 22:24:21 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4.0-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:bb4750590667d42b5f476e8c84bbfb8c1157d5e39d0a4d73884792417165644b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6910dd353dfd57bed56f7465cd51c75e8b8d0c0213fe745a77273d1d7a3f43c4`

```dockerfile
```

-	Layers:
	-	`sha256:4bfbb83e76361cdb9defcea46dc5c48423a4c288e606987803e7f5ee3edc2883`  
		Last Modified: Wed, 15 Apr 2026 22:24:20 GMT  
		Size: 30.8 KB (30752 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.4.0-windowsservercore`

```console
$ docker pull docker@sha256:d74502081e87e340ae439759f8ec2ea8904f7c6d482c2e01ef2d63e4eab78fce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32690; amd64
	-	windows version 10.0.20348.5020; amd64

### `docker:29.4.0-windowsservercore` - windows version 10.0.26100.32690; amd64

```console
$ docker pull docker@sha256:d46ee739eeb7f2f3919de6950a0c17a20bb1d22971380a4bb658f91004b6e533
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2185608492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:451cb635e20acafc0c39412eaf4ae9baa78105ff334cffab02ee607ff7e6d625`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Mon, 13 Apr 2026 07:00:46 GMT
RUN Install update 10.0.26100.32690
# Tue, 14 Apr 2026 21:01:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Apr 2026 21:02:06 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Apr 2026 21:02:07 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 14 Apr 2026 21:02:08 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.4.0.zip
# Tue, 14 Apr 2026 21:02:20 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 14 Apr 2026 21:02:20 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 14 Apr 2026 21:02:21 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.windows-amd64.exe
# Tue, 14 Apr 2026 21:02:21 GMT
ENV DOCKER_BUILDX_SHA256=832ddf42373203ee3836a7cb3b16fe5080231491e7edb32019ac0f6fe03b99ed
# Tue, 14 Apr 2026 21:02:35 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 14 Apr 2026 21:02:35 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 14 Apr 2026 21:02:36 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-windows-x86_64.exe
# Tue, 14 Apr 2026 21:02:37 GMT
ENV DOCKER_COMPOSE_SHA256=f7ad2f6965c88153e4902019ec86e95414f0025cba0b6440f328f935a1f8b12b
# Tue, 14 Apr 2026 21:02:43 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3642e4b8bb65ad3768f9f74a0dc48bb2e3294779b5d51573a234bfbe4f65324e`  
		Last Modified: Tue, 14 Apr 2026 18:48:19 GMT  
		Size: 606.9 MB (606926634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68ac02bb5872fbad22e76d99d54ab9b35a1e35759bbddff4f282081ba61100d5`  
		Last Modified: Tue, 14 Apr 2026 21:02:53 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774f3049f1ff5e124ea4f250ee1167ecf42896b3e9bcd067e2f4926ab7a0602d`  
		Last Modified: Tue, 14 Apr 2026 21:02:52 GMT  
		Size: 369.0 KB (368971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae8c2209515b42fd04e40e13a7bca32c3f1f16411393fc4cee562ca8f641bb7`  
		Last Modified: Tue, 14 Apr 2026 21:02:52 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3790546541b36e26bd73f9dfdaf940ebe9fe8013ff0a1cf891fba5e7701b36f`  
		Last Modified: Tue, 14 Apr 2026 21:02:51 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:445fc7e4e770e7d61fdf3492872b7e8bca998a26fffc4515e6344d6952d41f0f`  
		Last Modified: Tue, 14 Apr 2026 21:02:53 GMT  
		Size: 20.2 MB (20155911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b10e1a8a2bc350119623c441e4e0d952f69a7c50a192f764cb4e772b2359ea46`  
		Last Modified: Tue, 14 Apr 2026 21:02:50 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e015ae5429fcbb9151f7c03f83907b5d7d7e627e93ac5666dd54c102cf6f9909`  
		Last Modified: Tue, 14 Apr 2026 21:02:50 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ccf5f62308e0033a83afd116f4287e8951801b466ac66e960370bbd100b0c2b`  
		Last Modified: Tue, 14 Apr 2026 21:02:50 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:308fbcfb831872272d007db361ab5130df2705896b45ad22706bc3ed69a4208b`  
		Last Modified: Tue, 14 Apr 2026 21:02:52 GMT  
		Size: 23.4 MB (23435945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b688d291c4ee097cfa7d6bd989a5730f385d7ed44f7e307e89f8243f044db00a`  
		Last Modified: Tue, 14 Apr 2026 21:02:48 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:391e7d1ca3eae4c8c6acd6553f00297119056613a326ddae9eecb91f055806f4`  
		Last Modified: Tue, 14 Apr 2026 21:02:48 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebbf7aced575c80864697740f99f4f025250da7e7180003679632024cb1987f3`  
		Last Modified: Tue, 14 Apr 2026 21:02:48 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91a6dca9753cc712a25b48c9dbe9e9556c8e7bedfc0f97baf1d62b4cc5503798`  
		Last Modified: Tue, 14 Apr 2026 21:02:50 GMT  
		Size: 11.6 MB (11649820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:29.4.0-windowsservercore` - windows version 10.0.20348.5020; amd64

```console
$ docker pull docker@sha256:dfeb15b1635155bf333f2033fd733a796d52ede5fa96f898b11e57c12e2412a0
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2125867669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17085df04e58942536df91898016031a94b7bdce5841470b1904db146ee78bca`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Tue, 14 Apr 2026 20:56:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Apr 2026 20:56:45 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Apr 2026 20:56:47 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 14 Apr 2026 20:56:48 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.4.0.zip
# Tue, 14 Apr 2026 20:57:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 14 Apr 2026 20:57:06 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 14 Apr 2026 20:57:07 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.windows-amd64.exe
# Tue, 14 Apr 2026 20:57:08 GMT
ENV DOCKER_BUILDX_SHA256=832ddf42373203ee3836a7cb3b16fe5080231491e7edb32019ac0f6fe03b99ed
# Tue, 14 Apr 2026 20:57:26 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 14 Apr 2026 20:57:27 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 14 Apr 2026 20:57:27 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-windows-x86_64.exe
# Tue, 14 Apr 2026 20:57:28 GMT
ENV DOCKER_COMPOSE_SHA256=f7ad2f6965c88153e4902019ec86e95414f0025cba0b6440f328f935a1f8b12b
# Tue, 14 Apr 2026 20:57:41 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7111ae68f8961455d230dc12d44c2193d29b7c981e35417323613a0c1aa06384`  
		Last Modified: Tue, 14 Apr 2026 17:31:38 GMT  
		Size: 581.2 MB (581192160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4911c7412282b7f1d93fad64ba92d82b42d1ac47c62c4ff886b516f02ea28a55`  
		Last Modified: Tue, 14 Apr 2026 20:57:50 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:151b1d340c8ca7ccd1a0024ff46837779a87b23f90be4512b66ca317e849176b`  
		Last Modified: Tue, 14 Apr 2026 20:57:49 GMT  
		Size: 468.6 KB (468589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c05f9fed2a2861e1aad93076abf9515f202306cf4c6e381ac7b874a9c1d1196`  
		Last Modified: Tue, 14 Apr 2026 20:57:48 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c7405e2df63bc9fec89f85fb677309b86bf973025d8f6b08da62e988f2a629`  
		Last Modified: Tue, 14 Apr 2026 20:57:48 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7f5562b59f5d6e8946261211a66a4f3d8e26a59a704ca4ac6c6405a3ec5f055`  
		Last Modified: Tue, 14 Apr 2026 20:57:50 GMT  
		Size: 20.1 MB (20130256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6f3b1f33de25d313624bac12844dba1d78714061572c4a74d1fe93ad71ce9ad`  
		Last Modified: Tue, 14 Apr 2026 20:57:46 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b55352e1cad29fb0adf25f61e251a05aa1b8ddefb796d15d4793e871bfbaad`  
		Last Modified: Tue, 14 Apr 2026 20:57:47 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a54c516e756ba1351d4ab57988ca90f91af80ca4cce2b27e45eb8dd2ab1ac579`  
		Last Modified: Tue, 14 Apr 2026 20:57:46 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:935fbf8b04da4242e47da7bfee8df2b984a65ed241ffa13f675e09c528cabf8c`  
		Last Modified: Tue, 14 Apr 2026 20:57:54 GMT  
		Size: 23.4 MB (23419466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c62827bb4e356ec246f0a9426681e101860c87ca41a8081887faa7a911a04b19`  
		Last Modified: Tue, 14 Apr 2026 20:57:45 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:830e8d77d7ec0a09f8111f5d4fbe1b1bc385938ec59812da38a864323c7e4963`  
		Last Modified: Tue, 14 Apr 2026 20:57:45 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2405085b41ebd2fbc5a8f4683c3debadbd731eb6e54352fab4de5f2f74bc187d`  
		Last Modified: Tue, 14 Apr 2026 20:57:45 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5d8306d6e8e4e9eb43d89651b670cda922a16548c151c2bdbb51db4656787e6`  
		Last Modified: Tue, 14 Apr 2026 20:57:47 GMT  
		Size: 11.6 MB (11626371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.4.0-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:bba4a40903cac7bbfad1686d3aef377f0f7294e2311b9da2e962d1cf4526c500
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `docker:29.4.0-windowsservercore-ltsc2022` - windows version 10.0.20348.5020; amd64

```console
$ docker pull docker@sha256:dfeb15b1635155bf333f2033fd733a796d52ede5fa96f898b11e57c12e2412a0
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2125867669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17085df04e58942536df91898016031a94b7bdce5841470b1904db146ee78bca`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Tue, 14 Apr 2026 20:56:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Apr 2026 20:56:45 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Apr 2026 20:56:47 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 14 Apr 2026 20:56:48 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.4.0.zip
# Tue, 14 Apr 2026 20:57:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 14 Apr 2026 20:57:06 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 14 Apr 2026 20:57:07 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.windows-amd64.exe
# Tue, 14 Apr 2026 20:57:08 GMT
ENV DOCKER_BUILDX_SHA256=832ddf42373203ee3836a7cb3b16fe5080231491e7edb32019ac0f6fe03b99ed
# Tue, 14 Apr 2026 20:57:26 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 14 Apr 2026 20:57:27 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 14 Apr 2026 20:57:27 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-windows-x86_64.exe
# Tue, 14 Apr 2026 20:57:28 GMT
ENV DOCKER_COMPOSE_SHA256=f7ad2f6965c88153e4902019ec86e95414f0025cba0b6440f328f935a1f8b12b
# Tue, 14 Apr 2026 20:57:41 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7111ae68f8961455d230dc12d44c2193d29b7c981e35417323613a0c1aa06384`  
		Last Modified: Tue, 14 Apr 2026 17:31:38 GMT  
		Size: 581.2 MB (581192160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4911c7412282b7f1d93fad64ba92d82b42d1ac47c62c4ff886b516f02ea28a55`  
		Last Modified: Tue, 14 Apr 2026 20:57:50 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:151b1d340c8ca7ccd1a0024ff46837779a87b23f90be4512b66ca317e849176b`  
		Last Modified: Tue, 14 Apr 2026 20:57:49 GMT  
		Size: 468.6 KB (468589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c05f9fed2a2861e1aad93076abf9515f202306cf4c6e381ac7b874a9c1d1196`  
		Last Modified: Tue, 14 Apr 2026 20:57:48 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c7405e2df63bc9fec89f85fb677309b86bf973025d8f6b08da62e988f2a629`  
		Last Modified: Tue, 14 Apr 2026 20:57:48 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7f5562b59f5d6e8946261211a66a4f3d8e26a59a704ca4ac6c6405a3ec5f055`  
		Last Modified: Tue, 14 Apr 2026 20:57:50 GMT  
		Size: 20.1 MB (20130256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6f3b1f33de25d313624bac12844dba1d78714061572c4a74d1fe93ad71ce9ad`  
		Last Modified: Tue, 14 Apr 2026 20:57:46 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b55352e1cad29fb0adf25f61e251a05aa1b8ddefb796d15d4793e871bfbaad`  
		Last Modified: Tue, 14 Apr 2026 20:57:47 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a54c516e756ba1351d4ab57988ca90f91af80ca4cce2b27e45eb8dd2ab1ac579`  
		Last Modified: Tue, 14 Apr 2026 20:57:46 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:935fbf8b04da4242e47da7bfee8df2b984a65ed241ffa13f675e09c528cabf8c`  
		Last Modified: Tue, 14 Apr 2026 20:57:54 GMT  
		Size: 23.4 MB (23419466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c62827bb4e356ec246f0a9426681e101860c87ca41a8081887faa7a911a04b19`  
		Last Modified: Tue, 14 Apr 2026 20:57:45 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:830e8d77d7ec0a09f8111f5d4fbe1b1bc385938ec59812da38a864323c7e4963`  
		Last Modified: Tue, 14 Apr 2026 20:57:45 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2405085b41ebd2fbc5a8f4683c3debadbd731eb6e54352fab4de5f2f74bc187d`  
		Last Modified: Tue, 14 Apr 2026 20:57:45 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5d8306d6e8e4e9eb43d89651b670cda922a16548c151c2bdbb51db4656787e6`  
		Last Modified: Tue, 14 Apr 2026 20:57:47 GMT  
		Size: 11.6 MB (11626371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.4.0-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:7453a45c03a9501b7dfb80e7846d848c74853c4eed947a7ea01ce577f840a92e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32690; amd64

### `docker:29.4.0-windowsservercore-ltsc2025` - windows version 10.0.26100.32690; amd64

```console
$ docker pull docker@sha256:d46ee739eeb7f2f3919de6950a0c17a20bb1d22971380a4bb658f91004b6e533
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2185608492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:451cb635e20acafc0c39412eaf4ae9baa78105ff334cffab02ee607ff7e6d625`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Mon, 13 Apr 2026 07:00:46 GMT
RUN Install update 10.0.26100.32690
# Tue, 14 Apr 2026 21:01:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Apr 2026 21:02:06 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Apr 2026 21:02:07 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 14 Apr 2026 21:02:08 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.4.0.zip
# Tue, 14 Apr 2026 21:02:20 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 14 Apr 2026 21:02:20 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 14 Apr 2026 21:02:21 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.windows-amd64.exe
# Tue, 14 Apr 2026 21:02:21 GMT
ENV DOCKER_BUILDX_SHA256=832ddf42373203ee3836a7cb3b16fe5080231491e7edb32019ac0f6fe03b99ed
# Tue, 14 Apr 2026 21:02:35 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 14 Apr 2026 21:02:35 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 14 Apr 2026 21:02:36 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-windows-x86_64.exe
# Tue, 14 Apr 2026 21:02:37 GMT
ENV DOCKER_COMPOSE_SHA256=f7ad2f6965c88153e4902019ec86e95414f0025cba0b6440f328f935a1f8b12b
# Tue, 14 Apr 2026 21:02:43 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3642e4b8bb65ad3768f9f74a0dc48bb2e3294779b5d51573a234bfbe4f65324e`  
		Last Modified: Tue, 14 Apr 2026 18:48:19 GMT  
		Size: 606.9 MB (606926634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68ac02bb5872fbad22e76d99d54ab9b35a1e35759bbddff4f282081ba61100d5`  
		Last Modified: Tue, 14 Apr 2026 21:02:53 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774f3049f1ff5e124ea4f250ee1167ecf42896b3e9bcd067e2f4926ab7a0602d`  
		Last Modified: Tue, 14 Apr 2026 21:02:52 GMT  
		Size: 369.0 KB (368971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae8c2209515b42fd04e40e13a7bca32c3f1f16411393fc4cee562ca8f641bb7`  
		Last Modified: Tue, 14 Apr 2026 21:02:52 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3790546541b36e26bd73f9dfdaf940ebe9fe8013ff0a1cf891fba5e7701b36f`  
		Last Modified: Tue, 14 Apr 2026 21:02:51 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:445fc7e4e770e7d61fdf3492872b7e8bca998a26fffc4515e6344d6952d41f0f`  
		Last Modified: Tue, 14 Apr 2026 21:02:53 GMT  
		Size: 20.2 MB (20155911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b10e1a8a2bc350119623c441e4e0d952f69a7c50a192f764cb4e772b2359ea46`  
		Last Modified: Tue, 14 Apr 2026 21:02:50 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e015ae5429fcbb9151f7c03f83907b5d7d7e627e93ac5666dd54c102cf6f9909`  
		Last Modified: Tue, 14 Apr 2026 21:02:50 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ccf5f62308e0033a83afd116f4287e8951801b466ac66e960370bbd100b0c2b`  
		Last Modified: Tue, 14 Apr 2026 21:02:50 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:308fbcfb831872272d007db361ab5130df2705896b45ad22706bc3ed69a4208b`  
		Last Modified: Tue, 14 Apr 2026 21:02:52 GMT  
		Size: 23.4 MB (23435945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b688d291c4ee097cfa7d6bd989a5730f385d7ed44f7e307e89f8243f044db00a`  
		Last Modified: Tue, 14 Apr 2026 21:02:48 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:391e7d1ca3eae4c8c6acd6553f00297119056613a326ddae9eecb91f055806f4`  
		Last Modified: Tue, 14 Apr 2026 21:02:48 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebbf7aced575c80864697740f99f4f025250da7e7180003679632024cb1987f3`  
		Last Modified: Tue, 14 Apr 2026 21:02:48 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91a6dca9753cc712a25b48c9dbe9e9556c8e7bedfc0f97baf1d62b4cc5503798`  
		Last Modified: Tue, 14 Apr 2026 21:02:50 GMT  
		Size: 11.6 MB (11649820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:cli`

```console
$ docker pull docker@sha256:2efe7c8e806b35050def6ba1ba0ddad67b521a0a6d37f4910b3d88f11b495d03
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
$ docker pull docker@sha256:bb21349a52c00b206ad8b5c03fa52023c741c4cf11f269d40d40b9ebaac73d96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65215798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b7281830dcb31636378f562663cd54df1ce82f631d1cd037968aae8c1034bc2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:16:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 15 Apr 2026 20:16:25 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 15 Apr 2026 20:16:25 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 15 Apr 2026 20:16:27 GMT
ENV DOCKER_VERSION=29.4.0
# Wed, 15 Apr 2026 20:16:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 15 Apr 2026 20:16:27 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Wed, 15 Apr 2026 20:16:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 15 Apr 2026 20:16:28 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 15 Apr 2026 20:16:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 15 Apr 2026 20:16:29 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 15 Apr 2026 20:16:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:16:29 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Apr 2026 20:16:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 15 Apr 2026 20:16:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:16:30 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00fef3bc4d7adc06c42d060d3a4fad2da6d129c5d2dac575a0a34e5276837acc`  
		Last Modified: Wed, 15 Apr 2026 20:16:37 GMT  
		Size: 8.4 MB (8390330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f8bdd90a189e988440fcec9f3b420d55047950b5f7601ba0e57b351852d7ba`  
		Last Modified: Wed, 15 Apr 2026 20:16:36 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4985eb1bbbfe749a8493542e038307f004a28671974b2a082ae06f9391c4aa64`  
		Last Modified: Wed, 15 Apr 2026 20:16:37 GMT  
		Size: 19.5 MB (19464794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859abcc7688b1a7cc3cc9e144132fc9069de384c58f57dcdc67bb82efa576352`  
		Last Modified: Wed, 15 Apr 2026 20:16:37 GMT  
		Size: 22.5 MB (22539232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c99a167aeca4fe59d6c36fcd7dd693309a219446eca7bcdc04b392e4d69c2c4`  
		Last Modified: Wed, 15 Apr 2026 20:16:38 GMT  
		Size: 11.0 MB (10955103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e81a750c9b2d394bb0113dc9e2ac999fdb73fc198aee986c23671ccc8b782c`  
		Last Modified: Wed, 15 Apr 2026 20:16:38 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ba37c8df4e2fbeeea282fc985c366a9d438cb9ac52b521a1ba48cc214ddd6c`  
		Last Modified: Wed, 15 Apr 2026 20:16:39 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26929be3c972c7f0a15b08c4029aaa790ccc1d494702813df05e37cf6c95ece4`  
		Last Modified: Wed, 15 Apr 2026 20:16:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:5c727440eaffe25d1a2f89a448a8aeef8118f192ce752f5f55b0e7dcf3bee15d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d4150275339c1686c0b7eab0e338d57f441efecf63ffadf5cfa59dfe3a3e9a0`

```dockerfile
```

-	Layers:
	-	`sha256:083400d83f577b87f30bc974ae857508bdaeb3c56dafaa2a3985dbc6a2be5c32`  
		Last Modified: Wed, 15 Apr 2026 20:16:36 GMT  
		Size: 38.1 KB (38056 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:b0448a7e451eb2df18d117260c232b9064f3b11bd751ac2e603c18bef0289a37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61521248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ab4c337f9a3ba981939d8eb77b75c53cbc28458c647ccce32e93d0f7a99ee4e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:11:18 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 15 Apr 2026 20:11:18 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 15 Apr 2026 20:11:18 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 15 Apr 2026 20:11:22 GMT
ENV DOCKER_VERSION=29.4.0
# Wed, 15 Apr 2026 20:11:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 15 Apr 2026 20:11:22 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Wed, 15 Apr 2026 20:11:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 15 Apr 2026 20:11:25 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 15 Apr 2026 20:11:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 15 Apr 2026 20:11:27 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 15 Apr 2026 20:11:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:11:27 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Apr 2026 20:11:27 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 15 Apr 2026 20:11:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:11:27 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e29b5a067225f28735c3f9c28db7a022b344731761dc5bd14d0b7a283cc13aa1`  
		Last Modified: Wed, 15 Apr 2026 20:11:34 GMT  
		Size: 8.3 MB (8297061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae71f1757016712f17b7c9321ecac9183912e0037f929b5050fa04410093a993`  
		Last Modified: Wed, 15 Apr 2026 20:11:33 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64a558c789f63340dd86a3d8d48163d7ca0b3475c2b5c1d8ca27e0afc43f81a`  
		Last Modified: Wed, 15 Apr 2026 20:11:35 GMT  
		Size: 18.1 MB (18109476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03bc6071f6b066b797f80197a5147fa49e7c18d34820ebbd67e8a05f503815a0`  
		Last Modified: Wed, 15 Apr 2026 20:11:35 GMT  
		Size: 21.2 MB (21151872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84372c97713792c82b059361309092a10362cb4b047854a0b862c3ebeb6f45a7`  
		Last Modified: Wed, 15 Apr 2026 20:11:35 GMT  
		Size: 10.4 MB (10388823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1411d774c190d6fe75a26c80337ed792c1219b393396b9dd4008440601b2e8bb`  
		Last Modified: Wed, 15 Apr 2026 20:11:36 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:213ded2f75d406b851e7f9d90ac09eacb9ecd070136e9e64a5e44a7b62246ab0`  
		Last Modified: Wed, 15 Apr 2026 20:11:36 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9546667a8b53db55a0c88114559b89b5a4c5288c765a0efd17abf18956634f`  
		Last Modified: Wed, 15 Apr 2026 20:11:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:bbcdf7618a730942664487ce478f3a269e4859185ac161e3578319a0f54ff6d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8a566184814fc34593f5137a7bba3c2c3aae7de569de008b69e5efb6fd4f2b8`

```dockerfile
```

-	Layers:
	-	`sha256:34582c23f82fc6f533690de02a4263c869ac6e2e06850e19652639cbf36d4f4c`  
		Last Modified: Wed, 15 Apr 2026 20:11:33 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:75b479961472cf73f0407e0b3c7576c45be650ab0f523fc539f33fde7777f22f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60479031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:254b0d5926521e59075cd4b154a10ba99b2e222f9e1b682d6ef3bda0b94beaef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:16:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 15 Apr 2026 20:16:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 15 Apr 2026 20:16:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 15 Apr 2026 20:16:18 GMT
ENV DOCKER_VERSION=29.4.0
# Wed, 15 Apr 2026 20:16:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 15 Apr 2026 20:16:18 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Wed, 15 Apr 2026 20:16:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 15 Apr 2026 20:16:20 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 15 Apr 2026 20:16:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 15 Apr 2026 20:16:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 15 Apr 2026 20:16:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:16:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Apr 2026 20:16:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 15 Apr 2026 20:16:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:16:22 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88cb38943f0f0a95a9ef76158143c405f36bad50621b2fd56aa2fc4f3615fd5`  
		Last Modified: Wed, 15 Apr 2026 20:16:29 GMT  
		Size: 7.6 MB (7595768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaaca956ad170283b847286ec873bec980d796519baf3f39fe964aded5374f8e`  
		Last Modified: Wed, 15 Apr 2026 20:16:28 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cdf1c13c7d0f067c56c9771266f9895d1041ebf30f39ab27603e18afb0c9081`  
		Last Modified: Wed, 15 Apr 2026 20:16:29 GMT  
		Size: 18.1 MB (18096362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813eda9384408e479910e06a79744324e1dce0b63fd42e5bce661a6e735e2f32`  
		Last Modified: Wed, 15 Apr 2026 20:16:29 GMT  
		Size: 21.1 MB (21129758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f4b664cfcad12fa1a9762a191ac3534cf78c30dd9df6eff79f75e17bd604215`  
		Last Modified: Wed, 15 Apr 2026 20:16:30 GMT  
		Size: 10.4 MB (10371870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f3580f46ae276e11707530d3b18cc55414bcb1f7a672d3cef371193e0e0947`  
		Last Modified: Wed, 15 Apr 2026 20:16:30 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d214a288fe8f0a47169af907737952cefa9e61f078490a75828a439107530b2`  
		Last Modified: Wed, 15 Apr 2026 20:16:31 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf0d872d260394713b2443444bb53d508d83624734c0239dcda7ff1830303db8`  
		Last Modified: Wed, 15 Apr 2026 20:16:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:70f0601152bac7df07b2933f0e46a2774591dbebc7e87523cc02d222b56c86b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e085d1943182e6d53f4b66b7d1654479506a41c31da6cbd8241cba54df3ce900`

```dockerfile
```

-	Layers:
	-	`sha256:368fab9b9711e124e80b9dedf4aa9bea5ba28ad952bacb0003647ef444f12135`  
		Last Modified: Wed, 15 Apr 2026 20:16:28 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:9d3f67fe1f4cf51c084744dec419b466b7075f5b365ef4b9b791187d9c2d4127
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.0 MB (61008901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dea3a61a70d2ba11898616b2f246eaeef9d1c75b7041f2e45826da60d2e47276`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:13:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 15 Apr 2026 20:13:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 15 Apr 2026 20:13:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 15 Apr 2026 20:14:02 GMT
ENV DOCKER_VERSION=29.4.0
# Wed, 15 Apr 2026 20:14:02 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 15 Apr 2026 20:14:02 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Wed, 15 Apr 2026 20:14:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 15 Apr 2026 20:14:03 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 15 Apr 2026 20:14:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 15 Apr 2026 20:14:04 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 15 Apr 2026 20:14:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:14:04 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Apr 2026 20:14:04 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 15 Apr 2026 20:14:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:14:04 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1f08e8ea565813fe5c533f3bf89a6fcb79b8ef2eb46e2872f132234aa070cf`  
		Last Modified: Wed, 15 Apr 2026 20:14:10 GMT  
		Size: 8.5 MB (8450092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ff0f79f131dfea84e2ad6ee3723888525425bfc628525e86c3cc1b288bace3`  
		Last Modified: Wed, 15 Apr 2026 20:14:10 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35bf88d1a58dc1d9ced6e216552eef44b2392e515454985dcd3f25372d12693`  
		Last Modified: Wed, 15 Apr 2026 20:14:11 GMT  
		Size: 17.9 MB (17921079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0aa9505e9a0f5469b8905ecd253d1fd12569434350a1c94898126c02a4a9c57`  
		Last Modified: Wed, 15 Apr 2026 20:14:11 GMT  
		Size: 20.5 MB (20453111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ff9179479c44e683ee3838185f58e7d707974096437fdccedcb7b1f316aa35`  
		Last Modified: Wed, 15 Apr 2026 20:14:11 GMT  
		Size: 10.0 MB (9982600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0771ed595b2bb7d830d904c0ed7f259d39bb70d0da784d731a39f7a1ceeacb04`  
		Last Modified: Wed, 15 Apr 2026 20:14:12 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627cec3b548e33f50bcd1682915056d5dfd8e5b28476d6c4842c0eb790b1f954`  
		Last Modified: Wed, 15 Apr 2026 20:14:12 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c67b1b44bc81549ba5caf988b00dabcb0c2ca6cee73ef7d756e26b08b1028e`  
		Last Modified: Wed, 15 Apr 2026 20:14:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:e021182c1f750cfc367850ea8b786139b8a3c428c84711dcaf82dad470636664
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a194ccda70da01232600045e81eff9a9985e4f5f2d0762a6d6f356e6cff9fe0`

```dockerfile
```

-	Layers:
	-	`sha256:c94d9b9821f47c73547b7085c1041bda87c05335abab499b01c9fcc9f12a80bf`  
		Last Modified: Wed, 15 Apr 2026 20:14:10 GMT  
		Size: 38.3 KB (38258 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind`

```console
$ docker pull docker@sha256:a6dd5322747a95cd8e3207bd8d415a8fd20ec34e9c00f06dc019cbd912013489
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
$ docker pull docker@sha256:4d2c6e334de4b26d492c0a8cc5438e3dbf1a02eee899fc0d4d39b96202c943a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.5 MB (140522901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:304d326357dcfc523ea9ea01226e742f15d0d548d8eaec0e14c3b39387303000`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:16:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 15 Apr 2026 20:16:25 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 15 Apr 2026 20:16:25 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 15 Apr 2026 20:16:27 GMT
ENV DOCKER_VERSION=29.4.0
# Wed, 15 Apr 2026 20:16:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 15 Apr 2026 20:16:27 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Wed, 15 Apr 2026 20:16:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 15 Apr 2026 20:16:28 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 15 Apr 2026 20:16:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 15 Apr 2026 20:16:29 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 15 Apr 2026 20:16:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:16:29 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Apr 2026 20:16:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 15 Apr 2026 20:16:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:16:30 GMT
CMD ["sh"]
# Wed, 15 Apr 2026 21:19:01 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 15 Apr 2026 21:19:02 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 15 Apr 2026 21:19:02 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 15 Apr 2026 21:19:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 15 Apr 2026 21:19:05 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 15 Apr 2026 21:19:05 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 15 Apr 2026 21:19:05 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:19:05 GMT
VOLUME [/var/lib/docker]
# Wed, 15 Apr 2026 21:19:05 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 15 Apr 2026 21:19:05 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 15 Apr 2026 21:19:05 GMT
CMD []
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00fef3bc4d7adc06c42d060d3a4fad2da6d129c5d2dac575a0a34e5276837acc`  
		Last Modified: Wed, 15 Apr 2026 20:16:37 GMT  
		Size: 8.4 MB (8390330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f8bdd90a189e988440fcec9f3b420d55047950b5f7601ba0e57b351852d7ba`  
		Last Modified: Wed, 15 Apr 2026 20:16:36 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4985eb1bbbfe749a8493542e038307f004a28671974b2a082ae06f9391c4aa64`  
		Last Modified: Wed, 15 Apr 2026 20:16:37 GMT  
		Size: 19.5 MB (19464794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859abcc7688b1a7cc3cc9e144132fc9069de384c58f57dcdc67bb82efa576352`  
		Last Modified: Wed, 15 Apr 2026 20:16:37 GMT  
		Size: 22.5 MB (22539232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c99a167aeca4fe59d6c36fcd7dd693309a219446eca7bcdc04b392e4d69c2c4`  
		Last Modified: Wed, 15 Apr 2026 20:16:38 GMT  
		Size: 11.0 MB (10955103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e81a750c9b2d394bb0113dc9e2ac999fdb73fc198aee986c23671ccc8b782c`  
		Last Modified: Wed, 15 Apr 2026 20:16:38 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ba37c8df4e2fbeeea282fc985c366a9d438cb9ac52b521a1ba48cc214ddd6c`  
		Last Modified: Wed, 15 Apr 2026 20:16:39 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26929be3c972c7f0a15b08c4029aaa790ccc1d494702813df05e37cf6c95ece4`  
		Last Modified: Wed, 15 Apr 2026 20:16:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72409ebb253eee0d0ac41d3def31dd521fd7fbb44646380257fce88e92956e1b`  
		Last Modified: Wed, 15 Apr 2026 21:19:16 GMT  
		Size: 6.9 MB (6941794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61b7bb0bfe4127ecc181695a6617bce6875877794291f6f411f1503400774934`  
		Last Modified: Wed, 15 Apr 2026 21:19:15 GMT  
		Size: 92.4 KB (92386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f322cdda1c007efd5a7874085a0a278df1d8cba0c79c539cecdfd441528c5063`  
		Last Modified: Wed, 15 Apr 2026 21:19:16 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b195c7fa897ae20e300894f9c01ab27baa6d026f2966d14da47768c0504f7e0d`  
		Last Modified: Wed, 15 Apr 2026 21:19:18 GMT  
		Size: 68.3 MB (68266921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d71ba441d54fb7122eab57ffb2e5cc6805c4abe5aa1229a369d61713d35c4a`  
		Last Modified: Wed, 15 Apr 2026 21:19:17 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471eb30b983e8a0f853e3d3be9271df608fd2048cec340fa2eaef5e93dccfdd6`  
		Last Modified: Wed, 15 Apr 2026 21:19:17 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:1c8aa5173659195543e7f2199b877ec50c9f568416a96a31cd42b2fcd07923ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36f6b76c4e162e68e3741832b1fa66576d6705a81ed60bdeeded8cbffb74e2ff`

```dockerfile
```

-	Layers:
	-	`sha256:4c3c193ad694d685d8594f91321d9d1fe73498db66cfb3767583e03cba34f0eb`  
		Last Modified: Wed, 15 Apr 2026 21:19:15 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:b23cae1ff183bc4e75d88eaf9ba1c6549849f1d134d11fc442d0f885b1f58d4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 MB (132507536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c664d0b218f2b2a9a4e105a5162c0ba967e6162e60df351421a2b174c2b02b2f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:11:18 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 15 Apr 2026 20:11:18 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 15 Apr 2026 20:11:18 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 15 Apr 2026 20:11:22 GMT
ENV DOCKER_VERSION=29.4.0
# Wed, 15 Apr 2026 20:11:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 15 Apr 2026 20:11:22 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Wed, 15 Apr 2026 20:11:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 15 Apr 2026 20:11:25 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 15 Apr 2026 20:11:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 15 Apr 2026 20:11:27 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 15 Apr 2026 20:11:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:11:27 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Apr 2026 20:11:27 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 15 Apr 2026 20:11:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:11:27 GMT
CMD ["sh"]
# Wed, 15 Apr 2026 21:19:39 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 15 Apr 2026 21:19:40 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 15 Apr 2026 21:19:40 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 15 Apr 2026 21:19:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 15 Apr 2026 21:19:44 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 15 Apr 2026 21:19:44 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 15 Apr 2026 21:19:44 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:19:44 GMT
VOLUME [/var/lib/docker]
# Wed, 15 Apr 2026 21:19:44 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 15 Apr 2026 21:19:44 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 15 Apr 2026 21:19:44 GMT
CMD []
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e29b5a067225f28735c3f9c28db7a022b344731761dc5bd14d0b7a283cc13aa1`  
		Last Modified: Wed, 15 Apr 2026 20:11:34 GMT  
		Size: 8.3 MB (8297061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae71f1757016712f17b7c9321ecac9183912e0037f929b5050fa04410093a993`  
		Last Modified: Wed, 15 Apr 2026 20:11:33 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64a558c789f63340dd86a3d8d48163d7ca0b3475c2b5c1d8ca27e0afc43f81a`  
		Last Modified: Wed, 15 Apr 2026 20:11:35 GMT  
		Size: 18.1 MB (18109476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03bc6071f6b066b797f80197a5147fa49e7c18d34820ebbd67e8a05f503815a0`  
		Last Modified: Wed, 15 Apr 2026 20:11:35 GMT  
		Size: 21.2 MB (21151872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84372c97713792c82b059361309092a10362cb4b047854a0b862c3ebeb6f45a7`  
		Last Modified: Wed, 15 Apr 2026 20:11:35 GMT  
		Size: 10.4 MB (10388823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1411d774c190d6fe75a26c80337ed792c1219b393396b9dd4008440601b2e8bb`  
		Last Modified: Wed, 15 Apr 2026 20:11:36 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:213ded2f75d406b851e7f9d90ac09eacb9ecd070136e9e64a5e44a7b62246ab0`  
		Last Modified: Wed, 15 Apr 2026 20:11:36 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9546667a8b53db55a0c88114559b89b5a4c5288c765a0efd17abf18956634f`  
		Last Modified: Wed, 15 Apr 2026 20:11:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db0f2e08cd52770499a4a7b14b1d7035c2bed565f5d1658d36f77ba8cae62ad5`  
		Last Modified: Wed, 15 Apr 2026 21:19:55 GMT  
		Size: 7.3 MB (7278394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810c7f3c3226c75491d45b3028f6aa4e32c04edce7619e9c304e5c7054c6e3e8`  
		Last Modified: Wed, 15 Apr 2026 21:19:55 GMT  
		Size: 91.7 KB (91683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80b9397e0c604f4cffa37ef63fc68b0849fbe399433ee3b1b24e32ea5c1b6138`  
		Last Modified: Wed, 15 Apr 2026 21:19:55 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:578128484de3ef92c76816591ca072998f01b1381725e18fd1c7a4baa20bc9f8`  
		Last Modified: Wed, 15 Apr 2026 21:19:56 GMT  
		Size: 63.6 MB (63610209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2209085b94038497f0af62b68d75961a5b080cb35551dcc8d0eefab6b722484a`  
		Last Modified: Wed, 15 Apr 2026 21:19:56 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b27ed318c8e6661d6fa40585004daf813302e8af45e485fdf0173af3947bc2`  
		Last Modified: Wed, 15 Apr 2026 21:19:56 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:a01657f9a7e1e95bc00dd7bf0d40d8f4e73263519d316ff513e77cd827e24f6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48c770ff5e3d911a2d76c733a01cc1a9e96597d1aeb12c3470e57cf12936aa28`

```dockerfile
```

-	Layers:
	-	`sha256:147b649936864607c8d1c5530d9427c37768a5718de420c9941b6f3b6625b9d5`  
		Last Modified: Wed, 15 Apr 2026 21:19:54 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:20d1ab4a0712e057c1adc25f5703a97b31a7f387b43adc77bb7308d4397970e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130593641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ca74a271ab95685bc02e667fcb161e01b626e71e3d25886e49bfab8239d7ded`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:16:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 15 Apr 2026 20:16:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 15 Apr 2026 20:16:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 15 Apr 2026 20:16:18 GMT
ENV DOCKER_VERSION=29.4.0
# Wed, 15 Apr 2026 20:16:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 15 Apr 2026 20:16:18 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Wed, 15 Apr 2026 20:16:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 15 Apr 2026 20:16:20 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 15 Apr 2026 20:16:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 15 Apr 2026 20:16:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 15 Apr 2026 20:16:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:16:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Apr 2026 20:16:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 15 Apr 2026 20:16:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:16:22 GMT
CMD ["sh"]
# Wed, 15 Apr 2026 21:27:26 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 15 Apr 2026 21:27:28 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 15 Apr 2026 21:27:28 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 15 Apr 2026 21:27:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 15 Apr 2026 21:27:31 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 15 Apr 2026 21:27:31 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 15 Apr 2026 21:27:31 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:27:31 GMT
VOLUME [/var/lib/docker]
# Wed, 15 Apr 2026 21:27:31 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 15 Apr 2026 21:27:31 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 15 Apr 2026 21:27:31 GMT
CMD []
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88cb38943f0f0a95a9ef76158143c405f36bad50621b2fd56aa2fc4f3615fd5`  
		Last Modified: Wed, 15 Apr 2026 20:16:29 GMT  
		Size: 7.6 MB (7595768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaaca956ad170283b847286ec873bec980d796519baf3f39fe964aded5374f8e`  
		Last Modified: Wed, 15 Apr 2026 20:16:28 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cdf1c13c7d0f067c56c9771266f9895d1041ebf30f39ab27603e18afb0c9081`  
		Last Modified: Wed, 15 Apr 2026 20:16:29 GMT  
		Size: 18.1 MB (18096362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813eda9384408e479910e06a79744324e1dce0b63fd42e5bce661a6e735e2f32`  
		Last Modified: Wed, 15 Apr 2026 20:16:29 GMT  
		Size: 21.1 MB (21129758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f4b664cfcad12fa1a9762a191ac3534cf78c30dd9df6eff79f75e17bd604215`  
		Last Modified: Wed, 15 Apr 2026 20:16:30 GMT  
		Size: 10.4 MB (10371870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f3580f46ae276e11707530d3b18cc55414bcb1f7a672d3cef371193e0e0947`  
		Last Modified: Wed, 15 Apr 2026 20:16:30 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d214a288fe8f0a47169af907737952cefa9e61f078490a75828a439107530b2`  
		Last Modified: Wed, 15 Apr 2026 20:16:31 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf0d872d260394713b2443444bb53d508d83624734c0239dcda7ff1830303db8`  
		Last Modified: Wed, 15 Apr 2026 20:16:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89db5f2f3e615ce6454e5c1c42292805de5a924c4769cb726472a5f992eef448`  
		Last Modified: Wed, 15 Apr 2026 21:27:42 GMT  
		Size: 6.6 MB (6577217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a486198c8f3ba2ab5d5c0c2444157dbdb3a24ef48b6dcbe399e92e72a5e6c28`  
		Last Modified: Wed, 15 Apr 2026 21:27:42 GMT  
		Size: 88.0 KB (88036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba24e0fe682bf1faf33f78d5b19ecad454f21527c9a6c33cfb4c1d694b52779`  
		Last Modified: Wed, 15 Apr 2026 21:27:42 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ca224f3bf33d1172adfccf0c242f89893fde617bd5885ef7545ecd22e41ef4f`  
		Last Modified: Wed, 15 Apr 2026 21:27:44 GMT  
		Size: 63.4 MB (63443351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac3934cb427133bc539854b45e314e2dc44838a979414cf67dd89810b967f06`  
		Last Modified: Wed, 15 Apr 2026 21:27:43 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5e8455627c95fe22aa58fead7cbf2a0934fd4d57d760756577ec0b8c9bf4bc`  
		Last Modified: Wed, 15 Apr 2026 21:27:43 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:9376e04ebe10bd90bf0a7a85bddeb4c723ab3c8e9ae5290a6f522143cdbed03d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58ce25b3cedf687af0bcb158bb0a1d2a8523dfeadcddc68360fc3394f815f730`

```dockerfile
```

-	Layers:
	-	`sha256:ecdd6391528d66bfad436f41aef96daa292510a5ddd3f115f031dd1728b3dd36`  
		Last Modified: Wed, 15 Apr 2026 21:27:42 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:553d694bc3ae2a92b67b73072e3923a8d2256e609b568c60d08e4544e8f39ff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.1 MB (130126872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5c1c78f7262d1e00eef13317919dc25b6d65c96115e46f851ab09818f2ddf0b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:13:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 15 Apr 2026 20:13:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 15 Apr 2026 20:13:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 15 Apr 2026 20:14:02 GMT
ENV DOCKER_VERSION=29.4.0
# Wed, 15 Apr 2026 20:14:02 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 15 Apr 2026 20:14:02 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Wed, 15 Apr 2026 20:14:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 15 Apr 2026 20:14:03 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 15 Apr 2026 20:14:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 15 Apr 2026 20:14:04 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 15 Apr 2026 20:14:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:14:04 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Apr 2026 20:14:04 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 15 Apr 2026 20:14:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:14:04 GMT
CMD ["sh"]
# Wed, 15 Apr 2026 21:33:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 15 Apr 2026 21:33:18 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 15 Apr 2026 21:33:18 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 15 Apr 2026 21:33:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 15 Apr 2026 21:33:21 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 15 Apr 2026 21:33:21 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 15 Apr 2026 21:33:21 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:33:21 GMT
VOLUME [/var/lib/docker]
# Wed, 15 Apr 2026 21:33:21 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 15 Apr 2026 21:33:21 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 15 Apr 2026 21:33:21 GMT
CMD []
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1f08e8ea565813fe5c533f3bf89a6fcb79b8ef2eb46e2872f132234aa070cf`  
		Last Modified: Wed, 15 Apr 2026 20:14:10 GMT  
		Size: 8.5 MB (8450092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ff0f79f131dfea84e2ad6ee3723888525425bfc628525e86c3cc1b288bace3`  
		Last Modified: Wed, 15 Apr 2026 20:14:10 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35bf88d1a58dc1d9ced6e216552eef44b2392e515454985dcd3f25372d12693`  
		Last Modified: Wed, 15 Apr 2026 20:14:11 GMT  
		Size: 17.9 MB (17921079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0aa9505e9a0f5469b8905ecd253d1fd12569434350a1c94898126c02a4a9c57`  
		Last Modified: Wed, 15 Apr 2026 20:14:11 GMT  
		Size: 20.5 MB (20453111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ff9179479c44e683ee3838185f58e7d707974096437fdccedcb7b1f316aa35`  
		Last Modified: Wed, 15 Apr 2026 20:14:11 GMT  
		Size: 10.0 MB (9982600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0771ed595b2bb7d830d904c0ed7f259d39bb70d0da784d731a39f7a1ceeacb04`  
		Last Modified: Wed, 15 Apr 2026 20:14:12 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627cec3b548e33f50bcd1682915056d5dfd8e5b28476d6c4842c0eb790b1f954`  
		Last Modified: Wed, 15 Apr 2026 20:14:12 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c67b1b44bc81549ba5caf988b00dabcb0c2ca6cee73ef7d756e26b08b1028e`  
		Last Modified: Wed, 15 Apr 2026 20:14:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c169b754493e049763aeab1727fe430cecafcd9032c4389b3053958aebc360c9`  
		Last Modified: Wed, 15 Apr 2026 21:33:31 GMT  
		Size: 7.2 MB (7219816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbba1f41e162f643c431dbb55a4cfb94284235c55c0c226f2f85fdc2797d7d3`  
		Last Modified: Wed, 15 Apr 2026 21:33:30 GMT  
		Size: 101.2 KB (101171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc3e20cde46cbbd2b898524e10c8ed94082175c8c21daf98b34e7a6006aafee`  
		Last Modified: Wed, 15 Apr 2026 21:33:30 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ae4baf5361489e96a43c6d29d47fdd4eb63dd088b10e8bf91df746925678ea`  
		Last Modified: Wed, 15 Apr 2026 21:33:32 GMT  
		Size: 61.8 MB (61790985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7fa8aac1af219d886ca4026da0a5a043fde1dae9d3e8534dd78f23360b8763`  
		Last Modified: Wed, 15 Apr 2026 21:33:32 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f667dde4f795a12a4a9d7129f07e71678ffec2ae9a15d680f09fd672a64ab154`  
		Last Modified: Wed, 15 Apr 2026 21:33:32 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:71c18f631e3205680e2fcd0ea55f0f373c7fb19de8336794fe07f3d4793786b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48d9407668f8511b7b181ffcfea6ce22705df56aaf20a9dd84a0930f31f6ecf7`

```dockerfile
```

-	Layers:
	-	`sha256:623b2bc83b8d25632b5e152b95570ef2a7af85709fedfa2ae3ed9d312b61c77c`  
		Last Modified: Wed, 15 Apr 2026 21:33:30 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind-rootless`

```console
$ docker pull docker@sha256:76944d96ec8f4d759b5c8d9bf5f0787813f278e46aa078ae65338216739cb0fd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:e89e2c0f44ba58a65f9f9dc8b04aea6ee7f31c76a7ff8048465f2576746fadb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.5 MB (161524750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ceb46e5e927ba19a62569af7c8eb32cbcef000cd7379578db1e3a3e4fe943aa`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:16:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 15 Apr 2026 20:16:25 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 15 Apr 2026 20:16:25 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 15 Apr 2026 20:16:27 GMT
ENV DOCKER_VERSION=29.4.0
# Wed, 15 Apr 2026 20:16:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 15 Apr 2026 20:16:27 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Wed, 15 Apr 2026 20:16:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 15 Apr 2026 20:16:28 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 15 Apr 2026 20:16:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 15 Apr 2026 20:16:29 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 15 Apr 2026 20:16:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:16:29 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Apr 2026 20:16:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 15 Apr 2026 20:16:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:16:30 GMT
CMD ["sh"]
# Wed, 15 Apr 2026 21:19:01 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 15 Apr 2026 21:19:02 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 15 Apr 2026 21:19:02 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 15 Apr 2026 21:19:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 15 Apr 2026 21:19:05 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 15 Apr 2026 21:19:05 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 15 Apr 2026 21:19:05 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:19:05 GMT
VOLUME [/var/lib/docker]
# Wed, 15 Apr 2026 21:19:05 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 15 Apr 2026 21:19:05 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 15 Apr 2026 21:19:05 GMT
CMD []
# Wed, 15 Apr 2026 22:12:18 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Wed, 15 Apr 2026 22:12:18 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 15 Apr 2026 22:12:18 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 15 Apr 2026 22:12:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 15 Apr 2026 22:12:19 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 15 Apr 2026 22:12:19 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 15 Apr 2026 22:12:19 GMT
USER rootless
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00fef3bc4d7adc06c42d060d3a4fad2da6d129c5d2dac575a0a34e5276837acc`  
		Last Modified: Wed, 15 Apr 2026 20:16:37 GMT  
		Size: 8.4 MB (8390330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f8bdd90a189e988440fcec9f3b420d55047950b5f7601ba0e57b351852d7ba`  
		Last Modified: Wed, 15 Apr 2026 20:16:36 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4985eb1bbbfe749a8493542e038307f004a28671974b2a082ae06f9391c4aa64`  
		Last Modified: Wed, 15 Apr 2026 20:16:37 GMT  
		Size: 19.5 MB (19464794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859abcc7688b1a7cc3cc9e144132fc9069de384c58f57dcdc67bb82efa576352`  
		Last Modified: Wed, 15 Apr 2026 20:16:37 GMT  
		Size: 22.5 MB (22539232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c99a167aeca4fe59d6c36fcd7dd693309a219446eca7bcdc04b392e4d69c2c4`  
		Last Modified: Wed, 15 Apr 2026 20:16:38 GMT  
		Size: 11.0 MB (10955103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e81a750c9b2d394bb0113dc9e2ac999fdb73fc198aee986c23671ccc8b782c`  
		Last Modified: Wed, 15 Apr 2026 20:16:38 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ba37c8df4e2fbeeea282fc985c366a9d438cb9ac52b521a1ba48cc214ddd6c`  
		Last Modified: Wed, 15 Apr 2026 20:16:39 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26929be3c972c7f0a15b08c4029aaa790ccc1d494702813df05e37cf6c95ece4`  
		Last Modified: Wed, 15 Apr 2026 20:16:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72409ebb253eee0d0ac41d3def31dd521fd7fbb44646380257fce88e92956e1b`  
		Last Modified: Wed, 15 Apr 2026 21:19:16 GMT  
		Size: 6.9 MB (6941794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61b7bb0bfe4127ecc181695a6617bce6875877794291f6f411f1503400774934`  
		Last Modified: Wed, 15 Apr 2026 21:19:15 GMT  
		Size: 92.4 KB (92386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f322cdda1c007efd5a7874085a0a278df1d8cba0c79c539cecdfd441528c5063`  
		Last Modified: Wed, 15 Apr 2026 21:19:16 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b195c7fa897ae20e300894f9c01ab27baa6d026f2966d14da47768c0504f7e0d`  
		Last Modified: Wed, 15 Apr 2026 21:19:18 GMT  
		Size: 68.3 MB (68266921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d71ba441d54fb7122eab57ffb2e5cc6805c4abe5aa1229a369d61713d35c4a`  
		Last Modified: Wed, 15 Apr 2026 21:19:17 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471eb30b983e8a0f853e3d3be9271df608fd2048cec340fa2eaef5e93dccfdd6`  
		Last Modified: Wed, 15 Apr 2026 21:19:17 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d603a61ab9bf085d4c5ed544ebdc6930cedac60c151b8c3d844ec4a5e1907a3f`  
		Last Modified: Wed, 15 Apr 2026 22:12:32 GMT  
		Size: 3.4 MB (3420096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f6cf84eabf10318aff4902301c0a7eb0d5e3a1fbedc2457d5a03e48ec176798`  
		Last Modified: Wed, 15 Apr 2026 22:12:26 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c7e42a9e418d966d88e75d7076fb61e32f5f036331ad87079c2af72fee32a29`  
		Last Modified: Wed, 15 Apr 2026 22:12:28 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:707634342cc50aaa8f17842865d9fe9c4d140289067e551027f32d44235c5e64`  
		Last Modified: Wed, 15 Apr 2026 22:12:36 GMT  
		Size: 17.6 MB (17580415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5efa74639426aef15709b77e6fe19278595bf047f2e03f5a8449cc234b9df8c2`  
		Last Modified: Wed, 15 Apr 2026 22:12:32 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:16263b4914888c6b7270d1a2b9da8845365aacaafbf2ae86d9c3e093373eb29c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9072388f94ef26c4fd86a7769ed365d8a261d4df812abb3ef6950a2400d130af`

```dockerfile
```

-	Layers:
	-	`sha256:f9339be88cc342b92f34d4da76922c287e26b230e4ebab8ba0b5ce74a00df08b`  
		Last Modified: Wed, 15 Apr 2026 22:12:24 GMT  
		Size: 30.6 KB (30589 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:b4fad2141f6e11611acfc843f2434ba2a41e6915639963b943fa2ba4b51e87d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.4 MB (151405559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95e9af8ffe8cf19d9949f80c4fe0f01db4518273f5f1e3f6470799d230530909`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:13:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 15 Apr 2026 20:13:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 15 Apr 2026 20:13:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 15 Apr 2026 20:14:02 GMT
ENV DOCKER_VERSION=29.4.0
# Wed, 15 Apr 2026 20:14:02 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 15 Apr 2026 20:14:02 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Wed, 15 Apr 2026 20:14:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 15 Apr 2026 20:14:03 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 15 Apr 2026 20:14:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 15 Apr 2026 20:14:04 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 15 Apr 2026 20:14:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:14:04 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Apr 2026 20:14:04 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 15 Apr 2026 20:14:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:14:04 GMT
CMD ["sh"]
# Wed, 15 Apr 2026 21:33:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 15 Apr 2026 21:33:18 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 15 Apr 2026 21:33:18 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 15 Apr 2026 21:33:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 15 Apr 2026 21:33:21 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 15 Apr 2026 21:33:21 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 15 Apr 2026 21:33:21 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:33:21 GMT
VOLUME [/var/lib/docker]
# Wed, 15 Apr 2026 21:33:21 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 15 Apr 2026 21:33:21 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 15 Apr 2026 21:33:21 GMT
CMD []
# Wed, 15 Apr 2026 22:24:13 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Wed, 15 Apr 2026 22:24:13 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 15 Apr 2026 22:24:13 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 15 Apr 2026 22:24:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 15 Apr 2026 22:24:14 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 15 Apr 2026 22:24:14 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 15 Apr 2026 22:24:14 GMT
USER rootless
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1f08e8ea565813fe5c533f3bf89a6fcb79b8ef2eb46e2872f132234aa070cf`  
		Last Modified: Wed, 15 Apr 2026 20:14:10 GMT  
		Size: 8.5 MB (8450092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ff0f79f131dfea84e2ad6ee3723888525425bfc628525e86c3cc1b288bace3`  
		Last Modified: Wed, 15 Apr 2026 20:14:10 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35bf88d1a58dc1d9ced6e216552eef44b2392e515454985dcd3f25372d12693`  
		Last Modified: Wed, 15 Apr 2026 20:14:11 GMT  
		Size: 17.9 MB (17921079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0aa9505e9a0f5469b8905ecd253d1fd12569434350a1c94898126c02a4a9c57`  
		Last Modified: Wed, 15 Apr 2026 20:14:11 GMT  
		Size: 20.5 MB (20453111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ff9179479c44e683ee3838185f58e7d707974096437fdccedcb7b1f316aa35`  
		Last Modified: Wed, 15 Apr 2026 20:14:11 GMT  
		Size: 10.0 MB (9982600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0771ed595b2bb7d830d904c0ed7f259d39bb70d0da784d731a39f7a1ceeacb04`  
		Last Modified: Wed, 15 Apr 2026 20:14:12 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627cec3b548e33f50bcd1682915056d5dfd8e5b28476d6c4842c0eb790b1f954`  
		Last Modified: Wed, 15 Apr 2026 20:14:12 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c67b1b44bc81549ba5caf988b00dabcb0c2ca6cee73ef7d756e26b08b1028e`  
		Last Modified: Wed, 15 Apr 2026 20:14:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c169b754493e049763aeab1727fe430cecafcd9032c4389b3053958aebc360c9`  
		Last Modified: Wed, 15 Apr 2026 21:33:31 GMT  
		Size: 7.2 MB (7219816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbba1f41e162f643c431dbb55a4cfb94284235c55c0c226f2f85fdc2797d7d3`  
		Last Modified: Wed, 15 Apr 2026 21:33:30 GMT  
		Size: 101.2 KB (101171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc3e20cde46cbbd2b898524e10c8ed94082175c8c21daf98b34e7a6006aafee`  
		Last Modified: Wed, 15 Apr 2026 21:33:30 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ae4baf5361489e96a43c6d29d47fdd4eb63dd088b10e8bf91df746925678ea`  
		Last Modified: Wed, 15 Apr 2026 21:33:32 GMT  
		Size: 61.8 MB (61790985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7fa8aac1af219d886ca4026da0a5a043fde1dae9d3e8534dd78f23360b8763`  
		Last Modified: Wed, 15 Apr 2026 21:33:32 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f667dde4f795a12a4a9d7129f07e71678ffec2ae9a15d680f09fd672a64ab154`  
		Last Modified: Wed, 15 Apr 2026 21:33:32 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9012b0d6da5801eab238bb387dbb36b8d6a39d5aa7039815d1c9e2a24833a04`  
		Last Modified: Wed, 15 Apr 2026 22:24:20 GMT  
		Size: 3.4 MB (3394534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:960aa9d16806e38df09387de191ea1c727cc5093bc76be222ed5d2a7ca369379`  
		Last Modified: Wed, 15 Apr 2026 22:24:20 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78adb818d73519733cf9dc2e2f2fdf7f7b19abf1d6a5f6050937e7df4fca78d3`  
		Last Modified: Wed, 15 Apr 2026 22:24:20 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f755f683e7f98d710321e727c122d4fd09ba183d051ff46907c74d640b25fcc8`  
		Last Modified: Wed, 15 Apr 2026 22:24:21 GMT  
		Size: 17.9 MB (17882814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d3922b05d8ff64a19ec81b180d6950d39f6867f3dee697b2c3495cb2625bcc`  
		Last Modified: Wed, 15 Apr 2026 22:24:21 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:bb4750590667d42b5f476e8c84bbfb8c1157d5e39d0a4d73884792417165644b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6910dd353dfd57bed56f7465cd51c75e8b8d0c0213fe745a77273d1d7a3f43c4`

```dockerfile
```

-	Layers:
	-	`sha256:4bfbb83e76361cdb9defcea46dc5c48423a4c288e606987803e7f5ee3edc2883`  
		Last Modified: Wed, 15 Apr 2026 22:24:20 GMT  
		Size: 30.8 KB (30752 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:latest`

```console
$ docker pull docker@sha256:a6dd5322747a95cd8e3207bd8d415a8fd20ec34e9c00f06dc019cbd912013489
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
$ docker pull docker@sha256:4d2c6e334de4b26d492c0a8cc5438e3dbf1a02eee899fc0d4d39b96202c943a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.5 MB (140522901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:304d326357dcfc523ea9ea01226e742f15d0d548d8eaec0e14c3b39387303000`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:16:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 15 Apr 2026 20:16:25 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 15 Apr 2026 20:16:25 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 15 Apr 2026 20:16:27 GMT
ENV DOCKER_VERSION=29.4.0
# Wed, 15 Apr 2026 20:16:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 15 Apr 2026 20:16:27 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Wed, 15 Apr 2026 20:16:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 15 Apr 2026 20:16:28 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 15 Apr 2026 20:16:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 15 Apr 2026 20:16:29 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 15 Apr 2026 20:16:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:16:29 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Apr 2026 20:16:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 15 Apr 2026 20:16:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:16:30 GMT
CMD ["sh"]
# Wed, 15 Apr 2026 21:19:01 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 15 Apr 2026 21:19:02 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 15 Apr 2026 21:19:02 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 15 Apr 2026 21:19:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 15 Apr 2026 21:19:05 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 15 Apr 2026 21:19:05 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 15 Apr 2026 21:19:05 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:19:05 GMT
VOLUME [/var/lib/docker]
# Wed, 15 Apr 2026 21:19:05 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 15 Apr 2026 21:19:05 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 15 Apr 2026 21:19:05 GMT
CMD []
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00fef3bc4d7adc06c42d060d3a4fad2da6d129c5d2dac575a0a34e5276837acc`  
		Last Modified: Wed, 15 Apr 2026 20:16:37 GMT  
		Size: 8.4 MB (8390330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f8bdd90a189e988440fcec9f3b420d55047950b5f7601ba0e57b351852d7ba`  
		Last Modified: Wed, 15 Apr 2026 20:16:36 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4985eb1bbbfe749a8493542e038307f004a28671974b2a082ae06f9391c4aa64`  
		Last Modified: Wed, 15 Apr 2026 20:16:37 GMT  
		Size: 19.5 MB (19464794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859abcc7688b1a7cc3cc9e144132fc9069de384c58f57dcdc67bb82efa576352`  
		Last Modified: Wed, 15 Apr 2026 20:16:37 GMT  
		Size: 22.5 MB (22539232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c99a167aeca4fe59d6c36fcd7dd693309a219446eca7bcdc04b392e4d69c2c4`  
		Last Modified: Wed, 15 Apr 2026 20:16:38 GMT  
		Size: 11.0 MB (10955103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e81a750c9b2d394bb0113dc9e2ac999fdb73fc198aee986c23671ccc8b782c`  
		Last Modified: Wed, 15 Apr 2026 20:16:38 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ba37c8df4e2fbeeea282fc985c366a9d438cb9ac52b521a1ba48cc214ddd6c`  
		Last Modified: Wed, 15 Apr 2026 20:16:39 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26929be3c972c7f0a15b08c4029aaa790ccc1d494702813df05e37cf6c95ece4`  
		Last Modified: Wed, 15 Apr 2026 20:16:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72409ebb253eee0d0ac41d3def31dd521fd7fbb44646380257fce88e92956e1b`  
		Last Modified: Wed, 15 Apr 2026 21:19:16 GMT  
		Size: 6.9 MB (6941794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61b7bb0bfe4127ecc181695a6617bce6875877794291f6f411f1503400774934`  
		Last Modified: Wed, 15 Apr 2026 21:19:15 GMT  
		Size: 92.4 KB (92386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f322cdda1c007efd5a7874085a0a278df1d8cba0c79c539cecdfd441528c5063`  
		Last Modified: Wed, 15 Apr 2026 21:19:16 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b195c7fa897ae20e300894f9c01ab27baa6d026f2966d14da47768c0504f7e0d`  
		Last Modified: Wed, 15 Apr 2026 21:19:18 GMT  
		Size: 68.3 MB (68266921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d71ba441d54fb7122eab57ffb2e5cc6805c4abe5aa1229a369d61713d35c4a`  
		Last Modified: Wed, 15 Apr 2026 21:19:17 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471eb30b983e8a0f853e3d3be9271df608fd2048cec340fa2eaef5e93dccfdd6`  
		Last Modified: Wed, 15 Apr 2026 21:19:17 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:1c8aa5173659195543e7f2199b877ec50c9f568416a96a31cd42b2fcd07923ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36f6b76c4e162e68e3741832b1fa66576d6705a81ed60bdeeded8cbffb74e2ff`

```dockerfile
```

-	Layers:
	-	`sha256:4c3c193ad694d685d8594f91321d9d1fe73498db66cfb3767583e03cba34f0eb`  
		Last Modified: Wed, 15 Apr 2026 21:19:15 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v6

```console
$ docker pull docker@sha256:b23cae1ff183bc4e75d88eaf9ba1c6549849f1d134d11fc442d0f885b1f58d4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 MB (132507536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c664d0b218f2b2a9a4e105a5162c0ba967e6162e60df351421a2b174c2b02b2f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:11:18 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 15 Apr 2026 20:11:18 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 15 Apr 2026 20:11:18 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 15 Apr 2026 20:11:22 GMT
ENV DOCKER_VERSION=29.4.0
# Wed, 15 Apr 2026 20:11:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 15 Apr 2026 20:11:22 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Wed, 15 Apr 2026 20:11:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 15 Apr 2026 20:11:25 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 15 Apr 2026 20:11:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 15 Apr 2026 20:11:27 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 15 Apr 2026 20:11:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:11:27 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Apr 2026 20:11:27 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 15 Apr 2026 20:11:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:11:27 GMT
CMD ["sh"]
# Wed, 15 Apr 2026 21:19:39 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 15 Apr 2026 21:19:40 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 15 Apr 2026 21:19:40 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 15 Apr 2026 21:19:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 15 Apr 2026 21:19:44 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 15 Apr 2026 21:19:44 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 15 Apr 2026 21:19:44 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:19:44 GMT
VOLUME [/var/lib/docker]
# Wed, 15 Apr 2026 21:19:44 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 15 Apr 2026 21:19:44 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 15 Apr 2026 21:19:44 GMT
CMD []
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e29b5a067225f28735c3f9c28db7a022b344731761dc5bd14d0b7a283cc13aa1`  
		Last Modified: Wed, 15 Apr 2026 20:11:34 GMT  
		Size: 8.3 MB (8297061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae71f1757016712f17b7c9321ecac9183912e0037f929b5050fa04410093a993`  
		Last Modified: Wed, 15 Apr 2026 20:11:33 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64a558c789f63340dd86a3d8d48163d7ca0b3475c2b5c1d8ca27e0afc43f81a`  
		Last Modified: Wed, 15 Apr 2026 20:11:35 GMT  
		Size: 18.1 MB (18109476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03bc6071f6b066b797f80197a5147fa49e7c18d34820ebbd67e8a05f503815a0`  
		Last Modified: Wed, 15 Apr 2026 20:11:35 GMT  
		Size: 21.2 MB (21151872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84372c97713792c82b059361309092a10362cb4b047854a0b862c3ebeb6f45a7`  
		Last Modified: Wed, 15 Apr 2026 20:11:35 GMT  
		Size: 10.4 MB (10388823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1411d774c190d6fe75a26c80337ed792c1219b393396b9dd4008440601b2e8bb`  
		Last Modified: Wed, 15 Apr 2026 20:11:36 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:213ded2f75d406b851e7f9d90ac09eacb9ecd070136e9e64a5e44a7b62246ab0`  
		Last Modified: Wed, 15 Apr 2026 20:11:36 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9546667a8b53db55a0c88114559b89b5a4c5288c765a0efd17abf18956634f`  
		Last Modified: Wed, 15 Apr 2026 20:11:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db0f2e08cd52770499a4a7b14b1d7035c2bed565f5d1658d36f77ba8cae62ad5`  
		Last Modified: Wed, 15 Apr 2026 21:19:55 GMT  
		Size: 7.3 MB (7278394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810c7f3c3226c75491d45b3028f6aa4e32c04edce7619e9c304e5c7054c6e3e8`  
		Last Modified: Wed, 15 Apr 2026 21:19:55 GMT  
		Size: 91.7 KB (91683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80b9397e0c604f4cffa37ef63fc68b0849fbe399433ee3b1b24e32ea5c1b6138`  
		Last Modified: Wed, 15 Apr 2026 21:19:55 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:578128484de3ef92c76816591ca072998f01b1381725e18fd1c7a4baa20bc9f8`  
		Last Modified: Wed, 15 Apr 2026 21:19:56 GMT  
		Size: 63.6 MB (63610209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2209085b94038497f0af62b68d75961a5b080cb35551dcc8d0eefab6b722484a`  
		Last Modified: Wed, 15 Apr 2026 21:19:56 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b27ed318c8e6661d6fa40585004daf813302e8af45e485fdf0173af3947bc2`  
		Last Modified: Wed, 15 Apr 2026 21:19:56 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:a01657f9a7e1e95bc00dd7bf0d40d8f4e73263519d316ff513e77cd827e24f6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48c770ff5e3d911a2d76c733a01cc1a9e96597d1aeb12c3470e57cf12936aa28`

```dockerfile
```

-	Layers:
	-	`sha256:147b649936864607c8d1c5530d9427c37768a5718de420c9941b6f3b6625b9d5`  
		Last Modified: Wed, 15 Apr 2026 21:19:54 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v7

```console
$ docker pull docker@sha256:20d1ab4a0712e057c1adc25f5703a97b31a7f387b43adc77bb7308d4397970e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130593641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ca74a271ab95685bc02e667fcb161e01b626e71e3d25886e49bfab8239d7ded`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:16:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 15 Apr 2026 20:16:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 15 Apr 2026 20:16:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 15 Apr 2026 20:16:18 GMT
ENV DOCKER_VERSION=29.4.0
# Wed, 15 Apr 2026 20:16:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 15 Apr 2026 20:16:18 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Wed, 15 Apr 2026 20:16:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 15 Apr 2026 20:16:20 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 15 Apr 2026 20:16:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 15 Apr 2026 20:16:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 15 Apr 2026 20:16:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:16:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Apr 2026 20:16:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 15 Apr 2026 20:16:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:16:22 GMT
CMD ["sh"]
# Wed, 15 Apr 2026 21:27:26 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 15 Apr 2026 21:27:28 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 15 Apr 2026 21:27:28 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 15 Apr 2026 21:27:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 15 Apr 2026 21:27:31 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 15 Apr 2026 21:27:31 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 15 Apr 2026 21:27:31 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:27:31 GMT
VOLUME [/var/lib/docker]
# Wed, 15 Apr 2026 21:27:31 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 15 Apr 2026 21:27:31 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 15 Apr 2026 21:27:31 GMT
CMD []
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88cb38943f0f0a95a9ef76158143c405f36bad50621b2fd56aa2fc4f3615fd5`  
		Last Modified: Wed, 15 Apr 2026 20:16:29 GMT  
		Size: 7.6 MB (7595768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaaca956ad170283b847286ec873bec980d796519baf3f39fe964aded5374f8e`  
		Last Modified: Wed, 15 Apr 2026 20:16:28 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cdf1c13c7d0f067c56c9771266f9895d1041ebf30f39ab27603e18afb0c9081`  
		Last Modified: Wed, 15 Apr 2026 20:16:29 GMT  
		Size: 18.1 MB (18096362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813eda9384408e479910e06a79744324e1dce0b63fd42e5bce661a6e735e2f32`  
		Last Modified: Wed, 15 Apr 2026 20:16:29 GMT  
		Size: 21.1 MB (21129758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f4b664cfcad12fa1a9762a191ac3534cf78c30dd9df6eff79f75e17bd604215`  
		Last Modified: Wed, 15 Apr 2026 20:16:30 GMT  
		Size: 10.4 MB (10371870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f3580f46ae276e11707530d3b18cc55414bcb1f7a672d3cef371193e0e0947`  
		Last Modified: Wed, 15 Apr 2026 20:16:30 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d214a288fe8f0a47169af907737952cefa9e61f078490a75828a439107530b2`  
		Last Modified: Wed, 15 Apr 2026 20:16:31 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf0d872d260394713b2443444bb53d508d83624734c0239dcda7ff1830303db8`  
		Last Modified: Wed, 15 Apr 2026 20:16:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89db5f2f3e615ce6454e5c1c42292805de5a924c4769cb726472a5f992eef448`  
		Last Modified: Wed, 15 Apr 2026 21:27:42 GMT  
		Size: 6.6 MB (6577217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a486198c8f3ba2ab5d5c0c2444157dbdb3a24ef48b6dcbe399e92e72a5e6c28`  
		Last Modified: Wed, 15 Apr 2026 21:27:42 GMT  
		Size: 88.0 KB (88036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba24e0fe682bf1faf33f78d5b19ecad454f21527c9a6c33cfb4c1d694b52779`  
		Last Modified: Wed, 15 Apr 2026 21:27:42 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ca224f3bf33d1172adfccf0c242f89893fde617bd5885ef7545ecd22e41ef4f`  
		Last Modified: Wed, 15 Apr 2026 21:27:44 GMT  
		Size: 63.4 MB (63443351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac3934cb427133bc539854b45e314e2dc44838a979414cf67dd89810b967f06`  
		Last Modified: Wed, 15 Apr 2026 21:27:43 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5e8455627c95fe22aa58fead7cbf2a0934fd4d57d760756577ec0b8c9bf4bc`  
		Last Modified: Wed, 15 Apr 2026 21:27:43 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:9376e04ebe10bd90bf0a7a85bddeb4c723ab3c8e9ae5290a6f522143cdbed03d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58ce25b3cedf687af0bcb158bb0a1d2a8523dfeadcddc68360fc3394f815f730`

```dockerfile
```

-	Layers:
	-	`sha256:ecdd6391528d66bfad436f41aef96daa292510a5ddd3f115f031dd1728b3dd36`  
		Last Modified: Wed, 15 Apr 2026 21:27:42 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:553d694bc3ae2a92b67b73072e3923a8d2256e609b568c60d08e4544e8f39ff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.1 MB (130126872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5c1c78f7262d1e00eef13317919dc25b6d65c96115e46f851ab09818f2ddf0b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:13:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 15 Apr 2026 20:13:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 15 Apr 2026 20:13:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 15 Apr 2026 20:14:02 GMT
ENV DOCKER_VERSION=29.4.0
# Wed, 15 Apr 2026 20:14:02 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 15 Apr 2026 20:14:02 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Wed, 15 Apr 2026 20:14:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 15 Apr 2026 20:14:03 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 15 Apr 2026 20:14:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 15 Apr 2026 20:14:04 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 15 Apr 2026 20:14:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:14:04 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Apr 2026 20:14:04 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 15 Apr 2026 20:14:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:14:04 GMT
CMD ["sh"]
# Wed, 15 Apr 2026 21:33:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 15 Apr 2026 21:33:18 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 15 Apr 2026 21:33:18 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 15 Apr 2026 21:33:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 15 Apr 2026 21:33:21 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 15 Apr 2026 21:33:21 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 15 Apr 2026 21:33:21 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:33:21 GMT
VOLUME [/var/lib/docker]
# Wed, 15 Apr 2026 21:33:21 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 15 Apr 2026 21:33:21 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 15 Apr 2026 21:33:21 GMT
CMD []
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1f08e8ea565813fe5c533f3bf89a6fcb79b8ef2eb46e2872f132234aa070cf`  
		Last Modified: Wed, 15 Apr 2026 20:14:10 GMT  
		Size: 8.5 MB (8450092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ff0f79f131dfea84e2ad6ee3723888525425bfc628525e86c3cc1b288bace3`  
		Last Modified: Wed, 15 Apr 2026 20:14:10 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35bf88d1a58dc1d9ced6e216552eef44b2392e515454985dcd3f25372d12693`  
		Last Modified: Wed, 15 Apr 2026 20:14:11 GMT  
		Size: 17.9 MB (17921079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0aa9505e9a0f5469b8905ecd253d1fd12569434350a1c94898126c02a4a9c57`  
		Last Modified: Wed, 15 Apr 2026 20:14:11 GMT  
		Size: 20.5 MB (20453111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ff9179479c44e683ee3838185f58e7d707974096437fdccedcb7b1f316aa35`  
		Last Modified: Wed, 15 Apr 2026 20:14:11 GMT  
		Size: 10.0 MB (9982600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0771ed595b2bb7d830d904c0ed7f259d39bb70d0da784d731a39f7a1ceeacb04`  
		Last Modified: Wed, 15 Apr 2026 20:14:12 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627cec3b548e33f50bcd1682915056d5dfd8e5b28476d6c4842c0eb790b1f954`  
		Last Modified: Wed, 15 Apr 2026 20:14:12 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c67b1b44bc81549ba5caf988b00dabcb0c2ca6cee73ef7d756e26b08b1028e`  
		Last Modified: Wed, 15 Apr 2026 20:14:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c169b754493e049763aeab1727fe430cecafcd9032c4389b3053958aebc360c9`  
		Last Modified: Wed, 15 Apr 2026 21:33:31 GMT  
		Size: 7.2 MB (7219816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbba1f41e162f643c431dbb55a4cfb94284235c55c0c226f2f85fdc2797d7d3`  
		Last Modified: Wed, 15 Apr 2026 21:33:30 GMT  
		Size: 101.2 KB (101171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc3e20cde46cbbd2b898524e10c8ed94082175c8c21daf98b34e7a6006aafee`  
		Last Modified: Wed, 15 Apr 2026 21:33:30 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ae4baf5361489e96a43c6d29d47fdd4eb63dd088b10e8bf91df746925678ea`  
		Last Modified: Wed, 15 Apr 2026 21:33:32 GMT  
		Size: 61.8 MB (61790985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7fa8aac1af219d886ca4026da0a5a043fde1dae9d3e8534dd78f23360b8763`  
		Last Modified: Wed, 15 Apr 2026 21:33:32 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f667dde4f795a12a4a9d7129f07e71678ffec2ae9a15d680f09fd672a64ab154`  
		Last Modified: Wed, 15 Apr 2026 21:33:32 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:71c18f631e3205680e2fcd0ea55f0f373c7fb19de8336794fe07f3d4793786b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48d9407668f8511b7b181ffcfea6ce22705df56aaf20a9dd84a0930f31f6ecf7`

```dockerfile
```

-	Layers:
	-	`sha256:623b2bc83b8d25632b5e152b95570ef2a7af85709fedfa2ae3ed9d312b61c77c`  
		Last Modified: Wed, 15 Apr 2026 21:33:30 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:windowsservercore`

```console
$ docker pull docker@sha256:d74502081e87e340ae439759f8ec2ea8904f7c6d482c2e01ef2d63e4eab78fce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32690; amd64
	-	windows version 10.0.20348.5020; amd64

### `docker:windowsservercore` - windows version 10.0.26100.32690; amd64

```console
$ docker pull docker@sha256:d46ee739eeb7f2f3919de6950a0c17a20bb1d22971380a4bb658f91004b6e533
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2185608492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:451cb635e20acafc0c39412eaf4ae9baa78105ff334cffab02ee607ff7e6d625`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Mon, 13 Apr 2026 07:00:46 GMT
RUN Install update 10.0.26100.32690
# Tue, 14 Apr 2026 21:01:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Apr 2026 21:02:06 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Apr 2026 21:02:07 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 14 Apr 2026 21:02:08 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.4.0.zip
# Tue, 14 Apr 2026 21:02:20 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 14 Apr 2026 21:02:20 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 14 Apr 2026 21:02:21 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.windows-amd64.exe
# Tue, 14 Apr 2026 21:02:21 GMT
ENV DOCKER_BUILDX_SHA256=832ddf42373203ee3836a7cb3b16fe5080231491e7edb32019ac0f6fe03b99ed
# Tue, 14 Apr 2026 21:02:35 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 14 Apr 2026 21:02:35 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 14 Apr 2026 21:02:36 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-windows-x86_64.exe
# Tue, 14 Apr 2026 21:02:37 GMT
ENV DOCKER_COMPOSE_SHA256=f7ad2f6965c88153e4902019ec86e95414f0025cba0b6440f328f935a1f8b12b
# Tue, 14 Apr 2026 21:02:43 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3642e4b8bb65ad3768f9f74a0dc48bb2e3294779b5d51573a234bfbe4f65324e`  
		Last Modified: Tue, 14 Apr 2026 18:48:19 GMT  
		Size: 606.9 MB (606926634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68ac02bb5872fbad22e76d99d54ab9b35a1e35759bbddff4f282081ba61100d5`  
		Last Modified: Tue, 14 Apr 2026 21:02:53 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774f3049f1ff5e124ea4f250ee1167ecf42896b3e9bcd067e2f4926ab7a0602d`  
		Last Modified: Tue, 14 Apr 2026 21:02:52 GMT  
		Size: 369.0 KB (368971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae8c2209515b42fd04e40e13a7bca32c3f1f16411393fc4cee562ca8f641bb7`  
		Last Modified: Tue, 14 Apr 2026 21:02:52 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3790546541b36e26bd73f9dfdaf940ebe9fe8013ff0a1cf891fba5e7701b36f`  
		Last Modified: Tue, 14 Apr 2026 21:02:51 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:445fc7e4e770e7d61fdf3492872b7e8bca998a26fffc4515e6344d6952d41f0f`  
		Last Modified: Tue, 14 Apr 2026 21:02:53 GMT  
		Size: 20.2 MB (20155911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b10e1a8a2bc350119623c441e4e0d952f69a7c50a192f764cb4e772b2359ea46`  
		Last Modified: Tue, 14 Apr 2026 21:02:50 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e015ae5429fcbb9151f7c03f83907b5d7d7e627e93ac5666dd54c102cf6f9909`  
		Last Modified: Tue, 14 Apr 2026 21:02:50 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ccf5f62308e0033a83afd116f4287e8951801b466ac66e960370bbd100b0c2b`  
		Last Modified: Tue, 14 Apr 2026 21:02:50 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:308fbcfb831872272d007db361ab5130df2705896b45ad22706bc3ed69a4208b`  
		Last Modified: Tue, 14 Apr 2026 21:02:52 GMT  
		Size: 23.4 MB (23435945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b688d291c4ee097cfa7d6bd989a5730f385d7ed44f7e307e89f8243f044db00a`  
		Last Modified: Tue, 14 Apr 2026 21:02:48 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:391e7d1ca3eae4c8c6acd6553f00297119056613a326ddae9eecb91f055806f4`  
		Last Modified: Tue, 14 Apr 2026 21:02:48 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebbf7aced575c80864697740f99f4f025250da7e7180003679632024cb1987f3`  
		Last Modified: Tue, 14 Apr 2026 21:02:48 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91a6dca9753cc712a25b48c9dbe9e9556c8e7bedfc0f97baf1d62b4cc5503798`  
		Last Modified: Tue, 14 Apr 2026 21:02:50 GMT  
		Size: 11.6 MB (11649820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.20348.5020; amd64

```console
$ docker pull docker@sha256:dfeb15b1635155bf333f2033fd733a796d52ede5fa96f898b11e57c12e2412a0
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2125867669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17085df04e58942536df91898016031a94b7bdce5841470b1904db146ee78bca`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Tue, 14 Apr 2026 20:56:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Apr 2026 20:56:45 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Apr 2026 20:56:47 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 14 Apr 2026 20:56:48 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.4.0.zip
# Tue, 14 Apr 2026 20:57:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 14 Apr 2026 20:57:06 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 14 Apr 2026 20:57:07 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.windows-amd64.exe
# Tue, 14 Apr 2026 20:57:08 GMT
ENV DOCKER_BUILDX_SHA256=832ddf42373203ee3836a7cb3b16fe5080231491e7edb32019ac0f6fe03b99ed
# Tue, 14 Apr 2026 20:57:26 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 14 Apr 2026 20:57:27 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 14 Apr 2026 20:57:27 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-windows-x86_64.exe
# Tue, 14 Apr 2026 20:57:28 GMT
ENV DOCKER_COMPOSE_SHA256=f7ad2f6965c88153e4902019ec86e95414f0025cba0b6440f328f935a1f8b12b
# Tue, 14 Apr 2026 20:57:41 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7111ae68f8961455d230dc12d44c2193d29b7c981e35417323613a0c1aa06384`  
		Last Modified: Tue, 14 Apr 2026 17:31:38 GMT  
		Size: 581.2 MB (581192160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4911c7412282b7f1d93fad64ba92d82b42d1ac47c62c4ff886b516f02ea28a55`  
		Last Modified: Tue, 14 Apr 2026 20:57:50 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:151b1d340c8ca7ccd1a0024ff46837779a87b23f90be4512b66ca317e849176b`  
		Last Modified: Tue, 14 Apr 2026 20:57:49 GMT  
		Size: 468.6 KB (468589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c05f9fed2a2861e1aad93076abf9515f202306cf4c6e381ac7b874a9c1d1196`  
		Last Modified: Tue, 14 Apr 2026 20:57:48 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c7405e2df63bc9fec89f85fb677309b86bf973025d8f6b08da62e988f2a629`  
		Last Modified: Tue, 14 Apr 2026 20:57:48 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7f5562b59f5d6e8946261211a66a4f3d8e26a59a704ca4ac6c6405a3ec5f055`  
		Last Modified: Tue, 14 Apr 2026 20:57:50 GMT  
		Size: 20.1 MB (20130256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6f3b1f33de25d313624bac12844dba1d78714061572c4a74d1fe93ad71ce9ad`  
		Last Modified: Tue, 14 Apr 2026 20:57:46 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b55352e1cad29fb0adf25f61e251a05aa1b8ddefb796d15d4793e871bfbaad`  
		Last Modified: Tue, 14 Apr 2026 20:57:47 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a54c516e756ba1351d4ab57988ca90f91af80ca4cce2b27e45eb8dd2ab1ac579`  
		Last Modified: Tue, 14 Apr 2026 20:57:46 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:935fbf8b04da4242e47da7bfee8df2b984a65ed241ffa13f675e09c528cabf8c`  
		Last Modified: Tue, 14 Apr 2026 20:57:54 GMT  
		Size: 23.4 MB (23419466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c62827bb4e356ec246f0a9426681e101860c87ca41a8081887faa7a911a04b19`  
		Last Modified: Tue, 14 Apr 2026 20:57:45 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:830e8d77d7ec0a09f8111f5d4fbe1b1bc385938ec59812da38a864323c7e4963`  
		Last Modified: Tue, 14 Apr 2026 20:57:45 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2405085b41ebd2fbc5a8f4683c3debadbd731eb6e54352fab4de5f2f74bc187d`  
		Last Modified: Tue, 14 Apr 2026 20:57:45 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5d8306d6e8e4e9eb43d89651b670cda922a16548c151c2bdbb51db4656787e6`  
		Last Modified: Tue, 14 Apr 2026 20:57:47 GMT  
		Size: 11.6 MB (11626371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:bba4a40903cac7bbfad1686d3aef377f0f7294e2311b9da2e962d1cf4526c500
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.5020; amd64

```console
$ docker pull docker@sha256:dfeb15b1635155bf333f2033fd733a796d52ede5fa96f898b11e57c12e2412a0
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2125867669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17085df04e58942536df91898016031a94b7bdce5841470b1904db146ee78bca`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Tue, 14 Apr 2026 20:56:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Apr 2026 20:56:45 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Apr 2026 20:56:47 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 14 Apr 2026 20:56:48 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.4.0.zip
# Tue, 14 Apr 2026 20:57:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 14 Apr 2026 20:57:06 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 14 Apr 2026 20:57:07 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.windows-amd64.exe
# Tue, 14 Apr 2026 20:57:08 GMT
ENV DOCKER_BUILDX_SHA256=832ddf42373203ee3836a7cb3b16fe5080231491e7edb32019ac0f6fe03b99ed
# Tue, 14 Apr 2026 20:57:26 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 14 Apr 2026 20:57:27 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 14 Apr 2026 20:57:27 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-windows-x86_64.exe
# Tue, 14 Apr 2026 20:57:28 GMT
ENV DOCKER_COMPOSE_SHA256=f7ad2f6965c88153e4902019ec86e95414f0025cba0b6440f328f935a1f8b12b
# Tue, 14 Apr 2026 20:57:41 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7111ae68f8961455d230dc12d44c2193d29b7c981e35417323613a0c1aa06384`  
		Last Modified: Tue, 14 Apr 2026 17:31:38 GMT  
		Size: 581.2 MB (581192160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4911c7412282b7f1d93fad64ba92d82b42d1ac47c62c4ff886b516f02ea28a55`  
		Last Modified: Tue, 14 Apr 2026 20:57:50 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:151b1d340c8ca7ccd1a0024ff46837779a87b23f90be4512b66ca317e849176b`  
		Last Modified: Tue, 14 Apr 2026 20:57:49 GMT  
		Size: 468.6 KB (468589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c05f9fed2a2861e1aad93076abf9515f202306cf4c6e381ac7b874a9c1d1196`  
		Last Modified: Tue, 14 Apr 2026 20:57:48 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c7405e2df63bc9fec89f85fb677309b86bf973025d8f6b08da62e988f2a629`  
		Last Modified: Tue, 14 Apr 2026 20:57:48 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7f5562b59f5d6e8946261211a66a4f3d8e26a59a704ca4ac6c6405a3ec5f055`  
		Last Modified: Tue, 14 Apr 2026 20:57:50 GMT  
		Size: 20.1 MB (20130256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6f3b1f33de25d313624bac12844dba1d78714061572c4a74d1fe93ad71ce9ad`  
		Last Modified: Tue, 14 Apr 2026 20:57:46 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b55352e1cad29fb0adf25f61e251a05aa1b8ddefb796d15d4793e871bfbaad`  
		Last Modified: Tue, 14 Apr 2026 20:57:47 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a54c516e756ba1351d4ab57988ca90f91af80ca4cce2b27e45eb8dd2ab1ac579`  
		Last Modified: Tue, 14 Apr 2026 20:57:46 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:935fbf8b04da4242e47da7bfee8df2b984a65ed241ffa13f675e09c528cabf8c`  
		Last Modified: Tue, 14 Apr 2026 20:57:54 GMT  
		Size: 23.4 MB (23419466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c62827bb4e356ec246f0a9426681e101860c87ca41a8081887faa7a911a04b19`  
		Last Modified: Tue, 14 Apr 2026 20:57:45 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:830e8d77d7ec0a09f8111f5d4fbe1b1bc385938ec59812da38a864323c7e4963`  
		Last Modified: Tue, 14 Apr 2026 20:57:45 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2405085b41ebd2fbc5a8f4683c3debadbd731eb6e54352fab4de5f2f74bc187d`  
		Last Modified: Tue, 14 Apr 2026 20:57:45 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5d8306d6e8e4e9eb43d89651b670cda922a16548c151c2bdbb51db4656787e6`  
		Last Modified: Tue, 14 Apr 2026 20:57:47 GMT  
		Size: 11.6 MB (11626371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:7453a45c03a9501b7dfb80e7846d848c74853c4eed947a7ea01ce577f840a92e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32690; amd64

### `docker:windowsservercore-ltsc2025` - windows version 10.0.26100.32690; amd64

```console
$ docker pull docker@sha256:d46ee739eeb7f2f3919de6950a0c17a20bb1d22971380a4bb658f91004b6e533
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2185608492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:451cb635e20acafc0c39412eaf4ae9baa78105ff334cffab02ee607ff7e6d625`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Mon, 13 Apr 2026 07:00:46 GMT
RUN Install update 10.0.26100.32690
# Tue, 14 Apr 2026 21:01:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Apr 2026 21:02:06 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Apr 2026 21:02:07 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 14 Apr 2026 21:02:08 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.4.0.zip
# Tue, 14 Apr 2026 21:02:20 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 14 Apr 2026 21:02:20 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 14 Apr 2026 21:02:21 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.windows-amd64.exe
# Tue, 14 Apr 2026 21:02:21 GMT
ENV DOCKER_BUILDX_SHA256=832ddf42373203ee3836a7cb3b16fe5080231491e7edb32019ac0f6fe03b99ed
# Tue, 14 Apr 2026 21:02:35 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 14 Apr 2026 21:02:35 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 14 Apr 2026 21:02:36 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-windows-x86_64.exe
# Tue, 14 Apr 2026 21:02:37 GMT
ENV DOCKER_COMPOSE_SHA256=f7ad2f6965c88153e4902019ec86e95414f0025cba0b6440f328f935a1f8b12b
# Tue, 14 Apr 2026 21:02:43 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3642e4b8bb65ad3768f9f74a0dc48bb2e3294779b5d51573a234bfbe4f65324e`  
		Last Modified: Tue, 14 Apr 2026 18:48:19 GMT  
		Size: 606.9 MB (606926634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68ac02bb5872fbad22e76d99d54ab9b35a1e35759bbddff4f282081ba61100d5`  
		Last Modified: Tue, 14 Apr 2026 21:02:53 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774f3049f1ff5e124ea4f250ee1167ecf42896b3e9bcd067e2f4926ab7a0602d`  
		Last Modified: Tue, 14 Apr 2026 21:02:52 GMT  
		Size: 369.0 KB (368971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae8c2209515b42fd04e40e13a7bca32c3f1f16411393fc4cee562ca8f641bb7`  
		Last Modified: Tue, 14 Apr 2026 21:02:52 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3790546541b36e26bd73f9dfdaf940ebe9fe8013ff0a1cf891fba5e7701b36f`  
		Last Modified: Tue, 14 Apr 2026 21:02:51 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:445fc7e4e770e7d61fdf3492872b7e8bca998a26fffc4515e6344d6952d41f0f`  
		Last Modified: Tue, 14 Apr 2026 21:02:53 GMT  
		Size: 20.2 MB (20155911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b10e1a8a2bc350119623c441e4e0d952f69a7c50a192f764cb4e772b2359ea46`  
		Last Modified: Tue, 14 Apr 2026 21:02:50 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e015ae5429fcbb9151f7c03f83907b5d7d7e627e93ac5666dd54c102cf6f9909`  
		Last Modified: Tue, 14 Apr 2026 21:02:50 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ccf5f62308e0033a83afd116f4287e8951801b466ac66e960370bbd100b0c2b`  
		Last Modified: Tue, 14 Apr 2026 21:02:50 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:308fbcfb831872272d007db361ab5130df2705896b45ad22706bc3ed69a4208b`  
		Last Modified: Tue, 14 Apr 2026 21:02:52 GMT  
		Size: 23.4 MB (23435945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b688d291c4ee097cfa7d6bd989a5730f385d7ed44f7e307e89f8243f044db00a`  
		Last Modified: Tue, 14 Apr 2026 21:02:48 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:391e7d1ca3eae4c8c6acd6553f00297119056613a326ddae9eecb91f055806f4`  
		Last Modified: Tue, 14 Apr 2026 21:02:48 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebbf7aced575c80864697740f99f4f025250da7e7180003679632024cb1987f3`  
		Last Modified: Tue, 14 Apr 2026 21:02:48 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91a6dca9753cc712a25b48c9dbe9e9556c8e7bedfc0f97baf1d62b4cc5503798`  
		Last Modified: Tue, 14 Apr 2026 21:02:50 GMT  
		Size: 11.6 MB (11649820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
