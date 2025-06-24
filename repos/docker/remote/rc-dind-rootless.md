## `docker:rc-dind-rootless`

```console
$ docker pull docker@sha256:93557dd83c1fca9894752766b534038c1fdb805a697dcfee6265429b3ad6d5d3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:rc-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:1f1a558a7ae71271915c28d7bc1782d7830c6c17694ef460cad62c4cec059a23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.5 MB (163484650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33d3b0658003aff2d90af84a1734030926b25013cbf399d940155c53bb117183`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 23 Jun 2025 17:04:23 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
ENV DOCKER_VERSION=28.3.0-rc.2
# Mon, 23 Jun 2025 17:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.3.0-rc.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.3.0-rc.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.3.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.3.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Mon, 23 Jun 2025 17:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.2
# Mon, 23 Jun 2025 17:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-x86_64'; 			sha256='95db7bb2ed5d5fc790a12559b9092d641637c2d0190939c282b52a7af572a8a7'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-armv6'; 			sha256='863412d376cb1341e2a6889aa58dc4b674a58350ceccc357c71284109a5cb4a2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-armv7'; 			sha256='33aa26709150e835992a8af58d590e32151473f78daea549ccd70bd5f96c3bbf'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-aarch64'; 			sha256='d2c195cf553e55d06761c192133a6a7b4d67d275c7f5ce673bbf8ecf20814061'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-ppc64le'; 			sha256='6c72243b9585cc741c8e90937fd28ca2c8f2fee8a7636b30d1bbf312df27e157'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-riscv64'; 			sha256='8448828a5fa46170b92fec62d928b753ba91e86cccace24a04187324b65836ac'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-s390x'; 			sha256='39d47d8aa2cec059b4dc5e9b627a1176bcce33d9090f237806cf59264fe55e89'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Jun 2025 17:04:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Jun 2025 17:04:23 GMT
CMD ["sh"]
# Mon, 23 Jun 2025 17:04:23 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.3.0-rc.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.3.0-rc.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.3.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.3.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 23 Jun 2025 17:04:23 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
VOLUME [/var/lib/docker]
# Mon, 23 Jun 2025 17:04:23 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 23 Jun 2025 17:04:23 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 23 Jun 2025 17:04:23 GMT
CMD []
# Mon, 23 Jun 2025 17:04:23 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-28.3.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-28.3.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 23 Jun 2025 17:04:23 GMT
USER rootless
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc9d79f8211ca5f0ae319dd670ed871de8854629c84d10d10a509a74ea71a120`  
		Last Modified: Mon, 23 Jun 2025 22:43:37 GMT  
		Size: 8.2 MB (8207450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25dd1c3fe042ef8c0b31892371d122ab71a3531aac39c36990641881d5c775ff`  
		Last Modified: Mon, 23 Jun 2025 22:27:06 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:491a95b3e7e4594569a69d79611329fd849b4550a78887833d19b66878adefe3`  
		Last Modified: Mon, 23 Jun 2025 22:43:37 GMT  
		Size: 20.5 MB (20460214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2052eec1fcdfd51e52eb33466259175cb3754349653c558b4da839ad60857c2`  
		Last Modified: Mon, 23 Jun 2025 22:43:37 GMT  
		Size: 21.7 MB (21664161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2891f97182d20dcefb7f871b1bd7780ce831bc5c005bb1dc44c9f2da5e671f6`  
		Last Modified: Mon, 23 Jun 2025 22:43:36 GMT  
		Size: 21.3 MB (21253077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ac2a2bd86dee4e9a6511d9fc00935fb504452c468892b5a6b6639048eb8579`  
		Last Modified: Mon, 23 Jun 2025 22:17:52 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9334a663f6014177b797e46f1ac25aeac8622400c2284a31f2490cac85fe1f8`  
		Last Modified: Mon, 23 Jun 2025 22:17:55 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d7f75badbcca98d88f6930538405d39877707cb617b5517d2f8d8a101e2e07`  
		Last Modified: Mon, 23 Jun 2025 22:27:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2002e5ae7ab5bd5595ce107240a2cd01c8563e6fb6543d152a56d202c51b530a`  
		Last Modified: Mon, 23 Jun 2025 22:44:10 GMT  
		Size: 6.9 MB (6905600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0ad049ac5293d9cc9a11c9e24e85b82ab2123b6bed32bc8bdb6e4be0a3940c`  
		Last Modified: Mon, 23 Jun 2025 22:44:08 GMT  
		Size: 90.5 KB (90488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f77a4e0753f4d3270a18ea0458d3bed19d8d6a45b29015d28c6b95e3294376`  
		Last Modified: Mon, 23 Jun 2025 22:44:05 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a316315461878a581c80b6fe1cf972b08011a9d5e482a53f0d7c8549c88852d8`  
		Last Modified: Mon, 23 Jun 2025 22:44:09 GMT  
		Size: 62.5 MB (62517892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e55e6d33f75a1edf5836106d664229284ad0ac1b044cbb6b1f4d089d4ece12a`  
		Last Modified: Mon, 23 Jun 2025 22:44:05 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06307480ab5438e5d4e4db6eb14251ff0a849a6ef8f753dd9def458aff92fdb7`  
		Last Modified: Mon, 23 Jun 2025 22:44:05 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f89db96f72c2002b1f1ce8580245c041e401818cfba19457323099fdc52561`  
		Last Modified: Mon, 23 Jun 2025 23:17:40 GMT  
		Size: 993.3 KB (993271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91e3c8b5696771263fee8deae5d8ae56d1b48321a2b291a27d07825c9bd96bb`  
		Last Modified: Mon, 23 Jun 2025 23:17:45 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a400ceabafc97bcb10c9305f28241181bf233c956da9c1094a77faa2f0dbec`  
		Last Modified: Mon, 23 Jun 2025 23:17:49 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33690d7c5fc480a56f5f5985c2f90cd08d15455815f44bc70258e03c9e28fc9c`  
		Last Modified: Tue, 24 Jun 2025 02:07:58 GMT  
		Size: 17.6 MB (17586164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:000214e05b106ddebb7ba7a82eb0254b9cc4d6a8f7f0642a853df9777988705a`  
		Last Modified: Mon, 23 Jun 2025 23:17:53 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:3566bc1426afd8e9f2ff176769273b61f3fcb2b3d29c04aa8cef5f17c9adcb04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 KB (30204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83f4cd2d101d8cec1ab4aeeb74b683f3f0213a41987103912b40306efd567c7d`

```dockerfile
```

-	Layers:
	-	`sha256:84baa9b96f7dd721e9f7ce4d444e5c92814bd8f46df56faab4f7c4cb6ca86f10`  
		Last Modified: Tue, 24 Jun 2025 02:07:44 GMT  
		Size: 30.2 KB (30204 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:594f1d375cc1e635e3a24c2422877e14df9f0761bf03a6b1b59cba43c62bd069
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.7 MB (154690715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14549b1c321677fbd59adc31e661c3b26b0a9faeca064e0cbf0785ee36173c19`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 23 Jun 2025 17:04:23 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
ENV DOCKER_VERSION=28.3.0-rc.2
# Mon, 23 Jun 2025 17:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.3.0-rc.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.3.0-rc.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.3.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.3.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Mon, 23 Jun 2025 17:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.2
# Mon, 23 Jun 2025 17:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-x86_64'; 			sha256='95db7bb2ed5d5fc790a12559b9092d641637c2d0190939c282b52a7af572a8a7'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-armv6'; 			sha256='863412d376cb1341e2a6889aa58dc4b674a58350ceccc357c71284109a5cb4a2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-armv7'; 			sha256='33aa26709150e835992a8af58d590e32151473f78daea549ccd70bd5f96c3bbf'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-aarch64'; 			sha256='d2c195cf553e55d06761c192133a6a7b4d67d275c7f5ce673bbf8ecf20814061'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-ppc64le'; 			sha256='6c72243b9585cc741c8e90937fd28ca2c8f2fee8a7636b30d1bbf312df27e157'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-riscv64'; 			sha256='8448828a5fa46170b92fec62d928b753ba91e86cccace24a04187324b65836ac'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-s390x'; 			sha256='39d47d8aa2cec059b4dc5e9b627a1176bcce33d9090f237806cf59264fe55e89'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Jun 2025 17:04:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Jun 2025 17:04:23 GMT
CMD ["sh"]
# Mon, 23 Jun 2025 17:04:23 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.3.0-rc.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.3.0-rc.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.3.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.3.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 23 Jun 2025 17:04:23 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
VOLUME [/var/lib/docker]
# Mon, 23 Jun 2025 17:04:23 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 23 Jun 2025 17:04:23 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 23 Jun 2025 17:04:23 GMT
CMD []
# Mon, 23 Jun 2025 17:04:23 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-28.3.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-28.3.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 23 Jun 2025 17:04:23 GMT
USER rootless
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97387c91ee3c7373fcee444a1b646ca70965b590344120d317908c147a2b1ca`  
		Last Modified: Mon, 23 Jun 2025 22:17:14 GMT  
		Size: 8.2 MB (8229009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23dd6fd942c69d848277a60172548feb0fa2621741c486ffbfea35c861a0b6ba`  
		Last Modified: Mon, 23 Jun 2025 22:17:12 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a2fae78b07b72b55406cc9af117544dab46fca428d0a5bba5b14d8a585838ff`  
		Last Modified: Mon, 23 Jun 2025 22:17:14 GMT  
		Size: 19.3 MB (19267905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b8bce1b6cf15a61d47b8888b5714ea47d844d46c355a5f154f7735d18603c24`  
		Last Modified: Mon, 23 Jun 2025 22:17:14 GMT  
		Size: 19.8 MB (19819446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beab20993d24bc858c2c5a5172f2996980b66aed8d0e004cfdcf056df6f33694`  
		Last Modified: Mon, 23 Jun 2025 22:17:14 GMT  
		Size: 19.5 MB (19486789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2af553b5792cc05d1e2713d1fcd588572300a08ab5a0be3403423b3ba1c97b84`  
		Last Modified: Mon, 23 Jun 2025 22:17:13 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133afbf723fb46838c04b12d78546b52fa59100bdf4d900b0d0a20f645b578db`  
		Last Modified: Mon, 23 Jun 2025 22:17:13 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9dec9abfd3cc049bc95f125f1a628efbba68a7450da771ee5a217c0860379e8`  
		Last Modified: Mon, 23 Jun 2025 22:17:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:552cbafa6d19750d9cc475a54f9765c6d4c261e92f187968e27f59755584bbf8`  
		Last Modified: Mon, 23 Jun 2025 23:07:19 GMT  
		Size: 7.1 MB (7141630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9daf477bc8c04f0b7f19e056655fa919cd3bf060947e669bd31cde28b0378d01`  
		Last Modified: Mon, 23 Jun 2025 22:46:35 GMT  
		Size: 99.6 KB (99637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:264ce81b6525650a5f999d343a1d0bc3c606036184038bc9bd3d8187acb64431`  
		Last Modified: Mon, 23 Jun 2025 22:46:38 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4280f861bedf24b7ddca6cec49e20fc4acaeb923f21bbfd309af87445a1e67e`  
		Last Modified: Mon, 23 Jun 2025 23:07:22 GMT  
		Size: 57.5 MB (57460541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db53ac3d4ea28151984d66521638255640eeb23332d8b7d0025a0ec067ccf72`  
		Last Modified: Mon, 23 Jun 2025 22:46:41 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e968deecec6fe225163e0a3bd14094bcb740fc40f93e912810fd2f4db554b4b7`  
		Last Modified: Mon, 23 Jun 2025 22:46:44 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bde36de6f01bb8f899fef77286c21f3eea10e436e93146d5b81057ce3aeadd4d`  
		Last Modified: Mon, 23 Jun 2025 23:18:14 GMT  
		Size: 1.0 MB (1023003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb3d8e5391eeb8261e6e54396fc0febc367cec9803589dbdcaffef3cf98145d`  
		Last Modified: Mon, 23 Jun 2025 23:18:21 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3a324e3289ad24abd7d499bbd7addce08cc8936a2d7cd906fa1b050caa6b73e`  
		Last Modified: Mon, 23 Jun 2025 23:18:24 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af66ff9dad50a4c60e5877c92769860ad705e56bfca9c16fbc8b502c7032f823`  
		Last Modified: Tue, 24 Jun 2025 02:08:00 GMT  
		Size: 18.0 MB (18017322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db558a320a93f7ade4928febb7d664e5c86f9d965dbc67d8493fc078d50fa068`  
		Last Modified: Mon, 23 Jun 2025 23:18:28 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:b77bffa13cd431193d7e4a41d05b33fca6b50cbc98202c8edf25a07a8570dc52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.4 KB (30361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1a0070221488fe21129b8d23ac5b370512081d0e0cd8142432545b02a435636`

```dockerfile
```

-	Layers:
	-	`sha256:fb63373e5b6e9f81fa13f7252a50d8305b4f72e908a4a957296b1308bf4b99b2`  
		Last Modified: Tue, 24 Jun 2025 02:07:48 GMT  
		Size: 30.4 KB (30361 bytes)  
		MIME: application/vnd.in-toto+json
