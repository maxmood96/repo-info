## `docker:rc-dind`

```console
$ docker pull docker@sha256:58c259b235c288029e3cdf5655bd037feff651c3cc56625f2b58751e6520a427
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

### `docker:rc-dind` - linux; amd64

```console
$ docker pull docker@sha256:b3bd0c9a6c23e68ac29cd7f209eeaf4c41f460ab51ca99ff78bbbdbe2c19c1f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.4 MB (132412875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4722cf87f7408722671519a1204c145a462315724caf976a68975553cc586fcb`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Mon, 17 Jun 2024 22:51:04 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
ENV DOCKER_VERSION=27.0.0-rc.2
# Mon, 17 Jun 2024 22:51:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.0.0-rc.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.0.0-rc.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.0.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.0.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
ENV DOCKER_BUILDX_VERSION=0.15.0
# Mon, 17 Jun 2024 22:51:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-amd64'; 			sha256='6569bb8b026b56d49a31aca80b61b4d0da1dbbf23ad6c925752790a9a350c9c5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-arm-v6'; 			sha256='78627fe5baeef2ea6eb50a2a1206c5c479f8984f6637c75825c79f6a4b93fea7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-arm-v7'; 			sha256='e48879480cf6dcfb76a743577b94a548d15e152b0d4fad82e12bb27f11ba0b26'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-arm64'; 			sha256='ad23578106a3a4f0a7bc9d8bdc9ba9155fa7b19889fba46f8f2c59fb10ab73fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-ppc64le'; 			sha256='3ec0f7f76a7abd93b2dfaa5ff314357113a66bce9eea205e206545de34a97471'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-riscv64'; 			sha256='6afcab070d6f939c13d9c1f3aeb9083fef58cb91c22d0b174f9dba7a6549a219'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-s390x'; 			sha256='3fbd476b321d8b844358f796f3158a2f6df78d4d16acc2fc8a82265a2642c39d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.1
# Mon, 17 Jun 2024 22:51:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-x86_64'; 			sha256='ddc876fe2a89d5b7ea455146b0975bfe52904eecba9b192193377d6f99d69ad9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-armv6'; 			sha256='5f244291153cdd7facfe5007aa37f393d139c245b870025b8e86ef88a8de2705'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-armv7'; 			sha256='9dcfa9523dc912370417b7ccc3d81900bbb98dd9addbff0d218398bbe9078bbd'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-aarch64'; 			sha256='16e93b9c2fc147d29ca1acbb8ceab6a50a0e26af777f43dc7a753cb883142617'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-ppc64le'; 			sha256='f351bfdbb6bb9d18b33672ccba6dd31c53a3bd1b81f9e9052fc6d9125e7d5719'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-riscv64'; 			sha256='9940bd7533bcbd087d5301b8348136bc8922aa75739e3e359d8367e2f6dd7005'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-s390x'; 			sha256='6f4b6bb51987b2f61b91cfe4017a8d162e86b82ba3ae074b99b06a1ebe4387ed'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 17 Jun 2024 22:51:04 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 17 Jun 2024 22:51:04 GMT
CMD ["sh"]
# Mon, 17 Jun 2024 22:51:04 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.0.0-rc.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.0.0-rc.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.0.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.0.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 17 Jun 2024 22:51:04 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
VOLUME [/var/lib/docker]
# Mon, 17 Jun 2024 22:51:04 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 17 Jun 2024 22:51:04 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 17 Jun 2024 22:51:04 GMT
CMD []
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c415a03c50fe66b63f658f2ba29fbd1e5c2dab4fa071c10aee9c68ccbce426`  
		Last Modified: Mon, 17 Jun 2024 23:52:55 GMT  
		Size: 2.0 MB (2010485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05013e8d1fa1d9930d2850b4117ba4fe435b083f778b522ec2ddb20c8c224168`  
		Last Modified: Mon, 17 Jun 2024 23:52:55 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f2d6d10376ecb853440118e81441825e64e2c8b9b1dd9f0efff920ea0aeccfb`  
		Last Modified: Mon, 17 Jun 2024 23:52:56 GMT  
		Size: 18.1 MB (18069007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07dc34b51319e34d5ba80a07c2fae2cb95f92eba9dfc10228c04b4fe469bd4b7`  
		Last Modified: Mon, 17 Jun 2024 23:52:56 GMT  
		Size: 18.2 MB (18177613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a508ab1e584d60d6e8c6efdf4879084a937ea6a7bacf9cabb2f65291c3dffc6`  
		Last Modified: Mon, 17 Jun 2024 23:52:57 GMT  
		Size: 18.8 MB (18776599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0999fbeff7c2b3ab7040f9524e86b8b174a7048c7dff527f366dd32943a3eca`  
		Last Modified: Mon, 17 Jun 2024 23:52:56 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10b6c1b0586e5261a33c2df8a22ef8be02579bc5dd1be4fd572a5cbef3044624`  
		Last Modified: Mon, 17 Jun 2024 23:52:57 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0023a1449c94d3a3c089c052865832505689e2a1e8a5716ba75d940d20d032`  
		Last Modified: Mon, 17 Jun 2024 23:52:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf3d0bbdf9153827d5885a6860541c155569e315f123dc20ce1b469c686ef5b`  
		Last Modified: Tue, 18 Jun 2024 00:49:05 GMT  
		Size: 14.9 MB (14906054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:697fc28c2263e8c5ac4849a3b30093f4f14e91d603d56c9c85a31c9541d64da4`  
		Last Modified: Tue, 18 Jun 2024 00:49:04 GMT  
		Size: 89.2 KB (89183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1af91cb402a2754ddf279b3fff61ecf625521952d2fcfd0097fea82ac5618593`  
		Last Modified: Tue, 18 Jun 2024 00:49:05 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7f25ff88e72302d65ea79caceb8f0831b1b28aac5b81f2290010c085cbfdead`  
		Last Modified: Tue, 18 Jun 2024 00:49:05 GMT  
		Size: 56.8 MB (56753884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dec557fbd1d3ca63e3f079f30a11adfe1292bb4d3ee2e0ea53c5f24e9f1c56ba`  
		Last Modified: Tue, 18 Jun 2024 00:49:05 GMT  
		Size: 1.5 KB (1508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8438cd4fa46b33e150773f87ea80dd62e7f5fa3d59026747cc745b2e42d1e94c`  
		Last Modified: Tue, 18 Jun 2024 00:49:05 GMT  
		Size: 3.3 KB (3254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-dind` - unknown; unknown

```console
$ docker pull docker@sha256:311ca5250d6fc0672fd9ea4745ad6d036a2b2f1792fe28abc4eee405c4a2684b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 KB (34046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e73a20c928ae1ff50b30f2bd8d33c4d008294e0f0fba3b1f3e203c0b4f08c143`

```dockerfile
```

-	Layers:
	-	`sha256:c8cd40dc8d2babdb741737989b1abf1a78fa59c9c6cfa37c06e9704528af8328`  
		Last Modified: Tue, 18 Jun 2024 00:49:04 GMT  
		Size: 34.0 KB (34046 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:91401bdf27179ef67450a1ba62ac4c7017f92900a551aa2d035bfd8e2149f9e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.4 MB (124448972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f321cd278533b7592fad7c96d1d8da531506bee35e1b35b62373452c352bae5c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 22 May 2024 17:56:54 GMT
ADD file:5103c8a26cd2dfa76f84be7e1886df206b2131d04cf3079dfd1b6385cc796428 in / 
# Wed, 22 May 2024 17:56:55 GMT
CMD ["/bin/sh"]
# Mon, 17 Jun 2024 22:51:04 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
ENV DOCKER_VERSION=27.0.0-rc.2
# Mon, 17 Jun 2024 22:51:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.0.0-rc.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.0.0-rc.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.0.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.0.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
ENV DOCKER_BUILDX_VERSION=0.15.0
# Mon, 17 Jun 2024 22:51:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-amd64'; 			sha256='6569bb8b026b56d49a31aca80b61b4d0da1dbbf23ad6c925752790a9a350c9c5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-arm-v6'; 			sha256='78627fe5baeef2ea6eb50a2a1206c5c479f8984f6637c75825c79f6a4b93fea7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-arm-v7'; 			sha256='e48879480cf6dcfb76a743577b94a548d15e152b0d4fad82e12bb27f11ba0b26'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-arm64'; 			sha256='ad23578106a3a4f0a7bc9d8bdc9ba9155fa7b19889fba46f8f2c59fb10ab73fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-ppc64le'; 			sha256='3ec0f7f76a7abd93b2dfaa5ff314357113a66bce9eea205e206545de34a97471'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-riscv64'; 			sha256='6afcab070d6f939c13d9c1f3aeb9083fef58cb91c22d0b174f9dba7a6549a219'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-s390x'; 			sha256='3fbd476b321d8b844358f796f3158a2f6df78d4d16acc2fc8a82265a2642c39d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.1
# Mon, 17 Jun 2024 22:51:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-x86_64'; 			sha256='ddc876fe2a89d5b7ea455146b0975bfe52904eecba9b192193377d6f99d69ad9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-armv6'; 			sha256='5f244291153cdd7facfe5007aa37f393d139c245b870025b8e86ef88a8de2705'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-armv7'; 			sha256='9dcfa9523dc912370417b7ccc3d81900bbb98dd9addbff0d218398bbe9078bbd'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-aarch64'; 			sha256='16e93b9c2fc147d29ca1acbb8ceab6a50a0e26af777f43dc7a753cb883142617'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-ppc64le'; 			sha256='f351bfdbb6bb9d18b33672ccba6dd31c53a3bd1b81f9e9052fc6d9125e7d5719'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-riscv64'; 			sha256='9940bd7533bcbd087d5301b8348136bc8922aa75739e3e359d8367e2f6dd7005'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-s390x'; 			sha256='6f4b6bb51987b2f61b91cfe4017a8d162e86b82ba3ae074b99b06a1ebe4387ed'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 17 Jun 2024 22:51:04 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 17 Jun 2024 22:51:04 GMT
CMD ["sh"]
# Mon, 17 Jun 2024 22:51:04 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.0.0-rc.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.0.0-rc.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.0.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.0.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 17 Jun 2024 22:51:04 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
VOLUME [/var/lib/docker]
# Mon, 17 Jun 2024 22:51:04 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 17 Jun 2024 22:51:04 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 17 Jun 2024 22:51:04 GMT
CMD []
```

-	Layers:
	-	`sha256:b0da55d51ed2f4a2e9c4e3ca1e420bac26a1a37098e2f1437841049c51df7320`  
		Last Modified: Wed, 22 May 2024 17:57:17 GMT  
		Size: 3.4 MB (3365055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2542faface5bae0b5d14b82d3e6183d4e5563bff6f3affda3a98565f63409958`  
		Last Modified: Mon, 17 Jun 2024 23:52:50 GMT  
		Size: 2.0 MB (1993292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8317922e3f3dd871674dcf604aab6d64e8e68db0fdc188c4007c4ef7c0c58826`  
		Last Modified: Mon, 17 Jun 2024 23:52:50 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8db86e1ae797994751670ce22b40adb2c0e32090c3cae95ceec315b4afeeb32`  
		Last Modified: Mon, 17 Jun 2024 23:52:51 GMT  
		Size: 16.3 MB (16340363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05e7843fbb803dd95114e7556198894a1320f751825883b5485cd9345b7ebd7`  
		Last Modified: Mon, 17 Jun 2024 23:52:51 GMT  
		Size: 17.0 MB (17010707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5884cfbc0a91ce10e86f69efe5b545a13f31ef1a89acf54b7d0b18f27a22fcd0`  
		Last Modified: Mon, 17 Jun 2024 23:52:52 GMT  
		Size: 17.7 MB (17738752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d205caeb2c3a802dacc8fd2c3c728799211b19e912c58501045eea76213e1fad`  
		Last Modified: Mon, 17 Jun 2024 23:52:51 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf97c9c651389a1c3349117b72dbe3f271306c7a29a0206bcd5576303d5c597`  
		Last Modified: Mon, 17 Jun 2024 23:52:55 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:176e30315448c5d8f87b330b2dd05d9a825448ce9365130ecaa41309d9ebf415`  
		Last Modified: Mon, 17 Jun 2024 23:52:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba18d092a0e841709692ec1dd92b48f469c3a43606a8607e5e94fa280351c3d0`  
		Last Modified: Tue, 18 Jun 2024 00:48:58 GMT  
		Size: 14.9 MB (14858363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c73288b35ce082472bdb12d72e1100b60ae14c4cba3cd7dc813d5847db3c565`  
		Last Modified: Tue, 18 Jun 2024 00:48:57 GMT  
		Size: 88.4 KB (88399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7980b154250b18c5b56fddc7d9b0877df86a741eeb0f4665a48f7ef419cb4ddb`  
		Last Modified: Tue, 18 Jun 2024 00:48:57 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65518fc35523f4429e6facf269f937c7eb8d3a7988fbba6beaa250fbfc7aa79`  
		Last Modified: Tue, 18 Jun 2024 00:48:59 GMT  
		Size: 53.0 MB (53046085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be2658e617b106c7cdf07cd7923f57c79d1314a2f4facd1804a3df5fe7bbd750`  
		Last Modified: Tue, 18 Jun 2024 00:48:58 GMT  
		Size: 1.5 KB (1510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d2f59f54b5c0836225eb41cbc444fb601002006fc10ee13b38599a7fa4e9e4`  
		Last Modified: Tue, 18 Jun 2024 00:48:58 GMT  
		Size: 3.3 KB (3255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-dind` - unknown; unknown

```console
$ docker pull docker@sha256:f365007f658e877955a4d1ef598f123641869234daa110ee68805926a1692f0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 KB (34249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99a8e7f7aecce3b2f3333aa04effd208aeea2d36cfb5ec1efcdbf779b872f3a2`

```dockerfile
```

-	Layers:
	-	`sha256:acea72297c64ea5821807e28795e3932eb1babb6263b0b99a8d23e775bcd94bd`  
		Last Modified: Tue, 18 Jun 2024 00:48:56 GMT  
		Size: 34.2 KB (34249 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:86a3cd97fade88f6543e703f06b820a89468ac7c7092251fcbe16d754c72c427
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.6 MB (122643417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf00ce90014cb6c37344eb4e10b9217068217f0a468e7ec0d7c9cf0e9df0d089`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 22 May 2024 18:07:12 GMT
ADD file:d6a90589cd9e92525c68e44f296baf2a57e5bda9e32ed5f7d45d6ad9a6595e26 in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Mon, 17 Jun 2024 22:51:04 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
ENV DOCKER_VERSION=27.0.0-rc.2
# Mon, 17 Jun 2024 22:51:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.0.0-rc.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.0.0-rc.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.0.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.0.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
ENV DOCKER_BUILDX_VERSION=0.15.0
# Mon, 17 Jun 2024 22:51:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-amd64'; 			sha256='6569bb8b026b56d49a31aca80b61b4d0da1dbbf23ad6c925752790a9a350c9c5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-arm-v6'; 			sha256='78627fe5baeef2ea6eb50a2a1206c5c479f8984f6637c75825c79f6a4b93fea7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-arm-v7'; 			sha256='e48879480cf6dcfb76a743577b94a548d15e152b0d4fad82e12bb27f11ba0b26'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-arm64'; 			sha256='ad23578106a3a4f0a7bc9d8bdc9ba9155fa7b19889fba46f8f2c59fb10ab73fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-ppc64le'; 			sha256='3ec0f7f76a7abd93b2dfaa5ff314357113a66bce9eea205e206545de34a97471'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-riscv64'; 			sha256='6afcab070d6f939c13d9c1f3aeb9083fef58cb91c22d0b174f9dba7a6549a219'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-s390x'; 			sha256='3fbd476b321d8b844358f796f3158a2f6df78d4d16acc2fc8a82265a2642c39d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.1
# Mon, 17 Jun 2024 22:51:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-x86_64'; 			sha256='ddc876fe2a89d5b7ea455146b0975bfe52904eecba9b192193377d6f99d69ad9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-armv6'; 			sha256='5f244291153cdd7facfe5007aa37f393d139c245b870025b8e86ef88a8de2705'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-armv7'; 			sha256='9dcfa9523dc912370417b7ccc3d81900bbb98dd9addbff0d218398bbe9078bbd'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-aarch64'; 			sha256='16e93b9c2fc147d29ca1acbb8ceab6a50a0e26af777f43dc7a753cb883142617'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-ppc64le'; 			sha256='f351bfdbb6bb9d18b33672ccba6dd31c53a3bd1b81f9e9052fc6d9125e7d5719'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-riscv64'; 			sha256='9940bd7533bcbd087d5301b8348136bc8922aa75739e3e359d8367e2f6dd7005'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-s390x'; 			sha256='6f4b6bb51987b2f61b91cfe4017a8d162e86b82ba3ae074b99b06a1ebe4387ed'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 17 Jun 2024 22:51:04 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 17 Jun 2024 22:51:04 GMT
CMD ["sh"]
# Mon, 17 Jun 2024 22:51:04 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.0.0-rc.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.0.0-rc.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.0.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.0.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 17 Jun 2024 22:51:04 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
VOLUME [/var/lib/docker]
# Mon, 17 Jun 2024 22:51:04 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 17 Jun 2024 22:51:04 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 17 Jun 2024 22:51:04 GMT
CMD []
```

-	Layers:
	-	`sha256:8b416cac0b22b1e77fbe2d8d5f2f70f44878497f7c24dd739d8e56b317931303`  
		Last Modified: Wed, 22 May 2024 18:07:30 GMT  
		Size: 3.1 MB (3094035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07ef1c681cdd754917fb053121aa9ad399e9aad1e0d15e555a72d27bf50b3a0`  
		Last Modified: Mon, 17 Jun 2024 23:52:41 GMT  
		Size: 1.8 MB (1841229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361fa6970836ee5a0b385559ba3f81b64c4593fbce0f7dd5bf3ffd6f524d36a6`  
		Last Modified: Mon, 17 Jun 2024 23:52:41 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:967823ba350c586bbcfc4c4d81e2646415628208a81aa0ba3207c53a30007484`  
		Last Modified: Mon, 17 Jun 2024 23:52:42 GMT  
		Size: 16.3 MB (16332795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c65c95f27be9d92a52051261b903d140c8390adeec74cba156a66e49bbf2cec`  
		Last Modified: Mon, 17 Jun 2024 23:52:42 GMT  
		Size: 17.0 MB (16995849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12396a85c8c4e6177979e2f214d3013d50c540935e5c5f14ef7d5d8f41d52a50`  
		Last Modified: Mon, 17 Jun 2024 23:52:43 GMT  
		Size: 17.7 MB (17720916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78c599c739bd1eb86148c439563fae116b8893519d9a57834be5fd80dfb23daa`  
		Last Modified: Mon, 17 Jun 2024 23:52:42 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a7de0e03cf51bc7633975ce9f510beed8495b8b6d4b60d2a0d58072d4ec2523`  
		Last Modified: Mon, 17 Jun 2024 23:52:43 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f9c13cbe575ca98a38eb354f705440ba1d03f03169f2a6220a0ed61ed9466da`  
		Last Modified: Mon, 17 Jun 2024 23:52:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a510c2209226ad767ac445605812846347d572c5a9582c20d4c82e95d6caacd7`  
		Last Modified: Tue, 18 Jun 2024 00:49:01 GMT  
		Size: 13.5 MB (13520089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6266312df4519868b29793c420a3c2a0d690df2e9f1abd93a1bbd8501e5e3e4e`  
		Last Modified: Tue, 18 Jun 2024 00:49:00 GMT  
		Size: 84.5 KB (84466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f11c6cafa912b3a1a259ff1c7582ea910915d90ffd891da53e1c24ad9c8b4d`  
		Last Modified: Tue, 18 Jun 2024 00:49:00 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a7e05441f28797b63b7733bb513da62149430355f6e31b83fe74c7490770b93`  
		Last Modified: Tue, 18 Jun 2024 00:49:02 GMT  
		Size: 53.0 MB (53046082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da2c9c8b5c4fa5194538e94e539a3dac5e160fb909d1646e90f6cc976d5bc04`  
		Last Modified: Tue, 18 Jun 2024 00:49:01 GMT  
		Size: 1.5 KB (1509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d7b082ef7407b50b48c03684a2f47b524a72c63974bed84a92ded14ef496bb`  
		Last Modified: Tue, 18 Jun 2024 00:49:01 GMT  
		Size: 3.3 KB (3253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-dind` - unknown; unknown

```console
$ docker pull docker@sha256:8ac5193c7bed90d9daa2d40612eb910ea45788ea7b4e6b4cbe7a232eb61d014e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 KB (34249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aa5e7029b741e4f9fb9e61148b9b7d7159e61b0101d778fee35a6624362ae3e`

```dockerfile
```

-	Layers:
	-	`sha256:f65a64b9a507cc57775a999b0aca093b2b109a6ad3f240227137043605a87135`  
		Last Modified: Tue, 18 Jun 2024 00:49:00 GMT  
		Size: 34.2 KB (34249 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:b99d33fdfef9bc17176cbbeb707967b32e40a6db40d053adafbe872928c625ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.1 MB (125093974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0700430be9ec111f642e6736ac6e850b561467a47e6f10c9b08c02380acab942`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 22 May 2024 18:17:27 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 18:17:28 GMT
CMD ["/bin/sh"]
# Mon, 17 Jun 2024 22:51:04 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
ENV DOCKER_VERSION=27.0.0-rc.2
# Mon, 17 Jun 2024 22:51:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.0.0-rc.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.0.0-rc.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.0.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.0.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
ENV DOCKER_BUILDX_VERSION=0.15.0
# Mon, 17 Jun 2024 22:51:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-amd64'; 			sha256='6569bb8b026b56d49a31aca80b61b4d0da1dbbf23ad6c925752790a9a350c9c5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-arm-v6'; 			sha256='78627fe5baeef2ea6eb50a2a1206c5c479f8984f6637c75825c79f6a4b93fea7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-arm-v7'; 			sha256='e48879480cf6dcfb76a743577b94a548d15e152b0d4fad82e12bb27f11ba0b26'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-arm64'; 			sha256='ad23578106a3a4f0a7bc9d8bdc9ba9155fa7b19889fba46f8f2c59fb10ab73fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-ppc64le'; 			sha256='3ec0f7f76a7abd93b2dfaa5ff314357113a66bce9eea205e206545de34a97471'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-riscv64'; 			sha256='6afcab070d6f939c13d9c1f3aeb9083fef58cb91c22d0b174f9dba7a6549a219'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-s390x'; 			sha256='3fbd476b321d8b844358f796f3158a2f6df78d4d16acc2fc8a82265a2642c39d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.1
# Mon, 17 Jun 2024 22:51:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-x86_64'; 			sha256='ddc876fe2a89d5b7ea455146b0975bfe52904eecba9b192193377d6f99d69ad9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-armv6'; 			sha256='5f244291153cdd7facfe5007aa37f393d139c245b870025b8e86ef88a8de2705'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-armv7'; 			sha256='9dcfa9523dc912370417b7ccc3d81900bbb98dd9addbff0d218398bbe9078bbd'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-aarch64'; 			sha256='16e93b9c2fc147d29ca1acbb8ceab6a50a0e26af777f43dc7a753cb883142617'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-ppc64le'; 			sha256='f351bfdbb6bb9d18b33672ccba6dd31c53a3bd1b81f9e9052fc6d9125e7d5719'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-riscv64'; 			sha256='9940bd7533bcbd087d5301b8348136bc8922aa75739e3e359d8367e2f6dd7005'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-s390x'; 			sha256='6f4b6bb51987b2f61b91cfe4017a8d162e86b82ba3ae074b99b06a1ebe4387ed'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 17 Jun 2024 22:51:04 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 17 Jun 2024 22:51:04 GMT
CMD ["sh"]
# Mon, 17 Jun 2024 22:51:04 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.0.0-rc.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.0.0-rc.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.0.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.0.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 17 Jun 2024 22:51:04 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
VOLUME [/var/lib/docker]
# Mon, 17 Jun 2024 22:51:04 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 17 Jun 2024 22:51:04 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 17 Jun 2024 22:51:04 GMT
CMD []
```

-	Layers:
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a37c6920cf419f019cc2ece413c620d2c2c0c024b4f0c6e947adf6f650c0d32`  
		Last Modified: Tue, 18 Jun 2024 00:10:11 GMT  
		Size: 2.0 MB (2006612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:226cbf91e38cd25c76a4cf8d25355d629193815e2234ac234d08474c3f47d241`  
		Last Modified: Tue, 18 Jun 2024 00:10:10 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bebe42042517502c0a4214ec067e5e805812571248eb59007767634d4626c284`  
		Last Modified: Tue, 18 Jun 2024 00:10:11 GMT  
		Size: 17.0 MB (17029163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb7eeeea5f866d8f13beb04dcd0031ccd9fd374689779d555f0746a8fd0a7fe`  
		Last Modified: Tue, 18 Jun 2024 00:10:12 GMT  
		Size: 16.5 MB (16538686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca9f866f2e1c6ed3778e7a5e207db02ba4ef4dfe8a6482d489f68539d0418a0`  
		Last Modified: Tue, 18 Jun 2024 00:10:12 GMT  
		Size: 17.1 MB (17144849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:527ee42643cc834ef80264a74abff8cb77379bede35cda028db368b8ce5558b2`  
		Last Modified: Tue, 18 Jun 2024 00:10:12 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff0628e85c34c1cbad0cd6daef18eee405426305a16569c2fad2eee104c3432`  
		Last Modified: Tue, 18 Jun 2024 00:10:13 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82aa64d3a7abb094e57b17ffec25482c5d47d599a88fb847a1b788e9afda51bd`  
		Last Modified: Tue, 18 Jun 2024 00:10:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d087116c8c715dcc196689ef1890a21a4cb6ed678f02ce5a5cf7c3d27d453f0`  
		Last Modified: Tue, 18 Jun 2024 00:53:08 GMT  
		Size: 15.8 MB (15812082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0077b1d5de1ba5bb5fdb530b4cf8ab206d445ae5ac92d400c6b9d4aac257eeb3`  
		Last Modified: Tue, 18 Jun 2024 00:53:07 GMT  
		Size: 98.6 KB (98628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca4d4c824cc7d38d27b3cb58f35826c784abff2b247be745a903af8b6a3b0f98`  
		Last Modified: Tue, 18 Jun 2024 00:53:07 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af2f7edae1a6c565c3a42fd9673c9f6c998e3730c179e7f77f3a492fc3a86d36`  
		Last Modified: Tue, 18 Jun 2024 00:53:09 GMT  
		Size: 52.4 MB (52369220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c93abac44889ca87b8ff30c14bddfa261b3e273b12a2f6c4adb7a9d31f6b8db`  
		Last Modified: Tue, 18 Jun 2024 00:53:08 GMT  
		Size: 1.5 KB (1510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:192493a6cad163c9396addcfe00b3e7460a5838b9eb86967c2dbfc291c9dd238`  
		Last Modified: Tue, 18 Jun 2024 00:53:08 GMT  
		Size: 3.3 KB (3252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-dind` - unknown; unknown

```console
$ docker pull docker@sha256:d215bfa52d449ed7e245359e67d79201fb2f68762901a5c6fdc08edf23bb4137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf86f6e29c2a0831a377fe06c28041b953e2deed8a114e2953624d8bb6519cb8`

```dockerfile
```

-	Layers:
	-	`sha256:c989e05e2d4f803223255117ada66673ea79b6b71473a70b21412017b0deaec8`  
		Last Modified: Tue, 18 Jun 2024 00:53:07 GMT  
		Size: 34.5 KB (34522 bytes)  
		MIME: application/vnd.in-toto+json
