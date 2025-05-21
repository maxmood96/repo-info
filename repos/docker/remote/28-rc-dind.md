## `docker:28-rc-dind`

```console
$ docker pull docker@sha256:d1a5319e5fe3ea8ad73bb528cf25675e743f84491979a11911e4c5135d2809f2
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

### `docker:28-rc-dind` - linux; amd64

```console
$ docker pull docker@sha256:0e5a5e332b4cedd74daebc35c894ec7c09aceb00d44db664c939c60d44424c67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.3 MB (143302238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:899293a05ef9195e8c7e853c85b9ada242e964b5e5fe917ea9050a2df590db38`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 23:19:20 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 19 May 2025 23:19:20 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 19 May 2025 23:19:20 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 19 May 2025 23:19:20 GMT
ENV DOCKER_VERSION=28.2.0-rc.1
# Mon, 19 May 2025 23:19:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.2.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.2.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.2.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.2.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 19 May 2025 23:19:20 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Mon, 19 May 2025 23:19:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 19 May 2025 23:19:20 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.1
# Mon, 19 May 2025 23:19:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-x86_64'; 			sha256='8c410e789d3fa688201170a8efb52048ee0dcb0d4cde44ce92a1bb6949f49fcb'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-armv6'; 			sha256='4726dc002180e66122087c4b48bc58c78a7cb97c92811ff2100296c73a426222'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-armv7'; 			sha256='583299ca517b1d32cd9739b58e747770ce0e8a38cf72818d023fa5d6fb973098'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-aarch64'; 			sha256='a1ad63fe3f1feffb096df472bcd793e9635907a51e5861a0e0bf78b0c4fefa18'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-ppc64le'; 			sha256='7c208fb561bd5a7f79d16774b0b8f5c9da12f6dbe71601a8a40e4664da9ab822'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-riscv64'; 			sha256='c6de2c0d930ec37a4465ecb786aa59153fac518acbec37b5f92c23760fcb20a9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-s390x'; 			sha256='c06364ce6bcd14c2b8c7c595789249d2c041f0b79ff50f59356471f7fd938611'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 19 May 2025 23:19:20 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 19 May 2025 23:19:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 19 May 2025 23:19:20 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 19 May 2025 23:19:20 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 19 May 2025 23:19:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 19 May 2025 23:19:20 GMT
CMD ["sh"]
# Mon, 19 May 2025 23:19:20 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 19 May 2025 23:19:20 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 19 May 2025 23:19:20 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 19 May 2025 23:19:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.2.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.2.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.2.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.2.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 19 May 2025 23:19:20 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 19 May 2025 23:19:20 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 19 May 2025 23:19:20 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 19 May 2025 23:19:20 GMT
VOLUME [/var/lib/docker]
# Mon, 19 May 2025 23:19:20 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 19 May 2025 23:19:20 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 19 May 2025 23:19:20 GMT
CMD []
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51837d8ad19248820f2edf9b7be692ac6d3f79224261e893794928540cd1093a`  
		Last Modified: Wed, 21 May 2025 18:49:54 GMT  
		Size: 8.1 MB (8062909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdc12716d263c1854fba60a93b610acc1777ed00c64e724308ea5b003cb87ac3`  
		Last Modified: Wed, 21 May 2025 18:49:54 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ffdaa08d66d8c01d9a013e7c9475ff55c5869c1825f1e9b1389db8d61f8bdb6`  
		Last Modified: Wed, 21 May 2025 18:49:55 GMT  
		Size: 20.1 MB (20090873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434b626b2e853b9bd0c47469e4a7edc1700a7c5b004ab0fa0e33530c25d3df7f`  
		Last Modified: Wed, 21 May 2025 18:49:55 GMT  
		Size: 21.3 MB (21290151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d09a313cfcb7831bb7d8c542ceb6d27f5939243b1a569f8bd60fd4efda8359f`  
		Last Modified: Wed, 21 May 2025 18:49:56 GMT  
		Size: 21.2 MB (21208008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43b81363fb9f71d40d1d06dd23aa9a8b7141cc505e802fe9219ff8721eb3be30`  
		Last Modified: Wed, 21 May 2025 18:49:56 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0afa799a23cb992d26939280aca6c24494a91f64be379603c0fecace3f0751fe`  
		Last Modified: Wed, 21 May 2025 18:49:56 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102b51a23ac0aa4b570d00a7300e8bcd3726e1ca421b2e09b95370c0cd88942b`  
		Last Modified: Wed, 21 May 2025 18:49:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec657727d6ef8c71ffac6de547610f6e0e5c77020c45b7640e6935e45e68545`  
		Last Modified: Wed, 21 May 2025 19:05:09 GMT  
		Size: 6.7 MB (6732985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e2c6568839441edef62f72ceb2b33c532fcb0ccf7209a4f9509598874288243`  
		Last Modified: Wed, 21 May 2025 19:05:08 GMT  
		Size: 90.3 KB (90333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d508600607de2c2ca5ab8e82624d285445071d258c5110f197e82284afd925da`  
		Last Modified: Wed, 21 May 2025 19:05:09 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27d2522c24a8eec946fb17a600f14fdc7b097185e6768b6060ba98eca441e435`  
		Last Modified: Wed, 21 May 2025 19:05:10 GMT  
		Size: 62.2 MB (62176587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63ab0e7b3e589c9c3b3d24c894213d8759a6d3d0d73bb2939aadfd0db0948637`  
		Last Modified: Wed, 21 May 2025 19:05:09 GMT  
		Size: 1.7 KB (1686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a22f3831bbe8938f7e1128fd87babe0a31ceef6481e7c7572e911aafac7a8b`  
		Last Modified: Wed, 21 May 2025 19:05:09 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-rc-dind` - unknown; unknown

```console
$ docker pull docker@sha256:be009f1cc03536d6320b9736b8b459b5e3a6132d1505007dcea4173c430c8905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.1 KB (34115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fe14dd3adf0a7217a519d956a56b2403ec75de904dedaf1874dce5d6c9ad3b7`

```dockerfile
```

-	Layers:
	-	`sha256:fe5a5f8dc96d9b2f08aea0d97179f587b5bdbebeb7349e4ca8f0c547211758f4`  
		Last Modified: Wed, 21 May 2025 19:05:08 GMT  
		Size: 34.1 KB (34115 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-rc-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:7dfdcd8939e4f7bbc1230c5618f5ea756fdb4478650f1d3f81cbd904a03d4a95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.3 MB (134338101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b34e4fd60239203501c6ebb5c7c7e58766e10132dceae08c38c6f170c656e0c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 23:19:20 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 19 May 2025 23:19:20 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 19 May 2025 23:19:20 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 19 May 2025 23:19:20 GMT
ENV DOCKER_VERSION=28.2.0-rc.1
# Mon, 19 May 2025 23:19:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.2.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.2.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.2.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.2.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 19 May 2025 23:19:20 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Mon, 19 May 2025 23:19:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 19 May 2025 23:19:20 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.1
# Mon, 19 May 2025 23:19:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-x86_64'; 			sha256='8c410e789d3fa688201170a8efb52048ee0dcb0d4cde44ce92a1bb6949f49fcb'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-armv6'; 			sha256='4726dc002180e66122087c4b48bc58c78a7cb97c92811ff2100296c73a426222'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-armv7'; 			sha256='583299ca517b1d32cd9739b58e747770ce0e8a38cf72818d023fa5d6fb973098'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-aarch64'; 			sha256='a1ad63fe3f1feffb096df472bcd793e9635907a51e5861a0e0bf78b0c4fefa18'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-ppc64le'; 			sha256='7c208fb561bd5a7f79d16774b0b8f5c9da12f6dbe71601a8a40e4664da9ab822'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-riscv64'; 			sha256='c6de2c0d930ec37a4465ecb786aa59153fac518acbec37b5f92c23760fcb20a9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-s390x'; 			sha256='c06364ce6bcd14c2b8c7c595789249d2c041f0b79ff50f59356471f7fd938611'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 19 May 2025 23:19:20 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 19 May 2025 23:19:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 19 May 2025 23:19:20 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 19 May 2025 23:19:20 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 19 May 2025 23:19:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 19 May 2025 23:19:20 GMT
CMD ["sh"]
# Mon, 19 May 2025 23:19:20 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 19 May 2025 23:19:20 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 19 May 2025 23:19:20 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 19 May 2025 23:19:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.2.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.2.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.2.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.2.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 19 May 2025 23:19:20 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 19 May 2025 23:19:20 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 19 May 2025 23:19:20 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 19 May 2025 23:19:20 GMT
VOLUME [/var/lib/docker]
# Mon, 19 May 2025 23:19:20 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 19 May 2025 23:19:20 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 19 May 2025 23:19:20 GMT
CMD []
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e40b3641449ca47aef50c48f620eb6d3a3bc2292e5cf4ea267f5f03e6c7bc`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 8.0 MB (7978133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df16922f358c97f513c6d0b9457abb36aefc588e45374edd23692381878a7`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23da9b0b6e5db5763d752fbe340551b18f77636d702b049f2a7caa844165eea6`  
		Last Modified: Mon, 19 May 2025 23:45:43 GMT  
		Size: 18.1 MB (18102612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:748f70647eb147a91740c8bf7eb26c27af7ebc3464f67b5161b93e458ae0c7b1`  
		Last Modified: Wed, 21 May 2025 21:17:57 GMT  
		Size: 19.9 MB (19943305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a990be4fd91fe635384454a5c47e08ab81e709b51e10b25476690624aff1e72`  
		Last Modified: Wed, 21 May 2025 21:17:57 GMT  
		Size: 19.9 MB (19935934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ce428f605067c622b828a0e2d679e08f91c16f86c4aa638e384aaf2c046bf5`  
		Last Modified: Wed, 21 May 2025 21:17:56 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0838f3c98d2fd644d2f55abad5c127b816d60cba81887a4d5c015b85e94ede5`  
		Last Modified: Wed, 21 May 2025 21:17:56 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65acf5b95d797d91d24860817ecccab76dd2d00e2ec43d31257547cb557a299f`  
		Last Modified: Wed, 21 May 2025 21:17:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d911c7f01ac9436cd3baa214360ee68ae0f053681188c557b8d617fc16fb268`  
		Last Modified: Wed, 21 May 2025 22:07:32 GMT  
		Size: 7.0 MB (7036883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15534e1ac7b8efaf2245aee3a34bfc332b02478604b2071fb22934cdecafff08`  
		Last Modified: Wed, 21 May 2025 22:07:31 GMT  
		Size: 89.9 KB (89868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d187a0662a9deb878e33144e7160d29ba514ac6c105d45fa8723511568bb455f`  
		Last Modified: Wed, 21 May 2025 22:07:31 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e4c233c65df8264b30f0bb9c118be1cd50cb4b575bbed6bbb1090ac5bfd5603`  
		Last Modified: Wed, 21 May 2025 22:07:34 GMT  
		Size: 57.9 MB (57878452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499dec430412048cc122b01fbb63b2110fd3d6468c1aa2e147ee7fd89e79402c`  
		Last Modified: Wed, 21 May 2025 22:07:33 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c096692745d964c45c8232473c75cb69b80e7a7fc2ab3ec33d81967e803f6544`  
		Last Modified: Wed, 21 May 2025 22:07:33 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-rc-dind` - unknown; unknown

```console
$ docker pull docker@sha256:0196ee15efd4085da50ce11561f5b35abb8f4de4f0eeb8767f16e0c5909e36d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 KB (34275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89981031c1bd91cc9730dbc15b4a9714fbbbbe2c1ef4879b9ea6bcc1b8e82db7`

```dockerfile
```

-	Layers:
	-	`sha256:3b7558cd6ad83b927e011ff1482bde4fc46f86459e14da1505f51809f3886e80`  
		Last Modified: Wed, 21 May 2025 22:07:31 GMT  
		Size: 34.3 KB (34275 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-rc-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:1f459592d56801dc1146766192c60fc9ced9d59b06bf88dd3a244bcf20781378
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.7 MB (132680552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51f25992720fb3a950875f4c6868e5122d29cfac32909f613bcdfb5e8fc5456f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 23:19:20 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 19 May 2025 23:19:20 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 19 May 2025 23:19:20 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 19 May 2025 23:19:20 GMT
ENV DOCKER_VERSION=28.2.0-rc.1
# Mon, 19 May 2025 23:19:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.2.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.2.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.2.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.2.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 19 May 2025 23:19:20 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Mon, 19 May 2025 23:19:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 19 May 2025 23:19:20 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.1
# Mon, 19 May 2025 23:19:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-x86_64'; 			sha256='8c410e789d3fa688201170a8efb52048ee0dcb0d4cde44ce92a1bb6949f49fcb'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-armv6'; 			sha256='4726dc002180e66122087c4b48bc58c78a7cb97c92811ff2100296c73a426222'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-armv7'; 			sha256='583299ca517b1d32cd9739b58e747770ce0e8a38cf72818d023fa5d6fb973098'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-aarch64'; 			sha256='a1ad63fe3f1feffb096df472bcd793e9635907a51e5861a0e0bf78b0c4fefa18'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-ppc64le'; 			sha256='7c208fb561bd5a7f79d16774b0b8f5c9da12f6dbe71601a8a40e4664da9ab822'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-riscv64'; 			sha256='c6de2c0d930ec37a4465ecb786aa59153fac518acbec37b5f92c23760fcb20a9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-s390x'; 			sha256='c06364ce6bcd14c2b8c7c595789249d2c041f0b79ff50f59356471f7fd938611'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 19 May 2025 23:19:20 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 19 May 2025 23:19:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 19 May 2025 23:19:20 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 19 May 2025 23:19:20 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 19 May 2025 23:19:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 19 May 2025 23:19:20 GMT
CMD ["sh"]
# Mon, 19 May 2025 23:19:20 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 19 May 2025 23:19:20 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 19 May 2025 23:19:20 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 19 May 2025 23:19:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.2.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.2.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.2.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.2.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 19 May 2025 23:19:20 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 19 May 2025 23:19:20 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 19 May 2025 23:19:20 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 19 May 2025 23:19:20 GMT
VOLUME [/var/lib/docker]
# Mon, 19 May 2025 23:19:20 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 19 May 2025 23:19:20 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 19 May 2025 23:19:20 GMT
CMD []
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ecfb548efcbbbb086aaaaff202f8dcb75387c16103727c68404c07cf6c1e312`  
		Last Modified: Wed, 21 May 2025 21:25:26 GMT  
		Size: 7.3 MB (7301785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41df49181be4cc8df8bb77d160cf22a26623b599261a83cc6d25f4cff68ce237`  
		Last Modified: Wed, 21 May 2025 21:25:26 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c485d3051b351ec38603845abd871f14f9ad19a4a148663c3ed55eaad27d7cad`  
		Last Modified: Wed, 21 May 2025 21:25:27 GMT  
		Size: 18.1 MB (18091486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9b5b40bfe328582a25cf981b1df038e0bd3895b2df68f3cd2ec5477ac741cf`  
		Last Modified: Wed, 21 May 2025 21:25:28 GMT  
		Size: 19.9 MB (19927230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc42c2a918ccd0bc8d33c6a461e2ee31e177aecd79f3aacd47b9bea954c5b3b4`  
		Last Modified: Wed, 21 May 2025 21:25:28 GMT  
		Size: 19.9 MB (19922888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5595e8b989caddb545869c59098bdf10dda020193432cf29427a1dbf855dd293`  
		Last Modified: Wed, 21 May 2025 21:25:28 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c87d0a8b02d5bb4dbdadbe7c060943f9da1e1ab230ece33071f3bf6796d7d3bd`  
		Last Modified: Wed, 21 May 2025 21:25:29 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ea01fdc025a5fb28927b7bd80e3e3bf03e1d1f8115507c32170f3c861741ee`  
		Last Modified: Wed, 21 May 2025 21:25:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4621447f1c7b2ac54140690e663f7e20689df1517de17407a0fcb46e2f1cae62`  
		Last Modified: Wed, 21 May 2025 22:07:45 GMT  
		Size: 6.4 MB (6366107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:199b5f2c5d2fc7007a1d57f9b5c0393e86a0549172cedca8b2cc10a85e30b535`  
		Last Modified: Wed, 21 May 2025 22:07:45 GMT  
		Size: 86.3 KB (86350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91a0ca79793bb99f664e21c7508ea8288f473ae9cc06b23c121b5670fabd1fc7`  
		Last Modified: Wed, 21 May 2025 22:07:45 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb6b366cad84e39f00c247434028fcee0844d340ea72f4cb6846561a3ae319d0`  
		Last Modified: Wed, 21 May 2025 22:07:47 GMT  
		Size: 57.9 MB (57878432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5da01998e72cc6cce08f95d360036420e273e22f930047a6f31629df22a70f6`  
		Last Modified: Wed, 21 May 2025 22:07:46 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fcc18b166a1ddd827816bdb9887f32a0ca67be350e12cfda8cd91f46a623d5d`  
		Last Modified: Wed, 21 May 2025 22:07:46 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-rc-dind` - unknown; unknown

```console
$ docker pull docker@sha256:029eb1302462c8a9f2da68d91cbae57640b6ffe2ab1f56758996ac407f3d8a04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 KB (34274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e2b8dc748a33290d3f909c24e14065f4eed79b2cf2bcc92eeb9fb0f7bb99d41`

```dockerfile
```

-	Layers:
	-	`sha256:cd2eca0931c4825fcaef7c62ebee5cc4997efea38244c2dda073201f6a3e79ba`  
		Last Modified: Wed, 21 May 2025 22:07:44 GMT  
		Size: 34.3 KB (34274 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-rc-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:377f56d89d7cbe691f3c581c6282b141278f5d9a40e896376b9bf66d31af4c18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.1 MB (134102810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f1061f51558eb6cfe724f6f49bf6f6b6981c083050a37f77163d474f4b95d2f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 23:19:20 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 19 May 2025 23:19:20 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 19 May 2025 23:19:20 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 19 May 2025 23:19:20 GMT
ENV DOCKER_VERSION=28.2.0-rc.1
# Mon, 19 May 2025 23:19:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.2.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.2.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.2.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.2.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 19 May 2025 23:19:20 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Mon, 19 May 2025 23:19:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 19 May 2025 23:19:20 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.1
# Mon, 19 May 2025 23:19:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-x86_64'; 			sha256='8c410e789d3fa688201170a8efb52048ee0dcb0d4cde44ce92a1bb6949f49fcb'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-armv6'; 			sha256='4726dc002180e66122087c4b48bc58c78a7cb97c92811ff2100296c73a426222'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-armv7'; 			sha256='583299ca517b1d32cd9739b58e747770ce0e8a38cf72818d023fa5d6fb973098'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-aarch64'; 			sha256='a1ad63fe3f1feffb096df472bcd793e9635907a51e5861a0e0bf78b0c4fefa18'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-ppc64le'; 			sha256='7c208fb561bd5a7f79d16774b0b8f5c9da12f6dbe71601a8a40e4664da9ab822'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-riscv64'; 			sha256='c6de2c0d930ec37a4465ecb786aa59153fac518acbec37b5f92c23760fcb20a9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-s390x'; 			sha256='c06364ce6bcd14c2b8c7c595789249d2c041f0b79ff50f59356471f7fd938611'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 19 May 2025 23:19:20 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 19 May 2025 23:19:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 19 May 2025 23:19:20 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 19 May 2025 23:19:20 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 19 May 2025 23:19:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 19 May 2025 23:19:20 GMT
CMD ["sh"]
# Mon, 19 May 2025 23:19:20 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 19 May 2025 23:19:20 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 19 May 2025 23:19:20 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 19 May 2025 23:19:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.2.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.2.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.2.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.2.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 19 May 2025 23:19:20 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 19 May 2025 23:19:20 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 19 May 2025 23:19:20 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 19 May 2025 23:19:20 GMT
VOLUME [/var/lib/docker]
# Mon, 19 May 2025 23:19:20 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 19 May 2025 23:19:20 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 19 May 2025 23:19:20 GMT
CMD []
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b618038d9435f5b89cad9da67abac3afab969c8a745d6eb5341959c5fa82ea6`  
		Last Modified: Wed, 21 May 2025 20:06:22 GMT  
		Size: 8.1 MB (8077235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b60745a14fff8d357868c569dedf32326e427c7dfdccad542945eb14a52247`  
		Last Modified: Wed, 21 May 2025 20:06:21 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adacfb828377bb616efd5d4ddd35d0bec22d61686dbec2b2a03df699adc7b1e2`  
		Last Modified: Wed, 21 May 2025 20:06:22 GMT  
		Size: 18.9 MB (18910994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76666b2c1651e42759d47b748680ce07a9d2e69f78de7ac55b4b0e42aaf854c`  
		Last Modified: Wed, 21 May 2025 20:06:22 GMT  
		Size: 19.5 MB (19469844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61b55412e11f646e93277edd843929b43af20259e80fa8d369a67398207f3237`  
		Last Modified: Wed, 21 May 2025 20:06:23 GMT  
		Size: 19.4 MB (19433940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbd0f66b27f31f9db9278fcbd37f755fcd7cc4dcf0ad3835d203b904807d3066`  
		Last Modified: Wed, 21 May 2025 20:06:23 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375446c722fd562400775354a3bed0663e5fc24e03d883e4b426d66082486824`  
		Last Modified: Wed, 21 May 2025 20:06:23 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1939d03f63355453c2971d66e1762ce2718e5d23dbff99d77b793b077d44b1`  
		Last Modified: Wed, 21 May 2025 20:06:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c298fe92d330f6a0b6cc8ff2bcc46e3e12aa29b0de2bbd3e994ac3a3c35c921`  
		Last Modified: Wed, 21 May 2025 21:00:58 GMT  
		Size: 7.0 MB (6978927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:903df33f232f961539f35fa69f26801d7e69b0bb78bb17a33af83ad787200778`  
		Last Modified: Wed, 21 May 2025 21:00:58 GMT  
		Size: 99.4 KB (99403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4822839219310c01693becf6e3780ad8b80f2de5eaab1c5a5a50d642fb91cff`  
		Last Modified: Wed, 21 May 2025 21:00:58 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f92f7968803b452163020eda6b6330f6084adad1f5bcf59ef1acbdf5c9aba0f`  
		Last Modified: Wed, 21 May 2025 21:01:00 GMT  
		Size: 57.1 MB (57131289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202d3e2e6fc569fb48ce56ccffc71478034bd16ed5d4c8ed749bda73363b425d`  
		Last Modified: Wed, 21 May 2025 21:00:59 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0d6cf7da7e06b5b08d179914ad2de6e8516973c10d2bf46fdafcbbcf606911`  
		Last Modified: Wed, 21 May 2025 21:00:59 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-rc-dind` - unknown; unknown

```console
$ docker pull docker@sha256:d836bdfdaadad7fc117a99e2ce8c9aa86a7c63d555786bcd53b3546b0668bf5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 KB (34327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e9ed10c13352741c32423ad6c6d36a9103530b7f826d74f8bc37b6c5843d56a`

```dockerfile
```

-	Layers:
	-	`sha256:d4cd8e95a0a7de8463c0e3b6177d43faf270cd09fe991e2b540699a6a9a9dc97`  
		Last Modified: Wed, 21 May 2025 21:00:57 GMT  
		Size: 34.3 KB (34327 bytes)  
		MIME: application/vnd.in-toto+json
