## `docker:24-dind`

```console
$ docker pull docker@sha256:8d19938b3a838f2e72128897063971858035035e62dd03586e29783b3908cb60
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

### `docker:24-dind` - linux; amd64

```console
$ docker pull docker@sha256:7745d3274e18edfffdae023044d0b8d8a69753c09b8ed789e93dc4cc6a301cbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.4 MB (126358407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19945dc03a22efdf6b7737fb3b6fc278a193e6837158032c88fcd3467858280e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 19 Jun 2024 00:17:01 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Wed, 19 Jun 2024 00:17:01 GMT
CMD ["/bin/sh"]
# Wed, 19 Jun 2024 00:17:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
ENV DOCKER_VERSION=24.0.9
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.9.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
ENV DOCKER_BUILDX_VERSION=0.15.1
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-amd64'; 			sha256='8d486f0088b7407a90ad675525ba4a17d0a537741b9b33fe3391a88cafa2dd0b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm-v6'; 			sha256='b4d1c41605b50b5549f1464461cfa72d010106bfb4606b45cc776daab4c25d7d'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm-v7'; 			sha256='eabc32a4a86f943c3996eb2df5efd0d02d12603e356941ed46c132c64cbcbcdf'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm64'; 			sha256='13f4ffd2b6922e941d6b6a9faee73ec9b8cab5b309ef90dfadf48142c2a47f34'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-ppc64le'; 			sha256='6b41769526c9102d2352ed6900de33ee4be2eaf1927cfb216cc832c718e5c990'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-riscv64'; 			sha256='52f5a974d8d1eb88d1defe0da5173d39df3608e554c3dcd1d45bde77c3d697f3'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-s390x'; 			sha256='689c88555c42708ac812e3063590f8681b675d7f2ca68c024299ec388963615d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
ENV DOCKER_COMPOSE_VERSION=2.28.1
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-x86_64'; 			sha256='5b480d4f9e3517b375f0fbb781b39c63cec934f44b13c43b8f1d0f22bf6de8c3'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-armv6'; 			sha256='ff366f16854e8febcdce21b750f6462abdcaa16209be490feaa8c2dd88b7884c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-armv7'; 			sha256='d829c0d3f85885ee29fcaf19d2b6001215820ad874a0b9cdc3172965acb80c50'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-aarch64'; 			sha256='1ce6f9842b10ee5f61218a62f3acfc5839a31cd6daa6e87e926bef63dd9fee20'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-ppc64le'; 			sha256='c02e6b718e94df66cd0a53349d6487dbc6da99aa582c0b9906637964ecd9bd15'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-riscv64'; 			sha256='9d5d8033a8cf3deb05c7a9ee7cdf0086cc24a526fa9a10b4a778cc9124f5ef25'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-s390x'; 			sha256='c8ac20d8fac6d982a83e3b5bb34cda5ac326fbfde9b43c64a290258a1d7fbb38'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 19 Jun 2024 00:17:01 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 19 Jun 2024 00:17:01 GMT
CMD ["sh"]
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.9.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
VOLUME [/var/lib/docker]
# Wed, 19 Jun 2024 00:17:01 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 19 Jun 2024 00:17:01 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 19 Jun 2024 00:17:01 GMT
CMD []
```

-	Layers:
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b3c8f86d8adf8a26bb880d3e31e18207d9772274804b4c8f33f38ca1de838c`  
		Last Modified: Mon, 24 Jun 2024 22:56:18 GMT  
		Size: 2.0 MB (2010471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1cc629b0ad4e4666bd6e43c4e6181ab51861d7ede28ab34559d4eb705c6a6e5`  
		Last Modified: Mon, 24 Jun 2024 22:56:18 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10744d7f8d2404d132a5e38b2067cc6cf05c19500655490758e5861dad332f2a`  
		Last Modified: Mon, 24 Jun 2024 22:56:19 GMT  
		Size: 16.4 MB (16410681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5dd789b2f44d9592fbc7dcdd7eda2509453194650afe33a81820998176cf22a`  
		Last Modified: Mon, 24 Jun 2024 22:56:19 GMT  
		Size: 18.2 MB (18178850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97b81ff04e451536c5028910c061de265700661f687d2ba607f5570e8faa43e`  
		Last Modified: Mon, 24 Jun 2024 22:56:20 GMT  
		Size: 18.8 MB (18792449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b5ffd5bcc48c457d09eddb28ce54d17121f05152add59ab4fc0a84b8dda2854`  
		Last Modified: Mon, 24 Jun 2024 22:56:19 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:220f0b582311cde04f4db7f9978c73f0669ced8e372b8c4681136236eb3e6964`  
		Last Modified: Mon, 24 Jun 2024 22:56:20 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1504b542afd2d44b747a6e504a4f75cfe636e3e4ee94caedfa572c60abfafe38`  
		Last Modified: Mon, 24 Jun 2024 22:56:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5037fee7d1d135b90bb4b1378c28324ba6690c89086c3c47d0f224b08beb5c5d`  
		Last Modified: Mon, 24 Jun 2024 23:57:56 GMT  
		Size: 12.5 MB (12504444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e61f9e852c05f320d7791e1478f62a9614af9201387892b536deecf24f4635b`  
		Last Modified: Mon, 24 Jun 2024 23:57:56 GMT  
		Size: 89.2 KB (89189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa5557ab215eed160a7e191eac54acf84438b47a382d5e52bb508450d623872e`  
		Last Modified: Mon, 24 Jun 2024 23:57:56 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c991fa10ea96f531ff2b5a8d83d142ab7925783545dad8d1ea343a87fc8f15e4`  
		Last Modified: Mon, 24 Jun 2024 23:57:57 GMT  
		Size: 54.7 MB (54740518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c9cbecceca108ece60a448930899f80ae2b1d61ef7558f2c458e2de7d0f6c95`  
		Last Modified: Mon, 24 Jun 2024 23:57:56 GMT  
		Size: 1.5 KB (1509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bd915a3bcb61b3b6fbf47c6d3b6a0c0a3fc69dfe6005984357f3ae382364e09`  
		Last Modified: Mon, 24 Jun 2024 23:57:56 GMT  
		Size: 3.3 KB (3262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:24-dind` - unknown; unknown

```console
$ docker pull docker@sha256:30ae28a4d5b38aaa75990b05977b19aa3024568712c9a46094dc25575be4d156
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b52aaed0e921e10dc6f398a92dfc1eb3785a37b705518c553af7c6099d5c57c`

```dockerfile
```

-	Layers:
	-	`sha256:64b797b77a1fb83157e724c772d283318398dad4d44e2649dac7e691ae09c341`  
		Last Modified: Mon, 24 Jun 2024 23:57:55 GMT  
		Size: 34.8 KB (34835 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:24-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:1e5e6b691381d8012b7cd193ec3df17f4c7f380ecdd463ce942c9c545fdaf89c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.4 MB (119437765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70209e2d0852de70afc34e31ad1e162f5196722f117f7c36a1a431e1480409cc`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 19 Jun 2024 00:17:01 GMT
ADD file:ef2635f09c1d2632408805d106fbc5d27fb307cb5f584bddc699b4b5ae577623 in / 
# Wed, 19 Jun 2024 00:17:01 GMT
CMD ["/bin/sh"]
# Wed, 19 Jun 2024 00:17:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
ENV DOCKER_VERSION=24.0.9
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.9.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
ENV DOCKER_BUILDX_VERSION=0.15.1
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-amd64'; 			sha256='8d486f0088b7407a90ad675525ba4a17d0a537741b9b33fe3391a88cafa2dd0b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm-v6'; 			sha256='b4d1c41605b50b5549f1464461cfa72d010106bfb4606b45cc776daab4c25d7d'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm-v7'; 			sha256='eabc32a4a86f943c3996eb2df5efd0d02d12603e356941ed46c132c64cbcbcdf'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm64'; 			sha256='13f4ffd2b6922e941d6b6a9faee73ec9b8cab5b309ef90dfadf48142c2a47f34'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-ppc64le'; 			sha256='6b41769526c9102d2352ed6900de33ee4be2eaf1927cfb216cc832c718e5c990'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-riscv64'; 			sha256='52f5a974d8d1eb88d1defe0da5173d39df3608e554c3dcd1d45bde77c3d697f3'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-s390x'; 			sha256='689c88555c42708ac812e3063590f8681b675d7f2ca68c024299ec388963615d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
ENV DOCKER_COMPOSE_VERSION=2.28.1
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-x86_64'; 			sha256='5b480d4f9e3517b375f0fbb781b39c63cec934f44b13c43b8f1d0f22bf6de8c3'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-armv6'; 			sha256='ff366f16854e8febcdce21b750f6462abdcaa16209be490feaa8c2dd88b7884c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-armv7'; 			sha256='d829c0d3f85885ee29fcaf19d2b6001215820ad874a0b9cdc3172965acb80c50'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-aarch64'; 			sha256='1ce6f9842b10ee5f61218a62f3acfc5839a31cd6daa6e87e926bef63dd9fee20'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-ppc64le'; 			sha256='c02e6b718e94df66cd0a53349d6487dbc6da99aa582c0b9906637964ecd9bd15'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-riscv64'; 			sha256='9d5d8033a8cf3deb05c7a9ee7cdf0086cc24a526fa9a10b4a778cc9124f5ef25'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-s390x'; 			sha256='c8ac20d8fac6d982a83e3b5bb34cda5ac326fbfde9b43c64a290258a1d7fbb38'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 19 Jun 2024 00:17:01 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 19 Jun 2024 00:17:01 GMT
CMD ["sh"]
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.9.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
VOLUME [/var/lib/docker]
# Wed, 19 Jun 2024 00:17:01 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 19 Jun 2024 00:17:01 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 19 Jun 2024 00:17:01 GMT
CMD []
```

-	Layers:
	-	`sha256:3d2af5f613c84e549fb09710d45b152d3cdf48eb7a37dc3e9c01e2b3975f4f76`  
		Last Modified: Thu, 20 Jun 2024 17:49:36 GMT  
		Size: 3.4 MB (3367154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d023b0d86d5f3c29ffac412805754ac7366e4ecc23c5177010d36847ad55a7`  
		Last Modified: Mon, 24 Jun 2024 16:53:24 GMT  
		Size: 2.0 MB (1993299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d6b44884f2fa15c4e561076223287af9c44c7cc4621122e79f252f814684c3`  
		Last Modified: Mon, 24 Jun 2024 16:53:23 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a488a320d44fd6dcc431783dcdb960b4d61148f58b93d4be251db2ef52f35cad`  
		Last Modified: Mon, 24 Jun 2024 16:54:58 GMT  
		Size: 15.1 MB (15132944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5c86afc22d0c51830d940cf48b7528f71c7a4def4ccdd9d673bcc12744a7f8a`  
		Last Modified: Mon, 24 Jun 2024 16:54:58 GMT  
		Size: 17.0 MB (17010827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:086c5639f2e194ca3a4a789a048295abc8359a383e26b94e7d09c353fbf76cf1`  
		Last Modified: Mon, 24 Jun 2024 23:38:55 GMT  
		Size: 17.8 MB (17751796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93f0e45f66f2a4c71856004592cbb5bdb62b6832c7d5e22fd56d6bbc1220832`  
		Last Modified: Mon, 24 Jun 2024 23:38:54 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fefa8552442c53cbe81c6f11803f7aa4e025e407fb8b76d876f690ecd19a80a`  
		Last Modified: Mon, 24 Jun 2024 23:38:54 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f19f439d49c3f370ea773478bf41bdb6e6b5fa3a56e81b55ee5247b7cd78272`  
		Last Modified: Mon, 24 Jun 2024 23:38:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0955451d39f7d84caa47d5d788409c83830b232ae0357ddf7001b0fcc42e7d02`  
		Last Modified: Mon, 24 Jun 2024 23:59:48 GMT  
		Size: 12.8 MB (12779982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:044213e3a02f5bb7c0f1a34e12d0d301643f3ea0ace0f53d9fcbf72223a66cfc`  
		Last Modified: Mon, 24 Jun 2024 23:59:47 GMT  
		Size: 88.4 KB (88390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d05b4f603ca42bb13ddb190117b4f4c14f54aebe75b4cd793a89b1665fd3581`  
		Last Modified: Mon, 24 Jun 2024 23:59:47 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdff61de415a7a4387061b8992c86c0abf5af476fd338551392bc0e73c85a721`  
		Last Modified: Mon, 24 Jun 2024 23:59:49 GMT  
		Size: 51.3 MB (51305406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d42aee2aef0e8b09fa42e864f047ad0164023c9563ad69fe776d60a203e197e`  
		Last Modified: Mon, 24 Jun 2024 23:59:48 GMT  
		Size: 1.5 KB (1509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87de4bccde94c399457cd6800b7e415845746bc571577f0734813be98d041dc2`  
		Last Modified: Mon, 24 Jun 2024 23:59:49 GMT  
		Size: 3.3 KB (3262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:24-dind` - unknown; unknown

```console
$ docker pull docker@sha256:63307be2e408adf183751587d6d257f453daed0e6d1bdcab7c837b098415ebf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.1 KB (35062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42cfc784d4ede2321990b9464904af9b24d45fc03268c3de88251fd1d4d53c51`

```dockerfile
```

-	Layers:
	-	`sha256:8ffb872e80cd7075054c56e42ec4f23ee1fac4f99e704132046275427288cc47`  
		Last Modified: Mon, 24 Jun 2024 23:59:47 GMT  
		Size: 35.1 KB (35062 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:24-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:fdfc4404c508fc06bcf6c84e9e4c3c55dcae29edeacfcddf4f665bf5e1639e5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.8 MB (117792483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72aba53f18a46f6daadc4517a20c0ebb5806c753adae05003f8dacf95ec23b48`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 19 Jun 2024 00:17:01 GMT
ADD file:4d58f44e3cedeba6fad741c79bc5acab1a9f2a2f597c854dc3bb8b8595ebf3e1 in / 
# Wed, 19 Jun 2024 00:17:01 GMT
CMD ["/bin/sh"]
# Wed, 19 Jun 2024 00:17:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
ENV DOCKER_VERSION=24.0.9
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.9.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
ENV DOCKER_BUILDX_VERSION=0.15.1
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-amd64'; 			sha256='8d486f0088b7407a90ad675525ba4a17d0a537741b9b33fe3391a88cafa2dd0b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm-v6'; 			sha256='b4d1c41605b50b5549f1464461cfa72d010106bfb4606b45cc776daab4c25d7d'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm-v7'; 			sha256='eabc32a4a86f943c3996eb2df5efd0d02d12603e356941ed46c132c64cbcbcdf'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm64'; 			sha256='13f4ffd2b6922e941d6b6a9faee73ec9b8cab5b309ef90dfadf48142c2a47f34'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-ppc64le'; 			sha256='6b41769526c9102d2352ed6900de33ee4be2eaf1927cfb216cc832c718e5c990'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-riscv64'; 			sha256='52f5a974d8d1eb88d1defe0da5173d39df3608e554c3dcd1d45bde77c3d697f3'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-s390x'; 			sha256='689c88555c42708ac812e3063590f8681b675d7f2ca68c024299ec388963615d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
ENV DOCKER_COMPOSE_VERSION=2.28.0
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.28.0/docker-compose-linux-x86_64'; 			sha256='359043c2336e243662d7038c3edfeadcd5b9fc28dabe6973dbaecf48c0c1f967'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.28.0/docker-compose-linux-armv6'; 			sha256='398d717e6cc9515ca0325035cfe626cbaaa1023754cfd22c13eab6b29ecc2d54'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.28.0/docker-compose-linux-armv7'; 			sha256='604c00f22176ca8291f43d22f066cfcc89f4c09de2113d287f72c0bdcf611e46'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.28.0/docker-compose-linux-aarch64'; 			sha256='296076f4d14d2a816ad750f6890355fc118692814e4b4542942794817f869d37'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.28.0/docker-compose-linux-ppc64le'; 			sha256='c88c097fa475f07140c01e3ca370a503b927f377f200114fa17e0bee6e0cbc4d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.28.0/docker-compose-linux-riscv64'; 			sha256='b563b99c5a1c03a1a83cb56ea1f7a492ef74e137afd0cbea485b828b6c61dbe5'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.28.0/docker-compose-linux-s390x'; 			sha256='f701bd64dc5b204352c788931b43de9c778d47eed1be7caa81b57fc47a09164d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 19 Jun 2024 00:17:01 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 19 Jun 2024 00:17:01 GMT
CMD ["sh"]
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.9.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
VOLUME [/var/lib/docker]
# Wed, 19 Jun 2024 00:17:01 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 19 Jun 2024 00:17:01 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 19 Jun 2024 00:17:01 GMT
CMD []
```

-	Layers:
	-	`sha256:3fb467f9cb36e54d3cb8806db734a6c640048f3dc270b506ec1f111640905b79`  
		Last Modified: Thu, 20 Jun 2024 18:00:55 GMT  
		Size: 3.1 MB (3094856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3be0ff3f8430a7c5e4c0602a3a190116b4a4d4d1d16b89c627d5436d8d3318a`  
		Last Modified: Mon, 24 Jun 2024 16:53:24 GMT  
		Size: 1.8 MB (1841225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0e90c200cd38a52aed6f4457d4fb93031e32aab75a2c05019a3a2dda9db6b7f`  
		Last Modified: Mon, 24 Jun 2024 16:53:24 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa96dd134bec9796b0042d2daf8f85aaa77a69f047108dda451821876b78d14`  
		Last Modified: Mon, 24 Jun 2024 16:54:50 GMT  
		Size: 15.1 MB (15129223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d5749edac0c7ab760208242f658c594b0d6b6ea3328705337eeee5fcca0011`  
		Last Modified: Mon, 24 Jun 2024 16:54:49 GMT  
		Size: 17.0 MB (16998041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb5d8dc385dec960007effa91138f7d64d88a8590f585c848b44d0c73dfd75f`  
		Last Modified: Mon, 24 Jun 2024 16:54:49 GMT  
		Size: 17.7 MB (17737554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a068aedb776b76c6c2bca0701808051f1b3b95e12fc04cd08d0d97a6af9021e1`  
		Last Modified: Mon, 24 Jun 2024 16:54:48 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac79c254fa9d7652b5eca7a6f3d388c2b6ada57fa9031c502307e33be779f743`  
		Last Modified: Mon, 24 Jun 2024 16:54:49 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96f549fa53bc41329581829f77197c9412df30ef8f26f5d90eb1219d9a19a893`  
		Last Modified: Mon, 24 Jun 2024 16:54:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7f89cbeb1b2dc9f1aef3fdd7e65236ee43cc9d90bc510f0180633c9c5fe259`  
		Last Modified: Mon, 24 Jun 2024 17:57:40 GMT  
		Size: 11.6 MB (11593739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0691a956a5bcb77952b00c5a9754cf4b24a45341a02e8c637fb24fda93a86ad`  
		Last Modified: Mon, 24 Jun 2024 17:57:39 GMT  
		Size: 84.5 KB (84469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e830a34bdad483428015c787cabdc02c9d562c9c9b87ca77bd4e9865754c286a`  
		Last Modified: Mon, 24 Jun 2024 17:57:39 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae63b1e03af9aecfc90caf74f429bd4b335e5be2525ca5febe01590979ff62bc`  
		Last Modified: Mon, 24 Jun 2024 17:57:42 GMT  
		Size: 51.3 MB (51305411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4f2433af22df258472061b6e7b795e17f4fc42a32ffa18be1d3b896d4f37f4`  
		Last Modified: Mon, 24 Jun 2024 17:57:40 GMT  
		Size: 1.5 KB (1511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a9bbc433d1542f648d7dc042d6c85b012e3af2cd7db6a6110331d90709e0ff1`  
		Last Modified: Mon, 24 Jun 2024 17:57:40 GMT  
		Size: 3.3 KB (3262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:24-dind` - unknown; unknown

```console
$ docker pull docker@sha256:9f6aadf507c28b4044db566b408eccaad723a07abbc5507176dacea4a9d8b5f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.1 KB (35062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a0de2d17df3cab8e46ca973782658384db37513494a85a1ba8b81fb580ce2cf`

```dockerfile
```

-	Layers:
	-	`sha256:16877c30569c0cb9013565c0c3f1cf3061a574fd6f4fc5e89c78cc4f6d3498a1`  
		Last Modified: Mon, 24 Jun 2024 17:57:39 GMT  
		Size: 35.1 KB (35062 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:24-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e53cac2e0d33a285e9198f97710d08dd4748a93803bc5eafc8870a0357c35c85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.4 MB (118418495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7153689a4396a3ec0df83a179aa966c143e1a2304a6dbb15ac98e5ad7f1e515`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 19 Jun 2024 00:17:01 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Wed, 19 Jun 2024 00:17:01 GMT
CMD ["/bin/sh"]
# Wed, 19 Jun 2024 00:17:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
ENV DOCKER_VERSION=24.0.9
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.9.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
ENV DOCKER_BUILDX_VERSION=0.15.1
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-amd64'; 			sha256='8d486f0088b7407a90ad675525ba4a17d0a537741b9b33fe3391a88cafa2dd0b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm-v6'; 			sha256='b4d1c41605b50b5549f1464461cfa72d010106bfb4606b45cc776daab4c25d7d'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm-v7'; 			sha256='eabc32a4a86f943c3996eb2df5efd0d02d12603e356941ed46c132c64cbcbcdf'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm64'; 			sha256='13f4ffd2b6922e941d6b6a9faee73ec9b8cab5b309ef90dfadf48142c2a47f34'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-ppc64le'; 			sha256='6b41769526c9102d2352ed6900de33ee4be2eaf1927cfb216cc832c718e5c990'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-riscv64'; 			sha256='52f5a974d8d1eb88d1defe0da5173d39df3608e554c3dcd1d45bde77c3d697f3'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-s390x'; 			sha256='689c88555c42708ac812e3063590f8681b675d7f2ca68c024299ec388963615d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
ENV DOCKER_COMPOSE_VERSION=2.28.1
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-x86_64'; 			sha256='5b480d4f9e3517b375f0fbb781b39c63cec934f44b13c43b8f1d0f22bf6de8c3'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-armv6'; 			sha256='ff366f16854e8febcdce21b750f6462abdcaa16209be490feaa8c2dd88b7884c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-armv7'; 			sha256='d829c0d3f85885ee29fcaf19d2b6001215820ad874a0b9cdc3172965acb80c50'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-aarch64'; 			sha256='1ce6f9842b10ee5f61218a62f3acfc5839a31cd6daa6e87e926bef63dd9fee20'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-ppc64le'; 			sha256='c02e6b718e94df66cd0a53349d6487dbc6da99aa582c0b9906637964ecd9bd15'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-riscv64'; 			sha256='9d5d8033a8cf3deb05c7a9ee7cdf0086cc24a526fa9a10b4a778cc9124f5ef25'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-s390x'; 			sha256='c8ac20d8fac6d982a83e3b5bb34cda5ac326fbfde9b43c64a290258a1d7fbb38'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 19 Jun 2024 00:17:01 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 19 Jun 2024 00:17:01 GMT
CMD ["sh"]
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.9.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
VOLUME [/var/lib/docker]
# Wed, 19 Jun 2024 00:17:01 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 19 Jun 2024 00:17:01 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 19 Jun 2024 00:17:01 GMT
CMD []
```

-	Layers:
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8748a3ec57e134ccd57f5380286f503c468960d14815d75e49f8a7fa00bbddb9`  
		Last Modified: Mon, 24 Jun 2024 22:58:31 GMT  
		Size: 2.0 MB (2006605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d843f0fef030adf942f4bea037cda5f4755db1a7f6127261095313118908a3f2`  
		Last Modified: Mon, 24 Jun 2024 22:58:31 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b523ee1c274dd41c3fa285d4fd0ec65cc83f86789b1d86071f7c71b8837bb6e`  
		Last Modified: Mon, 24 Jun 2024 22:58:55 GMT  
		Size: 15.5 MB (15459117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b32d2f6519fd28639ca4bd3f1b227d05dc3f6db6d10427414cf9196a836b32`  
		Last Modified: Mon, 24 Jun 2024 22:58:55 GMT  
		Size: 16.5 MB (16538038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dab95d0b07b5e906b10592bc731b86d22baecc483efaa08adb76b7b80e84d3a`  
		Last Modified: Mon, 24 Jun 2024 22:58:55 GMT  
		Size: 17.2 MB (17151903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d204c19bdab20f0a953183229ee611686021423157a35d9ee0cedadcbb1245f2`  
		Last Modified: Mon, 24 Jun 2024 22:58:55 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278bbbc3c126a4f51e6111b0504b82fdf93f3aa76be2310c9f16a688b93c97a8`  
		Last Modified: Mon, 24 Jun 2024 22:58:56 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d12f5250d85e84f03d10db07ffca206821a6ffc888ac29cfe19ae46216c40363`  
		Last Modified: Mon, 24 Jun 2024 22:58:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae8bdf8b464e925e9ce2adb6517a190811056258ba0624ac50af5ef98fcda48`  
		Last Modified: Mon, 24 Jun 2024 23:59:11 GMT  
		Size: 13.0 MB (12991249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03fd4ca722931f2b94b2f7fd9a7bb0920fdcc3cd4ca20ca76566d0e55bba58b`  
		Last Modified: Mon, 24 Jun 2024 23:59:11 GMT  
		Size: 98.6 KB (98626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc8b5100f2b241c71287326e652d99a14b99564314623db366ede6a4d78a857`  
		Last Modified: Mon, 24 Jun 2024 23:59:11 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d74feaaddc33a19ffc94e8d2c398f1c84b0e2525f96b9ab1ce9f6264704bd8`  
		Last Modified: Mon, 24 Jun 2024 23:59:12 GMT  
		Size: 50.1 MB (50076195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81ac12b69039714f5be82d3baa5abe3f54e1bcc308f760ca1612fb80597ce16`  
		Last Modified: Mon, 24 Jun 2024 23:59:12 GMT  
		Size: 1.5 KB (1509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a5a80ca2fa15e61766f58f1524bfb3437d29a20c5fa65a7ffc20040aecacebe`  
		Last Modified: Mon, 24 Jun 2024 23:59:12 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:24-dind` - unknown; unknown

```console
$ docker pull docker@sha256:f51b737541489856cb4d8c0899d700c62124b9fd5622d5b4b564063967e3a3c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.3 KB (35347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69c6ccd3b7699c5c15d675f4af83781794d048e4b175b5afd73aa739a75a9455`

```dockerfile
```

-	Layers:
	-	`sha256:c152f3a2012c9fd0a51329afc588c8582df06e3941613b62aa342f0b00f8b89d`  
		Last Modified: Mon, 24 Jun 2024 23:59:10 GMT  
		Size: 35.3 KB (35347 bytes)  
		MIME: application/vnd.in-toto+json
