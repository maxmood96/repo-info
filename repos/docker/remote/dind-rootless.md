## `docker:dind-rootless`

```console
$ docker pull docker@sha256:736a5b9015e149b42af36fdbcf81a0a41f0fbf4173bbe4e265278d03cbb9aa68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:3d5b0a0a81a2b8770652468b38847721050af219e94c5711a9a7bc8e8cdc1333
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.5 MB (134450185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:272062036ead322e794888251164e54b81a1f64cba944eda4f84db8d820accae`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 09 May 2023 23:11:10 GMT
ADD file:7625ddfd589fb824ee39f1b1eb387b98f3676420ff52f26eb9d975151e889667 in / 
# Tue, 09 May 2023 23:11:10 GMT
CMD ["/bin/sh"]
# Wed, 10 May 2023 10:04:23 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 10 May 2023 10:04:23 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_VERSION=23.0.6
# Wed, 10 May 2023 10:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Wed, 10 May 2023 10:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_COMPOSE_VERSION=2.17.3
# Wed, 10 May 2023 10:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-x86_64'; 			sha256='6abb771a438b8ef82b0ff0ef0e2e404032699104c3c40c59cd174b56214876c3'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-armv6'; 			sha256='e8c20e7e02faa623839ccb2af725ae0b343eafaf836b2386579e35c598d7468a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-armv7'; 			sha256='72c26a8ab6a519bd9c645a314d6ed33ed694efeda3f787123806990124446fe8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-aarch64'; 			sha256='07bdced6f502ab24b481f46aa6b205f97e2256e5cb11279648ac9c088220a38d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-ppc64le'; 			sha256='06075ea6594e42fd62360c029ed2b7cf294e8a50428cc3c8f0e022a68f672660'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-riscv64'; 			sha256='51c3e1b631be5845aecc9a66d4d0525c94dfec4d20a4ccf535a7f960f780e9f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.17.3/docker-compose-linux-s390x'; 			sha256='666a07a5605e985ac96608a315cdae8151e72196733147dd81b61dd42c0777fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 10 May 2023 10:04:23 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 10 May 2023 10:04:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 10 May 2023 10:04:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 10 May 2023 10:04:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 May 2023 10:04:23 GMT
CMD ["sh"]
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 15 May 2023 22:39:50 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 15 May 2023 22:39:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 15 May 2023 22:39:50 GMT
VOLUME [/var/lib/docker]
# Mon, 15 May 2023 22:39:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 15 May 2023 22:39:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 15 May 2023 22:39:50 GMT
CMD []
# Mon, 15 May 2023 22:39:50 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Mon, 15 May 2023 22:39:50 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Mon, 15 May 2023 22:39:50 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Mon, 15 May 2023 22:39:50 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 15 May 2023 22:39:50 GMT
USER rootless
```

-	Layers:
	-	`sha256:8a49fdb3b6a5ff2bd8ec6a86c05b2922a0f7454579ecc07637e94dfd1d0639b6`  
		Last Modified: Tue, 09 May 2023 23:11:26 GMT  
		Size: 3.4 MB (3397490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb60e7f5d22cf3e06856538fbb2c518c629c1bbe07d62a60d16e3c7fefa06f4`  
		Last Modified: Thu, 11 May 2023 19:23:43 GMT  
		Size: 2.0 MB (2014357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74671f55a8da50720028684fd32ee90f4fdeb79ffcadf0e7213a90cd50ef5c3`  
		Last Modified: Thu, 11 May 2023 19:23:42 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cd4867cc7bf586ebd914414a5e00dda99b3e26394f16e97a61f2c3fae0510b7`  
		Last Modified: Thu, 11 May 2023 19:24:57 GMT  
		Size: 16.3 MB (16250881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d94ad0c817fb4f64af0ec231ffd173b474d706777160f7af0ebbfcbc8f1aac`  
		Last Modified: Thu, 11 May 2023 19:24:56 GMT  
		Size: 16.0 MB (16001750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec5418c68f0ed0c1c4cc3743b52c6aaa2f12976d65acfb0e1a413b99ada47635`  
		Last Modified: Thu, 11 May 2023 19:24:56 GMT  
		Size: 16.4 MB (16384822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1082547c2e5b84d03cbe43b8c87a37a5fe218da4411681166a20d09140c4fedd`  
		Last Modified: Thu, 11 May 2023 19:24:53 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80b838ca0f73affc638b89a4ac48a914430602c5e8ef4a658b86840d7ac500a9`  
		Last Modified: Thu, 11 May 2023 19:24:53 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15f978d7223ae114154a42417cd2ba3ae70644ab8b0ea30ea16cea43c4024c8`  
		Last Modified: Thu, 11 May 2023 19:24:53 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1058b1c95dcd434f93391bf0ec0c404ae630b363de88563fa9a4a4d3c6889b90`  
		Last Modified: Thu, 11 May 2023 19:25:14 GMT  
		Size: 7.0 MB (7025224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac1c4c35af9e9b29cde02d3d5b488ed71b7821d39319354f4aba1a8ae8ace24`  
		Last Modified: Thu, 11 May 2023 19:25:12 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d938c8b2399339aaf8caeefbdc85c8b8dddf7d27d57d8c3d09bf070e0a4374b`  
		Last Modified: Thu, 11 May 2023 19:25:20 GMT  
		Size: 51.7 MB (51657452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b2885b54919758712d2ab1b9d1e43574e5fa8d8fe06612e193c876de7d221ea`  
		Last Modified: Thu, 11 May 2023 19:25:12 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3ce26085aa03b6fc712003b8cd4e3675c6975181aca50368e8af84866d7b9e`  
		Last Modified: Tue, 16 May 2023 00:21:06 GMT  
		Size: 2.8 KB (2796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c98ac734fba950213b5eef3e34a74cfb050771d2dcfb9e09bf8849e430a97171`  
		Last Modified: Tue, 16 May 2023 00:21:32 GMT  
		Size: 1.4 MB (1362380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a2dc52b58512c04b6f21d9013089f46e944d25ee401bf249410fbfee0a386a`  
		Last Modified: Tue, 16 May 2023 00:21:32 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d714531a153f83a639d0577eb97fbabde8a658d045e1a5934d0fdd66e1647e`  
		Last Modified: Tue, 16 May 2023 00:21:32 GMT  
		Size: 1.4 KB (1355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d363f0101be8e2f3cf083449298d611caf75351c46d338317982af0bac53317e`  
		Last Modified: Tue, 16 May 2023 00:21:35 GMT  
		Size: 20.3 MB (20347094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9fecae1fab5b25b43bb2d749c2266c981b255b6ab3505f483a58c208da98e4e`  
		Last Modified: Tue, 16 May 2023 00:21:32 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:d5fea20e13ddd78513d02a2331f6d31f1c48314431094bc8225a58a3e199628e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 MB (130662457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:025c163c83c0cec89c2e216140bc53ad1a14a3841a37e30e5c248eadf340561e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 09 May 2023 23:11:08 GMT
ADD file:df7fccc3453b6ec1401d27a1295b0882a83e731fde8f23db9d3f687a2b6b4e70 in / 
# Tue, 09 May 2023 23:11:08 GMT
CMD ["/bin/sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_VERSION=24.0.0
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.18.0
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-x86_64'; 			sha256='02b69f1f23167fce126b16d9d6b645362f5a6fa7fc9a073d3d080e45e12d32fc'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv6'; 			sha256='58cabf4745c8878a178e4283b5f272eb46fc4cb42b12ac47a487085838ae4a6c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-armv7'; 			sha256='9e2dc7e0f7d572e6733ba9d66d8ffa063c66c00a262e138a1df5b324c4580e9d'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-aarch64'; 			sha256='60444f990cd2e87cb1f3b5093d88afa6c8f58cb9c5477fdb31ff894deaee17c6'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-ppc64le'; 			sha256='18a29f9f67ce1c3afbfc4720194db1002feae681d78469ed0cd39e04da009761'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-riscv64'; 			sha256='c5ef1f3cb9bf2ab9f232f993d640c3f872d573494ad6b3081e6b8bc45bc58fe1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.18.0/docker-compose-linux-s390x'; 			sha256='51af79cf31b0916f40ed3d0bef30a71a03dea1d794458a5c62770c3d8e1efce5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 16 May 2023 17:59:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD ["sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
VOLUME [/var/lib/docker]
# Tue, 16 May 2023 17:59:38 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD []
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-24.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-24.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 16 May 2023 17:59:38 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 16 May 2023 17:59:38 GMT
USER rootless
```

-	Layers:
	-	`sha256:08409d4172603f40b56eb6b76240a1e6bd78baa0e96590dc7ff76c5f1a093af2`  
		Last Modified: Tue, 09 May 2023 23:11:23 GMT  
		Size: 3.3 MB (3342848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf127bdc9f4f627525a187a7bf41c41f4706220fb1fe5b5c7d6cbc52114a9224`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 2.0 MB (2024535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b4810136f4ceecd47a02cbf6a0c55b8d9de3b014cf917ac2bf8ee632787ba0`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a803316fb129ab772964c94e9e7e7736e81a0ad9f233ae92b462ade7ac585b55`  
		Last Modified: Wed, 17 May 2023 00:03:53 GMT  
		Size: 15.4 MB (15422540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4afab67718187f66bed185c88b7259f9a99d1d17b4ddd0e1c1c6f63eeb9ffc8`  
		Last Modified: Wed, 17 May 2023 00:03:51 GMT  
		Size: 14.4 MB (14441524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567bc94445bd1bf6d5e3b489d084e4edb47c768b77eb434f45954f869e201153`  
		Last Modified: Wed, 17 May 2023 00:03:52 GMT  
		Size: 14.9 MB (14861237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69eff66c35e2edfb48060dfb7dc3f00e542a1adba3fdc8e400c518e6a1b0cd8f`  
		Last Modified: Wed, 17 May 2023 00:03:49 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6196db0a937d0b72dbb1e2aa403f0a9d307550fe8d553cdea3c69f425059b9`  
		Last Modified: Wed, 17 May 2023 00:03:50 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f44004068cc3c6c728f3c29a87374142fe4076796bef369bdbd327e774a3a7`  
		Last Modified: Wed, 17 May 2023 00:03:50 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22442686bd72e2c0ecd000948826aebc8dcb3136fe1142b6ef334fa4a389f388`  
		Last Modified: Wed, 17 May 2023 00:04:11 GMT  
		Size: 7.2 MB (7245057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:538120297d91ba480effca7fc88d637aab474129879b223a9120eb3d7648e0c3`  
		Last Modified: Wed, 17 May 2023 00:04:10 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eaff4018a72e47b5a3546eb439499e864408cef1745148eb85b5af6026a7282`  
		Last Modified: Wed, 17 May 2023 00:04:15 GMT  
		Size: 49.5 MB (49455389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398e5219c811f7cb87f34450cf1a01a217122fcc492cbc68437dcee7fe05e156`  
		Last Modified: Wed, 17 May 2023 00:04:10 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a054eb5e9d233a1fae4b8399984152cfd30e385282d002072fb7d5db6b0fdd84`  
		Last Modified: Wed, 17 May 2023 00:04:10 GMT  
		Size: 2.8 KB (2789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00ee53f4852847948f043ca06a0787f96b227b7a89bd3a96c001e0a015ed0fa1`  
		Last Modified: Wed, 17 May 2023 00:04:45 GMT  
		Size: 1.4 MB (1413339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1da8cd837f1a67565e17645d233f693dd101d1f489eee2a9b9e539419953232`  
		Last Modified: Wed, 17 May 2023 00:04:45 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7da12c61e018b49d59351af2c58c6aa2d838fd2c66bd096040afd3f98b37e39d`  
		Last Modified: Wed, 17 May 2023 00:04:45 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826a4dc1d8c55308e6d04bed73f3d53650e3a05a030d0b8e398968bae5148d96`  
		Last Modified: Wed, 17 May 2023 00:04:48 GMT  
		Size: 22.4 MB (22447264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39be7db13eba707e002fc9857aa46ae80d8c6c28c3a28f380b1a580aecb6e388`  
		Last Modified: Wed, 17 May 2023 00:04:45 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
