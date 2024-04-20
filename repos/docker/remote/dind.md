## `docker:dind`

```console
$ docker pull docker@sha256:d948b3376a742d7acd335ef9e3587569bb5ff40e40069ed696f0060b301655b0
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

### `docker:dind` - linux; amd64

```console
$ docker pull docker@sha256:f95f0b3931e90bd65ec7542af140f72371f65dad1044e325ff04016e34db3b96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.1 MB (130131320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1d643fd08d494e2ac09b3b2f02a73e163bc857bb6f3346d42145794ecd73d82`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Thu, 18 Apr 2024 21:40:47 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 18 Apr 2024 21:40:47 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 18 Apr 2024 21:40:47 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 18 Apr 2024 21:40:47 GMT
ENV DOCKER_VERSION=26.0.2
# Thu, 18 Apr 2024 21:40:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.0.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.0.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.0.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.0.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 18 Apr 2024 21:40:47 GMT
ENV DOCKER_BUILDX_VERSION=0.14.0
# Thu, 18 Apr 2024 21:40:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-amd64'; 			sha256='32f8f17eca35bf2efe6c0e47f40e4692a876f34531b421efc984799a5b41226e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-arm-v6'; 			sha256='7a23989eb26ad27e1b7c11a38dda6a8e6a94562969c19165cf8f49e70203ad20'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-arm-v7'; 			sha256='53b2d827510c6cff41503454caeb0d6613d5ed11201ba10f5ad6c22466cc178c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-arm64'; 			sha256='38bf0ea9c48743edb8243f14272be65a2bad7092228068337aea584309ea664c'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-ppc64le'; 			sha256='847e665e8f1fef3b85c6a5139d9bc57a81bae84d6a882d3ed71e2b5e2bd94bf6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-riscv64'; 			sha256='c853c01f71b6b778b430d985813069d1ca4f2b2e7e039723298350839a556d2b'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-s390x'; 			sha256='6ed2520cf5b7b4b1a985622c61b62d8f65634634b0ef8b3d0594dc1550032d9d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 18 Apr 2024 21:40:47 GMT
ENV DOCKER_COMPOSE_VERSION=2.26.1
# Thu, 18 Apr 2024 21:40:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-x86_64'; 			sha256='2f61856d1b8c9de29ffdaedaa1c6d0a5fc5c79da45068f1f4310feed8d3a3f61'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-armv6'; 			sha256='69ce7a9753e53856b92bb75823893e116d993f92f1e389e0f1a4dae45f79296e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-armv7'; 			sha256='82138d1784ba968b59546d19acad85dbca7bbe67f6614ffb84ef4c3cd72f7a4a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-aarch64'; 			sha256='c86efb0d6347b72af6690f06fbd30ed17023fe67e23e28647cacb4b3f6bfb451'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-ppc64le'; 			sha256='4f4dfc8d6834edfd884d8d5326db0bae3a48f25fe31403684be07faea8822aed'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-riscv64'; 			sha256='575f13c8d567d38bf83fc0885163a505564517f013f01f2e5cd12d989cf88fee'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-s390x'; 			sha256='cbcced8480b8c2ed90c0eb3d4d6c45d6ce8ea0d590961b7ef303bd136c8e85c9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 18 Apr 2024 21:40:47 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 18 Apr 2024 21:40:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:40:47 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 18 Apr 2024 21:40:47 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 18 Apr 2024 21:40:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Apr 2024 21:40:47 GMT
CMD ["sh"]
# Thu, 18 Apr 2024 21:40:47 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 18 Apr 2024 21:40:47 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 18 Apr 2024 21:40:47 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 18 Apr 2024 21:40:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.0.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.0.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.0.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.0.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 18 Apr 2024 21:40:47 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 18 Apr 2024 21:40:47 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 18 Apr 2024 21:40:47 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:40:47 GMT
VOLUME [/var/lib/docker]
# Thu, 18 Apr 2024 21:40:47 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 18 Apr 2024 21:40:47 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 18 Apr 2024 21:40:47 GMT
CMD []
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c25b9a5f512769a7cca11a973d9aade8b4fad3f9f7f14dd880efce0a540b7e8b`  
		Last Modified: Fri, 19 Apr 2024 22:50:35 GMT  
		Size: 2.0 MB (2026152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e9881a2ac04155903f3b65981ab60d832fd35c0503587c547c9d358d49a895`  
		Last Modified: Fri, 19 Apr 2024 22:50:34 GMT  
		Size: 550.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:700f7b49cf75fb51fa507bea477b0ec47d1ecd3f40a90862386d513259c4666a`  
		Last Modified: Fri, 19 Apr 2024 22:50:35 GMT  
		Size: 17.0 MB (16977144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dee9f74c01c4b004fb3130a3b8e399f75e11cb6354ca95bf8debea221a4ccb1e`  
		Last Modified: Fri, 19 Apr 2024 22:50:35 GMT  
		Size: 18.1 MB (18078217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f955c3e9d8ce4a6470bcd57272e55eaddf57c509b1e1f9aaa7612b0dda9acae6`  
		Last Modified: Fri, 19 Apr 2024 22:50:36 GMT  
		Size: 18.7 MB (18669510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0ca727e67ae16fbc6f3d41b2818c291282cecaf13c673c2e8520486145f3ee6`  
		Last Modified: Fri, 19 Apr 2024 22:50:36 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6d63c8680c5f525b554a123320ba752875fff5f161d8db093d2088af27c0be`  
		Last Modified: Fri, 19 Apr 2024 22:50:37 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d017e0df6b32138b1bcd494ac3ccfa83a86f440b67323b0fb83998832267ea60`  
		Last Modified: Fri, 19 Apr 2024 22:50:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a270b779d899dbaab217c559e55be899f6efafb587ac0df7934539cf5e92e423`  
		Last Modified: Fri, 19 Apr 2024 22:56:16 GMT  
		Size: 14.4 MB (14355037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3b75a415cd75ac79173d68d1161f95adeba6e03d4cb656c7340acf29d8db66`  
		Last Modified: Fri, 19 Apr 2024 22:56:16 GMT  
		Size: 89.1 KB (89138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f3d01750d517f15cf07edc6912a20814d37f33190fc832a392e61519781e824`  
		Last Modified: Fri, 19 Apr 2024 22:56:16 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d76575b70a15250dc0bd731a80548b805f0956a49ab1cff7ef621fc935f9a54`  
		Last Modified: Fri, 19 Apr 2024 22:56:17 GMT  
		Size: 56.5 MB (56519069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b7bc76bbba629a37ad4fcab49df3124f7ebd76c0a6986a2a9864f67eb3d81e`  
		Last Modified: Fri, 19 Apr 2024 22:56:17 GMT  
		Size: 1.5 KB (1510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f330396ec7a4c9863f81a6d93c0d8650c12a7009e7993068670bd67db90e9c`  
		Last Modified: Fri, 19 Apr 2024 22:56:17 GMT  
		Size: 3.2 KB (3250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:a1dffe08fd717acd075334059232b9e89779c614e4109e2f1ceeb4cc5f1ddc80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **863.5 KB (863548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02fca4eb91fab87dac46f57f508af07c8c44e1f291173f8ce3fedabda08fde5a`

```dockerfile
```

-	Layers:
	-	`sha256:2d5f14bbf2e98563df7427bac1117b7f3c147b29d3224b8bd04d5835c1095088`  
		Last Modified: Fri, 19 Apr 2024 22:56:16 GMT  
		Size: 827.3 KB (827291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b2397917f6b858c1adf77f28f9d17dd641ff77b40615e036a83974b25cf5b8d`  
		Last Modified: Fri, 19 Apr 2024 22:56:16 GMT  
		Size: 36.3 KB (36257 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:4c4b2cc3fd035198f53041074462775c6651018df77500e5cc27e332deb5805c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.4 MB (122418936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c3dd5102717d5707822713bdaee350eab8742a338dabd1b2653f88e11e882d6`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Thu, 18 Apr 2024 21:40:47 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 18 Apr 2024 21:40:47 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 18 Apr 2024 21:40:47 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 18 Apr 2024 21:40:47 GMT
ENV DOCKER_VERSION=26.0.2
# Thu, 18 Apr 2024 21:40:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.0.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.0.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.0.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.0.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 18 Apr 2024 21:40:47 GMT
ENV DOCKER_BUILDX_VERSION=0.14.0
# Thu, 18 Apr 2024 21:40:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-amd64'; 			sha256='32f8f17eca35bf2efe6c0e47f40e4692a876f34531b421efc984799a5b41226e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-arm-v6'; 			sha256='7a23989eb26ad27e1b7c11a38dda6a8e6a94562969c19165cf8f49e70203ad20'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-arm-v7'; 			sha256='53b2d827510c6cff41503454caeb0d6613d5ed11201ba10f5ad6c22466cc178c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-arm64'; 			sha256='38bf0ea9c48743edb8243f14272be65a2bad7092228068337aea584309ea664c'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-ppc64le'; 			sha256='847e665e8f1fef3b85c6a5139d9bc57a81bae84d6a882d3ed71e2b5e2bd94bf6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-riscv64'; 			sha256='c853c01f71b6b778b430d985813069d1ca4f2b2e7e039723298350839a556d2b'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-s390x'; 			sha256='6ed2520cf5b7b4b1a985622c61b62d8f65634634b0ef8b3d0594dc1550032d9d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 18 Apr 2024 21:40:47 GMT
ENV DOCKER_COMPOSE_VERSION=2.26.1
# Thu, 18 Apr 2024 21:40:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-x86_64'; 			sha256='2f61856d1b8c9de29ffdaedaa1c6d0a5fc5c79da45068f1f4310feed8d3a3f61'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-armv6'; 			sha256='69ce7a9753e53856b92bb75823893e116d993f92f1e389e0f1a4dae45f79296e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-armv7'; 			sha256='82138d1784ba968b59546d19acad85dbca7bbe67f6614ffb84ef4c3cd72f7a4a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-aarch64'; 			sha256='c86efb0d6347b72af6690f06fbd30ed17023fe67e23e28647cacb4b3f6bfb451'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-ppc64le'; 			sha256='4f4dfc8d6834edfd884d8d5326db0bae3a48f25fe31403684be07faea8822aed'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-riscv64'; 			sha256='575f13c8d567d38bf83fc0885163a505564517f013f01f2e5cd12d989cf88fee'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-s390x'; 			sha256='cbcced8480b8c2ed90c0eb3d4d6c45d6ce8ea0d590961b7ef303bd136c8e85c9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 18 Apr 2024 21:40:47 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 18 Apr 2024 21:40:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:40:47 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 18 Apr 2024 21:40:47 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 18 Apr 2024 21:40:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Apr 2024 21:40:47 GMT
CMD ["sh"]
# Thu, 18 Apr 2024 21:40:47 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 18 Apr 2024 21:40:47 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 18 Apr 2024 21:40:47 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 18 Apr 2024 21:40:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.0.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.0.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.0.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.0.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 18 Apr 2024 21:40:47 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 18 Apr 2024 21:40:47 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 18 Apr 2024 21:40:47 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:40:47 GMT
VOLUME [/var/lib/docker]
# Thu, 18 Apr 2024 21:40:47 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 18 Apr 2024 21:40:47 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 18 Apr 2024 21:40:47 GMT
CMD []
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d295e3a3b46913424fde607d3e771752e6b7eeb8e288b8d9551c5d557d80db1`  
		Last Modified: Fri, 19 Apr 2024 22:54:01 GMT  
		Size: 2.1 MB (2116782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6506740d0b54257c16df0fad45597132ba9e2a5e48bdb69e44b58e893a42ecce`  
		Last Modified: Fri, 19 Apr 2024 22:54:00 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f002aab477516e622c3a7912dff407f79bf61ce872620f847316efe4e1f74b8`  
		Last Modified: Fri, 19 Apr 2024 22:54:02 GMT  
		Size: 15.4 MB (15356416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee8a5a5ed75cb7c9d72745230e7ffd09c2779eb79b2a01829b8d7dfac7e7015`  
		Last Modified: Fri, 19 Apr 2024 22:54:02 GMT  
		Size: 16.9 MB (16915876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c89551b8bec72dae53d57c41fa8c7a4e26f6e008abc80cc89d7ec517d443226`  
		Last Modified: Fri, 19 Apr 2024 22:54:03 GMT  
		Size: 17.6 MB (17631475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e4aa9d5d49ce781c3a8c4bab8b51e130b7e17b4a64851b6c2207c3d0496e30d`  
		Last Modified: Fri, 19 Apr 2024 22:54:02 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbf54ce4917da8d41d1a3cd7ab8544879cf4fd1041e7dfe1562ac82aa518f247`  
		Last Modified: Fri, 19 Apr 2024 22:54:03 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ad6acf8aa89901b90b2840aa1031c6677066ff9118b93186f7d723277c6695`  
		Last Modified: Fri, 19 Apr 2024 22:54:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f009ecce66514e43d5ca64c728c611ac379f814b0407b7e4fa3e64724fe8119`  
		Last Modified: Fri, 19 Apr 2024 23:34:03 GMT  
		Size: 14.3 MB (14316657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b48f8d2743869a6a29342283c2bfd2a4f7ef6e7a0a9d6ba46ecae0f3285e281e`  
		Last Modified: Fri, 19 Apr 2024 23:34:03 GMT  
		Size: 88.4 KB (88359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b938dcd3f0b700c8565b0a8ae27362570144f442a8faa8138511a1628c83d6e`  
		Last Modified: Fri, 19 Apr 2024 23:34:04 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a2eba2ac34ff8dfb583f4a577d99dc73621fb0d031edb53a28ba65097dac075`  
		Last Modified: Fri, 19 Apr 2024 23:34:05 GMT  
		Size: 52.8 MB (52819643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c8528f3fc855421cfd8eeb1c1a3531a9e25b9d3c8153fa662d652d4372ed15`  
		Last Modified: Fri, 19 Apr 2024 23:34:04 GMT  
		Size: 1.5 KB (1510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f9de831cbe8bee372fc7c1c2d33047147f7f3181b128a2aaa03f8ad01bccc2`  
		Last Modified: Fri, 19 Apr 2024 23:34:04 GMT  
		Size: 3.3 KB (3251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:ae9c925e4f8e1f157fd9cc2ae7ca824051bec5f51a4f78252deb8f9f22905387
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.3 KB (36262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5e6b3f32a1e228b649ea207cbfead5839af0882e6916911843f25f8a60f82ef`

```dockerfile
```

-	Layers:
	-	`sha256:7843ba4824c647b3b4a3b5e0c78d068b6ff1da52dc45e5ee75f944aef80ca9c7`  
		Last Modified: Fri, 19 Apr 2024 23:34:02 GMT  
		Size: 36.3 KB (36262 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:6ec9969caddaeedc4fc6888f409851b8bf217415e57198d4dbdc22998d3678b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.6 MB (120624087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc0ec6bcc244c793931d8be17166fd2e9207b59f06e3a3852d1ebbf0aae3c6fe`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Thu, 18 Apr 2024 21:40:47 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 18 Apr 2024 21:40:47 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 18 Apr 2024 21:40:47 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 18 Apr 2024 21:40:47 GMT
ENV DOCKER_VERSION=26.0.2
# Thu, 18 Apr 2024 21:40:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.0.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.0.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.0.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.0.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 18 Apr 2024 21:40:47 GMT
ENV DOCKER_BUILDX_VERSION=0.14.0
# Thu, 18 Apr 2024 21:40:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-amd64'; 			sha256='32f8f17eca35bf2efe6c0e47f40e4692a876f34531b421efc984799a5b41226e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-arm-v6'; 			sha256='7a23989eb26ad27e1b7c11a38dda6a8e6a94562969c19165cf8f49e70203ad20'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-arm-v7'; 			sha256='53b2d827510c6cff41503454caeb0d6613d5ed11201ba10f5ad6c22466cc178c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-arm64'; 			sha256='38bf0ea9c48743edb8243f14272be65a2bad7092228068337aea584309ea664c'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-ppc64le'; 			sha256='847e665e8f1fef3b85c6a5139d9bc57a81bae84d6a882d3ed71e2b5e2bd94bf6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-riscv64'; 			sha256='c853c01f71b6b778b430d985813069d1ca4f2b2e7e039723298350839a556d2b'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-s390x'; 			sha256='6ed2520cf5b7b4b1a985622c61b62d8f65634634b0ef8b3d0594dc1550032d9d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 18 Apr 2024 21:40:47 GMT
ENV DOCKER_COMPOSE_VERSION=2.26.1
# Thu, 18 Apr 2024 21:40:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-x86_64'; 			sha256='2f61856d1b8c9de29ffdaedaa1c6d0a5fc5c79da45068f1f4310feed8d3a3f61'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-armv6'; 			sha256='69ce7a9753e53856b92bb75823893e116d993f92f1e389e0f1a4dae45f79296e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-armv7'; 			sha256='82138d1784ba968b59546d19acad85dbca7bbe67f6614ffb84ef4c3cd72f7a4a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-aarch64'; 			sha256='c86efb0d6347b72af6690f06fbd30ed17023fe67e23e28647cacb4b3f6bfb451'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-ppc64le'; 			sha256='4f4dfc8d6834edfd884d8d5326db0bae3a48f25fe31403684be07faea8822aed'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-riscv64'; 			sha256='575f13c8d567d38bf83fc0885163a505564517f013f01f2e5cd12d989cf88fee'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-s390x'; 			sha256='cbcced8480b8c2ed90c0eb3d4d6c45d6ce8ea0d590961b7ef303bd136c8e85c9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 18 Apr 2024 21:40:47 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 18 Apr 2024 21:40:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:40:47 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 18 Apr 2024 21:40:47 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 18 Apr 2024 21:40:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Apr 2024 21:40:47 GMT
CMD ["sh"]
# Thu, 18 Apr 2024 21:40:47 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 18 Apr 2024 21:40:47 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 18 Apr 2024 21:40:47 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 18 Apr 2024 21:40:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.0.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.0.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.0.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.0.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 18 Apr 2024 21:40:47 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 18 Apr 2024 21:40:47 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 18 Apr 2024 21:40:47 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:40:47 GMT
VOLUME [/var/lib/docker]
# Thu, 18 Apr 2024 21:40:47 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 18 Apr 2024 21:40:47 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 18 Apr 2024 21:40:47 GMT
CMD []
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62203ebc003cf77a4ff92a3c67a89cd14dcf1adf84fb125d2f3329ad08ad9a61`  
		Last Modified: Sat, 16 Mar 2024 15:21:10 GMT  
		Size: 1.9 MB (1896160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8418dd6a88f431ade9efd4277500a4c6483d9ac98459ff95a86dbfde7d02e2a`  
		Last Modified: Sat, 16 Mar 2024 15:21:10 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdba6056ccaefe750f1bf47894a97cfc852a20698b6248b0410d1b292577c06e`  
		Last Modified: Fri, 19 Apr 2024 23:03:36 GMT  
		Size: 15.3 MB (15349194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21e7f9b82fa07d6ea48df760cc2b4c3a39e010f538e48bb3ad7b5150237e3700`  
		Last Modified: Fri, 19 Apr 2024 23:03:36 GMT  
		Size: 16.9 MB (16901904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f41ecc08302226ea8603566661acd930845d981149c25e21aceabf9586700a43`  
		Last Modified: Fri, 19 Apr 2024 23:03:37 GMT  
		Size: 17.6 MB (17616603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7046b6af7443e3b9221d313ba36dae457ce25ad7d7d8f14f025e457d76fff3b4`  
		Last Modified: Fri, 19 Apr 2024 23:03:36 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a0ab16bfc127a282facd2417a1ad2c62068de6c5a6e46effaba79440ca5b435`  
		Last Modified: Fri, 19 Apr 2024 23:03:37 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab3b08239b1d6bd68f235c1dc1f97236a70525306d1bfafd8c678552632e71e`  
		Last Modified: Fri, 19 Apr 2024 23:03:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fa061313b4e38408cefb3558e08bf92f967593b9002239700a84508c1fc4889`  
		Last Modified: Fri, 19 Apr 2024 23:40:51 GMT  
		Size: 13.0 MB (13029152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e6c731988693f1fb4913ea5054c2664ea79d1de9c80dc3e0ea8533b8db53330`  
		Last Modified: Fri, 19 Apr 2024 23:40:50 GMT  
		Size: 84.3 KB (84290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1378543b23cf9cd2a08f141a200e884fd3a58834b0a89e71aa2ddd6994f99a19`  
		Last Modified: Fri, 19 Apr 2024 23:40:50 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e59a06125c370827ccfb5b3f3a882b03347b5c38dce53be918712c9427e0500`  
		Last Modified: Fri, 19 Apr 2024 23:40:52 GMT  
		Size: 52.8 MB (52819569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf24f74036d8bc850599ed719307b40f55f9da5323c30194a16a6f2ee77d93c6`  
		Last Modified: Fri, 19 Apr 2024 23:40:51 GMT  
		Size: 1.5 KB (1508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb070ed7c8c1403258fdde1cd59dc892663d0c194ea60f3f12abba4b44403db`  
		Last Modified: Fri, 19 Apr 2024 23:40:51 GMT  
		Size: 3.2 KB (3247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:1f05cdc5fbe81a42b022a4be6b27de869e6b1ab4973f9ae110c4b8526dfc366e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **860.9 KB (860931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cff730862cc3e7ebaee19565712357a01a029bc77d79398d43cb4ad1c0d88d37`

```dockerfile
```

-	Layers:
	-	`sha256:8c6ed509e5a166c0e78538e9457ed610939fe6e6da3de2a87d258e539c968a12`  
		Last Modified: Fri, 19 Apr 2024 23:40:49 GMT  
		Size: 824.5 KB (824450 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d07ed86c76726b8270a6ec20eb9e76be0f996a8a2661b607fef8459fa1895b4`  
		Last Modified: Fri, 19 Apr 2024 23:40:49 GMT  
		Size: 36.5 KB (36481 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:472a1e2ac04a6ff391927a0d573497ea86302b582ca5c5063ad9b5d0471cc6c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.7 MB (121714275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96b4312f4468115e8ad04a4b3832e4e6bd7d5155bf80aaa0ef612178fb2c2dc3`
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

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:1d48de40cadd26d749aff3b67608b76955ab8974c225ba3bc1a42f4626faa0ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **859.3 KB (859269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31209a14874fd4203caf4da1a66c1ae110011ef365be97982ab1863c2f3c32bd`

```dockerfile
```

-	Layers:
	-	`sha256:9b3ed83b7c26fa3888f3f4f0073e818b6892d5f750418b7df89b0d896f79b74c`  
		Last Modified: Fri, 12 Apr 2024 05:55:13 GMT  
		Size: 822.9 KB (822941 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3eaa4a1350df8fd4f46b49926fe9841479394bc1b57a2450637847d6a99d26b3`  
		Last Modified: Fri, 12 Apr 2024 05:55:13 GMT  
		Size: 36.3 KB (36328 bytes)  
		MIME: application/vnd.in-toto+json
