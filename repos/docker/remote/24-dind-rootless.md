## `docker:24-dind-rootless`

```console
$ docker pull docker@sha256:05f40e4ce53efa4f3254398230dc27bc1df366f1c422e78a07ca0d1e725c2876
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:24-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:d6d3a01fcfa37d48f82fd2b5bc8ffc9b1cda630cd3f8e555399e69f41829227e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.7 MB (146687589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fece14f788377ccbe9bf5dc3d892a955a4bef97c197eb0e6f4b8319e6b8b4d25`
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
ENV DOCKER_COMPOSE_VERSION=2.24.7
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-x86_64'; 			sha256='19c9deb6f4d3915f5c93441b8d2da751a09af82df62d55eab097c2cbfebd519f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-armv6'; 			sha256='c9fb575152f757a5edcce8ca0a399de6ba8dfacd80a8c730f56f0957cadb5858'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-armv7'; 			sha256='72ec3b7726b5784cf4ac14e2c32781f5090cb57a2951cfc59b24a74a88e9ce79'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-aarch64'; 			sha256='86fa6982c55e1bb741ac71ebbbb78c715224eeb46a820364ec6075cf87047d53'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-ppc64le'; 			sha256='236176989b202caebce42629d57f6faad310159c1c1b826feb63a097910bd0a5'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-riscv64'; 			sha256='eacbc70fd96c4c9a20bd58fc91a756372ece659211b9f566da33e15112c0b2af'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-s390x'; 			sha256='23a643f8994c945683f62669cd0f44bc106d3312ea04c3dda39d7514f0b1035e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:984fa9af98bb10aa86254aca73e6aa450c704b423fb43fc16f5e658388b6d950`  
		Last Modified: Thu, 14 Mar 2024 17:49:10 GMT  
		Size: 2.0 MB (2018455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86469d8f26b8f1446e768c2f161ca2b987f2730e208fb464651aa1ecc21c16e7`  
		Last Modified: Thu, 14 Mar 2024 17:49:10 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592b0372dcb60fe4ba3d20c4af41830c246f46bd0c4d0b0089dbea2d7a1c24fc`  
		Last Modified: Thu, 14 Mar 2024 17:49:10 GMT  
		Size: 16.4 MB (16410669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47d87962ebdd312cd917d0280be1c3ccf47ad7833a3f5e19b2c7ef94f7ca91f`  
		Last Modified: Thu, 14 Mar 2024 17:49:10 GMT  
		Size: 18.0 MB (17982282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b649fb73e513dd994e7abc3b55df92c212e61d2ea4a8c0802ae7529d8b18aff9`  
		Last Modified: Thu, 14 Mar 2024 17:49:11 GMT  
		Size: 18.2 MB (18214531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4379c9ce0d791fdaeafbe4cf3cb664e0c82a95057d1733127e0d843bbe0cd6a6`  
		Last Modified: Thu, 14 Mar 2024 17:49:11 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ee1688f4eda9adce4bd4993ed878ad00d0048e42acf91a0207a7b2713dbfac5`  
		Last Modified: Thu, 14 Mar 2024 17:49:11 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b807ab40a9ccbc354eb008b7d499feb7e16ce516a78633a9e86d93611a51715d`  
		Last Modified: Thu, 14 Mar 2024 17:49:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e6e1d49311f2f5bdf9debdf5301129c0db7b21fb1e9d47496d114a8da90b0e`  
		Last Modified: Thu, 14 Mar 2024 18:49:19 GMT  
		Size: 12.2 MB (12156083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b057b52e92d10168be8ea6e9508e2d9f563df2f7fda697044bcf6c1aca6d64`  
		Last Modified: Thu, 14 Mar 2024 18:49:18 GMT  
		Size: 88.9 KB (88861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a93eb015ee555a131dc9c7f73c879eb7e61bef5cbd42b6e741392f60ba93b594`  
		Last Modified: Thu, 14 Mar 2024 18:49:19 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d8a531b7f54c3bb42edbe73cd8e29818289b5f7e7bce282fbe3e5d7b3aaa75`  
		Last Modified: Thu, 14 Mar 2024 18:49:21 GMT  
		Size: 54.7 MB (54740522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b901eec7fb2ca230cba76303ab2d1fb5d7c94588b988b93c6995cb0dfea66ad9`  
		Last Modified: Thu, 14 Mar 2024 18:49:19 GMT  
		Size: 1.5 KB (1509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:772a7fd2e85d202936821263fa453041481c5f64524c4d5d4b20552281325397`  
		Last Modified: Thu, 14 Mar 2024 18:49:20 GMT  
		Size: 3.2 KB (3250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd4dc5cd6c545f333299e90db2c217aaf615699c7cd1ce0f41a36be1be092fe6`  
		Last Modified: Thu, 14 Mar 2024 19:48:05 GMT  
		Size: 981.3 KB (981311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1339714843dd670fa03534b67c510b262d60a3ca3bae0a7f7a4eb72b3613e5`  
		Last Modified: Thu, 14 Mar 2024 19:48:05 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a2c1657ce018dd9226060032c111e86aa18f8abc7040025b37ae3cead8c3f9`  
		Last Modified: Thu, 14 Mar 2024 19:48:05 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634b197f5f566f2b9f68a0bdf04c3c296a24ef13096258e6f5f8b3f7ba2edfcf`  
		Last Modified: Thu, 14 Mar 2024 19:48:05 GMT  
		Size: 20.7 MB (20676193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ded986a48ebc9569330b3a36712e9b420e39e50fba0b8d1d9ed190e8f8fd3d97`  
		Last Modified: Thu, 14 Mar 2024 19:48:06 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:24-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:8d3b9b333063ffc28719f49e541879742ef9ee4ac220496ca68aa4f7b19c4e87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **927.6 KB (927642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f72026747bd807e3e8fe21628dace25d8e01178e3ed17c5d4de57a1bc88586b`

```dockerfile
```

-	Layers:
	-	`sha256:e734e99e95bb2d083154da7d197dc0f6f6c2bdeee5ecb51be6c3f4fb2c847f01`  
		Last Modified: Thu, 14 Mar 2024 19:48:05 GMT  
		Size: 894.7 KB (894698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5daf2aec8f6892ba62008bb2a92b59c98368bec8bca86924bcaedd2c8e590272`  
		Last Modified: Thu, 14 Mar 2024 19:48:05 GMT  
		Size: 32.9 KB (32944 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:24-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:db3a9cb3885ab7a3ade8bd64c4d9f232558375a748b5bda93d73c39fb1f19fcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.1 MB (140128904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6be4a37cfcc458b9c3b8939c639f8b7c69cc262ceb1fbab0514cf3325aa522b`
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
ENV DOCKER_BUILDX_VERSION=0.13.0
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.13.0/buildx-v0.13.0.linux-amd64'; 			sha256='ddd69ee2ca3dd61760e771dcd2f3453dc677dfeb42c9484cc2321b96bc1b7c57'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.13.0/buildx-v0.13.0.linux-arm-v6'; 			sha256='6aea498b2a168bcd13f919e85e0670c2e5a71abab8ecd6bfe52874d14680f617'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.13.0/buildx-v0.13.0.linux-arm-v7'; 			sha256='1566b6f3cf69d06ade467d9928e19f6a6682182fe3008bc9a0c83385d5637fa9'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.13.0/buildx-v0.13.0.linux-arm64'; 			sha256='fa36eb4deab2fac6ddf5fdeddcf16999bc9d5fb1d632e0ba7e572b519df8a656'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.13.0/buildx-v0.13.0.linux-ppc64le'; 			sha256='aced23b7832c690703d0cb6339d4ccdbac9b45f0392b865b131aba9b572ae3c1'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.13.0/buildx-v0.13.0.linux-riscv64'; 			sha256='c15e51986d59398552b3ecd50b4ca75779e42c878e34761df54616ac02165207'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.13.0/buildx-v0.13.0.linux-s390x'; 			sha256='c3578ab9814e4c2d0f917721b1dfd140b85e40602f6128745178a051cf4d0196'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.7
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-x86_64'; 			sha256='19c9deb6f4d3915f5c93441b8d2da751a09af82df62d55eab097c2cbfebd519f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-armv6'; 			sha256='c9fb575152f757a5edcce8ca0a399de6ba8dfacd80a8c730f56f0957cadb5858'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-armv7'; 			sha256='72ec3b7726b5784cf4ac14e2c32781f5090cb57a2951cfc59b24a74a88e9ce79'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-aarch64'; 			sha256='86fa6982c55e1bb741ac71ebbbb78c715224eeb46a820364ec6075cf87047d53'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-ppc64le'; 			sha256='236176989b202caebce42629d57f6faad310159c1c1b826feb63a097910bd0a5'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-riscv64'; 			sha256='eacbc70fd96c4c9a20bd58fc91a756372ece659211b9f566da33e15112c0b2af'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-s390x'; 			sha256='23a643f8994c945683f62669cd0f44bc106d3312ea04c3dda39d7514f0b1035e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:1445a503f72c73d6089a1119111ac23a281bc485cb856ca4679fe872c1a9ac8f`  
		Last Modified: Thu, 07 Mar 2024 18:50:58 GMT  
		Size: 2.0 MB (2019674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15768397550ab4bff548e50cb3f24c0a65a8e000b6e0f00a9930bd55c3889118`  
		Last Modified: Thu, 07 Mar 2024 18:50:57 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c4e815474b167ef0027b9bf9f1401500f0b730de65b12a8cfb7b019aa6bc70a`  
		Last Modified: Thu, 07 Mar 2024 18:51:59 GMT  
		Size: 15.5 MB (15459114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:498cbfe675db03fbba27922abf6cdfe04d67abc37cdc5661c2b83847a0e9595c`  
		Last Modified: Thu, 07 Mar 2024 18:52:00 GMT  
		Size: 16.3 MB (16349459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31173aeb3064c2067c3eeee8c2aa7bcad1c33efa7ace7728f414e76f6a2c15a5`  
		Last Modified: Thu, 07 Mar 2024 18:52:00 GMT  
		Size: 16.6 MB (16643002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8be9544bdba034068af854ec8b8d43d61db1eaa278476359eb325b9574dc9139`  
		Last Modified: Thu, 07 Mar 2024 18:51:59 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df633ccbc910e533e7b1d5e1894a12bb6df9dff2bf7f127b70db7d93d9af013`  
		Last Modified: Thu, 07 Mar 2024 18:52:00 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e355faf45be3adf608cb72a4d2190e7f90d573efadc5b695ed5b0997cd545dd`  
		Last Modified: Thu, 07 Mar 2024 18:52:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad61385ba1a834982739ceed5245bc475d27b6d86af07f447d4bf98566fdd5fc`  
		Last Modified: Thu, 07 Mar 2024 22:01:29 GMT  
		Size: 12.6 MB (12626851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:867019ac11c5ca6170035d9bfb28628a94ee17e4a7512420569de85154845b5c`  
		Last Modified: Thu, 07 Mar 2024 22:01:28 GMT  
		Size: 98.4 KB (98382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8a131949ec896f4361c01fd5f4c997c3e339944c97d2ebe39dd11aaf8e3d3b2`  
		Last Modified: Thu, 07 Mar 2024 22:01:28 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d3948c41ef086cda8bdaee48dd59de337810605032c5bdf9516efa56def4075`  
		Last Modified: Thu, 07 Mar 2024 22:01:30 GMT  
		Size: 50.1 MB (50076175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39fd8d00326e3cc7f9ccc45659669c12a82b0b37003af4ff440055990a07effe`  
		Last Modified: Thu, 07 Mar 2024 22:01:29 GMT  
		Size: 1.5 KB (1510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:831e21a83945aaeacf1447ae4e2986e95a59bc7c249bae7e1cdabe869c3201e7`  
		Last Modified: Thu, 07 Mar 2024 22:01:30 GMT  
		Size: 3.2 KB (3250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:077eaef0fd877a076621db99cc4a69f6050eb967aaba0b6f10d2fd42a2c4bfd8`  
		Last Modified: Thu, 07 Mar 2024 22:59:07 GMT  
		Size: 1.0 MB (1022483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc7bd5253bc965d9d70e0d717b79c6c01bd227928baf5499ea88dfb577531811`  
		Last Modified: Thu, 07 Mar 2024 22:59:07 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98d810ac7da09c2318228ad7b8568fbb64418aee373cb79db0d5c4504f9259b8`  
		Last Modified: Thu, 07 Mar 2024 22:59:07 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:129ba5538f1b1ad8da0cd58bfb074ba151353d3245e790e8a01e86da0d29b561`  
		Last Modified: Thu, 07 Mar 2024 22:59:09 GMT  
		Size: 22.5 MB (22476095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:838dd3b2513cbe6fffdb67b1ae720319b6008d8beab9d3a6430d1ddd4545cc73`  
		Last Modified: Thu, 07 Mar 2024 22:59:08 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:24-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:d2d692cb0b2b5cb4888bed25b9bab62c660de6c09e90664e42cbdd93cdd873fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **928.9 KB (928887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:063c0a702dab406a1bc2054b9f6ccddcc87fccf0e28867d5933494774be542c6`

```dockerfile
```

-	Layers:
	-	`sha256:3a40058af6a319f6f0144cf2c325457e6a213c5e191b55e615241b47509cf53a`  
		Last Modified: Thu, 07 Mar 2024 22:59:06 GMT  
		Size: 895.9 KB (895882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b1a0ba6153f829ddda6f242d1ca1f27fe10608464316d9ca1f7fbfa4b49c304`  
		Last Modified: Thu, 07 Mar 2024 22:59:06 GMT  
		Size: 33.0 KB (33005 bytes)  
		MIME: application/vnd.in-toto+json
