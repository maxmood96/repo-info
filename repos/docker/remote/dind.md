## `docker:dind`

```console
$ docker pull docker@sha256:57d2908af2383f6a40c781f3ef48a88f27eb11aba08a2d786c5bab15f2cf2b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:dind` - linux; amd64

```console
$ docker pull docker@sha256:5ff506edc91614933ae78748222c5e50a0daba30d9f932edd606f789f538e497
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.0 MB (108962210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f32379d825c05eb3fbffeaf8c950416a33fea07f013d747407491c51975a116`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Tue, 22 Nov 2022 22:19:28 GMT
ADD file:587cae71969871d3c6456d844a8795df9b64b12c710c275295a1182b46f630e7 in / 
# Tue, 22 Nov 2022 22:19:29 GMT
CMD ["/bin/sh"]
# Tue, 29 Nov 2022 01:27:01 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 29 Nov 2022 01:27:02 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Fri, 16 Dec 2022 23:19:56 GMT
ENV DOCKER_VERSION=20.10.22
# Fri, 16 Dec 2022 23:19:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.22.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.22.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.22.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.22.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 16 Dec 2022 23:19:59 GMT
ENV DOCKER_BUILDX_VERSION=0.9.1
# Fri, 16 Dec 2022 23:20:02 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-amd64'; 			sha256='a7fb95177792ca8ffc7243fad7bf2f33738b8b999a184b6201f002a63c43d136'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm-v6'; 			sha256='159925b4e679eb66e7f0312c7d57a97e68a418c1fa602a00dd8b29b6406768f0'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm-v7'; 			sha256='ba8e5359ce9ba24fec6da07f73591c1b20ac0797a2248b0ef8088f57ae3340fc'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm64'; 			sha256='bbf6a76bf9aef9c5759ff225b97ce23a24fc11e4fa3cdcae36e5dcf1de2cffc5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-ppc64le'; 			sha256='1b2441886e556c720c1bf12f18f240113cc45f9eb404c0f162166ca1c96c1b60'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-riscv64'; 			sha256='c32372dad653fc70eb756b2cffd026e74425e807c01accaeed4559da881ff57c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-s390x'; 			sha256='90b0ecf315d741888920dddeac9fe2e141123c4fe79465b7b10fe23521c9c366'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Thu, 05 Jan 2023 21:21:49 GMT
ENV DOCKER_COMPOSE_VERSION=2.15.0
# Thu, 05 Jan 2023 21:21:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.15.0/docker-compose-linux-x86_64'; 			sha256='ba481d45be2b137a2a185abd05f61d6d7766dbedfa038f16e4705760767a206e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.15.0/docker-compose-linux-armv6'; 			sha256='0f46aea568f35decc22e1db6af76decaf1c36b9bb374610bc08c3b3618170f8f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.15.0/docker-compose-linux-armv7'; 			sha256='343b552c61d74446fc8e8ce7695f878cb2ad49f7fae98deb7fb76a37f24c251e'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.15.0/docker-compose-linux-aarch64'; 			sha256='634e397090ca0e857a898d853ab08d7e2f226328b305026c143c68d6ce0686de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.15.0/docker-compose-linux-ppc64le'; 			sha256='236831ebb63ad30fe716bf22946c91e21b1277bff2785a8538e616168a0d93f1'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.15.0/docker-compose-linux-riscv64'; 			sha256='365d9bf34ae7a2ad0dc028d13363c8c427db1300b1335834a4e06b7e4fa412af'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.15.0/docker-compose-linux-s390x'; 			sha256='8072776b50f34d135f90c8118da60749435b2474afee3df96bbd9c95755f7a2f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Thu, 05 Jan 2023 21:21:52 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 05 Jan 2023 21:21:52 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 05 Jan 2023 21:21:52 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 05 Jan 2023 21:21:53 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 05 Jan 2023 21:21:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Jan 2023 21:21:53 GMT
CMD ["sh"]
# Thu, 05 Jan 2023 21:21:58 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 05 Jan 2023 21:21:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 05 Jan 2023 21:22:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.22.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.22.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.22.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.22.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version
# Thu, 05 Jan 2023 21:22:04 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Thu, 05 Jan 2023 21:22:04 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Thu, 05 Jan 2023 21:22:05 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Thu, 05 Jan 2023 21:22:05 GMT
VOLUME [/var/lib/docker]
# Thu, 05 Jan 2023 21:22:05 GMT
EXPOSE 2375 2376
# Thu, 05 Jan 2023 21:22:05 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 05 Jan 2023 21:22:05 GMT
CMD []
```

-	Layers:
	-	`sha256:c158987b05517b6f2c5913f3acef1f2182a32345a304fe357e3ace5fadcad715`  
		Last Modified: Tue, 22 Nov 2022 22:19:52 GMT  
		Size: 3.4 MB (3370706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93eea1d5d8e5eb7f3c01c44eb6652605d4b5ad66cf819d1e3b6053733f2f13cf`  
		Last Modified: Tue, 29 Nov 2022 01:28:59 GMT  
		Size: 2.1 MB (2064254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08b41ddca615c02560ac2876c1f1a4f4f0c2fe3f8b091488146e1098c5a3eda4`  
		Last Modified: Fri, 16 Dec 2022 23:22:29 GMT  
		Size: 14.0 MB (13982924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de76f94013e41735f015f26d3c3df1af256e1fd761926325deaf30759c53494`  
		Last Modified: Fri, 16 Dec 2022 23:22:28 GMT  
		Size: 15.2 MB (15204113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e300e409a8eec7162a8676943a73b3d129627668357ef158f85947a66122251`  
		Last Modified: Thu, 05 Jan 2023 21:24:20 GMT  
		Size: 14.5 MB (14477427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7564aa83a2f2bd29071dfacfbb67290825ccdc246baf8c4e5483d419668070f`  
		Last Modified: Thu, 05 Jan 2023 21:24:17 GMT  
		Size: 551.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b771ef457284440567ed829304474bf81f2806a564c77b9398f1d6ee475101b`  
		Last Modified: Thu, 05 Jan 2023 21:24:18 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:323fe0eabec356c8896653ec7f8ba3a99ad59f4683be47e2edd4d6cada58ca80`  
		Last Modified: Thu, 05 Jan 2023 21:24:18 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45a9b1f00d8c71f36fbbc05d53145a6461b01f22d58bcdad2da2861ae8e657cc`  
		Last Modified: Thu, 05 Jan 2023 21:24:48 GMT  
		Size: 6.8 MB (6837950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4cbb2c68dd211a3732940e6f91584a976dbd20befd6a5a1afb225294d9ba0c0`  
		Last Modified: Thu, 05 Jan 2023 21:24:47 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14f9fa2e7fe7226a68bd8e0a9e69c083048dab820c2b0b6c61a4aa8d87c91b31`  
		Last Modified: Thu, 05 Jan 2023 21:24:55 GMT  
		Size: 53.0 MB (53017992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6240f6f8ff419159a31faea2c13d2526e74dec0db8090d6728f9ca67d1e201a2`  
		Last Modified: Thu, 05 Jan 2023 21:24:47 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d439a12187dfebb34b9e65fe913b74899ceac59d4eff3f637d338a8a45fda0`  
		Last Modified: Thu, 05 Jan 2023 21:24:47 GMT  
		Size: 2.8 KB (2751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:3b2e62cc5c1e90a3fb4276e736e0b1a2a033d61c157d33a51cdb8f725e4940e0
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.5 MB (100547815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b338730b6e940d613bf08de0812f38f0470a6e83b862047f9d96b82393add73f`
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
# Mon, 09 Jan 2023 17:29:40 GMT
ENV DOCKER_VERSION=20.10.22
# Mon, 09 Jan 2023 17:29:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.22.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.22.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.22.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.22.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Mon, 09 Jan 2023 17:29:42 GMT
ENV DOCKER_BUILDX_VERSION=0.9.1
# Mon, 09 Jan 2023 17:29:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-amd64'; 			sha256='a7fb95177792ca8ffc7243fad7bf2f33738b8b999a184b6201f002a63c43d136'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm-v6'; 			sha256='159925b4e679eb66e7f0312c7d57a97e68a418c1fa602a00dd8b29b6406768f0'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm-v7'; 			sha256='ba8e5359ce9ba24fec6da07f73591c1b20ac0797a2248b0ef8088f57ae3340fc'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm64'; 			sha256='bbf6a76bf9aef9c5759ff225b97ce23a24fc11e4fa3cdcae36e5dcf1de2cffc5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-ppc64le'; 			sha256='1b2441886e556c720c1bf12f18f240113cc45f9eb404c0f162166ca1c96c1b60'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-riscv64'; 			sha256='c32372dad653fc70eb756b2cffd026e74425e807c01accaeed4559da881ff57c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-s390x'; 			sha256='90b0ecf315d741888920dddeac9fe2e141123c4fe79465b7b10fe23521c9c366'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Mon, 09 Jan 2023 17:29:44 GMT
ENV DOCKER_COMPOSE_VERSION=2.15.0
# Mon, 09 Jan 2023 17:29:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.15.0/docker-compose-linux-x86_64'; 			sha256='ba481d45be2b137a2a185abd05f61d6d7766dbedfa038f16e4705760767a206e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.15.0/docker-compose-linux-armv6'; 			sha256='0f46aea568f35decc22e1db6af76decaf1c36b9bb374610bc08c3b3618170f8f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.15.0/docker-compose-linux-armv7'; 			sha256='343b552c61d74446fc8e8ce7695f878cb2ad49f7fae98deb7fb76a37f24c251e'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.15.0/docker-compose-linux-aarch64'; 			sha256='634e397090ca0e857a898d853ab08d7e2f226328b305026c143c68d6ce0686de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.15.0/docker-compose-linux-ppc64le'; 			sha256='236831ebb63ad30fe716bf22946c91e21b1277bff2785a8538e616168a0d93f1'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.15.0/docker-compose-linux-riscv64'; 			sha256='365d9bf34ae7a2ad0dc028d13363c8c427db1300b1335834a4e06b7e4fa412af'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.15.0/docker-compose-linux-s390x'; 			sha256='8072776b50f34d135f90c8118da60749435b2474afee3df96bbd9c95755f7a2f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Mon, 09 Jan 2023 17:29:47 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 09 Jan 2023 17:29:47 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 09 Jan 2023 17:29:47 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Jan 2023 17:29:47 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 09 Jan 2023 17:29:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Jan 2023 17:29:47 GMT
CMD ["sh"]
# Mon, 09 Jan 2023 17:29:53 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 09 Jan 2023 17:29:53 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 09 Jan 2023 17:29:56 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.22.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.22.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.22.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.22.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version
# Mon, 09 Jan 2023 17:29:57 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Mon, 09 Jan 2023 17:29:58 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 09 Jan 2023 17:29:58 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Mon, 09 Jan 2023 17:29:58 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Jan 2023 17:29:58 GMT
EXPOSE 2375 2376
# Mon, 09 Jan 2023 17:29:58 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Jan 2023 17:29:58 GMT
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
	-	`sha256:3e5567070d966674de4065d4af430ca10957d42583f6fb752fa8a33d1cbaafc1`  
		Last Modified: Mon, 09 Jan 2023 17:32:10 GMT  
		Size: 12.7 MB (12743371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84d0f0d9717536c71f21f59fe9bd4193c98236f16044817911d210c56103f508`  
		Last Modified: Mon, 09 Jan 2023 17:32:09 GMT  
		Size: 13.8 MB (13764599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97f76f4c77dd1811c1522df255cfb813d9ed74dcd779f3f9e23c709483733c5`  
		Last Modified: Mon, 09 Jan 2023 17:32:09 GMT  
		Size: 13.1 MB (13069171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c224378d7d2092b72a23f1897dc47b083406ed054f112929088e0351f5550e`  
		Last Modified: Mon, 09 Jan 2023 17:32:07 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:496ca6e97232fa7036123430ba2b7196a7255d49b01a2cffb02bb7d9918447ed`  
		Last Modified: Mon, 09 Jan 2023 17:32:07 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:695dc555807585f128a263fdcbe39fa32785481673636af9c69ec48e807acdc1`  
		Last Modified: Mon, 09 Jan 2023 17:32:07 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ec7c94494f08e97aee85b8246d708a18b039777ec56e316d86b15026641914f`  
		Last Modified: Mon, 09 Jan 2023 17:32:37 GMT  
		Size: 7.0 MB (6991068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36dfa07401333c294973ed803100efedae636e92c8f6f99ac23759f5ff4ce0b9`  
		Last Modified: Mon, 09 Jan 2023 17:32:36 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd83e8cf04e91a7bc34d75583b2d809dedcd1a9acfb5bc687131072049471744`  
		Last Modified: Mon, 09 Jan 2023 17:32:42 GMT  
		Size: 48.7 MB (48676636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c7e73c2afe7ad11be3c21dc9be1d632319066f031a30df8046dd403df1b6123`  
		Last Modified: Mon, 09 Jan 2023 17:32:36 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa33b1efb8a71c8a4574874f511de3408c9507cba869ef173794541cdabd56b3`  
		Last Modified: Mon, 09 Jan 2023 17:32:36 GMT  
		Size: 2.7 KB (2744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
