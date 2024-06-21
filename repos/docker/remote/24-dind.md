## `docker:24-dind`

```console
$ docker pull docker@sha256:f09f47201a5b96c258fc5f21d9ec59bdc435ffaf6b7b20cba1986efa7cad4a74
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

### `docker:24-dind` - linux; amd64

```console
$ docker pull docker@sha256:2cb2ad775c13ff56b0a57c295ad531f6da9c0dc94ace1a736f9e90baba0521c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126341268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fa40faec440423214536891c909402a7611404ed90e09af0e7fba66cf5c26a6`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 23 Feb 2024 19:50:50 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Fri, 23 Feb 2024 19:50:50 GMT
CMD ["/bin/sh"]
# Fri, 23 Feb 2024 19:50:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
ENV DOCKER_VERSION=24.0.9
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.9.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
ENV DOCKER_BUILDX_VERSION=0.15.0
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-amd64'; 			sha256='6569bb8b026b56d49a31aca80b61b4d0da1dbbf23ad6c925752790a9a350c9c5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-arm-v6'; 			sha256='78627fe5baeef2ea6eb50a2a1206c5c479f8984f6637c75825c79f6a4b93fea7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-arm-v7'; 			sha256='e48879480cf6dcfb76a743577b94a548d15e152b0d4fad82e12bb27f11ba0b26'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-arm64'; 			sha256='ad23578106a3a4f0a7bc9d8bdc9ba9155fa7b19889fba46f8f2c59fb10ab73fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-ppc64le'; 			sha256='3ec0f7f76a7abd93b2dfaa5ff314357113a66bce9eea205e206545de34a97471'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-riscv64'; 			sha256='6afcab070d6f939c13d9c1f3aeb9083fef58cb91c22d0b174f9dba7a6549a219'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-s390x'; 			sha256='3fbd476b321d8b844358f796f3158a2f6df78d4d16acc2fc8a82265a2642c39d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.1
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-x86_64'; 			sha256='ddc876fe2a89d5b7ea455146b0975bfe52904eecba9b192193377d6f99d69ad9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-armv6'; 			sha256='5f244291153cdd7facfe5007aa37f393d139c245b870025b8e86ef88a8de2705'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-armv7'; 			sha256='9dcfa9523dc912370417b7ccc3d81900bbb98dd9addbff0d218398bbe9078bbd'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-aarch64'; 			sha256='16e93b9c2fc147d29ca1acbb8ceab6a50a0e26af777f43dc7a753cb883142617'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-ppc64le'; 			sha256='f351bfdbb6bb9d18b33672ccba6dd31c53a3bd1b81f9e9052fc6d9125e7d5719'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-riscv64'; 			sha256='9940bd7533bcbd087d5301b8348136bc8922aa75739e3e359d8367e2f6dd7005'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-s390x'; 			sha256='6f4b6bb51987b2f61b91cfe4017a8d162e86b82ba3ae074b99b06a1ebe4387ed'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 23 Feb 2024 19:50:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Feb 2024 19:50:50 GMT
CMD ["sh"]
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.9.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
VOLUME [/var/lib/docker]
# Fri, 23 Feb 2024 19:50:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 23 Feb 2024 19:50:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 23 Feb 2024 19:50:50 GMT
CMD []
```

-	Layers:
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5338763768566e529f8d2d330ac732ec4182af87ac25aff78946ea68a3828bee`  
		Last Modified: Thu, 20 Jun 2024 20:55:01 GMT  
		Size: 2.0 MB (2010473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fde7a1aa1d6812594d13c94f5d9497b3cb851969577d6e9d7858d834f68ef5f2`  
		Last Modified: Thu, 20 Jun 2024 20:55:00 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:256b709ced3145ce9a871ae5feb17020b627a3be504a2213b80e0dcd820a7e06`  
		Last Modified: Thu, 20 Jun 2024 20:55:01 GMT  
		Size: 16.4 MB (16410674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23c43c5c4dd96511a180e36c78ffaffb1f7df7992b553497db3c6d477fa51f2`  
		Last Modified: Thu, 20 Jun 2024 20:55:02 GMT  
		Size: 18.2 MB (18177590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7835a3d2b983ebf13f223fdd3f303680c5c5be2e619e0d8b958e189df9e6581`  
		Last Modified: Thu, 20 Jun 2024 20:55:05 GMT  
		Size: 18.8 MB (18776615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b441481a5073212a24ff214774ed17eccb4dfcb6b9b0025233b722f23754e9`  
		Last Modified: Thu, 20 Jun 2024 20:55:02 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251b59d36856b96078d762eda3153bb2ef193620b39be5ca1cca07cacb941d8c`  
		Last Modified: Thu, 20 Jun 2024 20:55:03 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3a0677a344a910e9af6572ba293a064d77b5d0554ef56ef4317e2e143b53149`  
		Last Modified: Thu, 20 Jun 2024 20:55:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc7ec5f2b741c66fb5e2f9947de664f26dcf41525344f7de31ee3ad1e3db8923`  
		Last Modified: Thu, 20 Jun 2024 21:55:31 GMT  
		Size: 12.5 MB (12504432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d166ee1e73d5c3c07df7669549b26df891aeeb1963a9397bbb07ac90dfe7f0c3`  
		Last Modified: Thu, 20 Jun 2024 21:55:31 GMT  
		Size: 89.2 KB (89186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cba3c447ea83fdb03dca0b48620c039e0e0f2a03a2b021f9d791bfa88b5fe21`  
		Last Modified: Thu, 20 Jun 2024 21:55:31 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7ce48d9cfa2ceb8dcbcc79b37c5f144313d9f2cc171ade47d730e03a6999651`  
		Last Modified: Thu, 20 Jun 2024 21:55:32 GMT  
		Size: 54.7 MB (54740499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d587f217b5335fa97f85801c0f8919b70bc09be9aa4aabce85a520eb32da75`  
		Last Modified: Thu, 20 Jun 2024 21:55:32 GMT  
		Size: 1.5 KB (1510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd1dba44a96f9737a5bbc2ec7abbfcbb375c6e8ca2ceaa8d778dceb82078311f`  
		Last Modified: Thu, 20 Jun 2024 21:55:32 GMT  
		Size: 3.3 KB (3255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:24-dind` - unknown; unknown

```console
$ docker pull docker@sha256:d0df82419c11055bb6c626ccfdce24633f5d57b0dd49e3d003a8c1bfdf966db1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dd5f49b2bbabbee3f255fa1f03ac097480b8a9d6d1d045e7aa2c163c9ac6c49`

```dockerfile
```

-	Layers:
	-	`sha256:60788089fccf8a98b26e1b6e528f12ca88508ea86f2301287375f7dc3081c437`  
		Last Modified: Thu, 20 Jun 2024 21:55:31 GMT  
		Size: 34.8 KB (34836 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:24-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:98beb4ca9f89d2b899d707bb67ea7be184ea999f7662970fe2d8aff336ca3bb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.5 MB (121500758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:471310fc848468378c3273088c3c5a1322d6f3ade6fb18a93a5311adcd9c3b86`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 23 Feb 2024 19:50:50 GMT
ADD file:5103c8a26cd2dfa76f84be7e1886df206b2131d04cf3079dfd1b6385cc796428 in / 
# Fri, 23 Feb 2024 19:50:50 GMT
CMD ["/bin/sh"]
# Fri, 23 Feb 2024 19:50:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
ENV DOCKER_VERSION=24.0.9
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.9.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
ENV DOCKER_BUILDX_VERSION=0.15.0
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-amd64'; 			sha256='6569bb8b026b56d49a31aca80b61b4d0da1dbbf23ad6c925752790a9a350c9c5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-arm-v6'; 			sha256='78627fe5baeef2ea6eb50a2a1206c5c479f8984f6637c75825c79f6a4b93fea7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-arm-v7'; 			sha256='e48879480cf6dcfb76a743577b94a548d15e152b0d4fad82e12bb27f11ba0b26'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-arm64'; 			sha256='ad23578106a3a4f0a7bc9d8bdc9ba9155fa7b19889fba46f8f2c59fb10ab73fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-ppc64le'; 			sha256='3ec0f7f76a7abd93b2dfaa5ff314357113a66bce9eea205e206545de34a97471'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-riscv64'; 			sha256='6afcab070d6f939c13d9c1f3aeb9083fef58cb91c22d0b174f9dba7a6549a219'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-s390x'; 			sha256='3fbd476b321d8b844358f796f3158a2f6df78d4d16acc2fc8a82265a2642c39d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.1
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-x86_64'; 			sha256='ddc876fe2a89d5b7ea455146b0975bfe52904eecba9b192193377d6f99d69ad9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-armv6'; 			sha256='5f244291153cdd7facfe5007aa37f393d139c245b870025b8e86ef88a8de2705'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-armv7'; 			sha256='9dcfa9523dc912370417b7ccc3d81900bbb98dd9addbff0d218398bbe9078bbd'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-aarch64'; 			sha256='16e93b9c2fc147d29ca1acbb8ceab6a50a0e26af777f43dc7a753cb883142617'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-ppc64le'; 			sha256='f351bfdbb6bb9d18b33672ccba6dd31c53a3bd1b81f9e9052fc6d9125e7d5719'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-riscv64'; 			sha256='9940bd7533bcbd087d5301b8348136bc8922aa75739e3e359d8367e2f6dd7005'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-s390x'; 			sha256='6f4b6bb51987b2f61b91cfe4017a8d162e86b82ba3ae074b99b06a1ebe4387ed'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 23 Feb 2024 19:50:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Feb 2024 19:50:50 GMT
CMD ["sh"]
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.9.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
VOLUME [/var/lib/docker]
# Fri, 23 Feb 2024 19:50:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 23 Feb 2024 19:50:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 23 Feb 2024 19:50:50 GMT
CMD []
```

-	Layers:
	-	`sha256:b0da55d51ed2f4a2e9c4e3ca1e420bac26a1a37098e2f1437841049c51df7320`  
		Last Modified: Wed, 22 May 2024 17:57:17 GMT  
		Size: 3.4 MB (3365055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37cc3921df5257d82d5f947c4026d8074af5c4d7e9307f821fe12ed84d11dbd5`  
		Last Modified: Wed, 12 Jun 2024 17:55:46 GMT  
		Size: 2.0 MB (1993321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a779dee551fffb6e92da0afeaa8132f89aeee927cee10dfb3bd0648e29db439`  
		Last Modified: Wed, 12 Jun 2024 17:55:45 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f34edea10d490c86de7cfd600f6fe0d9b91b10f4aa4bae818329e1d4429a5b`  
		Last Modified: Wed, 12 Jun 2024 17:56:51 GMT  
		Size: 15.1 MB (15132941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d89002622e2b742f7d95155000773f351803ca275c1121961ec4e6e77c80c8c`  
		Last Modified: Wed, 12 Jun 2024 17:56:52 GMT  
		Size: 17.0 MB (17010710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914237da576ac9fbd78a3de96dd49a2f9008c5900ae0e578e1be81761e483bae`  
		Last Modified: Wed, 12 Jun 2024 17:56:52 GMT  
		Size: 17.7 MB (17738765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0059116f510d9d3da6ba79cc2502d84229247012fe0fc7e0b3ae07612bb32a8`  
		Last Modified: Wed, 12 Jun 2024 17:56:51 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d23771f0e8ae8ada14fcc59aa3de383df6452e9015a0f50ecf0211e1fa80ca`  
		Last Modified: Wed, 12 Jun 2024 17:56:52 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15ac3fce71a22edf89646521e5c27a709eddc3499522e544c9485fa6565c5f4`  
		Last Modified: Wed, 12 Jun 2024 17:56:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22c5212ff91a681e2b35c446fa2df1a3b4975adb9204c4ada69cb921989d122f`  
		Last Modified: Wed, 12 Jun 2024 18:56:06 GMT  
		Size: 14.9 MB (14858204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02073e1f2e551cf17d23ac49d7ffaed828416b4ffc0b2f4647f623c0e8e046c6`  
		Last Modified: Wed, 12 Jun 2024 18:56:06 GMT  
		Size: 88.4 KB (88396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15317e66b74f11dcd20c4176914596a9844f50d78fe95551bc4da4a2df762872`  
		Last Modified: Wed, 12 Jun 2024 18:56:06 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:347b8c4a525f66c672030c56cc6b4b5f8596d4a4fa4465a01fc8c0115ed73c24`  
		Last Modified: Wed, 12 Jun 2024 18:56:08 GMT  
		Size: 51.3 MB (51305408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eca64ea44ff5e5b13e8e0d4267245a599b9060d17abf7761efb1a2294ddfa86`  
		Last Modified: Wed, 12 Jun 2024 18:56:07 GMT  
		Size: 1.5 KB (1510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4596344b710d0d312af2907458e5e1f9ae49050151bcd32980a6e74e360800d6`  
		Last Modified: Wed, 12 Jun 2024 18:56:07 GMT  
		Size: 3.3 KB (3255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:24-dind` - unknown; unknown

```console
$ docker pull docker@sha256:d6209f209d078c2c3aab603aab126cc28669de23e8ac4bc7bd6c272134ab339f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.1 KB (35061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26d6a3d83540b355df0e8872e3b60d783f36df0d36edb433383cd14029748fdf`

```dockerfile
```

-	Layers:
	-	`sha256:f02379aa0dd785de28acb9587ccf0bf87d229b6b881f988356a88ca2588ee8b6`  
		Last Modified: Wed, 12 Jun 2024 18:56:05 GMT  
		Size: 35.1 KB (35061 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:24-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:029d564e673cd02b3069c8bf2ca26210e63b6b2396bee6e2afb61b95f6a2b56b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.7 MB (119699073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ddb02e3db6f76581af2e51f494c3c0034ccf5e92b974bdb834fddfd252cc5e8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 23 Feb 2024 19:50:50 GMT
ADD file:d6a90589cd9e92525c68e44f296baf2a57e5bda9e32ed5f7d45d6ad9a6595e26 in / 
# Fri, 23 Feb 2024 19:50:50 GMT
CMD ["/bin/sh"]
# Fri, 23 Feb 2024 19:50:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
ENV DOCKER_VERSION=24.0.9
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.9.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
ENV DOCKER_BUILDX_VERSION=0.15.0
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-amd64'; 			sha256='6569bb8b026b56d49a31aca80b61b4d0da1dbbf23ad6c925752790a9a350c9c5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-arm-v6'; 			sha256='78627fe5baeef2ea6eb50a2a1206c5c479f8984f6637c75825c79f6a4b93fea7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-arm-v7'; 			sha256='e48879480cf6dcfb76a743577b94a548d15e152b0d4fad82e12bb27f11ba0b26'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-arm64'; 			sha256='ad23578106a3a4f0a7bc9d8bdc9ba9155fa7b19889fba46f8f2c59fb10ab73fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-ppc64le'; 			sha256='3ec0f7f76a7abd93b2dfaa5ff314357113a66bce9eea205e206545de34a97471'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-riscv64'; 			sha256='6afcab070d6f939c13d9c1f3aeb9083fef58cb91c22d0b174f9dba7a6549a219'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-s390x'; 			sha256='3fbd476b321d8b844358f796f3158a2f6df78d4d16acc2fc8a82265a2642c39d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.1
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-x86_64'; 			sha256='ddc876fe2a89d5b7ea455146b0975bfe52904eecba9b192193377d6f99d69ad9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-armv6'; 			sha256='5f244291153cdd7facfe5007aa37f393d139c245b870025b8e86ef88a8de2705'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-armv7'; 			sha256='9dcfa9523dc912370417b7ccc3d81900bbb98dd9addbff0d218398bbe9078bbd'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-aarch64'; 			sha256='16e93b9c2fc147d29ca1acbb8ceab6a50a0e26af777f43dc7a753cb883142617'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-ppc64le'; 			sha256='f351bfdbb6bb9d18b33672ccba6dd31c53a3bd1b81f9e9052fc6d9125e7d5719'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-riscv64'; 			sha256='9940bd7533bcbd087d5301b8348136bc8922aa75739e3e359d8367e2f6dd7005'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-s390x'; 			sha256='6f4b6bb51987b2f61b91cfe4017a8d162e86b82ba3ae074b99b06a1ebe4387ed'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 23 Feb 2024 19:50:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Feb 2024 19:50:50 GMT
CMD ["sh"]
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.9.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
VOLUME [/var/lib/docker]
# Fri, 23 Feb 2024 19:50:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 23 Feb 2024 19:50:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 23 Feb 2024 19:50:50 GMT
CMD []
```

-	Layers:
	-	`sha256:8b416cac0b22b1e77fbe2d8d5f2f70f44878497f7c24dd739d8e56b317931303`  
		Last Modified: Wed, 22 May 2024 18:07:30 GMT  
		Size: 3.1 MB (3094035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca4176f76244fd438271e663ab7a8dda92f04446dfdc569bef106849aa6b3290`  
		Last Modified: Wed, 12 Jun 2024 17:55:46 GMT  
		Size: 1.8 MB (1841233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a779dee551fffb6e92da0afeaa8132f89aeee927cee10dfb3bd0648e29db439`  
		Last Modified: Wed, 12 Jun 2024 17:55:45 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60213d2757a1dc5958273f58b84647bf720693a7ace21806e85256f15c0bf49`  
		Last Modified: Wed, 12 Jun 2024 17:56:49 GMT  
		Size: 15.1 MB (15129221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7916f3f1bc6108cc9d462044c4c1e7b915d6488e5a26067e58c64131e1c9ba7`  
		Last Modified: Wed, 12 Jun 2024 17:56:49 GMT  
		Size: 17.0 MB (16995852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad69b557e055787ff7e010e1fef7e7dec2db75bdb29753f76ec7b5d8e04b478`  
		Last Modified: Wed, 12 Jun 2024 17:56:49 GMT  
		Size: 17.7 MB (17720916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7690701493b71bdd30b6e4cb6ac71b0f19e4a335e0ca037039e2432054614707`  
		Last Modified: Wed, 12 Jun 2024 17:56:48 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05c83d72fd4c005d45f57c2023d7a2b765f7cd4cbde853abd3a6cfb07f034f8d`  
		Last Modified: Wed, 12 Jun 2024 17:56:49 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3dc9b8aad62a755394fdf8f0f7898d19e60c1e6831575c7d9b9a211c1750806`  
		Last Modified: Wed, 12 Jun 2024 17:56:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ead39667b4d85b842b852b58bb79aecde1bdd7217c005e850c7d68c777eb3b`  
		Last Modified: Wed, 12 Jun 2024 19:01:49 GMT  
		Size: 13.5 MB (13520004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ad33cf3914359bb8ad49e942feb201a769f2b0e8c6e77054834d8e9c3c3717`  
		Last Modified: Wed, 12 Jun 2024 19:01:48 GMT  
		Size: 84.5 KB (84459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cadd9390442b888ab1a9a0a1198695702804b3bb6991353daa2aacaa4d04bce5`  
		Last Modified: Wed, 12 Jun 2024 19:01:48 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db2f4bd6a4dc867ce2309bda6584eee7260a398ddf47e938a9ccd5fa576f8c31`  
		Last Modified: Wed, 12 Jun 2024 19:01:50 GMT  
		Size: 51.3 MB (51305399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2195fe4cddacc32f76d8b3631ca91e8579fe75dc5da01d65d48c01b0a69bc2d5`  
		Last Modified: Wed, 12 Jun 2024 19:01:49 GMT  
		Size: 1.5 KB (1508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:076c50981d1366bf6230edc8b2604678f59daa2a47cbb8b6d908eb16f12e0343`  
		Last Modified: Wed, 12 Jun 2024 19:01:49 GMT  
		Size: 3.3 KB (3254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:24-dind` - unknown; unknown

```console
$ docker pull docker@sha256:95fe473a776365038c592f794ed7dec09fad6207dc2206fdbd741447e1ef193c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.1 KB (35062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8c28d5172e7b103269bcf45c7d6e241c98aaf92946bc527f4c978e70dd1ce37`

```dockerfile
```

-	Layers:
	-	`sha256:7be256cd5ba814931bd52ab7cf2c85598653f8cfc9f22b2c3610db38be6bb8c9`  
		Last Modified: Wed, 12 Jun 2024 19:01:47 GMT  
		Size: 35.1 KB (35062 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:24-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:cfe4226b8b885faa22bf44904114afc239607d36b4ee2ab0749d6ea55cde99e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121230817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2c22dcc48345506c4ed94e9fe0f06c4beffc71a941a45ecf42776cf2b329bc9`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 23 Feb 2024 19:50:50 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Fri, 23 Feb 2024 19:50:50 GMT
CMD ["/bin/sh"]
# Fri, 23 Feb 2024 19:50:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
ENV DOCKER_VERSION=24.0.9
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.9.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
ENV DOCKER_BUILDX_VERSION=0.15.0
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-amd64'; 			sha256='6569bb8b026b56d49a31aca80b61b4d0da1dbbf23ad6c925752790a9a350c9c5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-arm-v6'; 			sha256='78627fe5baeef2ea6eb50a2a1206c5c479f8984f6637c75825c79f6a4b93fea7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-arm-v7'; 			sha256='e48879480cf6dcfb76a743577b94a548d15e152b0d4fad82e12bb27f11ba0b26'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-arm64'; 			sha256='ad23578106a3a4f0a7bc9d8bdc9ba9155fa7b19889fba46f8f2c59fb10ab73fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-ppc64le'; 			sha256='3ec0f7f76a7abd93b2dfaa5ff314357113a66bce9eea205e206545de34a97471'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-riscv64'; 			sha256='6afcab070d6f939c13d9c1f3aeb9083fef58cb91c22d0b174f9dba7a6549a219'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-s390x'; 			sha256='3fbd476b321d8b844358f796f3158a2f6df78d4d16acc2fc8a82265a2642c39d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.1
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-x86_64'; 			sha256='ddc876fe2a89d5b7ea455146b0975bfe52904eecba9b192193377d6f99d69ad9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-armv6'; 			sha256='5f244291153cdd7facfe5007aa37f393d139c245b870025b8e86ef88a8de2705'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-armv7'; 			sha256='9dcfa9523dc912370417b7ccc3d81900bbb98dd9addbff0d218398bbe9078bbd'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-aarch64'; 			sha256='16e93b9c2fc147d29ca1acbb8ceab6a50a0e26af777f43dc7a753cb883142617'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-ppc64le'; 			sha256='f351bfdbb6bb9d18b33672ccba6dd31c53a3bd1b81f9e9052fc6d9125e7d5719'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-riscv64'; 			sha256='9940bd7533bcbd087d5301b8348136bc8922aa75739e3e359d8367e2f6dd7005'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-s390x'; 			sha256='6f4b6bb51987b2f61b91cfe4017a8d162e86b82ba3ae074b99b06a1ebe4387ed'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 23 Feb 2024 19:50:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Feb 2024 19:50:50 GMT
CMD ["sh"]
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.9.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
VOLUME [/var/lib/docker]
# Fri, 23 Feb 2024 19:50:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 23 Feb 2024 19:50:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 23 Feb 2024 19:50:50 GMT
CMD []
```

-	Layers:
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0782eb4e77d74d9b9a314d9b56833c86c46848b438a32b37ea5557573243ce67`  
		Last Modified: Wed, 12 Jun 2024 18:30:18 GMT  
		Size: 2.0 MB (2006611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8746dd4cbb23fdb5e4bb3f089b9f4b73a6bd3204e0454cd67ed85adb2827ee50`  
		Last Modified: Wed, 12 Jun 2024 18:30:18 GMT  
		Size: 452.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d251f23dcd036bc3e6e8a42754613b59bd37eb5936c06882d857738b5370a210`  
		Last Modified: Wed, 12 Jun 2024 18:30:46 GMT  
		Size: 15.5 MB (15459110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b347aa6775503e62c9f11acde6b8159ccda5c6324c2652b01c5fed538d98abd2`  
		Last Modified: Wed, 12 Jun 2024 18:30:46 GMT  
		Size: 16.5 MB (16538684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450f0d74103b8922b37a8b32ca7992eae11401ccbe6c3df4e7a33321c851c5ed`  
		Last Modified: Wed, 12 Jun 2024 18:30:47 GMT  
		Size: 17.1 MB (17144869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48ae2d0907a46dfa08409c9101f0edb6103164f673961ede20b345da062739b`  
		Last Modified: Wed, 12 Jun 2024 18:30:46 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d27298211e9a62e57bea436de1c78f6bf37f07d6b1bf6e34740a57ac3bab58f7`  
		Last Modified: Wed, 12 Jun 2024 18:30:47 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:468e87477176c1ec0821b3350c6111affbeb5ef2c69ccd9456c218534d0d6009`  
		Last Modified: Wed, 12 Jun 2024 18:30:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2833bb8ce8f3cfcec0bb819590bacabc28d75d3e90249428059502445ecceabb`  
		Last Modified: Wed, 12 Jun 2024 19:54:11 GMT  
		Size: 15.8 MB (15812001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374127e549047629fa05a1b3daf0fab4fbdfe3e330fba5c6b1baec6a5dd0de0a`  
		Last Modified: Wed, 12 Jun 2024 19:54:11 GMT  
		Size: 98.6 KB (98628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09fa3c2e278a048e4305947bc4a709f9a975c368db55397e90bedaeb295ffa85`  
		Last Modified: Wed, 12 Jun 2024 19:54:10 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f3ac91f01471a00f246e5611c261ccfc90178c1d13af15a99e6543cc16be053`  
		Last Modified: Wed, 12 Jun 2024 19:54:12 GMT  
		Size: 50.1 MB (50076180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8016491d82678b83f352596f53af88ab39c7b746b79283de813b6b992505d3c`  
		Last Modified: Wed, 12 Jun 2024 19:54:12 GMT  
		Size: 1.5 KB (1510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103ca35ed5aef2cb3aeb089c775813fe30862320be8d34a4e572895a603703a9`  
		Last Modified: Wed, 12 Jun 2024 19:54:12 GMT  
		Size: 3.3 KB (3255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:24-dind` - unknown; unknown

```console
$ docker pull docker@sha256:984b3d036d73045ca16615ff1d6c2b3c4b14e75119351d22fa042e90053bd50b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.3 KB (35347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7b112899ed65f51e5c76437d5a3658234dda08cdcfe6f3fbc9d8b5afece0453`

```dockerfile
```

-	Layers:
	-	`sha256:61eeaa432a06623fa5793d7cb52ac832c54c8345949755cd387b156751fc5616`  
		Last Modified: Wed, 12 Jun 2024 19:54:10 GMT  
		Size: 35.3 KB (35347 bytes)  
		MIME: application/vnd.in-toto+json
