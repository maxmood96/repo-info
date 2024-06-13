## `docker:rc-dind-rootless`

```console
$ docker pull docker@sha256:1315e81b0319092f406906b9dd4943e1895048f24b1e9857b67e9787eaefdb1d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:rc-dind-rootless` - linux; amd64

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

### `docker:rc-dind-rootless` - unknown; unknown

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

### `docker:rc-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:78b52125b862cfcd5abbb90f4375567334864efc2cc236d31794cd2c4a183564
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.9 MB (142910225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:008e841ec0dc8e4456f623bb1c109bdec6a9969a77b7c34373f5e17f00b96378`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Thu, 07 Mar 2024 21:18:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
ENV DOCKER_VERSION=26.0.0-rc2
# Thu, 07 Mar 2024 21:18:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-26.0.0-rc2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-26.0.0-rc2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-26.0.0-rc2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-26.0.0-rc2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
ENV DOCKER_BUILDX_VERSION=0.13.1
# Thu, 07 Mar 2024 21:18:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-amd64'; 			sha256='3e2bc8ed25a9125d6aeec07df4e0211edea6288e075b524160ef3fd305d3d74c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm-v6'; 			sha256='643063c656098e312533fe5ee3411523fa06cc3926bd2e96b4c6239b9cecbf88'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm-v7'; 			sha256='8d42e7823237e777b121070fda6ad68159539aa6597aedfa7630384643ad6f9a'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm64'; 			sha256='3ba35a5d38361a64b62aeb9d20acc835ff6862a711cb438e610026b29c0ac489'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-ppc64le'; 			sha256='1d16f7b15706d98523889a1ca50e9dfc44bbaec1f736d883a0528805795b9de2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-riscv64'; 			sha256='202221c9b7fb881d092986e8ec2497ee71729f17c4afd912384a086af700e1ad'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-s390x'; 			sha256='71d7c39192b1b07790eb71e46742cc69a559f3eb00a1512f4a8d2ea1067408da'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.25.0
# Thu, 07 Mar 2024 21:18:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-x86_64'; 			sha256='53641b8a28419f947bc58c085e0c39b97a209b6e875a25c585e7fab44ff48576'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-armv6'; 			sha256='a123b79b530a65c7381ca8bb3b29cde7177f4f260984a127d998c9696cae794c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-armv7'; 			sha256='8ea72e93e8da8259d7d5d051f3c65dc14c44a23d5ebc6939394d7d03b147e238'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-aarch64'; 			sha256='b9f303c9f9db75ecf18ea6fc516b3dc54a3e54f3b3d8e7f1a449416522958bc5'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-ppc64le'; 			sha256='dc067ab61239cef3d2e145d37fcd68c1fc2320c6728d77a9a4ec4fb0e6c6dd64'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-riscv64'; 			sha256='a17f07604fa74c661e62d5e27ae358f8a611f42bb9a4a147cec76b8bb591bea4'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-s390x'; 			sha256='9e613275e5fa46cb864d3f2fccb10e3239b879527d075490b03e381df56c397c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 07 Mar 2024 21:18:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 Mar 2024 21:18:50 GMT
CMD ["sh"]
# Thu, 07 Mar 2024 21:18:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-26.0.0-rc2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-26.0.0-rc2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-26.0.0-rc2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-26.0.0-rc2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 07 Mar 2024 21:18:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
VOLUME [/var/lib/docker]
# Thu, 07 Mar 2024 21:18:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 07 Mar 2024 21:18:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 07 Mar 2024 21:18:50 GMT
CMD []
# Thu, 07 Mar 2024 21:18:50 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-26.0.0-rc2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-26.0.0-rc2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 07 Mar 2024 21:18:50 GMT
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
	-	`sha256:0b1fd8107a0166ec2911f8f43a2a5e067961d5963e722b47e61856820dd946c8`  
		Last Modified: Mon, 18 Mar 2024 22:51:05 GMT  
		Size: 15.9 MB (15936587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7f3e440238097c0c767248819bba9d596e55a79b8eb3e25da8bd16e03ea05e5`  
		Last Modified: Mon, 18 Mar 2024 22:51:06 GMT  
		Size: 16.3 MB (16349514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f677fe87a3f5798ccdc2e06a7e8db90c3afbe88459e3dfd23707f0cc9e47ebb`  
		Last Modified: Mon, 18 Mar 2024 22:51:06 GMT  
		Size: 16.6 MB (16646385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:540ce7efad7a51b0915b014a5e04762666981161df191f26548e78f51be5a318`  
		Last Modified: Mon, 18 Mar 2024 22:51:05 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ad2a99d95baf2767c815ab3a5a825daf12e9d9308d31461a91d1282c5d2375`  
		Last Modified: Mon, 18 Mar 2024 22:51:06 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95dc950dc93070da3a2b5d02565dae19fe24e817c4dd9ea11a52dc68fb132adb`  
		Last Modified: Mon, 18 Mar 2024 22:51:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36d3c5b6288c7755a5c220d0745660053eddee657a09ae16c26b349678e29520`  
		Last Modified: Mon, 18 Mar 2024 23:53:15 GMT  
		Size: 12.6 MB (12626611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6b762eee4ec5328138a4d393a74c84deadbafe675f09aa428a12d695ab1a7a7`  
		Last Modified: Mon, 18 Mar 2024 23:53:15 GMT  
		Size: 98.4 KB (98383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca2721186303e204524ed82419068792431b289fd1ac001f824cbb1ac17acb4`  
		Last Modified: Mon, 18 Mar 2024 23:53:15 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea9e248815d5d13c087a61c67ca6111a7d1d485c01b4240c29a924666a61a7a`  
		Last Modified: Mon, 18 Mar 2024 23:53:17 GMT  
		Size: 52.0 MB (52014239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:733fab59b60d5be26cfad73f827f857b30482d4b6e35d93b1cd721c3c0d447f7`  
		Last Modified: Mon, 18 Mar 2024 23:53:16 GMT  
		Size: 1.5 KB (1509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79857979182097a4617aaf48be183f178d463e80071208d098cc57c68637422f`  
		Last Modified: Mon, 18 Mar 2024 23:53:16 GMT  
		Size: 3.2 KB (3250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ff881fd7be676bf9819ef33c630463b5dfba7c8a2a4c5c81d9d949709f0e0e`  
		Last Modified: Tue, 19 Mar 2024 00:51:09 GMT  
		Size: 1.0 MB (1022483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0911e3b692b5de97896000a29a2bf933d39b6415c8c23b4843b86828856042b`  
		Last Modified: Tue, 19 Mar 2024 00:51:09 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:293455c2a45bf7a0039761f35ecf7243c23c46630c1ae17d2f4dff3753223689`  
		Last Modified: Tue, 19 Mar 2024 00:51:09 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:912a798661e8ab62f4234d9395b437fec55970c722c57c6679537ce91e52a89d`  
		Last Modified: Tue, 19 Mar 2024 00:51:10 GMT  
		Size: 22.8 MB (22838647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2af20a8e84b74e3f2b3bad295a5091db0020b4c44140a0ed9d18cf53ad7c29`  
		Last Modified: Tue, 19 Mar 2024 00:51:10 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:25f44b34ec7584a8f932c70f7d61350d067c4c22438639c148db31c043468d6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **917.0 KB (916962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a287bf4beb3501b10a095121604a03558f048142825bf4c79d56b72c8aed98e`

```dockerfile
```

-	Layers:
	-	`sha256:11a7918a55d06bbd57f05a551dc93005be3eb54d84861725562f80480d48266c`  
		Last Modified: Tue, 19 Mar 2024 00:51:08 GMT  
		Size: 883.9 KB (883906 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f8284a16cca78d536f5d7d16e1bba5cbdfbcf693e5ddc36e5adb394d6e4d4e1`  
		Last Modified: Tue, 19 Mar 2024 00:51:08 GMT  
		Size: 33.1 KB (33056 bytes)  
		MIME: application/vnd.in-toto+json
