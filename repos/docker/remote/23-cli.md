## `docker:23-cli`

```console
$ docker pull docker@sha256:feec0f145144107a705cff7a865717b4f954b625749225894e90a4fb87a46022
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:23-cli` - linux; amd64

```console
$ docker pull docker@sha256:da129b3dff83a9a0ec7d52da79d08da499b050012b7d6d280e5e43771ffc2c8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54077338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25316cdcb69684f0ec3ffedc22067875d3e21d4f36eb63891602247ae74e19c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:24 GMT
ADD file:9a4f77dfaba7fd2aa78186e4ef0e7486ad55101cefc1fabbc1b385601bb38920 in / 
# Wed, 29 Mar 2023 18:19:24 GMT
CMD ["/bin/sh"]
# Wed, 26 Apr 2023 20:00:03 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 26 Apr 2023 20:00:03 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Apr 2023 20:00:03 GMT
ENV DOCKER_VERSION=23.0.5
# Wed, 26 Apr 2023 20:00:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.5.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Apr 2023 20:00:03 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Wed, 26 Apr 2023 20:00:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Apr 2023 20:00:03 GMT
ENV DOCKER_COMPOSE_VERSION=2.17.3
# Wed, 26 Apr 2023 20:00:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-x86_64'; 			sha256='6abb771a438b8ef82b0ff0ef0e2e404032699104c3c40c59cd174b56214876c3'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-armv6'; 			sha256='e8c20e7e02faa623839ccb2af725ae0b343eafaf836b2386579e35c598d7468a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-armv7'; 			sha256='72c26a8ab6a519bd9c645a314d6ed33ed694efeda3f787123806990124446fe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-aarch64'; 			sha256='07bdced6f502ab24b481f46aa6b205f97e2256e5cb11279648ac9c088220a38d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-ppc64le'; 			sha256='06075ea6594e42fd62360c029ed2b7cf294e8a50428cc3c8f0e022a68f672660'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-riscv64'; 			sha256='51c3e1b631be5845aecc9a66d4d0525c94dfec4d20a4ccf535a7f960f780e9f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-s390x'; 			sha256='666a07a5605e985ac96608a315cdae8151e72196733147dd81b61dd42c0777fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Apr 2023 20:00:03 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Apr 2023 20:00:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Apr 2023 20:00:03 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Apr 2023 20:00:03 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Apr 2023 20:00:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Apr 2023 20:00:03 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f56be85fc22e46face30e2c3de3f7fe7c15f8fd7c4e5add29d7f64b87abdaa09`  
		Last Modified: Wed, 29 Mar 2023 18:19:57 GMT  
		Size: 3.4 MB (3374563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ed9ddfd3b8fa49957c18f14a975161f97db10d02990506ab064fef3cd9f06e4`  
		Last Modified: Wed, 29 Mar 2023 18:45:22 GMT  
		Size: 2.1 MB (2063911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788e1ab5616a5765a2b424b3d6f91c26256c1713671000168eee6474fbdeeece`  
		Last Modified: Wed, 29 Mar 2023 18:45:21 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c585cb37f4e3cdfcc58cda3ff4b16db784769ea8bb06886e976a7f7b7f8af2df`  
		Last Modified: Wed, 26 Apr 2023 23:39:54 GMT  
		Size: 16.3 MB (16250447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f07ac151bd26527d97842aec073c55190fd84658e54cbdf252418765330fc601`  
		Last Modified: Wed, 26 Apr 2023 23:39:53 GMT  
		Size: 16.0 MB (16001753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ec0a365c4db516e5f46310682d8babca32f3d129bd48b23fd1a5286097ca34`  
		Last Modified: Wed, 26 Apr 2023 23:39:54 GMT  
		Size: 16.4 MB (16384832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e86e06bd107ec26313095c4be4a6309ac33263e158245714dc9fee646e744a1`  
		Last Modified: Wed, 26 Apr 2023 23:39:51 GMT  
		Size: 550.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:265c5956ad775b9c3e5cd36b4dd007cc924b24b103ca4c3337adcd0973833076`  
		Last Modified: Wed, 26 Apr 2023 23:39:51 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0326226f4470fe3de7c31149bbcaab29100f2ec71bf0e51e8721645130fe1be2`  
		Last Modified: Wed, 26 Apr 2023 23:39:51 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:23-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:058e0d8613324b377cd6cc91abbe8f5bd6f36c79b13913817a1eefcc266bd128
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49897593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d876f7f6afacb818687123d5c55a20b1ec86fd6f4ee39060da8e65d30f8819`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 29 Mar 2023 17:39:18 GMT
ADD file:e51d4089e73ad6dee52b31f0c8059a00c17df6e23f6741fe11b43bd84cc99008 in / 
# Wed, 29 Mar 2023 17:39:18 GMT
CMD ["/bin/sh"]
# Thu, 20 Apr 2023 17:06:00 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 20 Apr 2023 17:06:00 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 20 Apr 2023 17:06:00 GMT
ENV DOCKER_VERSION=23.0.4
# Thu, 20 Apr 2023 17:06:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 20 Apr 2023 17:06:00 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Thu, 20 Apr 2023 17:06:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 20 Apr 2023 17:06:00 GMT
ENV DOCKER_COMPOSE_VERSION=2.17.3
# Thu, 20 Apr 2023 17:06:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-x86_64'; 			sha256='6abb771a438b8ef82b0ff0ef0e2e404032699104c3c40c59cd174b56214876c3'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-armv6'; 			sha256='e8c20e7e02faa623839ccb2af725ae0b343eafaf836b2386579e35c598d7468a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-armv7'; 			sha256='72c26a8ab6a519bd9c645a314d6ed33ed694efeda3f787123806990124446fe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-aarch64'; 			sha256='07bdced6f502ab24b481f46aa6b205f97e2256e5cb11279648ac9c088220a38d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-ppc64le'; 			sha256='06075ea6594e42fd62360c029ed2b7cf294e8a50428cc3c8f0e022a68f672660'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-riscv64'; 			sha256='51c3e1b631be5845aecc9a66d4d0525c94dfec4d20a4ccf535a7f960f780e9f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-s390x'; 			sha256='666a07a5605e985ac96608a315cdae8151e72196733147dd81b61dd42c0777fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 20 Apr 2023 17:06:00 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 20 Apr 2023 17:06:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Apr 2023 17:06:00 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 20 Apr 2023 17:06:00 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 20 Apr 2023 17:06:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Apr 2023 17:06:00 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:c41833b44d910632b415cd89a9cdaa4d62c9725dc56c99a7ddadafd6719960f9`  
		Last Modified: Wed, 29 Mar 2023 17:39:44 GMT  
		Size: 3.3 MB (3261854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6343a5c1782164b247a48071eacb0a74cd75c4c98cac780bb97fad9418a29b7d`  
		Last Modified: Thu, 30 Mar 2023 05:48:09 GMT  
		Size: 2.0 MB (2036542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fb3fc37985f8c4b7d19deedc94fa0ae9a2dc0d4eb4d0fa64f081da502505fd9`  
		Last Modified: Thu, 30 Mar 2023 05:48:08 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0575e395e061ba2f90e1acceee0d550f08d3dcd0118c5949c588226ddf10a034`  
		Last Modified: Tue, 18 Apr 2023 00:40:27 GMT  
		Size: 15.3 MB (15320781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28a0dd61ea819e640adf4d87c8d222853359aa0c42f329d03bf18688859d3517`  
		Last Modified: Tue, 18 Apr 2023 00:40:26 GMT  
		Size: 14.4 MB (14441516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce86b966039a3a82e769b74beaf9982ab7ec992679ef634f476f21b21f5c34d`  
		Last Modified: Thu, 20 Apr 2023 22:34:58 GMT  
		Size: 14.8 MB (14835066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d10cc7f1ddca8b38cb952b4aa0197f1b5a3ef25d9c6560e4102528fd3a62b42`  
		Last Modified: Thu, 20 Apr 2023 22:34:56 GMT  
		Size: 551.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:714e529b432dc1c3fd189e19d6a7599166164a13fa1551e3625493fa8c58d835`  
		Last Modified: Thu, 20 Apr 2023 22:34:56 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d21675ac3ed310c74b8f4115c2f56d079194734958919f8d892163eef07f5a6c`  
		Last Modified: Thu, 20 Apr 2023 22:34:56 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
