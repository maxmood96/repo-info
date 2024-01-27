## `docker:24-dind-rootless`

```console
$ docker pull docker@sha256:ee6420daceb36b261e894a706ea255bb32b92f3d6a7a603e7c344a3dc4719503
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:24-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:3b8407055ea3f4fbe7723f8d883cd02775a18ee071ef39e4c03c35b19db91c65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.8 MB (140750247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f05972219aa2df88473a4055cf7e5c8abbed6ec5824504c44f51e30039ab14d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 26 Jan 2024 00:04:16 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Fri, 26 Jan 2024 00:04:16 GMT
CMD ["/bin/sh"]
# Fri, 26 Jan 2024 00:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
ENV DOCKER_VERSION=24.0.8
# Fri, 26 Jan 2024 00:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.8.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.8.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.8.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.8.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Fri, 26 Jan 2024 00:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-amd64'; 			sha256='716321df8ca9c82ffe96f37e9f4aa1199d4969795836dbd57ef72d12e3ac5085'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v6'; 			sha256='4b3c78b59c0383ab21327e2902af2ea317e3b85e442b1cd776f0c2a7bbbb2999'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v7'; 			sha256='fe0a9e7812051a72c47d009bf9373e76e23644cc3291c848ac4a9b6f237e9e75'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm64'; 			sha256='fb72d627f2ee080bba70375c367f4292867821e29ca9a8cf485622f6ede8f436'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-ppc64le'; 			sha256='1c649498d727183d82fb243e08856533ea90e8d63bfcd6f8b23b264dbcf7ea7a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-riscv64'; 			sha256='152e7b423c1ce888eb0a658321eb8c28cc1d09af01acd5c66eddf8474dddf55c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-s390x'; 			sha256='acee98a9f0550bf2c6c1161cf8067c031ddf0c566c41de7db27847bb72e8ee0b'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.3
# Fri, 26 Jan 2024 00:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-x86_64'; 			sha256='49b3b71e4428585f75294a83702d259f442a8fcdb2351864c6dcaa3f7e29b3aa'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-armv6'; 			sha256='20cf111b8f28dc0e5b390ef6685c5504fc243597737ca46dac27e19e3f34190d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-armv7'; 			sha256='d08bc3066c07effc6e7115197ce410d16c6c0974d5a746f0c6d02bc4c10b8348'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-aarch64'; 			sha256='c5a2bdf09db39c2aaf820ed9d6bab0ee9de187411ab37b869a7df20d3dbbceed'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-ppc64le'; 			sha256='e7e39ebbc2c42d17d5e6a2938f3ed9c5989380d569b84bbcc916000ec276527d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-riscv64'; 			sha256='5b9a52806b8363d170770548ca7baf25c1f96dca1da837265b2a42989c323e32'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-s390x'; 			sha256='258e548656bbce1a44459fcf579927b59a17b284e730d680843c19a699bf7739'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 26 Jan 2024 00:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 26 Jan 2024 00:04:16 GMT
CMD ["sh"]
# Fri, 26 Jan 2024 00:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.8.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.8.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.8.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.8.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 26 Jan 2024 00:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
VOLUME [/var/lib/docker]
# Fri, 26 Jan 2024 00:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 26 Jan 2024 00:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 26 Jan 2024 00:04:16 GMT
CMD []
# Fri, 26 Jan 2024 00:04:16 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-24.0.8.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-24.0.8.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 26 Jan 2024 00:04:16 GMT
USER rootless
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15fd777afe98c1c753c4f56bc842309a9a6cbc335afd6896e191ea93e236484c`  
		Last Modified: Sat, 27 Jan 2024 00:52:43 GMT  
		Size: 2.0 MB (2018455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5fb2711e6533c67af3a1bc476797713e8437ad8788c9654ebb093ef44fa87b5`  
		Last Modified: Sat, 27 Jan 2024 00:52:43 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1c61922c42a18bdaf6f864caffa4e36954223b341650cb2d893f537b91e3035`  
		Last Modified: Sat, 27 Jan 2024 00:52:43 GMT  
		Size: 16.4 MB (16409708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee48db4804436f15a546763ca3113bbf48492b32b008dbd3eb5dae031b5fb05`  
		Last Modified: Sat, 27 Jan 2024 00:52:44 GMT  
		Size: 17.2 MB (17195293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c607947ab3fc5983d5b0fa2be4a4ecba1274f706743668a99997d2fce62150`  
		Last Modified: Sat, 27 Jan 2024 00:52:44 GMT  
		Size: 18.2 MB (18175350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a470925cc6e6f61e7cbe6a4c13ec8d9118ade73974bdf37fc2058c239a54c1e0`  
		Last Modified: Sat, 27 Jan 2024 00:52:44 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b71181cee47f8a39e61ae1b5a006d9599221f8ef18a1fe1d032a92882493327`  
		Last Modified: Sat, 27 Jan 2024 00:52:44 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6fa315d033aa770f3c324afede4f25497f4c2c62188a2f4c6ae3419130ba5a`  
		Last Modified: Sat, 27 Jan 2024 00:52:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:709000dbc94d0aba15e49307f6d292554a43adaf4f1b55635f51c6354c055ba1`  
		Last Modified: Sat, 27 Jan 2024 01:53:40 GMT  
		Size: 7.1 MB (7068032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2142d42a3bb15471fda2f8250add54c601cbd13ac4ac62edccde241af475064`  
		Last Modified: Sat, 27 Jan 2024 01:53:40 GMT  
		Size: 83.6 KB (83638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff27e27b929504aaf33cd1649e1f0ff2233730b423be08c3bb3ad1da6f927b1`  
		Last Modified: Sat, 27 Jan 2024 01:53:40 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067d226fad3e1431bb2d0fa965d06a0a764359b3fc0b616a0fe9697df4cbdec0`  
		Last Modified: Sat, 27 Jan 2024 01:53:41 GMT  
		Size: 54.7 MB (54730890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d16a678b416f8f4576da2a07528d768c855aafb23a047a3c56c00b5bf2c81a`  
		Last Modified: Sat, 27 Jan 2024 01:53:41 GMT  
		Size: 1.5 KB (1509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa8c315ee3726e0fa9d6769f71571cc372ea246e3998fb7b489fe4b0346768a`  
		Last Modified: Sat, 27 Jan 2024 01:53:41 GMT  
		Size: 3.2 KB (3249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d7c667d7757219540a06fb02838d4640947b68cfb0b3132797b97d55ebb6da`  
		Last Modified: Sat, 27 Jan 2024 02:53:00 GMT  
		Size: 974.0 KB (974003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c791db6b5c53b43d105607133ca5d9258d57730c58e5dd32a336f5bfb24f5a`  
		Last Modified: Sat, 27 Jan 2024 02:53:00 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eacbbc9a6fe8ecb07ffaddf0bb3441dcb37792900db9b0f75d46577c76f4f8c1`  
		Last Modified: Sat, 27 Jan 2024 02:53:00 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e649daad5468940af52ae37a5ca499e9127efa3eac6c8e0467c07731bc0066`  
		Last Modified: Sat, 27 Jan 2024 02:53:00 GMT  
		Size: 20.7 MB (20676203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782c2ab99dae2ccf8ba834ef3b7c7dffb3f8e349ba198707a9e6fa500076aef1`  
		Last Modified: Sat, 27 Jan 2024 02:53:01 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:24-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:00fde3ce985d674a35b7d0128642bd7e1a787541139c2cd6b6bd78b9a3b4632d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **777.0 KB (776963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d7091ff5b334e5123930e5bf8a7dbb48c016b983a9cdb5144d5c3d99b581bfa`

```dockerfile
```

-	Layers:
	-	`sha256:4efed6e2a5c73c35900fccfe1d158080e8c8dc8c7c7757ae06751f24a1eeac53`  
		Last Modified: Sat, 27 Jan 2024 02:52:59 GMT  
		Size: 744.0 KB (744026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62e3ac7d986ef5257314fde8842ac7c9c59078eb94b025960502927debeaf4a6`  
		Last Modified: Sat, 27 Jan 2024 02:52:59 GMT  
		Size: 32.9 KB (32937 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:24-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:f2c2a72f5b2f9e0ce6259cacca6b7297513cb3513d741daf54810e3feecd7bf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.3 MB (136252698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5e79caa18f5c37e6ac23df10bf54b001c60af4e8010ea9f6cb71d11e19a1274`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 08 Dec 2023 01:39:30 GMT
ADD file:8182c73f869a899cf624a59c400acb8226776d15e4d3a0d240a94e65340540d0 in / 
# Fri, 08 Dec 2023 01:39:30 GMT
CMD ["/bin/sh"]
# Fri, 26 Jan 2024 00:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
ENV DOCKER_VERSION=24.0.8
# Fri, 26 Jan 2024 00:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.8.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.8.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.8.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.8.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Fri, 26 Jan 2024 00:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-amd64'; 			sha256='716321df8ca9c82ffe96f37e9f4aa1199d4969795836dbd57ef72d12e3ac5085'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v6'; 			sha256='4b3c78b59c0383ab21327e2902af2ea317e3b85e442b1cd776f0c2a7bbbb2999'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v7'; 			sha256='fe0a9e7812051a72c47d009bf9373e76e23644cc3291c848ac4a9b6f237e9e75'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm64'; 			sha256='fb72d627f2ee080bba70375c367f4292867821e29ca9a8cf485622f6ede8f436'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-ppc64le'; 			sha256='1c649498d727183d82fb243e08856533ea90e8d63bfcd6f8b23b264dbcf7ea7a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-riscv64'; 			sha256='152e7b423c1ce888eb0a658321eb8c28cc1d09af01acd5c66eddf8474dddf55c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-s390x'; 			sha256='acee98a9f0550bf2c6c1161cf8067c031ddf0c566c41de7db27847bb72e8ee0b'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.3
# Fri, 26 Jan 2024 00:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-x86_64'; 			sha256='49b3b71e4428585f75294a83702d259f442a8fcdb2351864c6dcaa3f7e29b3aa'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-armv6'; 			sha256='20cf111b8f28dc0e5b390ef6685c5504fc243597737ca46dac27e19e3f34190d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-armv7'; 			sha256='d08bc3066c07effc6e7115197ce410d16c6c0974d5a746f0c6d02bc4c10b8348'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-aarch64'; 			sha256='c5a2bdf09db39c2aaf820ed9d6bab0ee9de187411ab37b869a7df20d3dbbceed'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-ppc64le'; 			sha256='e7e39ebbc2c42d17d5e6a2938f3ed9c5989380d569b84bbcc916000ec276527d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-riscv64'; 			sha256='5b9a52806b8363d170770548ca7baf25c1f96dca1da837265b2a42989c323e32'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-s390x'; 			sha256='258e548656bbce1a44459fcf579927b59a17b284e730d680843c19a699bf7739'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 26 Jan 2024 00:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 26 Jan 2024 00:04:16 GMT
CMD ["sh"]
# Fri, 26 Jan 2024 00:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.8.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.8.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.8.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.8.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 26 Jan 2024 00:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
VOLUME [/var/lib/docker]
# Fri, 26 Jan 2024 00:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 26 Jan 2024 00:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 26 Jan 2024 00:04:16 GMT
CMD []
# Fri, 26 Jan 2024 00:04:16 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-24.0.8.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-24.0.8.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 26 Jan 2024 00:04:16 GMT
USER rootless
```

-	Layers:
	-	`sha256:c303524923177661067f7eb378c3dd5277088c2676ebd1cd78e68397bb80fdbf`  
		Last Modified: Fri, 08 Dec 2023 01:39:48 GMT  
		Size: 3.3 MB (3347794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d4959de38143abac793d31e4e8592696721305ff06281f8b9284aee380afcfe`  
		Last Modified: Thu, 14 Dec 2023 22:04:39 GMT  
		Size: 2.0 MB (2014899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf613c8d3eefad31faacee38beeedf68069e48ea01d8f083fa0a57ce343ed827`  
		Last Modified: Fri, 05 Jan 2024 02:15:00 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:166dedd3aee4146f44ff9ce60af0e31c33f5f9e49b049b189452f20715491f6b`  
		Last Modified: Fri, 26 Jan 2024 18:47:55 GMT  
		Size: 15.5 MB (15461799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d82a2654421afa37f9755240bf6cd53937685a08af74facf5ff07a902476a9`  
		Last Modified: Fri, 26 Jan 2024 18:47:54 GMT  
		Size: 15.6 MB (15640595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c734643d5daa6636a49077b921c4fd280314c942aedf641ba4c67929c601eec`  
		Last Modified: Fri, 26 Jan 2024 18:47:54 GMT  
		Size: 16.6 MB (16609712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75745e9a261c0e27d93e6044080163c1e4322cd6b5159db99707d91e7ed40532`  
		Last Modified: Fri, 26 Jan 2024 18:47:53 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8042b45b8fb3635bdb0be7adab09fa466032258c331465dcde8f7c1530a14a1b`  
		Last Modified: Fri, 26 Jan 2024 18:47:54 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b490ad17a39b02653bea38f74f2eb180cee8d310eecba525469fda38e9c5287d`  
		Last Modified: Fri, 26 Jan 2024 18:47:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bab867a571fe9e753f0c7e180903fbf669472b55bde56661cb1013968680e11`  
		Last Modified: Fri, 26 Jan 2024 20:15:06 GMT  
		Size: 9.5 MB (9509642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6013555a03a9bb27a2054b9ca2d97e790e30ceecb80fdfe2838f7aa25e7c9983`  
		Last Modified: Fri, 26 Jan 2024 20:15:05 GMT  
		Size: 93.1 KB (93070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b4fbef6ebcb6ade93c46e174ac1139586d664574766b31b765fff8dfa1239b`  
		Last Modified: Fri, 26 Jan 2024 20:15:05 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cec58ffb60f74c1cc4e046c098451d40d5afd4196b777f6a324cad9901d406c`  
		Last Modified: Fri, 26 Jan 2024 20:15:08 GMT  
		Size: 50.1 MB (50072901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c4a6fcce6c7d24a86fe5b1131cc1ee84f95b42252478fff7610867e122b66b`  
		Last Modified: Fri, 26 Jan 2024 20:15:06 GMT  
		Size: 1.5 KB (1509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:396b86c805163c1139e12a0ed35b4b432c9c5dd9c9c354364b67325a4e106044`  
		Last Modified: Fri, 26 Jan 2024 20:15:06 GMT  
		Size: 3.2 KB (3250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7efac898699cdda1dac4cdf1c2698e37f1142e53708cfa65d3ed9a1bc24cb329`  
		Last Modified: Fri, 26 Jan 2024 21:39:44 GMT  
		Size: 1.0 MB (1016235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8851ed0d3bd26cc3561ff65fb385e8d84386b241c3bb741d798017f83e40e85`  
		Last Modified: Fri, 26 Jan 2024 21:39:44 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818539b862c09f0434fd5f971a247fb075e664886e646122f10f7960baccfc02`  
		Last Modified: Fri, 26 Jan 2024 21:39:44 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91281952f522d839e84256f0bffd6c37eb4c7309423b6dfb832339be6490ec2b`  
		Last Modified: Fri, 26 Jan 2024 21:39:46 GMT  
		Size: 22.5 MB (22476099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d801ae2a9069983c33cdbb0004e6ea56cc3dbcc99ecf6a96076fb65903f95eb`  
		Last Modified: Fri, 26 Jan 2024 21:39:45 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:24-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:ec1e7547911cc63af2f6dc993f36e6e30f624f1b3cc18ccb035f53e47a105eb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **777.0 KB (777027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43b81768cfc0ea709e8f0fdc49122535572eb1bc93fc8c2520bcfb547a7c580c`

```dockerfile
```

-	Layers:
	-	`sha256:27f9b3401ba5ce5405d8da192480e612a91b2c4bfa1ad0aa506dee9239459809`  
		Last Modified: Fri, 26 Jan 2024 21:39:43 GMT  
		Size: 744.0 KB (744029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4de847b52f79834170f143e7e463c37b43c8a83d3e42d24a7651f1ac341c14c8`  
		Last Modified: Fri, 26 Jan 2024 21:39:43 GMT  
		Size: 33.0 KB (32998 bytes)  
		MIME: application/vnd.in-toto+json
