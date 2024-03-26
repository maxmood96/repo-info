## `docker:24-dind-rootless`

```console
$ docker pull docker@sha256:b78dd03e17e52a36a4fda7f320aca6c758f9df06d33587a9ac4d9cdf545df3be
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:24-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:38db2f8d8b74b01ccd4b89072823bc81831e3b243c3de2143a65e017a678a719
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.2 MB (147152487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e1f0532505cf954a974665405a84ec7d1a838bfffe905b7dc87ab0c9dac7078`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Thu, 01 Feb 2024 16:06:26 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
ENV DOCKER_VERSION=24.0.9
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.9.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
ENV DOCKER_BUILDX_VERSION=0.13.1
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-amd64'; 			sha256='3e2bc8ed25a9125d6aeec07df4e0211edea6288e075b524160ef3fd305d3d74c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm-v6'; 			sha256='643063c656098e312533fe5ee3411523fa06cc3926bd2e96b4c6239b9cecbf88'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm-v7'; 			sha256='8d42e7823237e777b121070fda6ad68159539aa6597aedfa7630384643ad6f9a'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm64'; 			sha256='3ba35a5d38361a64b62aeb9d20acc835ff6862a711cb438e610026b29c0ac489'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-ppc64le'; 			sha256='1d16f7b15706d98523889a1ca50e9dfc44bbaec1f736d883a0528805795b9de2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-riscv64'; 			sha256='202221c9b7fb881d092986e8ec2497ee71729f17c4afd912384a086af700e1ad'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-s390x'; 			sha256='71d7c39192b1b07790eb71e46742cc69a559f3eb00a1512f4a8d2ea1067408da'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
ENV DOCKER_COMPOSE_VERSION=2.26.0
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-linux-x86_64'; 			sha256='59c6b262bedc4a02f46c8400e830e660935684899c770c3f5e804a2b7079fc16'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-linux-armv6'; 			sha256='97dac0aa10961ea30a79f6fe2c4a13bfe4da562926365a63042fcceb88d9d125'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-linux-armv7'; 			sha256='d607ed69f5fe92ee1fd831cf764f977174c86192957a4de678c01db671c3dc52'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-linux-aarch64'; 			sha256='6f00ed24a846046b441c0f0a0f8c1e00194f4b0e33f2433fac0d2dd0e486fc80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-linux-ppc64le'; 			sha256='e3afa6956f6cd4fdbaa8fe19781ae07a1bb8fb2f4d54a1aac857090d6fe1710d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-linux-riscv64'; 			sha256='1d080f5bc04b4b97c61ce3f57ff4a7bd11299f486bc287833f162360be201a7d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-linux-s390x'; 			sha256='5f302fb8e7d973b53f1f9dc808d2b1af08f94687cb14b3f26cc7b358854184b5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 01 Feb 2024 16:06:26 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Feb 2024 16:06:26 GMT
CMD ["sh"]
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.9.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
VOLUME [/var/lib/docker]
# Thu, 01 Feb 2024 16:06:26 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 01 Feb 2024 16:06:26 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 01 Feb 2024 16:06:26 GMT
CMD []
# Thu, 01 Feb 2024 16:06:26 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-24.0.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-24.0.9.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 01 Feb 2024 16:06:26 GMT
USER rootless
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db287e1a31efcf9777aad3e2c2c3f291dcbc6699d6f724c84e214dc0c115480d`  
		Last Modified: Mon, 25 Mar 2024 19:12:09 GMT  
		Size: 2.0 MB (2026164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e831544aa5c9d57189049c63ea52987f006bbb75724b9deecb0726779e43b47`  
		Last Modified: Mon, 25 Mar 2024 19:12:09 GMT  
		Size: 550.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fb4489284b20da66de816b146752624ad53d3eda0e70a9d76dc7ddf939c983b`  
		Last Modified: Mon, 25 Mar 2024 19:12:10 GMT  
		Size: 16.4 MB (16410668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0468f26daa7d03bebe8f89ebccf4f8f3be57535a189c1b55bd421c992063c046`  
		Last Modified: Mon, 25 Mar 2024 19:12:10 GMT  
		Size: 18.0 MB (17982274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf3995726f3782ab957cc5185b026052ad131d846d69d6d4d7bd501541488294`  
		Last Modified: Mon, 25 Mar 2024 19:12:11 GMT  
		Size: 18.7 MB (18669704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aec7527505c01a9ff1503f472842cb806973fe24e89ced47e2a6c981bb6d0d23`  
		Last Modified: Mon, 25 Mar 2024 19:12:10 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d9503abbf3673059fff872da078d8b27f029454b55109ad29e4a24d2c22bac7`  
		Last Modified: Mon, 25 Mar 2024 19:12:11 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76772a122dd0128244aa2ff6fecdd261df83eb325cae7b3ee80f2839730032ef`  
		Last Modified: Mon, 25 Mar 2024 19:12:11 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f68ad44a1792b111a70bfc3c2fe686a1123935c055487f0eebb588a8dd1c31d2`  
		Last Modified: Mon, 25 Mar 2024 20:11:58 GMT  
		Size: 12.2 MB (12157613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef560c0b3457952325a69c7f758335131ecafd9a5a232256243f79ffae46392a`  
		Last Modified: Mon, 25 Mar 2024 20:11:57 GMT  
		Size: 89.1 KB (89123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e7c21509bd60c57df9610632c83c32ab39e0006c0bd5800ea1e797be588224`  
		Last Modified: Mon, 25 Mar 2024 20:11:57 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3460e0c19a0843ffa69741977c7ba8eab5afa0c7ca530d0942f255f9cd3e0f35`  
		Last Modified: Mon, 25 Mar 2024 20:11:59 GMT  
		Size: 54.7 MB (54740517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6407e2ae259ebc4f46af358b00d45bc4bd4c9be53c2bdcf5a6f9a4e3c6301be`  
		Last Modified: Mon, 25 Mar 2024 20:11:58 GMT  
		Size: 1.5 KB (1509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83644f0385bef6b73e7fadc12f143fec46ef31e61d5a91a027283b9478eba1e6`  
		Last Modified: Mon, 25 Mar 2024 20:11:58 GMT  
		Size: 3.2 KB (3248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f46c271eabf5bd4889443c981f476d67718e209e6f710d593f552165f2b98fe9`  
		Last Modified: Mon, 25 Mar 2024 21:11:21 GMT  
		Size: 981.6 KB (981566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b18ed5a8636e98b86c1cc5f068adaa87fa132956972d2c08ee44010b644c7d61`  
		Last Modified: Mon, 25 Mar 2024 21:11:20 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e771ecbba7712727332f54be8d323d5297a0542d83fe7711565261d23d746489`  
		Last Modified: Mon, 25 Mar 2024 21:11:21 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb309494c7033cb36d39cc9f80970a38de4217bcb5f89991c8b07cf14019be00`  
		Last Modified: Mon, 25 Mar 2024 21:11:21 GMT  
		Size: 20.7 MB (20676180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ac983835ed4164f42e14cdb1e5686cebcde2b6dc712368eed7393f31cba83b`  
		Last Modified: Mon, 25 Mar 2024 21:11:21 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:24-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:84530e5b3b82f5306d8462d1bc21b0f314796d454113e15c8d29530fb031b5b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **911.9 KB (911943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aa62cc7b3c7a7cd0cb6607fc838f67d81263b2888f48a854a05e10c508885be`

```dockerfile
```

-	Layers:
	-	`sha256:21d8061263c850e18157c8a12619234380ce808058f0937e582bab16279524cd`  
		Last Modified: Mon, 25 Mar 2024 21:11:20 GMT  
		Size: 879.0 KB (878999 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fee3ef8dfdf8e3d9c52ac4d1de4a2197c4e9f9984457d62492a4f52839fb5ce9`  
		Last Modified: Mon, 25 Mar 2024 21:11:20 GMT  
		Size: 32.9 KB (32944 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:24-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:221e710fa48b9857b22e61734e6362dc0ecc2199bba46fc699f4899657e666e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.1 MB (140132289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79afbbcad0218291b417de9694bbdfd6e15cea18295951f994180abb57231f5c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Thu, 01 Feb 2024 16:06:26 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
ENV DOCKER_VERSION=24.0.9
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.9.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
ENV DOCKER_BUILDX_VERSION=0.13.1
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-amd64'; 			sha256='3e2bc8ed25a9125d6aeec07df4e0211edea6288e075b524160ef3fd305d3d74c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm-v6'; 			sha256='643063c656098e312533fe5ee3411523fa06cc3926bd2e96b4c6239b9cecbf88'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm-v7'; 			sha256='8d42e7823237e777b121070fda6ad68159539aa6597aedfa7630384643ad6f9a'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm64'; 			sha256='3ba35a5d38361a64b62aeb9d20acc835ff6862a711cb438e610026b29c0ac489'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-ppc64le'; 			sha256='1d16f7b15706d98523889a1ca50e9dfc44bbaec1f736d883a0528805795b9de2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-riscv64'; 			sha256='202221c9b7fb881d092986e8ec2497ee71729f17c4afd912384a086af700e1ad'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-s390x'; 			sha256='71d7c39192b1b07790eb71e46742cc69a559f3eb00a1512f4a8d2ea1067408da'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
ENV DOCKER_COMPOSE_VERSION=2.25.0
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-x86_64'; 			sha256='53641b8a28419f947bc58c085e0c39b97a209b6e875a25c585e7fab44ff48576'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-armv6'; 			sha256='a123b79b530a65c7381ca8bb3b29cde7177f4f260984a127d998c9696cae794c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-armv7'; 			sha256='8ea72e93e8da8259d7d5d051f3c65dc14c44a23d5ebc6939394d7d03b147e238'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-aarch64'; 			sha256='b9f303c9f9db75ecf18ea6fc516b3dc54a3e54f3b3d8e7f1a449416522958bc5'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-ppc64le'; 			sha256='dc067ab61239cef3d2e145d37fcd68c1fc2320c6728d77a9a4ec4fb0e6c6dd64'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-riscv64'; 			sha256='a17f07604fa74c661e62d5e27ae358f8a611f42bb9a4a147cec76b8bb591bea4'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-s390x'; 			sha256='9e613275e5fa46cb864d3f2fccb10e3239b879527d075490b03e381df56c397c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 01 Feb 2024 16:06:26 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Feb 2024 16:06:26 GMT
CMD ["sh"]
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.9.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
VOLUME [/var/lib/docker]
# Thu, 01 Feb 2024 16:06:26 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 01 Feb 2024 16:06:26 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 01 Feb 2024 16:06:26 GMT
CMD []
# Thu, 01 Feb 2024 16:06:26 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-24.0.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-24.0.9.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 01 Feb 2024 16:06:26 GMT
USER rootless
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b275a3377f65492f727dc46aa2b70be6ec8ff96583fcd9a7b699692b5170bc`  
		Last Modified: Sat, 16 Mar 2024 04:06:09 GMT  
		Size: 2.0 MB (2019704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7c53acdebd8fb391eae546ed72149f049f8ab4d594f12c74c49be04cc3b9708`  
		Last Modified: Sat, 16 Mar 2024 04:06:08 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21e243595b6a4a5354eda3c1c4af2133475005f29ef8acc4da4821fc7fff21a2`  
		Last Modified: Sat, 16 Mar 2024 04:06:09 GMT  
		Size: 15.5 MB (15459111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1ea7a6c39e124859c5e26c544d7aff02e08d3965595d626d90a9d54bb420cd`  
		Last Modified: Sat, 16 Mar 2024 04:06:09 GMT  
		Size: 16.3 MB (16349525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db075556d6c3ec65e7212ebf5868c54a6b2a003f52befa03b0afa0aea93e98c0`  
		Last Modified: Mon, 18 Mar 2024 22:52:02 GMT  
		Size: 16.6 MB (16646403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c700a96bcdc706c72c84a269d64cf06bd721fc2b9a2a2bafb6d124007f7018a9`  
		Last Modified: Mon, 18 Mar 2024 22:52:01 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0372966def7c7241c44600727ffcc456f40f50233ee0e03dc9a6b57d21815372`  
		Last Modified: Mon, 18 Mar 2024 22:52:01 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1049c071c865dcd9c40f4a80d5902fa62c58d956ad1197278eda9b8ddcb0204`  
		Last Modified: Mon, 18 Mar 2024 22:52:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc57cf04b3492fc7ffe50e5e6dd6d2add34ad98b14aedf724addbc62ea6f6e8c`  
		Last Modified: Mon, 18 Mar 2024 23:54:25 GMT  
		Size: 12.6 MB (12626700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88b39887c91a4fdcc838ebe34eccf51f26f8ee5c5ba5e306136e0a07adcef0dd`  
		Last Modified: Mon, 18 Mar 2024 23:54:25 GMT  
		Size: 98.4 KB (98388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f92e21283fab8a1681b55b6bc70e8d93f48ee6de8e36a009d4be4a465b712f1`  
		Last Modified: Mon, 18 Mar 2024 23:54:25 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:831af8af4683aa4b9c89c1aefba4d75aa4e9086eee716afbde7033a93f5e0327`  
		Last Modified: Mon, 18 Mar 2024 23:54:28 GMT  
		Size: 50.1 MB (50076174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69eb9c9407f2780cf4782b8e6e65af1a1f620ecca5a988fb5e6aed2723aa1133`  
		Last Modified: Mon, 18 Mar 2024 23:54:26 GMT  
		Size: 1.5 KB (1510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58de5aa29ef2154b96b26ae30a51d36b224370eb6b211cb8eb0964fb2cf3600`  
		Last Modified: Mon, 18 Mar 2024 23:54:27 GMT  
		Size: 3.3 KB (3251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0795f202ed6af5f33a3899ae7a274729f51bb69a84f4543bdbeae03773ff2d23`  
		Last Modified: Tue, 19 Mar 2024 00:52:09 GMT  
		Size: 1.0 MB (1022486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ecf4e5822a9487403c88b9cb71d9e008fb1a99ac1cbdab306bb3a075c6f357c`  
		Last Modified: Tue, 19 Mar 2024 00:52:09 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f6f0352517b72969a65dad38b53d390d4fda8efb15b64bb59a12d00b1a3fff`  
		Last Modified: Tue, 19 Mar 2024 00:52:09 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68a148e722c7b2505f95cca1895196779a4b0aedac0da59a40a9467fad93c15d`  
		Last Modified: Tue, 19 Mar 2024 00:52:10 GMT  
		Size: 22.5 MB (22476115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c12cb2141eea9c4c567c1ae8140e03cb3479ba3365f0f6b7f6a64b1f4f5b7de`  
		Last Modified: Tue, 19 Mar 2024 00:52:10 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:24-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:d1c3d8ace50719b2c1ecac3cee47f0080376bf84610fe2c92f2c6ef8060ad112
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **928.1 KB (928067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d3011f783e1ae6a9f10ea032cb647fcb079d4f608e8f9243dd8672906cc24e8`

```dockerfile
```

-	Layers:
	-	`sha256:8956de2fb961bd7b3dcf94a514b30a9bba1bc3fa3bee307d0538a69957018fd7`  
		Last Modified: Tue, 19 Mar 2024 00:52:08 GMT  
		Size: 895.1 KB (895063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71004c07a6ed001796308c36940ed54f9b21bd631cb360acda8a5e8dc122a1bd`  
		Last Modified: Tue, 19 Mar 2024 00:52:07 GMT  
		Size: 33.0 KB (33004 bytes)  
		MIME: application/vnd.in-toto+json
