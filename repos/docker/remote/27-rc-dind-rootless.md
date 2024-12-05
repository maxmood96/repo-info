## `docker:27-rc-dind-rootless`

```console
$ docker pull docker@sha256:5c293fdc092fde1bd8a8127908a31efacb504f97388d31b1cc6b921e765f2953
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:27-rc-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:d8e8dc99bc42059208ea1495d87ea0dcc298c7f3d815631d73b160b351d1a2e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.8 MB (157769004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16b7e86b8e6ce620fa48360e6a292ea62e49cf7e2bf38f725909abece839365e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 04 Dec 2024 23:15:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 04 Dec 2024 23:15:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 04 Dec 2024 23:15:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 04 Dec 2024 23:15:41 GMT
ENV DOCKER_VERSION=27.4.0-rc.4
# Wed, 04 Dec 2024 23:15:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.4.0-rc.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.4.0-rc.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.4.0-rc.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.4.0-rc.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 04 Dec 2024 23:15:41 GMT
ENV DOCKER_BUILDX_VERSION=0.19.1
# Wed, 04 Dec 2024 23:15:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-amd64'; 			sha256='153eace3d30c9efe9a7b94ea06c9d15ace59c8e6268d3481b8c175bd3df020f9'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm-v6'; 			sha256='6f7e15248535bcae3730444bbf6164d076b9df7491b89040153f12d9e93a9f6b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm-v7'; 			sha256='b2bb531e4f217c94951173a9e403002f6b18868227f09715c295a63f837cf5e4'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm64'; 			sha256='9ecffda0a356957827de6b4ed86b151b420e84f81b2a58e2e2735506336ab891'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-ppc64le'; 			sha256='10ab6f3effac50e4150a3288013ad34e3cf4a0b307c7ffbf48dda9a5813e1bda'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-riscv64'; 			sha256='c89af9a424a109abd52205544377a9eac6027bb91c2fbe91d02cf91a6b53f7e8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-s390x'; 			sha256='cfaf3883fe66787297c8df69e25f95246a74d630b5e2b6627cc563246f94b4f9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 04 Dec 2024 23:15:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.31.0
# Wed, 04 Dec 2024 23:15:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-x86_64'; 			sha256='8b5d2cb358427e654ada217cfdfedc00c4273f7a8ee07f27003a18d15461b6cd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-armv6'; 			sha256='5812e2fe5e8fdbaa984679ad5809779a0a0f054a423a63f6d15167b5d643db43'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-armv7'; 			sha256='f8271667b0b0337cdd11a0f2920089f09b06bb4e5e3988e66ab23b5d18c3fa18'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-aarch64'; 			sha256='a1f85584584d0c3c489f31f015c97eb543f1f0949fdc5ce3ded88c05a5188729'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-ppc64le'; 			sha256='0f6149bb38f1722dea511fc80228d9bc7c3504cedaf662e09033d3aa89c70d93'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-riscv64'; 			sha256='f3f9a94dc4bb8773bdcd70680a177171e8aeb15b98b979fe51b447a5c97c52d1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-s390x'; 			sha256='6635a146193c797ed11ba3a6e9d7b1da5df0f1215ccd3c52f712001e58413f20'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 04 Dec 2024 23:15:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 04 Dec 2024 23:15:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 04 Dec 2024 23:15:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 04 Dec 2024 23:15:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 04 Dec 2024 23:15:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 04 Dec 2024 23:15:41 GMT
CMD ["sh"]
# Wed, 04 Dec 2024 23:15:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 04 Dec 2024 23:15:41 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 04 Dec 2024 23:15:41 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 04 Dec 2024 23:15:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.4.0-rc.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.4.0-rc.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.4.0-rc.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.4.0-rc.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 04 Dec 2024 23:15:41 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 04 Dec 2024 23:15:41 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 04 Dec 2024 23:15:41 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 04 Dec 2024 23:15:41 GMT
VOLUME [/var/lib/docker]
# Wed, 04 Dec 2024 23:15:41 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 04 Dec 2024 23:15:41 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 04 Dec 2024 23:15:41 GMT
CMD []
# Wed, 04 Dec 2024 23:15:41 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Wed, 04 Dec 2024 23:15:41 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 04 Dec 2024 23:15:41 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 04 Dec 2024 23:15:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-27.4.0-rc.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-27.4.0-rc.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 04 Dec 2024 23:15:41 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 04 Dec 2024 23:15:41 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 04 Dec 2024 23:15:41 GMT
USER rootless
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd21b15bbd4f1eec87b8472942d7938153c089164bf5a69c0e0856154295575`  
		Last Modified: Thu, 05 Dec 2024 01:27:32 GMT  
		Size: 7.9 MB (7889984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:730abdaa54c4b34e02331e1049be567fcafc7a055a03973cc006af52860046bc`  
		Last Modified: Thu, 05 Dec 2024 01:27:31 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bae9998d48cc26c147898ed7fc62864176c6510e92cb6bc77fab0ee798f8ce4d`  
		Last Modified: Thu, 05 Dec 2024 01:27:32 GMT  
		Size: 18.7 MB (18670112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d90d7f6b820c0d42567fb5fd6473c7e02bb259c3d42a1918d576dc2d8b99bdc`  
		Last Modified: Thu, 05 Dec 2024 01:27:32 GMT  
		Size: 18.8 MB (18797145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf9388af133ec6cd03b483f9e4b68d054afe9aa4ff81fe6afc5f228395c79699`  
		Last Modified: Thu, 05 Dec 2024 01:27:33 GMT  
		Size: 19.2 MB (19188652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0a0a9ba85388ad317ebab206be49bd4215c2168683babbad003dff85ca1770`  
		Last Modified: Thu, 05 Dec 2024 01:27:33 GMT  
		Size: 535.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:718e3eec59449a506a400d58f5222ae31fb77ea13cd357d42a167a6faaf5f055`  
		Last Modified: Thu, 05 Dec 2024 01:27:33 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2b55d95c50d8573ea047a7480a6253b94d290ad4914d5cdc27689d38d9b3166`  
		Last Modified: Thu, 05 Dec 2024 01:27:33 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3c97bd87e977fa900b8f69f3dfd8b16c593ce95c1d9b7c1e2e8f57841b89c3e`  
		Last Modified: Thu, 05 Dec 2024 02:07:40 GMT  
		Size: 9.1 MB (9067244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52deb432040d55863651708d5a6fdd264402ba4eb113778a127af71190abdb59`  
		Last Modified: Thu, 05 Dec 2024 02:07:39 GMT  
		Size: 89.2 KB (89237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf9cac15a7840e4f8250126d511ccef9d1618ab3d75d77b6841a07df2cc3c3ac`  
		Last Modified: Thu, 05 Dec 2024 02:07:39 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c540fcf1912b4605022bd9b1e9b311bb001dc8231a76e4b749ac8124d329433`  
		Last Modified: Thu, 05 Dec 2024 02:07:40 GMT  
		Size: 58.1 MB (58147991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50bd05e6c52995ab5f16f12e8a1d1d3fe9db2a73fa06ba919b75d025d9060e8f`  
		Last Modified: Thu, 05 Dec 2024 02:07:40 GMT  
		Size: 1.5 KB (1511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe3460de1bfb3a4dab1df07391a3bfe266447694f4a8268c154f333cd720c45e`  
		Last Modified: Thu, 05 Dec 2024 02:07:40 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd15c14726345cf2e334a7e669b6b17603b292fb11d290d878ef0be4c2d9c152`  
		Last Modified: Thu, 05 Dec 2024 03:07:26 GMT  
		Size: 981.6 KB (981581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3927f82b45097cbefa53ff7371dcb5dd3706c8f059246a7bbd0e0625fe72a3`  
		Last Modified: Thu, 05 Dec 2024 03:07:25 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e72f91c4732feaf44e3941e300e3a36ed0f8227a3111c15d77ad9a25a48c7aab`  
		Last Modified: Thu, 05 Dec 2024 03:07:25 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b65a362102590db6d0a4fcc929a7058300a38ce311bce28c6e1fdd2faac06e`  
		Last Modified: Thu, 05 Dec 2024 03:07:26 GMT  
		Size: 21.3 MB (21303865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e72156491051357176c46994a1bef9edfc5348049aa7fc52b2e09dc3e21ecf28`  
		Last Modified: Thu, 05 Dec 2024 03:07:26 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:74f495c289681888baf38edc0c57c460dc13c3a4d8e17f61c27871f840427c20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.4 KB (30370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:297f910a98db2d26da14064801c147a8591d1e04bc98f35a634d2eb3667e8917`

```dockerfile
```

-	Layers:
	-	`sha256:1506bdeef616daa16f985296bcdc34fda840a4e34142ba63d9c6aeffc866af24`  
		Last Modified: Thu, 05 Dec 2024 03:07:25 GMT  
		Size: 30.4 KB (30370 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-rc-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:5453c18f739723c43f84367a8c71f8c94032beeca884f307fb71aa6af470bd73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.2 MB (152202970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eebde0e3c9e1e965b97c636d3ecf143b3f51b4d931dc6f01701f6dd53046aafb`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 04 Dec 2024 23:15:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 04 Dec 2024 23:15:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 04 Dec 2024 23:15:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 04 Dec 2024 23:15:41 GMT
ENV DOCKER_VERSION=27.4.0-rc.4
# Wed, 04 Dec 2024 23:15:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.4.0-rc.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.4.0-rc.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.4.0-rc.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.4.0-rc.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 04 Dec 2024 23:15:41 GMT
ENV DOCKER_BUILDX_VERSION=0.19.1
# Wed, 04 Dec 2024 23:15:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-amd64'; 			sha256='153eace3d30c9efe9a7b94ea06c9d15ace59c8e6268d3481b8c175bd3df020f9'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm-v6'; 			sha256='6f7e15248535bcae3730444bbf6164d076b9df7491b89040153f12d9e93a9f6b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm-v7'; 			sha256='b2bb531e4f217c94951173a9e403002f6b18868227f09715c295a63f837cf5e4'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm64'; 			sha256='9ecffda0a356957827de6b4ed86b151b420e84f81b2a58e2e2735506336ab891'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-ppc64le'; 			sha256='10ab6f3effac50e4150a3288013ad34e3cf4a0b307c7ffbf48dda9a5813e1bda'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-riscv64'; 			sha256='c89af9a424a109abd52205544377a9eac6027bb91c2fbe91d02cf91a6b53f7e8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-s390x'; 			sha256='cfaf3883fe66787297c8df69e25f95246a74d630b5e2b6627cc563246f94b4f9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 04 Dec 2024 23:15:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.31.0
# Wed, 04 Dec 2024 23:15:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-x86_64'; 			sha256='8b5d2cb358427e654ada217cfdfedc00c4273f7a8ee07f27003a18d15461b6cd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-armv6'; 			sha256='5812e2fe5e8fdbaa984679ad5809779a0a0f054a423a63f6d15167b5d643db43'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-armv7'; 			sha256='f8271667b0b0337cdd11a0f2920089f09b06bb4e5e3988e66ab23b5d18c3fa18'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-aarch64'; 			sha256='a1f85584584d0c3c489f31f015c97eb543f1f0949fdc5ce3ded88c05a5188729'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-ppc64le'; 			sha256='0f6149bb38f1722dea511fc80228d9bc7c3504cedaf662e09033d3aa89c70d93'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-riscv64'; 			sha256='f3f9a94dc4bb8773bdcd70680a177171e8aeb15b98b979fe51b447a5c97c52d1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-s390x'; 			sha256='6635a146193c797ed11ba3a6e9d7b1da5df0f1215ccd3c52f712001e58413f20'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 04 Dec 2024 23:15:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 04 Dec 2024 23:15:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 04 Dec 2024 23:15:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 04 Dec 2024 23:15:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 04 Dec 2024 23:15:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 04 Dec 2024 23:15:41 GMT
CMD ["sh"]
# Wed, 04 Dec 2024 23:15:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 04 Dec 2024 23:15:41 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 04 Dec 2024 23:15:41 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 04 Dec 2024 23:15:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.4.0-rc.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.4.0-rc.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.4.0-rc.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.4.0-rc.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 04 Dec 2024 23:15:41 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 04 Dec 2024 23:15:41 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 04 Dec 2024 23:15:41 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 04 Dec 2024 23:15:41 GMT
VOLUME [/var/lib/docker]
# Wed, 04 Dec 2024 23:15:41 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 04 Dec 2024 23:15:41 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 04 Dec 2024 23:15:41 GMT
CMD []
# Wed, 04 Dec 2024 23:15:41 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Wed, 04 Dec 2024 23:15:41 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 04 Dec 2024 23:15:41 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 04 Dec 2024 23:15:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-27.4.0-rc.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-27.4.0-rc.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 04 Dec 2024 23:15:41 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 04 Dec 2024 23:15:41 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 04 Dec 2024 23:15:41 GMT
USER rootless
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a009e17f4dc05dabee0d38a9f3e3255fe4e8a9678f58c7a159fc2c2ca77a4d`  
		Last Modified: Thu, 05 Dec 2024 01:27:21 GMT  
		Size: 8.0 MB (7998249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1595925a5a90fcfa4f940a135fb5e1db4120b731667b85133d5bdb28898e034`  
		Last Modified: Thu, 05 Dec 2024 01:27:21 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1af072d56227d8b1b7ae55b503b511312941f2bd1c463de55ee805f1b2f5531`  
		Last Modified: Thu, 05 Dec 2024 01:27:22 GMT  
		Size: 17.6 MB (17619258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8b40c3a1432393d6915caa5950700e728cb6dc40aa3844e5666a495fc26387b`  
		Last Modified: Thu, 05 Dec 2024 01:27:22 GMT  
		Size: 17.1 MB (17094311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d83bb451ed8682bdfa162bc305e29f07855bd243c332d2ccecb7867ce1a884`  
		Last Modified: Thu, 05 Dec 2024 01:27:23 GMT  
		Size: 17.5 MB (17533147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ceb2e075ab6e99f2ed7470ae3b098f28507369156b4def4bfbef699e9052828`  
		Last Modified: Thu, 05 Dec 2024 01:27:22 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d05d15cafcc32afc225db5e5208c0475274e060392abeb5a5c2affbc78fb0a9`  
		Last Modified: Thu, 05 Dec 2024 01:27:23 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f23081dbeded38a453bb4cfad87df7eb60cb858cf380773b2b9fc2d79c68747`  
		Last Modified: Thu, 05 Dec 2024 01:27:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a1fbd643ec863534d2076bd921af4dc3d0a27ee01be7eebf3f0e845e9bbf751`  
		Last Modified: Thu, 05 Dec 2024 02:07:31 GMT  
		Size: 9.9 MB (9854902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa023838400b341639dd075987f185af1649ad505e4b0d01296e04806d866a9c`  
		Last Modified: Thu, 05 Dec 2024 02:07:30 GMT  
		Size: 98.7 KB (98656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ee242d41090660f721bd48e581cc91f6b121a1a281fb3b51eaa536a4b9fbb48`  
		Last Modified: Thu, 05 Dec 2024 02:07:30 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60da17b33939355ad6bc487efe32bc67b34ffcdef2bf58705553177b7d786341`  
		Last Modified: Thu, 05 Dec 2024 02:07:32 GMT  
		Size: 53.7 MB (53728442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60c72799557e140e2b5870d23e9f73276ebecf8a740fc0679c41ac54d61b33a`  
		Last Modified: Thu, 05 Dec 2024 02:07:31 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:565e96f3fcee6623616b67f46f2f71f9bfec23f7031f59a5137eff3e6768759c`  
		Last Modified: Thu, 05 Dec 2024 02:07:31 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce4da844fb42e42a8c86548d4cb67c35c73c613f1c388a315cf21a650758b74`  
		Last Modified: Thu, 05 Dec 2024 03:07:22 GMT  
		Size: 1.0 MB (1023833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce5a2ec81430852b6e8755c407ad159fe5e1e99ffaa6a05a6bafcda6ca599b91`  
		Last Modified: Thu, 05 Dec 2024 03:07:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a5e511fa9bc1105db1f21983f95e0a9d51aa903159745c87b61cef92c9c0182`  
		Last Modified: Thu, 05 Dec 2024 03:07:22 GMT  
		Size: 1.1 KB (1051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a549965e2a5326c10103c7acec14d9f5a2ad3871cd27f5a8c95ba75c68caea`  
		Last Modified: Thu, 05 Dec 2024 03:07:23 GMT  
		Size: 23.2 MB (23155145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6315468cf3e2814ca6b85d644c1c3c9deb5d3e42829012696d08633316c7c90f`  
		Last Modified: Thu, 05 Dec 2024 03:07:23 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:f7ed037da3120cc47a592e328df5dea831b58e87e0ad785ac18c5aeea4922dde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:845d1b81552d9e9b09c5044224fdaf169ce5d95935088a32b0b8937392ce4a8b`

```dockerfile
```

-	Layers:
	-	`sha256:71ffdb7302790080f091ac13632c2fccde152c1bc3769f7bf46bea99879aa363`  
		Last Modified: Thu, 05 Dec 2024 03:07:22 GMT  
		Size: 30.5 KB (30527 bytes)  
		MIME: application/vnd.in-toto+json
