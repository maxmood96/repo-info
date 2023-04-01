## `docker:rc`

```console
$ docker pull docker@sha256:e549f37f4cbcc307574ac7e83269a13cc076672954fd6218b99ee4316f0db76a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:rc` - linux; amd64

```console
$ docker pull docker@sha256:140ae586d6981c3c768308ad4d7ffb85cc859551625e601b2d4caf830aaf1eb5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.5 MB (110496114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee42dcbae0b8c84b1c19723ea29889d174e42f5d53febe8e816552b9c0f0f65`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Mon, 09 Jan 2023 17:05:20 GMT
ADD file:e4d600fc4c9c293efe360be7b30ee96579925d1b4634c94332e2ec73f7d8eca1 in / 
# Mon, 09 Jan 2023 17:05:20 GMT
CMD ["/bin/sh"]
# Mon, 09 Jan 2023 21:12:54 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Mon, 09 Jan 2023 21:12:54 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Thu, 02 Feb 2023 01:02:53 GMT
ENV DOCKER_VERSION=23.0.0-rc.4
# Thu, 02 Feb 2023 01:02:56 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-23.0.0-rc.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-23.0.0-rc.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-23.0.0-rc.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-23.0.0-rc.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Thu, 02 Feb 2023 01:02:57 GMT
ENV DOCKER_BUILDX_VERSION=0.10.2
# Thu, 02 Feb 2023 01:02:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-amd64'; 			sha256='ee5a5e3ebf5e5c73ac840993720bd1e72c4beb3b4ee9e85e2d6b4364cac87d89'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v6'; 			sha256='4d7c2e9eaed303306b40e0505577f4c7088c99f048a5870dd133cb7ad2336bd6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v7'; 			sha256='d74936a4e4e9266aeca66e6a545ed99d83753b4901e0f5210e7646c987591974'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm64'; 			sha256='5f6c706833221cd2cae267ac8612c1809f9d7e8f3fe87707ae86cb695c560cd9'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-ppc64le'; 			sha256='fe55ae43e009b4523523575f500257d7dafeb0aa637392b1853676b8a7a55b7b'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-riscv64'; 			sha256='b57cd352329baebca4cc8102806927de3f5402fff16f6f6e4a2e48080434472b'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-s390x'; 			sha256='9a3be43a3a6902617a8224b41177a840e1a638597a27d7b7c2d558adb8be3a24'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Thu, 02 Feb 2023 01:02:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.15.1
# Thu, 02 Feb 2023 01:03:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.15.1/docker-compose-linux-x86_64'; 			sha256='bcfd9ea51dee4c19dccdfaeef0e7956ef68bf14f3d175933742061a7271ef0f5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.15.1/docker-compose-linux-armv6'; 			sha256='a8934600100af88f535eb50b45c7d8d2ac37835221803ba2910e0b167b3af22e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.15.1/docker-compose-linux-armv7'; 			sha256='e5b03ac1258ad4243af0ac4afcb1c6cc8c9956b2483a50309cdb38cdb8387e37'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.15.1/docker-compose-linux-aarch64'; 			sha256='14d31297794868520cb2e61b543bb1c821aaa484af22b397904314ae8227f6a2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.15.1/docker-compose-linux-ppc64le'; 			sha256='bdada874a26d382b20ced7c170707a1ebcf9f20d7d6f394b962076968473ca9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.15.1/docker-compose-linux-riscv64'; 			sha256='9cc1b9c8de313a1e43b8f3dcca47c29eeb87af3de24c67448c463bf882166430'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.15.1/docker-compose-linux-s390x'; 			sha256='cf311824af115d0bece5d5d60a73464912dad07cdd00fdaa469dabbcad60f289'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Thu, 02 Feb 2023 01:03:02 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 02 Feb 2023 01:03:02 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 02 Feb 2023 01:03:02 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 02 Feb 2023 01:03:02 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 02 Feb 2023 01:03:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Feb 2023 01:03:03 GMT
CMD ["sh"]
# Thu, 02 Feb 2023 01:03:09 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 02 Feb 2023 01:03:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 02 Feb 2023 01:03:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-23.0.0-rc.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-23.0.0-rc.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-23.0.0-rc.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-23.0.0-rc.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version
# Thu, 02 Feb 2023 01:03:15 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Thu, 02 Feb 2023 01:03:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Thu, 02 Feb 2023 01:03:16 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Thu, 02 Feb 2023 01:03:16 GMT
VOLUME [/var/lib/docker]
# Thu, 02 Feb 2023 01:03:16 GMT
EXPOSE 2375 2376
# Thu, 02 Feb 2023 01:03:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 02 Feb 2023 01:03:16 GMT
CMD []
```

-	Layers:
	-	`sha256:8921db27df2831fa6eaa85321205a2470c669b855f3ec95d5a3c2b46de0442c9`  
		Last Modified: Mon, 09 Jan 2023 17:05:45 GMT  
		Size: 3.4 MB (3370628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea237885379427b44e97fa21c0d47eaa42f826dfd0833a69279002a7ce8f50d9`  
		Last Modified: Mon, 09 Jan 2023 21:14:56 GMT  
		Size: 2.1 MB (2064267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d53257546a96f1774f2cc095654742fb10e20c0095bf52722f923b214176f71f`  
		Last Modified: Thu, 02 Feb 2023 01:04:22 GMT  
		Size: 16.2 MB (16220801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c50bb2fc07a0012b1a737999cd259740fb31eff8473e4fb54beb3e78c91ce1d`  
		Last Modified: Thu, 02 Feb 2023 01:04:21 GMT  
		Size: 16.0 MB (15995568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9184e0b5a73b8a44307a5273ce06ab0ee9b980815db4a92e8af1ba0d57397502`  
		Last Modified: Thu, 02 Feb 2023 01:04:21 GMT  
		Size: 14.5 MB (14490919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92ac0535a7ba5cff761b52d5b9e18c9de90fadfc05d14217ad43acb0cff3d9f0`  
		Last Modified: Thu, 02 Feb 2023 01:04:18 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f61a5a4b5932c4fbeee7ef7450905f6169dca1afb0f3683678a0efd5c8587984`  
		Last Modified: Thu, 02 Feb 2023 01:04:18 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84bc4f89b25412df10efda6125845634283bfdd99922179b093fcd40bd467135`  
		Last Modified: Thu, 02 Feb 2023 01:04:18 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f38c633f3aea21c28e5145232c890df900e7ee8054ac33f83f135ff69fdc8403`  
		Last Modified: Thu, 02 Feb 2023 01:04:37 GMT  
		Size: 6.8 MB (6837908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d46a2279733ef156b6d9610c69bb322e3da2700bcea1d6262202b2e926af380`  
		Last Modified: Thu, 02 Feb 2023 01:04:35 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adcbdcf2f1e758e3f35dc9c1fc388feea39fc39d8e330010f6454f95b6bbe5d6`  
		Last Modified: Thu, 02 Feb 2023 01:04:43 GMT  
		Size: 51.5 MB (51509200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eaf8cd99e9258d46370c00417c5156066845a5ae3d2aed7c947f685ba14276a`  
		Last Modified: Thu, 02 Feb 2023 01:04:35 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4546350c42f77056c4323c68e785e49aba2549ed0f3df3a4df7d27f597768a5e`  
		Last Modified: Thu, 02 Feb 2023 01:04:35 GMT  
		Size: 2.7 KB (2745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:rc` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:38a634e342461675461118e82f4e7ebbdeaa5b05a8d4d0aa89a6a1340bf0331f
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.0 MB (102025927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d4dbb43cd423e3f65a435472da1e946b66562b86ac2e5c3ebee0bd3977a0fa7`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Mon, 09 Jan 2023 17:04:48 GMT
ADD file:3080f19f39259a4b77cc53975de0184c78d4335ceb9ffb77a2838d0539ad6f85 in / 
# Mon, 09 Jan 2023 17:04:49 GMT
CMD ["/bin/sh"]
# Mon, 09 Jan 2023 17:29:01 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Mon, 09 Jan 2023 17:29:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Wed, 01 Feb 2023 22:02:31 GMT
ENV DOCKER_VERSION=23.0.0-rc.4
# Wed, 01 Feb 2023 22:02:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-23.0.0-rc.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-23.0.0-rc.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-23.0.0-rc.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-23.0.0-rc.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Wed, 01 Feb 2023 22:02:33 GMT
ENV DOCKER_BUILDX_VERSION=0.10.2
# Wed, 01 Feb 2023 22:02:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-amd64'; 			sha256='ee5a5e3ebf5e5c73ac840993720bd1e72c4beb3b4ee9e85e2d6b4364cac87d89'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v6'; 			sha256='4d7c2e9eaed303306b40e0505577f4c7088c99f048a5870dd133cb7ad2336bd6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v7'; 			sha256='d74936a4e4e9266aeca66e6a545ed99d83753b4901e0f5210e7646c987591974'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm64'; 			sha256='5f6c706833221cd2cae267ac8612c1809f9d7e8f3fe87707ae86cb695c560cd9'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-ppc64le'; 			sha256='fe55ae43e009b4523523575f500257d7dafeb0aa637392b1853676b8a7a55b7b'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-riscv64'; 			sha256='b57cd352329baebca4cc8102806927de3f5402fff16f6f6e4a2e48080434472b'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-s390x'; 			sha256='9a3be43a3a6902617a8224b41177a840e1a638597a27d7b7c2d558adb8be3a24'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Wed, 01 Feb 2023 22:02:35 GMT
ENV DOCKER_COMPOSE_VERSION=2.15.1
# Wed, 01 Feb 2023 22:02:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.15.1/docker-compose-linux-x86_64'; 			sha256='bcfd9ea51dee4c19dccdfaeef0e7956ef68bf14f3d175933742061a7271ef0f5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.15.1/docker-compose-linux-armv6'; 			sha256='a8934600100af88f535eb50b45c7d8d2ac37835221803ba2910e0b167b3af22e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.15.1/docker-compose-linux-armv7'; 			sha256='e5b03ac1258ad4243af0ac4afcb1c6cc8c9956b2483a50309cdb38cdb8387e37'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.15.1/docker-compose-linux-aarch64'; 			sha256='14d31297794868520cb2e61b543bb1c821aaa484af22b397904314ae8227f6a2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.15.1/docker-compose-linux-ppc64le'; 			sha256='bdada874a26d382b20ced7c170707a1ebcf9f20d7d6f394b962076968473ca9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.15.1/docker-compose-linux-riscv64'; 			sha256='9cc1b9c8de313a1e43b8f3dcca47c29eeb87af3de24c67448c463bf882166430'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.15.1/docker-compose-linux-s390x'; 			sha256='cf311824af115d0bece5d5d60a73464912dad07cdd00fdaa469dabbcad60f289'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Wed, 01 Feb 2023 22:02:39 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 01 Feb 2023 22:02:39 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 01 Feb 2023 22:02:39 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 01 Feb 2023 22:02:39 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 01 Feb 2023 22:02:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Feb 2023 22:02:40 GMT
CMD ["sh"]
# Wed, 01 Feb 2023 22:02:44 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 01 Feb 2023 22:02:45 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 01 Feb 2023 22:02:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-23.0.0-rc.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-23.0.0-rc.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-23.0.0-rc.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-23.0.0-rc.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version
# Wed, 01 Feb 2023 22:02:49 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Wed, 01 Feb 2023 22:02:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 01 Feb 2023 22:02:50 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Wed, 01 Feb 2023 22:02:50 GMT
VOLUME [/var/lib/docker]
# Wed, 01 Feb 2023 22:02:50 GMT
EXPOSE 2375 2376
# Wed, 01 Feb 2023 22:02:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 01 Feb 2023 22:02:50 GMT
CMD []
```

-	Layers:
	-	`sha256:a9eaa45ef418e883481a13c7d84fa9904f2ec56789c52a87ba5a9e6483f2b74f`  
		Last Modified: Mon, 09 Jan 2023 17:05:12 GMT  
		Size: 3.3 MB (3259241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b7e78d5cc3f021297e04408059511c5dff9e32e8d9410a4f7815ccdd7d509eb`  
		Last Modified: Mon, 09 Jan 2023 17:30:59 GMT  
		Size: 2.0 MB (2036908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2a06a214416666f96081a64f68dd01e0e73a87f4605ef16bf1302320966e754`  
		Last Modified: Wed, 01 Feb 2023 22:03:55 GMT  
		Size: 15.3 MB (15293244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41cb09ffba3a419e11df3fd24ee4f18c6b9dd03e4bc4ed210e9f5a230736b5b2`  
		Last Modified: Wed, 01 Feb 2023 22:03:53 GMT  
		Size: 14.4 MB (14436884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2efabfcb7da8b0137b45fcd209267bcbd17c869d1a463f9d580ee9d189b9841`  
		Last Modified: Wed, 01 Feb 2023 22:03:53 GMT  
		Size: 13.1 MB (13080441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21d466fe1913573b22f3398173df333531c0981fe544576ca633c9dfeed08db9`  
		Last Modified: Wed, 01 Feb 2023 22:03:52 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2bf666ac09d6eab664a33541cfcc525212ed8860aac68d207956f8232e2ccd9`  
		Last Modified: Wed, 01 Feb 2023 22:03:51 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c79fe1669921f01ae18bf426bc83bed7bbc6925783bc436d9769ba8c1148bed9`  
		Last Modified: Wed, 01 Feb 2023 22:03:52 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb8115f8351fd5ce182d29f08ff118b56eb4c892b266d0caf2d05784c287a0ac`  
		Last Modified: Wed, 01 Feb 2023 22:04:09 GMT  
		Size: 7.0 MB (6991095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15daf83338e13f78528d7dbb6006a97a59195e0b35759a0d731a706cbc63a79`  
		Last Modified: Wed, 01 Feb 2023 22:04:08 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7c74426c7437da68521b507f45dd4e55c60e9494553bf3d31fd339cc914d097`  
		Last Modified: Wed, 01 Feb 2023 22:04:14 GMT  
		Size: 46.9 MB (46921288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba745a64fad1e7220617ae30ed57ff67aaed660afbc02812fe07216531c8ecb3`  
		Last Modified: Wed, 01 Feb 2023 22:04:08 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:508bf6165b5eda463027d2b89d006648f8996d2a75945f3847347bcf134a4131`  
		Last Modified: Wed, 01 Feb 2023 22:04:08 GMT  
		Size: 2.7 KB (2746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
