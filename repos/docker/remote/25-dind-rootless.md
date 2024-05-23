## `docker:25-dind-rootless`

```console
$ docker pull docker@sha256:1a73656417903d7253de681792e9ff20d00a50f344b611b0e1c65ae2babcc988
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:25-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:ecf47110c6fe9648c3c761846a14afdaeca81fec8201e08ff48f2123dc6cdb1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.6 MB (149625600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:670a3c30d245165b9e06be9c7f3ca0aedb9ecb2a115f4915fc2a26533ed9d6c9`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 19 Mar 2024 21:53:23 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Tue, 19 Mar 2024 21:53:23 GMT
CMD ["/bin/sh"]
# Tue, 19 Mar 2024 21:53:23 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
ENV DOCKER_VERSION=25.0.5
# Tue, 19 Mar 2024 21:53:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-25.0.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-25.0.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-25.0.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-25.0.5.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
ENV DOCKER_BUILDX_VERSION=0.14.1
# Tue, 19 Mar 2024 21:53:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-amd64'; 			sha256='68e4f8895331ade982de8085a8c137b8af65f3ef95040b6c6113552243638508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-arm-v6'; 			sha256='afa9324a987d71891a8a55d33fa913e4464377c71e7cc84ba68a5d4c5e803f74'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-arm-v7'; 			sha256='32f0f7d30e498c1461b97b2591e5ed348e69b6d864243a838db6d2e6dc08144d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-arm64'; 			sha256='82e776e50a84293c160e8c89c125b7a86295c7aa7f30751d6a7c051c171762c1'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-ppc64le'; 			sha256='64b62a17df3b0cd5bf88a1bc3f83cd50ebd56b403c2ebf4668b5d697fd324bc0'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-riscv64'; 			sha256='32042b4dba38724404a063ee9851ebea1c85b46ebbfb58e7350ece04975fdc9c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-s390x'; 			sha256='c273b1801cdb2c78079f9c33ecec266d5104973254e4e152d0205f14d7bf7bfc'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.0
# Tue, 19 Mar 2024 21:53:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-x86_64'; 			sha256='f3ba3bf1e4ab18e96c2d36526a075a02a78fb5f8e80d3e3ca9c5bf256d81d0a0'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-armv6'; 			sha256='ee467093d138f9c4d189b774552ef86ba253107bd91226b28f0c54edf62fe949'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-armv7'; 			sha256='8461b4d4a58eaaf04c4f482f0dabe57db9ef63229311a9583c6548b417f33c76'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-aarch64'; 			sha256='37a1c197fef5fda2a3df2d5ae0d7762ad2a00e30946ad06d4ad9fa8cef16d9e7'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-ppc64le'; 			sha256='faed2dd8f0568922dadf1a8fa155898d5be1feaa67568f2aa730a594ba6a44ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-riscv64'; 			sha256='71a09bd1980505a5f194cfab5df53bba55e493edf246f3ebb28cbfef8caf7715'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-s390x'; 			sha256='d38522261b481d7f20da7f80af67824afe2a1b54dd19215690febb0c49ad932d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 19 Mar 2024 21:53:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Mar 2024 21:53:23 GMT
CMD ["sh"]
# Tue, 19 Mar 2024 21:53:23 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-25.0.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-25.0.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-25.0.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-25.0.5.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 19 Mar 2024 21:53:23 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
VOLUME [/var/lib/docker]
# Tue, 19 Mar 2024 21:53:23 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 19 Mar 2024 21:53:23 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 19 Mar 2024 21:53:23 GMT
CMD []
# Tue, 19 Mar 2024 21:53:23 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-25.0.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-25.0.5.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 19 Mar 2024 21:53:23 GMT
USER rootless
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea6fac547c80e38613886768e157eb716571242d61a37dec1aabeee4bb8e7f0`  
		Last Modified: Wed, 22 May 2024 22:54:45 GMT  
		Size: 2.0 MB (2010473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512dfc90b83a8ec74ca4792e6840bd0835edc4db6a5c589663bf3ae3c02b67a1`  
		Last Modified: Wed, 22 May 2024 22:54:45 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d778da4f3c69a708d94aeb92a2c6b6a1401f699ed1f53885e9ede0451ca101`  
		Last Modified: Wed, 22 May 2024 22:54:45 GMT  
		Size: 16.9 MB (16902849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:990be585c6fe79b306b731919fc85aec7dcfa43912037c8161e43656d56501bb`  
		Last Modified: Wed, 22 May 2024 22:54:45 GMT  
		Size: 18.1 MB (18089094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0fe04470a02604ea5003cfb19d42d10a792437ecaa3bfe282d18a6334498b2f`  
		Last Modified: Wed, 22 May 2024 22:54:46 GMT  
		Size: 18.8 MB (18764665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1385b25639f95056b0a0ad39d03eb7c999f20a259860953cf6af2e66a0df433`  
		Last Modified: Wed, 22 May 2024 22:54:46 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a5cdab4c3e7ec5c3ff74649b3227b8d087997ea5602049589d7c1248c7035f9`  
		Last Modified: Wed, 22 May 2024 22:54:47 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5581d9f9b224472a78d4495a0215ce7e3be76cf1c7d4e79504d790a5ce8ec64f`  
		Last Modified: Wed, 22 May 2024 22:54:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3e8819721bf002b1b703131a208031f7ba26e7484af5743e83b8d448989bbc`  
		Last Modified: Wed, 22 May 2024 23:55:23 GMT  
		Size: 12.5 MB (12508620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6fdbd4a54bee901209da0c2f9bda20f4f5e5efa12d02702e02e716ca82c25ac`  
		Last Modified: Wed, 22 May 2024 23:55:23 GMT  
		Size: 89.2 KB (89183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35588ffe571d937c5046d9a1b42505e06f4a23b9ea45abac49633ba110dbcdb9`  
		Last Modified: Wed, 22 May 2024 23:55:23 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae944816a7fb7ad75d1d2b0e4e4b3b5adc173319fb488b9f3d45518834cd64fe`  
		Last Modified: Wed, 22 May 2024 23:55:24 GMT  
		Size: 55.7 MB (55662457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46a576f699a5adbcbe8a0bfe1f25a08455e1b09bc4b1c1842e5f26c55b321eb`  
		Last Modified: Wed, 22 May 2024 23:55:24 GMT  
		Size: 1.5 KB (1510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7660157b1d841fbcff7ee772753acf626560024283269bcb309afb35108194`  
		Last Modified: Wed, 22 May 2024 23:55:24 GMT  
		Size: 3.2 KB (3250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32248fb96b5ad056ce139d83b56785045a16b1fa86f009b03a47b3cf2cc2935d`  
		Last Modified: Thu, 23 May 2024 00:50:57 GMT  
		Size: 981.0 KB (980952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a867de9c93cb5c3d3345badc1d1121786f43a1934cd73149c537fe793be244ea`  
		Last Modified: Thu, 23 May 2024 00:50:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21973c4419b8be8d5d394618cd748907b4ec88ad8c9a65102e0d545e30e8479e`  
		Last Modified: Thu, 23 May 2024 00:50:58 GMT  
		Size: 1.1 KB (1051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d588533332b1d50738e7ecb15fceeff8f04916bb92169761e8e7f3c2748d689`  
		Last Modified: Thu, 23 May 2024 00:50:58 GMT  
		Size: 21.0 MB (20985920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0bf977aca99904c98ae3a054ec5ebdc24047895478e3a27264e220c756c897d`  
		Last Modified: Thu, 23 May 2024 00:50:58 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:25-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:bc0e349683bf65546fc10bddea1307aee7f78968cc812fb06444c7e447189001
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.7 KB (32729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaefb8437a5460e6237a5a4306c89df2eb2bdfe51933d7368d47c567dc154d76`

```dockerfile
```

-	Layers:
	-	`sha256:fbc65c9623215c21a1a3c0f08358a3d76380e5b3eb0ca9a56609261926ee0c76`  
		Last Modified: Thu, 23 May 2024 00:50:57 GMT  
		Size: 32.7 KB (32729 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:25-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:af7cbf5a0ab1b505a65c872e649f9479d3427ef38d8dc82e240d484caa0f2db8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.9 MB (144900449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7bdeec336fab1bc577cfd53a835f5ec2d98fb256eddee43ecda8aacdc2a4106`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Tue, 19 Mar 2024 21:53:23 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
ENV DOCKER_VERSION=25.0.5
# Tue, 19 Mar 2024 21:53:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-25.0.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-25.0.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-25.0.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-25.0.5.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
ENV DOCKER_BUILDX_VERSION=0.14.0
# Tue, 19 Mar 2024 21:53:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-amd64'; 			sha256='32f8f17eca35bf2efe6c0e47f40e4692a876f34531b421efc984799a5b41226e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-arm-v6'; 			sha256='7a23989eb26ad27e1b7c11a38dda6a8e6a94562969c19165cf8f49e70203ad20'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-arm-v7'; 			sha256='53b2d827510c6cff41503454caeb0d6613d5ed11201ba10f5ad6c22466cc178c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-arm64'; 			sha256='38bf0ea9c48743edb8243f14272be65a2bad7092228068337aea584309ea664c'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-ppc64le'; 			sha256='847e665e8f1fef3b85c6a5139d9bc57a81bae84d6a882d3ed71e2b5e2bd94bf6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-riscv64'; 			sha256='c853c01f71b6b778b430d985813069d1ca4f2b2e7e039723298350839a556d2b'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-s390x'; 			sha256='6ed2520cf5b7b4b1a985622c61b62d8f65634634b0ef8b3d0594dc1550032d9d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.0
# Tue, 19 Mar 2024 21:53:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-x86_64'; 			sha256='f3ba3bf1e4ab18e96c2d36526a075a02a78fb5f8e80d3e3ca9c5bf256d81d0a0'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-armv6'; 			sha256='ee467093d138f9c4d189b774552ef86ba253107bd91226b28f0c54edf62fe949'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-armv7'; 			sha256='8461b4d4a58eaaf04c4f482f0dabe57db9ef63229311a9583c6548b417f33c76'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-aarch64'; 			sha256='37a1c197fef5fda2a3df2d5ae0d7762ad2a00e30946ad06d4ad9fa8cef16d9e7'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-ppc64le'; 			sha256='faed2dd8f0568922dadf1a8fa155898d5be1feaa67568f2aa730a594ba6a44ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-riscv64'; 			sha256='71a09bd1980505a5f194cfab5df53bba55e493edf246f3ebb28cbfef8caf7715'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-s390x'; 			sha256='d38522261b481d7f20da7f80af67824afe2a1b54dd19215690febb0c49ad932d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 19 Mar 2024 21:53:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Mar 2024 21:53:23 GMT
CMD ["sh"]
# Tue, 19 Mar 2024 21:53:23 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-25.0.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-25.0.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-25.0.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-25.0.5.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 19 Mar 2024 21:53:23 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
VOLUME [/var/lib/docker]
# Tue, 19 Mar 2024 21:53:23 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 19 Mar 2024 21:53:23 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 19 Mar 2024 21:53:23 GMT
CMD []
# Tue, 19 Mar 2024 21:53:23 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-25.0.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-25.0.5.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 19 Mar 2024 21:53:23 GMT
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
	-	`sha256:e455ba1e9eb22f1596140518f8e1e5c15743906edc3ef81fc80d4ee093dde62b`  
		Last Modified: Wed, 20 Mar 2024 00:48:58 GMT  
		Size: 15.9 MB (15907325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5e449903e97f0ac2e2735f4a971dfc5d08fb136b4c9f8518ff126e9128a239d`  
		Last Modified: Sat, 20 Apr 2024 00:45:17 GMT  
		Size: 16.4 MB (16441660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd2250cdcb3699d096ae8a875ec78bf671002f104d7805bb5a46d0af217189e6`  
		Last Modified: Fri, 26 Apr 2024 07:43:05 GMT  
		Size: 17.1 MB (17134329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f23565beaf9f37e48867d4921b8d68d6955ef05941977f12f0d562db07eb7d`  
		Last Modified: Fri, 26 Apr 2024 07:43:04 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ad0d4c820e71e308aa33df43a7119e6e9d3aba310d12e53a80b2ca2bc20328f`  
		Last Modified: Fri, 26 Apr 2024 07:43:04 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:610886829f4df2220ba3ad103170461c4309a0b003853f18a87ec6aaf6ccbaf7`  
		Last Modified: Fri, 26 Apr 2024 07:43:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62c262ecb98609546519bc6ed13d30fa483511d4dd19624f6e8f07c4ab6dddd`  
		Last Modified: Fri, 26 Apr 2024 12:37:47 GMT  
		Size: 14.7 MB (14709757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe17b3c89b47c02798eadb65e37944640fbfc1ea5f09987f29841790fa186a23`  
		Last Modified: Fri, 26 Apr 2024 12:37:46 GMT  
		Size: 98.4 KB (98397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab2b7900b0cccd967be2cebbe6f50f31f703e35af3e77767b84669fefea669e`  
		Last Modified: Fri, 26 Apr 2024 12:37:46 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc0d3fe7f6b058b773a1f9e5fb71cd4cd7e240de1f181cd94bcda5ffc3363fa`  
		Last Modified: Fri, 26 Apr 2024 12:37:48 GMT  
		Size: 51.4 MB (51370494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b590db8b963dcb57f82cec2bdd4726e654fa001ce781f54dce82b6eaf4587701`  
		Last Modified: Fri, 26 Apr 2024 12:37:47 GMT  
		Size: 1.5 KB (1509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50457d6f3249f3f86041a16e52d7ae301bb2daeb8c7d7c224b7a0b3cf31a0eb2`  
		Last Modified: Fri, 26 Apr 2024 12:37:48 GMT  
		Size: 3.2 KB (3249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c03ade7a50c730c17230a8476524d344310cfc1be18fb8b513a51f5521bcd85`  
		Last Modified: Fri, 26 Apr 2024 15:18:22 GMT  
		Size: 1.0 MB (1022490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b306acfb23d15929a9a156ee8d7152ad2c824e65865c8fe0419dcf07e1fff230`  
		Last Modified: Fri, 26 Apr 2024 15:18:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0094d6b02d82dcc6373f3938396d9e9cbc0b10b2ac3a0fbc0736fb4f9ef14186`  
		Last Modified: Fri, 26 Apr 2024 15:18:22 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e39804e2d07c712cacaca3debed3413350ab32a05c3ab8579f90459a69ed2a`  
		Last Modified: Fri, 26 Apr 2024 15:18:23 GMT  
		Size: 22.8 MB (22838616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8be7187ff001bcc88a1894efcb982c7082aa6e2a57e21f3beb7bea33d9b1b04b`  
		Last Modified: Fri, 26 Apr 2024 15:18:23 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:25-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:2f3353fbdfa0af9e698d6d293e0dca0c0c417438a5ace02c8e82eb9f6276579d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **916.3 KB (916280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85778aed68b9b6966ce4b6bf1cff0d04008e67516a9d824f16b9b924b86cd759`

```dockerfile
```

-	Layers:
	-	`sha256:779f52adc6ed82743ff3bcb5d710b91ee37482c126679c4820d4c9067f3887fe`  
		Last Modified: Fri, 26 Apr 2024 15:18:22 GMT  
		Size: 883.3 KB (883271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7477760cb9db9a6ea97f8167f334fe0810e67261c5eaa3ecb8955daca4d297fa`  
		Last Modified: Fri, 26 Apr 2024 15:18:21 GMT  
		Size: 33.0 KB (33009 bytes)  
		MIME: application/vnd.in-toto+json
