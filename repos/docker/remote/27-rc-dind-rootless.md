## `docker:27-rc-dind-rootless`

```console
$ docker pull docker@sha256:6699e807066d472767aa10ed230cb683a5b41234e8eaaa2bfd098cbca45c8efa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:27-rc-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:23c4db710b76161056ac8b32a1fb40f29d002a826c11b23096cf6d7f4a95233c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.3 MB (154316057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:790e29b11ba00cd7c084f575726ebf7ac7c8cc427889a16b3e4ca70774cdaa8b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Wed, 12 Jun 2024 18:58:34 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 12 Jun 2024 18:58:34 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 12 Jun 2024 18:58:34 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 12 Jun 2024 18:58:34 GMT
ENV DOCKER_VERSION=27.0.0-rc.1
# Wed, 12 Jun 2024 18:58:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.0.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.0.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.0.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.0.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 12 Jun 2024 18:58:34 GMT
ENV DOCKER_BUILDX_VERSION=0.15.0
# Wed, 12 Jun 2024 18:58:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-amd64'; 			sha256='6569bb8b026b56d49a31aca80b61b4d0da1dbbf23ad6c925752790a9a350c9c5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-arm-v6'; 			sha256='78627fe5baeef2ea6eb50a2a1206c5c479f8984f6637c75825c79f6a4b93fea7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-arm-v7'; 			sha256='e48879480cf6dcfb76a743577b94a548d15e152b0d4fad82e12bb27f11ba0b26'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-arm64'; 			sha256='ad23578106a3a4f0a7bc9d8bdc9ba9155fa7b19889fba46f8f2c59fb10ab73fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-ppc64le'; 			sha256='3ec0f7f76a7abd93b2dfaa5ff314357113a66bce9eea205e206545de34a97471'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-riscv64'; 			sha256='6afcab070d6f939c13d9c1f3aeb9083fef58cb91c22d0b174f9dba7a6549a219'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-s390x'; 			sha256='3fbd476b321d8b844358f796f3158a2f6df78d4d16acc2fc8a82265a2642c39d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 12 Jun 2024 18:58:34 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.1
# Wed, 12 Jun 2024 18:58:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-x86_64'; 			sha256='ddc876fe2a89d5b7ea455146b0975bfe52904eecba9b192193377d6f99d69ad9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-armv6'; 			sha256='5f244291153cdd7facfe5007aa37f393d139c245b870025b8e86ef88a8de2705'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-armv7'; 			sha256='9dcfa9523dc912370417b7ccc3d81900bbb98dd9addbff0d218398bbe9078bbd'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-aarch64'; 			sha256='16e93b9c2fc147d29ca1acbb8ceab6a50a0e26af777f43dc7a753cb883142617'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-ppc64le'; 			sha256='f351bfdbb6bb9d18b33672ccba6dd31c53a3bd1b81f9e9052fc6d9125e7d5719'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-riscv64'; 			sha256='9940bd7533bcbd087d5301b8348136bc8922aa75739e3e359d8367e2f6dd7005'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-s390x'; 			sha256='6f4b6bb51987b2f61b91cfe4017a8d162e86b82ba3ae074b99b06a1ebe4387ed'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 12 Jun 2024 18:58:34 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 12 Jun 2024 18:58:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 12 Jun 2024 18:58:34 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 12 Jun 2024 18:58:34 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 12 Jun 2024 18:58:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 12 Jun 2024 18:58:34 GMT
CMD ["sh"]
# Wed, 12 Jun 2024 18:58:34 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 12 Jun 2024 18:58:34 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 12 Jun 2024 18:58:34 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 12 Jun 2024 18:58:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.0.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.0.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.0.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.0.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 12 Jun 2024 18:58:34 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 12 Jun 2024 18:58:34 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 12 Jun 2024 18:58:34 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 12 Jun 2024 18:58:34 GMT
VOLUME [/var/lib/docker]
# Wed, 12 Jun 2024 18:58:34 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 12 Jun 2024 18:58:34 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 12 Jun 2024 18:58:34 GMT
CMD []
# Wed, 12 Jun 2024 18:58:34 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Wed, 12 Jun 2024 18:58:34 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 12 Jun 2024 18:58:34 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 12 Jun 2024 18:58:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-27.0.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-27.0.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 12 Jun 2024 18:58:34 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 12 Jun 2024 18:58:34 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 12 Jun 2024 18:58:34 GMT
USER rootless
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaad74d7dfb9d5890d834441860e1e9bd92c97cbed9443df95502b8de05c9482`  
		Last Modified: Wed, 12 Jun 2024 21:52:26 GMT  
		Size: 2.0 MB (2010489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:655f112e7af66e9afa0bae4c2bd5d351b1330a288c5150da19dbcfd9e6a099f5`  
		Last Modified: Wed, 12 Jun 2024 21:52:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68da1c6614d473bd661ccc6f6fd67b1b06eb4500711171710ad0cc9d58764154`  
		Last Modified: Wed, 12 Jun 2024 21:52:26 GMT  
		Size: 18.1 MB (18070329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b232f8379812e580ec4d3f8ac222d7ff10a2a17e5621785d6902e579029d0999`  
		Last Modified: Wed, 12 Jun 2024 21:52:26 GMT  
		Size: 18.2 MB (18177608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4d93e97757ecd4e4cbafbc3ef37ce195af73c6677f460c4911e12053ac88a57`  
		Last Modified: Wed, 12 Jun 2024 21:52:27 GMT  
		Size: 18.8 MB (18776602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3bbd4b9f79d384d593f5e51991c42be5d8d5bd04deda7c0b142ef4c5d00233e`  
		Last Modified: Wed, 12 Jun 2024 21:52:27 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c099232670911a27dc13feb4e1786d070b3bb5812ec8e87439757d575a0bb9d`  
		Last Modified: Wed, 12 Jun 2024 21:52:27 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e42bc4a458777645f0038f37a7c2f6cfc6942bdd988bd39b69015b13c033d1f4`  
		Last Modified: Wed, 12 Jun 2024 21:52:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef16c6feafb8e533fa715707a9b353043292b6f83f1b601c2c846290969fa157`  
		Last Modified: Thu, 13 Jun 2024 01:58:55 GMT  
		Size: 14.9 MB (14906049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a5e7e915b2870e0928db7606dbda30e45acc63e2be4aa116f49171a36d5ea1a`  
		Last Modified: Thu, 13 Jun 2024 01:58:54 GMT  
		Size: 89.2 KB (89183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980ca1a90f90c01ab34b5f2c9875116d1ed0f41994716388dad5971099c95981`  
		Last Modified: Thu, 13 Jun 2024 01:58:54 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af66904465a98abc14194e77d25055b1e1cb479041aaa14141d28b7020458457`  
		Last Modified: Thu, 13 Jun 2024 01:58:56 GMT  
		Size: 56.7 MB (56691059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10262bb7945062b4314fca96bd768761509e124585d6e7d138eb6243c787631b`  
		Last Modified: Thu, 13 Jun 2024 01:58:55 GMT  
		Size: 1.5 KB (1509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e27dd0aad52cafb42e38d420adc10e87cb48655a40a531eb38d043e600408eea`  
		Last Modified: Thu, 13 Jun 2024 01:58:55 GMT  
		Size: 3.3 KB (3253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b724142da0df9335d2a330696b12d45ac952530a00b5789db6ba6cc8197b58b4`  
		Last Modified: Thu, 13 Jun 2024 18:13:42 GMT  
		Size: 981.0 KB (980958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68446fcec42189f054e4e5ce2b469838a1e9d880888b5980e3fa131fc3358531`  
		Last Modified: Thu, 13 Jun 2024 18:13:43 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1c661f16ca276b6c3b2bdcb6d1086a3aa1df522ce6efd3f1af4161ce1a0fd7`  
		Last Modified: Thu, 13 Jun 2024 18:13:42 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67dc8cf5bb92d4fd5803733834b68ba0c6c0b3d0e912e7dfeba6ed82767d4a36`  
		Last Modified: Thu, 13 Jun 2024 18:13:43 GMT  
		Size: 21.0 MB (20982377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1481887521defbc15bb18db35752bdd45d8bc003255555f173040b183d966bca`  
		Last Modified: Thu, 13 Jun 2024 18:13:43 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:2b2ca6e1d57acd023cbbdc703a4e05aef3bb64ba8a7d161b0a8701a950d6ca15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 KB (30338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50373118df5fd964b156816a196ea7b382bfae5a315d5a1c5a13bf6acc1342a4`

```dockerfile
```

-	Layers:
	-	`sha256:fce3df86837882cae4d76e9e79e072980a49f4c5fed883e4f116bef4ae0c3f8d`  
		Last Modified: Thu, 13 Jun 2024 18:13:42 GMT  
		Size: 30.3 KB (30338 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-rc-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:f74dafc105e84df83057f351ecc46211e07fb82a533b868fb2dc624c8c767d59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.9 MB (148893731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83a7ae512378823662b90edf476b150d396d382eef358763aea7d32087ded22a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 22 May 2024 18:17:27 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 18:17:28 GMT
CMD ["/bin/sh"]
# Wed, 12 Jun 2024 18:58:34 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 12 Jun 2024 18:58:34 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 12 Jun 2024 18:58:34 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 12 Jun 2024 18:58:34 GMT
ENV DOCKER_VERSION=27.0.0-rc.1
# Wed, 12 Jun 2024 18:58:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.0.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.0.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.0.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.0.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 12 Jun 2024 18:58:34 GMT
ENV DOCKER_BUILDX_VERSION=0.15.0
# Wed, 12 Jun 2024 18:58:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-amd64'; 			sha256='6569bb8b026b56d49a31aca80b61b4d0da1dbbf23ad6c925752790a9a350c9c5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-arm-v6'; 			sha256='78627fe5baeef2ea6eb50a2a1206c5c479f8984f6637c75825c79f6a4b93fea7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-arm-v7'; 			sha256='e48879480cf6dcfb76a743577b94a548d15e152b0d4fad82e12bb27f11ba0b26'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-arm64'; 			sha256='ad23578106a3a4f0a7bc9d8bdc9ba9155fa7b19889fba46f8f2c59fb10ab73fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-ppc64le'; 			sha256='3ec0f7f76a7abd93b2dfaa5ff314357113a66bce9eea205e206545de34a97471'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-riscv64'; 			sha256='6afcab070d6f939c13d9c1f3aeb9083fef58cb91c22d0b174f9dba7a6549a219'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-s390x'; 			sha256='3fbd476b321d8b844358f796f3158a2f6df78d4d16acc2fc8a82265a2642c39d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 12 Jun 2024 18:58:34 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.1
# Wed, 12 Jun 2024 18:58:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-x86_64'; 			sha256='ddc876fe2a89d5b7ea455146b0975bfe52904eecba9b192193377d6f99d69ad9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-armv6'; 			sha256='5f244291153cdd7facfe5007aa37f393d139c245b870025b8e86ef88a8de2705'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-armv7'; 			sha256='9dcfa9523dc912370417b7ccc3d81900bbb98dd9addbff0d218398bbe9078bbd'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-aarch64'; 			sha256='16e93b9c2fc147d29ca1acbb8ceab6a50a0e26af777f43dc7a753cb883142617'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-ppc64le'; 			sha256='f351bfdbb6bb9d18b33672ccba6dd31c53a3bd1b81f9e9052fc6d9125e7d5719'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-riscv64'; 			sha256='9940bd7533bcbd087d5301b8348136bc8922aa75739e3e359d8367e2f6dd7005'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-s390x'; 			sha256='6f4b6bb51987b2f61b91cfe4017a8d162e86b82ba3ae074b99b06a1ebe4387ed'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 12 Jun 2024 18:58:34 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 12 Jun 2024 18:58:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 12 Jun 2024 18:58:34 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 12 Jun 2024 18:58:34 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 12 Jun 2024 18:58:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 12 Jun 2024 18:58:34 GMT
CMD ["sh"]
# Wed, 12 Jun 2024 18:58:34 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 12 Jun 2024 18:58:34 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 12 Jun 2024 18:58:34 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 12 Jun 2024 18:58:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.0.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.0.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.0.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.0.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 12 Jun 2024 18:58:34 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 12 Jun 2024 18:58:34 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 12 Jun 2024 18:58:34 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 12 Jun 2024 18:58:34 GMT
VOLUME [/var/lib/docker]
# Wed, 12 Jun 2024 18:58:34 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 12 Jun 2024 18:58:34 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 12 Jun 2024 18:58:34 GMT
CMD []
# Wed, 12 Jun 2024 18:58:34 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Wed, 12 Jun 2024 18:58:34 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 12 Jun 2024 18:58:34 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 12 Jun 2024 18:58:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-27.0.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-27.0.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 12 Jun 2024 18:58:34 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 12 Jun 2024 18:58:34 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 12 Jun 2024 18:58:34 GMT
USER rootless
```

-	Layers:
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94752cfdf8fe0a1130043554baf33224305bb62315041b14f5c84860041d6e7a`  
		Last Modified: Wed, 12 Jun 2024 21:52:16 GMT  
		Size: 2.0 MB (2006618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d58a06fd3f5e180e2ea78f955666483807dec0ae5b19296f4e63f2134fbea90`  
		Last Modified: Wed, 12 Jun 2024 21:52:16 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f08ea8579301d52ffedb14dd14fc0f4b546ba98754d652090bf2b8f2dfa2e61`  
		Last Modified: Wed, 12 Jun 2024 21:52:16 GMT  
		Size: 17.0 MB (17029281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33dcf35d78dac2c393ad11eb8fac61328d24ada7cc584d15e7f345edaa37e237`  
		Last Modified: Wed, 12 Jun 2024 21:52:17 GMT  
		Size: 16.5 MB (16538687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f32e06403026496e555aa00a3b522337f8146cc899e54de8c413c05949ad6c00`  
		Last Modified: Wed, 12 Jun 2024 21:52:18 GMT  
		Size: 17.1 MB (17144858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc5e76ba006ace6584c6f915f632c45a71c6be3dc91b0e5ca5f3edee2aa9d66f`  
		Last Modified: Wed, 12 Jun 2024 21:52:17 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6ce5580358880049f903ce03f02641dac88a27cdab6611c58971abe8e319fe6`  
		Last Modified: Wed, 12 Jun 2024 21:52:18 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dcd5b2655c93cc356a72a8f2347b2fcd064effe033ef98e28380890e788c4b2`  
		Last Modified: Wed, 12 Jun 2024 21:52:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ce4b8c9e04caf070ac7438d29f388f2c09181cedf86cb9aea20563fb24d70c`  
		Last Modified: Thu, 13 Jun 2024 12:08:38 GMT  
		Size: 15.8 MB (15812078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4546027035ac6fae23ee7452a991122dbc537305449a4730055ece5a3f6a843b`  
		Last Modified: Thu, 13 Jun 2024 12:08:37 GMT  
		Size: 98.6 KB (98630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ad012c94c07ba5198123ed613694ee8d71501f14a74f286d860008dbde2a4e`  
		Last Modified: Thu, 13 Jun 2024 12:08:37 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4649649835c6103c4a3741dafffcf0e3d0d24da02c7d5c227e8891f1036ff38f`  
		Last Modified: Thu, 13 Jun 2024 12:08:39 GMT  
		Size: 52.3 MB (52307457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59dd100be58fa0ef142967c11759c1d4154bda59220677a9629c170cb2b4782a`  
		Last Modified: Thu, 13 Jun 2024 12:08:38 GMT  
		Size: 1.5 KB (1510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b3f92afb764ca89f0c5e1be0841514bae026ff6aace0fb59e7c0378b8472964`  
		Last Modified: Thu, 13 Jun 2024 12:08:38 GMT  
		Size: 3.3 KB (3255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1afe936a928432623850ae989f2449b6ccea3035390037f693f581fe85b77bbc`  
		Last Modified: Fri, 14 Jun 2024 02:35:54 GMT  
		Size: 1.0 MB (1023081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94fcaa62947085112659c8db77088d522086446fac82d9c893ea12be1a79a190`  
		Last Modified: Fri, 14 Jun 2024 02:35:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3df8e5425b876928eda70faf6ce0590717c492c8d485477dd940c43c9f9da4`  
		Last Modified: Fri, 14 Jun 2024 02:35:56 GMT  
		Size: 1.1 KB (1054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f144b68f890f26fe75f5ed11b8b4b5e52c14b90fc0446338caa5a5e2618e9c2`  
		Last Modified: Fri, 14 Jun 2024 02:35:55 GMT  
		Size: 22.8 MB (22836947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0cc65fccfceb70305a0d9d9cc2a42591c3b0ec4005997f28dfbd88ad69dd8c`  
		Last Modified: Fri, 14 Jun 2024 02:35:54 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:d5a02342c932a135c82880972c7f29c7bc3aa1a3f90dfeeb5684a797c89add53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20c8a47a8063f8b8923f5e9f50b4373c268fdf9ad83aa92f544a52592f8c6c47`

```dockerfile
```

-	Layers:
	-	`sha256:3edb8fb09b5caa9d89f9b6efd03b741de6e2a187043933de3bf9d6b61872eb80`  
		Last Modified: Fri, 14 Jun 2024 02:35:53 GMT  
		Size: 30.8 KB (30752 bytes)  
		MIME: application/vnd.in-toto+json
