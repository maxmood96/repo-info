## `docker:rc-git`

```console
$ docker pull docker@sha256:c9f574d8f3a9119c85e6aafcd25f8c2e12425d6c4e4cc820f577ed78aaa6e6f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:rc-git` - linux; amd64

```console
$ docker pull docker@sha256:0847d3fd0163ccb59ad929368a3efbce9a480670701258d77d38ad88d7b41464
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.3 MB (56287484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb73a3125b16828dfb6f4a24e4b87bdc0c6ec2ad6db21a98250d0007247045c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
# Thu, 02 Feb 2023 01:03:29 GMT
RUN apk add --no-cache git
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
	-	`sha256:30619d1c6caaee4423d66523ac44a5644965a406e8977c07c093d2194a063749`  
		Last Modified: Thu, 02 Feb 2023 01:05:24 GMT  
		Size: 4.1 MB (4143586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:rc-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:7b22bcca2f7d8089c8ed275d3326d4160e18880c9a4a9ceb1f35e1918c541d8b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52294338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d90d5c856d9d4b2faaba4e374dfd8e8d99eb69a2119464344bfa69d35a3b771`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
# Wed, 01 Feb 2023 22:03:02 GMT
RUN apk add --no-cache git
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
	-	`sha256:e4e73f567b0e4733e89817812d702d9b12c20341b92e557ec45906263da13936`  
		Last Modified: Wed, 01 Feb 2023 22:04:54 GMT  
		Size: 4.2 MB (4185904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
