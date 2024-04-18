## `docker:dind-rootless`

```console
$ docker pull docker@sha256:4162c19ca79fd3b9f6ca1e649fdcc661a0ee64190ee94f52a28d21dd13d9c213
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:0b6ca5b8603da1e532e5fb071c3035ed5289fa35c011116a97547ea2909db1c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.0 MB (152002100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:251c6c94cc3161087c84423a2795773b31023151e418cdc94145bbbe0c5b8508`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Thu, 11 Apr 2024 17:04:36 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 11 Apr 2024 17:04:36 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 11 Apr 2024 17:04:36 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 11 Apr 2024 17:04:36 GMT
ENV DOCKER_VERSION=26.0.1
# Thu, 11 Apr 2024 17:04:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 11 Apr 2024 17:04:36 GMT
ENV DOCKER_BUILDX_VERSION=0.13.1
# Thu, 11 Apr 2024 17:04:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-amd64'; 			sha256='3e2bc8ed25a9125d6aeec07df4e0211edea6288e075b524160ef3fd305d3d74c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm-v6'; 			sha256='643063c656098e312533fe5ee3411523fa06cc3926bd2e96b4c6239b9cecbf88'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm-v7'; 			sha256='8d42e7823237e777b121070fda6ad68159539aa6597aedfa7630384643ad6f9a'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm64'; 			sha256='3ba35a5d38361a64b62aeb9d20acc835ff6862a711cb438e610026b29c0ac489'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-ppc64le'; 			sha256='1d16f7b15706d98523889a1ca50e9dfc44bbaec1f736d883a0528805795b9de2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-riscv64'; 			sha256='202221c9b7fb881d092986e8ec2497ee71729f17c4afd912384a086af700e1ad'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-s390x'; 			sha256='71d7c39192b1b07790eb71e46742cc69a559f3eb00a1512f4a8d2ea1067408da'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 11 Apr 2024 17:04:36 GMT
ENV DOCKER_COMPOSE_VERSION=2.26.1
# Thu, 11 Apr 2024 17:04:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-x86_64'; 			sha256='2f61856d1b8c9de29ffdaedaa1c6d0a5fc5c79da45068f1f4310feed8d3a3f61'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-armv6'; 			sha256='69ce7a9753e53856b92bb75823893e116d993f92f1e389e0f1a4dae45f79296e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-armv7'; 			sha256='82138d1784ba968b59546d19acad85dbca7bbe67f6614ffb84ef4c3cd72f7a4a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-aarch64'; 			sha256='c86efb0d6347b72af6690f06fbd30ed17023fe67e23e28647cacb4b3f6bfb451'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-ppc64le'; 			sha256='4f4dfc8d6834edfd884d8d5326db0bae3a48f25fe31403684be07faea8822aed'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-riscv64'; 			sha256='575f13c8d567d38bf83fc0885163a505564517f013f01f2e5cd12d989cf88fee'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-s390x'; 			sha256='cbcced8480b8c2ed90c0eb3d4d6c45d6ce8ea0d590961b7ef303bd136c8e85c9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 11 Apr 2024 17:04:36 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 11 Apr 2024 17:04:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Apr 2024 17:04:36 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 11 Apr 2024 17:04:36 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 11 Apr 2024 17:04:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Apr 2024 17:04:36 GMT
CMD ["sh"]
# Thu, 11 Apr 2024 17:04:36 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 11 Apr 2024 17:04:36 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 11 Apr 2024 17:04:36 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 11 Apr 2024 17:04:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 11 Apr 2024 17:04:36 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 11 Apr 2024 17:04:36 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 11 Apr 2024 17:04:36 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Apr 2024 17:04:36 GMT
VOLUME [/var/lib/docker]
# Thu, 11 Apr 2024 17:04:36 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 11 Apr 2024 17:04:36 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 11 Apr 2024 17:04:36 GMT
CMD []
# Thu, 11 Apr 2024 17:04:36 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Thu, 11 Apr 2024 17:04:36 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 11 Apr 2024 17:04:36 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 11 Apr 2024 17:04:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-26.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-26.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 11 Apr 2024 17:04:36 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 11 Apr 2024 17:04:36 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 11 Apr 2024 17:04:36 GMT
USER rootless
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4e2d7dc11fc6f3947fe848e69c81e08487bb6d4400f50a0d58d7023186b1af7`  
		Last Modified: Fri, 12 Apr 2024 00:55:19 GMT  
		Size: 2.0 MB (2026153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f626593b7fc825e80737580a9374e2c17d9a47562f523f4a99ff39e0956c709`  
		Last Modified: Fri, 12 Apr 2024 00:55:19 GMT  
		Size: 550.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35989916a4c8263ee169b8b9ff611112f618196a8b04a819dca333dbcaeba40b`  
		Last Modified: Fri, 12 Apr 2024 00:55:20 GMT  
		Size: 17.0 MB (16977153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91720930f6b4756bc7d9fd0fa1902ac66411bf90f7b3d1d787001374ddfdca81`  
		Last Modified: Fri, 12 Apr 2024 00:55:19 GMT  
		Size: 18.0 MB (17982285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cb5f5ca57cf52d6a205b3b15046eaae6282d8339d8ec586ebbe81e60403b125`  
		Last Modified: Fri, 12 Apr 2024 00:55:20 GMT  
		Size: 18.7 MB (18669510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffceb7a3bb44d51b9386ccea1fab1eca073d3bd6198ac7213723f17249d0fe81`  
		Last Modified: Fri, 12 Apr 2024 00:55:20 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d958f8a5b7f66c13bab454433d0b0435b4fc03711c213a94a468583c6c681869`  
		Last Modified: Fri, 12 Apr 2024 00:55:21 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b87df04eca41347cbdcc745cf90a997cf3ef08df5fc9ed9f3a56d45ccb3ba656`  
		Last Modified: Fri, 12 Apr 2024 00:55:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a939a5ff634266780bfbc6ee8fc0d1b2ad6a2e4ebeae8d6e61698e5518e521`  
		Last Modified: Fri, 12 Apr 2024 01:53:39 GMT  
		Size: 14.4 MB (14355062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e0dc7f61ba8b9e34f5b661f64c2a82eb2062338fbd51ccefa133734518f45bf`  
		Last Modified: Fri, 12 Apr 2024 01:53:39 GMT  
		Size: 89.1 KB (89142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fefa731ee4e2aa139b7448ff66badaa7e5d495c9cb3fc501a07b7c4a75be3ee`  
		Last Modified: Fri, 12 Apr 2024 01:53:39 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e69fab3d884f835482b4b06848e04ca65a9311fe684d47f099779a2194fcfc5`  
		Last Modified: Fri, 12 Apr 2024 01:53:40 GMT  
		Size: 56.5 MB (56518643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9b60e39af46af34508c1390315974ea2e8a691555b4514bfe50fb3a62f6b4c`  
		Last Modified: Fri, 12 Apr 2024 01:53:40 GMT  
		Size: 1.5 KB (1509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5d3abca5eb35ba008e4319fec71973bab1d2a614cb4fbd78fd4f441d7753243`  
		Last Modified: Fri, 12 Apr 2024 01:53:40 GMT  
		Size: 3.2 KB (3250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5690e0ae6de82564098c1892e2c46c058c325b324336ae00366944bda6729863`  
		Last Modified: Fri, 12 Apr 2024 02:52:41 GMT  
		Size: 981.6 KB (981574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb930d28e962a394a44656147a2a1f2542ffceca245870fa4b3f7ad836f061f0`  
		Last Modified: Fri, 12 Apr 2024 02:52:41 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b378453fc1c5c650082aa621bb01f69bd340452fdb3b7fc16022d3ed9ba6fa`  
		Last Modified: Fri, 12 Apr 2024 02:52:41 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdcb4f5d8de452bcace5cfe7f654bcd26cb5df4be3f5cdef648674799d195503`  
		Last Modified: Fri, 12 Apr 2024 02:52:41 GMT  
		Size: 21.0 MB (20983892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f962b08a32aab0ae08c5e5c11598d0bb242d2ad045f697b60b99bf24c8904cb`  
		Last Modified: Fri, 12 Apr 2024 02:52:42 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:65d2741fee12320302fa82bb66364424451bcedb4569d0907eaa6fa375adb92a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **907.7 KB (907677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:741acc73110ee92eff5fd30cb4cb370838625ec8df618e0021cd7cdc66d5b020`

```dockerfile
```

-	Layers:
	-	`sha256:d7c446e98a97448286a08bdb6e0c1c35a0f627b8ec3c3b8885f90c42915a49bc`  
		Last Modified: Fri, 12 Apr 2024 02:52:41 GMT  
		Size: 874.4 KB (874421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4422a7c28583c0ce6a2d1ce8bed48769f06ca73737458a1a6e8415c73d690e7f`  
		Last Modified: Fri, 12 Apr 2024 02:52:40 GMT  
		Size: 33.3 KB (33256 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:a683b08b630fec7311cb47a2055d601854e9f56f49609c82e1b811d2c242d601
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.6 MB (145584191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cd2ad919c3b3f4f7861a4ba4631e4f43adf2c2b900c20ba60e72db03e53b18a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Thu, 11 Apr 2024 17:04:36 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 11 Apr 2024 17:04:36 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 11 Apr 2024 17:04:36 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 11 Apr 2024 17:04:36 GMT
ENV DOCKER_VERSION=26.0.1
# Thu, 11 Apr 2024 17:04:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 11 Apr 2024 17:04:36 GMT
ENV DOCKER_BUILDX_VERSION=0.13.1
# Thu, 11 Apr 2024 17:04:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-amd64'; 			sha256='3e2bc8ed25a9125d6aeec07df4e0211edea6288e075b524160ef3fd305d3d74c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm-v6'; 			sha256='643063c656098e312533fe5ee3411523fa06cc3926bd2e96b4c6239b9cecbf88'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm-v7'; 			sha256='8d42e7823237e777b121070fda6ad68159539aa6597aedfa7630384643ad6f9a'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm64'; 			sha256='3ba35a5d38361a64b62aeb9d20acc835ff6862a711cb438e610026b29c0ac489'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-ppc64le'; 			sha256='1d16f7b15706d98523889a1ca50e9dfc44bbaec1f736d883a0528805795b9de2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-riscv64'; 			sha256='202221c9b7fb881d092986e8ec2497ee71729f17c4afd912384a086af700e1ad'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-s390x'; 			sha256='71d7c39192b1b07790eb71e46742cc69a559f3eb00a1512f4a8d2ea1067408da'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 11 Apr 2024 17:04:36 GMT
ENV DOCKER_COMPOSE_VERSION=2.26.1
# Thu, 11 Apr 2024 17:04:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-x86_64'; 			sha256='2f61856d1b8c9de29ffdaedaa1c6d0a5fc5c79da45068f1f4310feed8d3a3f61'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-armv6'; 			sha256='69ce7a9753e53856b92bb75823893e116d993f92f1e389e0f1a4dae45f79296e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-armv7'; 			sha256='82138d1784ba968b59546d19acad85dbca7bbe67f6614ffb84ef4c3cd72f7a4a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-aarch64'; 			sha256='c86efb0d6347b72af6690f06fbd30ed17023fe67e23e28647cacb4b3f6bfb451'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-ppc64le'; 			sha256='4f4dfc8d6834edfd884d8d5326db0bae3a48f25fe31403684be07faea8822aed'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-riscv64'; 			sha256='575f13c8d567d38bf83fc0885163a505564517f013f01f2e5cd12d989cf88fee'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-s390x'; 			sha256='cbcced8480b8c2ed90c0eb3d4d6c45d6ce8ea0d590961b7ef303bd136c8e85c9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 11 Apr 2024 17:04:36 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 11 Apr 2024 17:04:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Apr 2024 17:04:36 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 11 Apr 2024 17:04:36 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 11 Apr 2024 17:04:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Apr 2024 17:04:36 GMT
CMD ["sh"]
# Thu, 11 Apr 2024 17:04:36 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 11 Apr 2024 17:04:36 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 11 Apr 2024 17:04:36 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 11 Apr 2024 17:04:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 11 Apr 2024 17:04:36 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 11 Apr 2024 17:04:36 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 11 Apr 2024 17:04:36 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Apr 2024 17:04:36 GMT
VOLUME [/var/lib/docker]
# Thu, 11 Apr 2024 17:04:36 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 11 Apr 2024 17:04:36 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 11 Apr 2024 17:04:36 GMT
CMD []
# Thu, 11 Apr 2024 17:04:36 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Thu, 11 Apr 2024 17:04:36 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 11 Apr 2024 17:04:36 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 11 Apr 2024 17:04:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-26.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-26.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 11 Apr 2024 17:04:36 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 11 Apr 2024 17:04:36 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 11 Apr 2024 17:04:36 GMT
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
	-	`sha256:4fb5cf902773a51a6e628078ef03ed735e2c0841e92f2e53f7ae2f48fb4ab559`  
		Last Modified: Fri, 12 Apr 2024 03:44:51 GMT  
		Size: 16.0 MB (15984991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1749f6ebff4520d54549192526997f5525c66dfa4fb41e96910f1cbc9e480b77`  
		Last Modified: Fri, 12 Apr 2024 03:44:50 GMT  
		Size: 16.3 MB (16349550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f06326e0b1011564f71b1a01e4b26597d2e777ac2e31b4b585397496c3e46f`  
		Last Modified: Fri, 12 Apr 2024 03:44:51 GMT  
		Size: 17.0 MB (17047138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d93f6908430805b2b7c337d4d62bd8d0500aa59fc3ae0b5126b19575ef817055`  
		Last Modified: Fri, 12 Apr 2024 03:44:50 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103ae574af062e961d6bdf6ec4dcc5a56ad4a8808c215d794e863366e004e0a8`  
		Last Modified: Fri, 12 Apr 2024 03:44:51 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abbd739fc523423f06f9b8a4c889062dfe60a9ee82bd2fadfa092d52fc1652fe`  
		Last Modified: Fri, 12 Apr 2024 03:44:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebbc25dbec5ecbdb417103aeb52e6a92a678bd75812eeccd13af9ecc8e815748`  
		Last Modified: Fri, 12 Apr 2024 05:55:14 GMT  
		Size: 14.7 MB (14709976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3156e70d2d598f3a68c55c849281a80faf7034e9d5cef94ed201ab8c2824e0d2`  
		Last Modified: Fri, 12 Apr 2024 05:55:13 GMT  
		Size: 98.4 KB (98393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2e0d8004e8d041338603f1a0c01e6e1d89caecc3db18097419b4bc45949c3b`  
		Last Modified: Fri, 12 Apr 2024 05:55:13 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56777486cf5bde6dc13f8574bcb2409255ccd8367c6619a13a1b80d0a8f114cc`  
		Last Modified: Fri, 12 Apr 2024 05:55:15 GMT  
		Size: 52.1 MB (52148493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe91d2deede02aeeacd648edd5c222efba095c9b91af47e28f24aa9c48b7fb7b`  
		Last Modified: Fri, 12 Apr 2024 05:55:14 GMT  
		Size: 1.5 KB (1507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a5c26707edd79190426b51c923e13ad52f2775e8583a18689c94c414a39b11`  
		Last Modified: Fri, 12 Apr 2024 05:55:14 GMT  
		Size: 3.2 KB (3246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c5ee2e56cc690103a7ff7e5b8f771f9017777669559eb8e38f832073024856`  
		Last Modified: Fri, 12 Apr 2024 06:51:45 GMT  
		Size: 1.0 MB (1022492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4add81dfbd1bbf1e3cf6fc38f57bd93e3ffbbc043c578fe2c7900d630ca86ec9`  
		Last Modified: Fri, 12 Apr 2024 06:51:44 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da406efe8d468b19458f3798026be4a83931dae358c5c58730e8d1718c804b5`  
		Last Modified: Fri, 12 Apr 2024 06:51:44 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:572eba0be9dc31a62967fcb6756ab311e87cda0714e5834de3862458b9f65af8`  
		Last Modified: Fri, 12 Apr 2024 06:51:45 GMT  
		Size: 22.8 MB (22845789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55ee1d6bfd6c4a0071e209ac64e98b7c79e523a3faaa2ee501ba8ea2349d73d`  
		Last Modified: Fri, 12 Apr 2024 06:51:45 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:61bca444390a9b4ca5e01fd4c99ad2cbec1a88a40d5ae64b110c5dc24d66074b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **902.8 KB (902782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:846a93d3c3c51c71b9fb698163ecb58bc8a73193c79a22c24cc71e1cee3aed27`

```dockerfile
```

-	Layers:
	-	`sha256:9b45439b62ec3f08926ef02bbf897f31e8c18b258a7940130faa811cb6c4eb63`  
		Last Modified: Fri, 12 Apr 2024 06:51:43 GMT  
		Size: 869.5 KB (869463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc74760976ff5ffbc14567ae8b0a0b24892703ee9a7622dec62db7714b6c4621`  
		Last Modified: Fri, 12 Apr 2024 06:51:43 GMT  
		Size: 33.3 KB (33319 bytes)  
		MIME: application/vnd.in-toto+json
