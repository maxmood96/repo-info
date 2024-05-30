## `docker:26-dind-rootless`

```console
$ docker pull docker@sha256:ba34bb01f29e9bdedb25ad291254d68e04a681f561ffa9851b02fe095bb9a40e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:26-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:4a223338840fe01f1c0b68f46ef0d4342ede182d9eac12e86addf21a20cba3f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.8 MB (151810412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6ce8bb15b8c6f875055ce8ee8ed72d1d4d223e71c31021b11045ba1533d4b42`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 16 May 2024 16:36:41 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Thu, 16 May 2024 16:36:41 GMT
CMD ["/bin/sh"]
# Thu, 16 May 2024 16:36:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 16 May 2024 16:36:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 16 May 2024 16:36:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 16 May 2024 16:36:41 GMT
ENV DOCKER_VERSION=26.1.3
# Thu, 16 May 2024 16:36:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 16 May 2024 16:36:41 GMT
ENV DOCKER_BUILDX_VERSION=0.14.1
# Thu, 16 May 2024 16:36:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-amd64'; 			sha256='68e4f8895331ade982de8085a8c137b8af65f3ef95040b6c6113552243638508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-arm-v6'; 			sha256='afa9324a987d71891a8a55d33fa913e4464377c71e7cc84ba68a5d4c5e803f74'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-arm-v7'; 			sha256='32f0f7d30e498c1461b97b2591e5ed348e69b6d864243a838db6d2e6dc08144d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-arm64'; 			sha256='82e776e50a84293c160e8c89c125b7a86295c7aa7f30751d6a7c051c171762c1'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-ppc64le'; 			sha256='64b62a17df3b0cd5bf88a1bc3f83cd50ebd56b403c2ebf4668b5d697fd324bc0'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-riscv64'; 			sha256='32042b4dba38724404a063ee9851ebea1c85b46ebbfb58e7350ece04975fdc9c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-s390x'; 			sha256='c273b1801cdb2c78079f9c33ecec266d5104973254e4e152d0205f14d7bf7bfc'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 16 May 2024 16:36:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.1
# Thu, 16 May 2024 16:36:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-x86_64'; 			sha256='ddc876fe2a89d5b7ea455146b0975bfe52904eecba9b192193377d6f99d69ad9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-armv6'; 			sha256='5f244291153cdd7facfe5007aa37f393d139c245b870025b8e86ef88a8de2705'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-armv7'; 			sha256='9dcfa9523dc912370417b7ccc3d81900bbb98dd9addbff0d218398bbe9078bbd'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-aarch64'; 			sha256='16e93b9c2fc147d29ca1acbb8ceab6a50a0e26af777f43dc7a753cb883142617'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-ppc64le'; 			sha256='f351bfdbb6bb9d18b33672ccba6dd31c53a3bd1b81f9e9052fc6d9125e7d5719'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-riscv64'; 			sha256='9940bd7533bcbd087d5301b8348136bc8922aa75739e3e359d8367e2f6dd7005'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-s390x'; 			sha256='6f4b6bb51987b2f61b91cfe4017a8d162e86b82ba3ae074b99b06a1ebe4387ed'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 16 May 2024 16:36:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 16 May 2024 16:36:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 May 2024 16:36:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 16 May 2024 16:36:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 16 May 2024 16:36:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 May 2024 16:36:41 GMT
CMD ["sh"]
# Thu, 16 May 2024 16:36:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 16 May 2024 16:36:41 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 16 May 2024 16:36:41 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 16 May 2024 16:36:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 16 May 2024 16:36:41 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 16 May 2024 16:36:41 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 16 May 2024 16:36:41 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 May 2024 16:36:41 GMT
VOLUME [/var/lib/docker]
# Thu, 16 May 2024 16:36:41 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 16 May 2024 16:36:41 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 16 May 2024 16:36:41 GMT
CMD []
# Thu, 16 May 2024 16:36:41 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Thu, 16 May 2024 16:36:41 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 16 May 2024 16:36:41 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 16 May 2024 16:36:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-26.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-26.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 16 May 2024 16:36:41 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 16 May 2024 16:36:41 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 16 May 2024 16:36:41 GMT
USER rootless
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:709fdef6a978cfbb39dd756c07e1a0ed5f0a42d4dc199bd9020866de914411da`  
		Last Modified: Wed, 29 May 2024 21:59:08 GMT  
		Size: 2.0 MB (2010488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee0e04186d54761ba365ffedecc9e7264f8e28d05203b2699d1727e3aa26735`  
		Last Modified: Wed, 29 May 2024 21:59:08 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5040cb473dd872951b8769f68e9e44087a1a2096a5420a861eb9566b1bf6b119`  
		Last Modified: Wed, 29 May 2024 21:59:08 GMT  
		Size: 18.0 MB (18031641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033d787e83ee73cbbc8805fb05618ad939dfc2236e149b8d63b69a39b8ec437f`  
		Last Modified: Wed, 29 May 2024 21:59:08 GMT  
		Size: 18.1 MB (18089104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca0e4ad1d5fbd6b290e5d760751f7776cbdaaa75cd734d349b9ee0a96d9b4ba3`  
		Last Modified: Wed, 29 May 2024 21:59:09 GMT  
		Size: 18.8 MB (18776603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:addd3fa802ed986e5ff024f772b4deb90df1ed0e04c2654aa61242748754f152`  
		Last Modified: Wed, 29 May 2024 21:59:09 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa82f68d13195fa56e1ef2f545edcbc253f102e8ef4c1bb98d761b1765d35696`  
		Last Modified: Wed, 29 May 2024 21:59:09 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945935a844942911fa16597c1b5d770c9b88a1e6c78c060238e65dbe75e8f73f`  
		Last Modified: Wed, 29 May 2024 21:59:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb849552362fa22cb8f22daab50414f3c3667489b615801f900502d8cf6faa19`  
		Last Modified: Wed, 29 May 2024 23:00:39 GMT  
		Size: 12.5 MB (12508608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b8dd1c36edff29943c3c5176e35bc796ebf9e4c8af7e33a796c74efb0edcf61`  
		Last Modified: Wed, 29 May 2024 23:00:39 GMT  
		Size: 89.2 KB (89188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c2644864cc446bc53b62b09f34cb7b3e22aea5ba02572528b852b337a02f7a1`  
		Last Modified: Wed, 29 May 2024 23:00:39 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:934d8d2105be3d0d74c592cb88b7ab8dc1329a2a4f164cf4c8c432665c3241f2`  
		Last Modified: Wed, 29 May 2024 23:00:40 GMT  
		Size: 56.7 MB (56711333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f324d3ecf330c9cd5d3f351ea4fc42f48c2c815a737752466f4a6f2032010f`  
		Last Modified: Wed, 29 May 2024 23:00:40 GMT  
		Size: 1.5 KB (1509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4382da9867cd89ca067dc2f27962640abadfd96f8c19461d09a619a2ee3b314`  
		Last Modified: Wed, 29 May 2024 23:00:40 GMT  
		Size: 3.3 KB (3253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d13bb8cc1a77846e3e74e4734e59f262534706661681ac93eb9c07ad606a61`  
		Last Modified: Wed, 29 May 2024 23:57:02 GMT  
		Size: 980.9 KB (980948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a8940651f96c78cb4897bed24fde0077ffce86bc521aeeb4591391af6d2a06`  
		Last Modified: Wed, 29 May 2024 23:57:01 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef3ce8a6c2b8698f2d9bc038a8751f27b8aa209e8c220412b7c0f5dc2a94ff0`  
		Last Modified: Wed, 29 May 2024 23:57:01 GMT  
		Size: 1.1 KB (1051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef01527cda44f450bb84c48aeef42d07c6414f3721004401da5d0f20b58f201`  
		Last Modified: Wed, 29 May 2024 23:57:02 GMT  
		Size: 21.0 MB (20981098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b53a226ac90b34effb99b512178983c5a92c16107e6845b3dddee00c3917d33`  
		Last Modified: Wed, 29 May 2024 23:57:02 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:26-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:103f7f4960fbe6daaf17f028483bbbb49b2a0843ef7a148b68261df410628e58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7329b3dae726a040bfe039aae64b713e759fe49066062ca4afa6091d1069a7d8`

```dockerfile
```

-	Layers:
	-	`sha256:2bb7d6c20b1d9e580d8c93f29978ef9ac20a924903b3c9520941613ad190f6f5`  
		Last Modified: Wed, 29 May 2024 23:57:01 GMT  
		Size: 30.5 KB (30537 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:26-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:07c6c2f291d0a933deb0d63be7749a97e2a8409d5034407fd4140c17f2030e46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.0 MB (145965782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88a53e90a846b92ceb37216cf7a4b64e70e86b7e375ad3f7916486ed5d512290`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 16 May 2024 16:36:41 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Thu, 16 May 2024 16:36:41 GMT
CMD ["/bin/sh"]
# Thu, 16 May 2024 16:36:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 16 May 2024 16:36:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 16 May 2024 16:36:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 16 May 2024 16:36:41 GMT
ENV DOCKER_VERSION=26.1.3
# Thu, 16 May 2024 16:36:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 16 May 2024 16:36:41 GMT
ENV DOCKER_BUILDX_VERSION=0.14.1
# Thu, 16 May 2024 16:36:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-amd64'; 			sha256='68e4f8895331ade982de8085a8c137b8af65f3ef95040b6c6113552243638508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-arm-v6'; 			sha256='afa9324a987d71891a8a55d33fa913e4464377c71e7cc84ba68a5d4c5e803f74'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-arm-v7'; 			sha256='32f0f7d30e498c1461b97b2591e5ed348e69b6d864243a838db6d2e6dc08144d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-arm64'; 			sha256='82e776e50a84293c160e8c89c125b7a86295c7aa7f30751d6a7c051c171762c1'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-ppc64le'; 			sha256='64b62a17df3b0cd5bf88a1bc3f83cd50ebd56b403c2ebf4668b5d697fd324bc0'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-riscv64'; 			sha256='32042b4dba38724404a063ee9851ebea1c85b46ebbfb58e7350ece04975fdc9c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-s390x'; 			sha256='c273b1801cdb2c78079f9c33ecec266d5104973254e4e152d0205f14d7bf7bfc'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 16 May 2024 16:36:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.1
# Thu, 16 May 2024 16:36:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-x86_64'; 			sha256='ddc876fe2a89d5b7ea455146b0975bfe52904eecba9b192193377d6f99d69ad9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-armv6'; 			sha256='5f244291153cdd7facfe5007aa37f393d139c245b870025b8e86ef88a8de2705'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-armv7'; 			sha256='9dcfa9523dc912370417b7ccc3d81900bbb98dd9addbff0d218398bbe9078bbd'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-aarch64'; 			sha256='16e93b9c2fc147d29ca1acbb8ceab6a50a0e26af777f43dc7a753cb883142617'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-ppc64le'; 			sha256='f351bfdbb6bb9d18b33672ccba6dd31c53a3bd1b81f9e9052fc6d9125e7d5719'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-riscv64'; 			sha256='9940bd7533bcbd087d5301b8348136bc8922aa75739e3e359d8367e2f6dd7005'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-s390x'; 			sha256='6f4b6bb51987b2f61b91cfe4017a8d162e86b82ba3ae074b99b06a1ebe4387ed'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 16 May 2024 16:36:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 16 May 2024 16:36:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 May 2024 16:36:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 16 May 2024 16:36:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 16 May 2024 16:36:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 May 2024 16:36:41 GMT
CMD ["sh"]
# Thu, 16 May 2024 16:36:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 16 May 2024 16:36:41 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 16 May 2024 16:36:41 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 16 May 2024 16:36:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 16 May 2024 16:36:41 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 16 May 2024 16:36:41 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 16 May 2024 16:36:41 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 May 2024 16:36:41 GMT
VOLUME [/var/lib/docker]
# Thu, 16 May 2024 16:36:41 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 16 May 2024 16:36:41 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 16 May 2024 16:36:41 GMT
CMD []
# Thu, 16 May 2024 16:36:41 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Thu, 16 May 2024 16:36:41 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 16 May 2024 16:36:41 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 16 May 2024 16:36:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-26.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-26.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 16 May 2024 16:36:41 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 16 May 2024 16:36:41 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 16 May 2024 16:36:41 GMT
USER rootless
```

-	Layers:
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11bff5120b86ac33e19177ec896d4d5049e656877d728c74bf1d6ad51be389ab`  
		Last Modified: Thu, 30 May 2024 05:24:10 GMT  
		Size: 2.0 MB (2006605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:177edc7d05485b510d768d84b0082dd4b3e7262dd9327fadf7299fa577e0ab33`  
		Last Modified: Thu, 30 May 2024 05:24:09 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e36e71ac0c5744edf9f5293e56145f2978cfd06fa251455ef556a96d9c2ddf`  
		Last Modified: Thu, 30 May 2024 05:24:11 GMT  
		Size: 17.0 MB (16988435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c970f5825c12d6151537ac916f08cf416bd519b99f25755d25718ba9c77c9c8e`  
		Last Modified: Thu, 30 May 2024 05:24:10 GMT  
		Size: 16.5 MB (16450837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac2c50cd8cc664f8813eebe6a85dcc9bfe4fbaedea1812c898cadab5a67bc24`  
		Last Modified: Thu, 30 May 2024 05:24:11 GMT  
		Size: 17.1 MB (17144848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3ee43940be90e31375c79d6413efd19884065f61af7233c07219da552a21e06`  
		Last Modified: Thu, 30 May 2024 05:24:11 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17a9190f34d19a17b65ade2fb55f03b026561c0427d7cc5f5018611fb86a3690`  
		Last Modified: Thu, 30 May 2024 05:24:12 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739fd8128a20396042fdffef649214ab40b9a6926b9befcca085fd295e85929c`  
		Last Modified: Thu, 30 May 2024 05:24:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a177ff2265dd70144c348341a4bda55145b5a9740e8bf783bae1cb393fb6883c`  
		Last Modified: Thu, 30 May 2024 18:49:39 GMT  
		Size: 13.0 MB (12993418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52b56673caa935041fa5a7f797ef3d4834d2cf2bde4abfac52a169282fa6404`  
		Last Modified: Thu, 30 May 2024 18:49:38 GMT  
		Size: 98.6 KB (98617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1877b3ac7f6e2a745964eb156ff0e2b13aa69f5926322578e146f97479c97f2b`  
		Last Modified: Thu, 30 May 2024 18:49:38 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4693073f736ef874f32ceb42b95ccb7e1f08d3481e0e2d4826ecd9fb474de5d5`  
		Last Modified: Thu, 30 May 2024 18:49:40 GMT  
		Size: 52.3 MB (52318654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16fa752890d741a853355fed3ad20dc0ad9f7c3f0eee564100456ec06ecad84c`  
		Last Modified: Thu, 30 May 2024 18:49:39 GMT  
		Size: 1.5 KB (1509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d15e15f61b9842ee3d5b4ed0b2a1818565027ed10384b188481368fdeff7ed5c`  
		Last Modified: Thu, 30 May 2024 18:49:39 GMT  
		Size: 3.3 KB (3254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb17226a174c259eefb3b97b9f658a17e1fb8efdacd703e7920a18c5dd60ef7`  
		Last Modified: Thu, 30 May 2024 20:51:47 GMT  
		Size: 1.0 MB (1023073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e33b6f8b36772df4aa28d5044eaea00789d3cac9efe3f69bffd2880470662a7`  
		Last Modified: Thu, 30 May 2024 20:51:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28eb0219c416eaf60f9aea69c7259a78c71115fe24ef0e876bb4656993894bf8`  
		Last Modified: Thu, 30 May 2024 20:51:46 GMT  
		Size: 1.1 KB (1052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af12eab346d0730ea2dff461c16fbfeda3f905da8f51fdf21b2715d151d66980`  
		Last Modified: Thu, 30 May 2024 20:51:47 GMT  
		Size: 22.8 MB (22845209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ef10bf62329eb84dd8d077d2fe4a2635c77f48f41b8247e345f8c351d006f92`  
		Last Modified: Thu, 30 May 2024 20:51:47 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:26-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:7153ea834e59ca1a625ce9b2cf9a2b47fac2e787b5daeff4504fb153e0ffb66c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 KB (30963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6502f1262bc5facea8a775ddadeda8daac12aec0cce9314aa2dcbc4f8ede525a`

```dockerfile
```

-	Layers:
	-	`sha256:e83ec4c51446e190c93e84c226fe5c2c5127f3650746d96ae5e2dfec8d64edfc`  
		Last Modified: Thu, 30 May 2024 20:51:47 GMT  
		Size: 31.0 KB (30963 bytes)  
		MIME: application/vnd.in-toto+json
