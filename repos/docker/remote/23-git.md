## `docker:23-git`

```console
$ docker pull docker@sha256:1087ac3621fe68a4e9d104d8af84769bb76fe9a28620cb46db06b5faa66d66f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:23-git` - linux; amd64

```console
$ docker pull docker@sha256:aeb809a2d8bedd4d542815244c38c1333afa4400a6f97320ddddd62dfb86881e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.6 MB (120580604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdf9f53565bea70998c8a8378949dbc9b554a7ba54ad5a066bf5fcac3df52d20`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 16 May 2023 17:59:38 GMT
ADD file:32ff5e7a78b890996ee4681cc0a26185d3e9acdb4eb1e2aaccb2411f922fed6b in / 
# Tue, 16 May 2023 17:59:38 GMT
CMD ["/bin/sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_VERSION=23.0.6
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_BUILDX_VERSION=0.11.2
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-amd64'; 			sha256='311568ee69715abc46163fd688e56c77ab0144ff32e116d0f293bfc3470e75b7'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-arm-v6'; 			sha256='c1bab0c7374406d5069f60b291971d71161fbd3c00e8a8fb1b68b9053eda8a4e'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-arm-v7'; 			sha256='4defdf463ca2516d3f58fef69a6f78cbbb8baf16d936cdfc54df4a4be0d48f7f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-arm64'; 			sha256='565e36085a35bba5104f37365ba796c111338eea1a0902b3a7ff42e2e1248815'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-ppc64le'; 			sha256='c5f5cb9957890873a537c7ff5c4eef36132339622baeabb37a4b9b7251ddf836'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-riscv64'; 			sha256='c0adc4b4625f7e3df7dcdec840568f918673f2ed4bcd03ca1e63ea2a5627ca35'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-s390x'; 			sha256='02916c76c3872fd0b3fa57e71403fee92b6be10f350b96a5ff99e7914dd277b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.20.3
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.20.3/docker-compose-linux-x86_64'; 			sha256='f45e4cb687df8b48a57f656097ce7175fa8e8bef70be407b011e29ff663f475f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.20.3/docker-compose-linux-armv6'; 			sha256='e2010f160f5077c6d4d777965d21147328dbfb29894e60a5fbbce716284fd3cf'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.20.3/docker-compose-linux-armv7'; 			sha256='f62e5fb2e1908152c5f3e250faa2057c3d3351207eedd4c042ff540bba5f7575'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.20.3/docker-compose-linux-aarch64'; 			sha256='9d6a6396b7604a390977ffff78379090f7c6910160bbd3b9669e2fcc635633c5'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.20.3/docker-compose-linux-ppc64le'; 			sha256='463d3d220da0fe49c40605a1fc9e4ed7414f47c0ac028c80c55d2e758e99d7ee'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.20.3/docker-compose-linux-riscv64'; 			sha256='03b0ec338482f61593074b62ffab482ae67ecdc5d868eb72bb8fe3f8a7680c91'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.20.3/docker-compose-linux-s390x'; 			sha256='3b24ddd85e859757801a8b9a7e53b96882fa5fd18cc12ee8750770f43b6afa14'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DIND_COMMIT=d58df1fc6c866447ce2cd129af10e5b507705624
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
RUN apk add --no-cache git # buildkit
```

-	Layers:
	-	`sha256:7264a8db6415046d36d16ba98b79778e18accee6ffa71850405994cffa9be7de`  
		Last Modified: Mon, 07 Aug 2023 19:20:54 GMT  
		Size: 3.4 MB (3401613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98bffc520d67dabddd6fb8658293a610f4bb31a46421110e49ffdc39bd72266a`  
		Last Modified: Fri, 11 Aug 2023 18:50:37 GMT  
		Size: 2.0 MB (2014276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d450dfcd6f7d26ecc4a80ef1a707893b0bc5d6dcb4120b84fc6db66d5cef9b`  
		Last Modified: Fri, 11 Aug 2023 18:50:38 GMT  
		Size: 16.3 MB (16250856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9b3ed45a0be2965d795fcb8562c8ee3ff24d51f6cf398480016c3f4a1edd9e`  
		Last Modified: Fri, 11 Aug 2023 18:50:38 GMT  
		Size: 17.5 MB (17459266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6d1d9e68d5c1d269761ca3674e7edeca26be5089b3641a08e438b7b45828a6`  
		Last Modified: Fri, 11 Aug 2023 18:50:38 GMT  
		Size: 17.8 MB (17775004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3b9891838a93724160d82f5b6b58815c8c57f08b41b1a5feecbaeff6fb6c3c`  
		Last Modified: Fri, 11 Aug 2023 18:50:38 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e62c4987c19cba64cc91c3bfd48af11048485b37daebc4c25657a983b80bea`  
		Last Modified: Fri, 11 Aug 2023 18:50:39 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63c5f95131a60cf19a61ab98bd062e0db9d29d0129f9fa9bfb9568e8f95dd58c`  
		Last Modified: Fri, 11 Aug 2023 18:50:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea690df0ecdafe20af5c9ef1c0e3a7aba137bc69f0406bb1c5b82dbff49ec533`  
		Last Modified: Fri, 11 Aug 2023 19:50:44 GMT  
		Size: 7.1 MB (7080066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d24c11514afe943e41f7465e47a6c324504f27747ed8e278767ee1f199f9ddcf`  
		Last Modified: Fri, 11 Aug 2023 19:50:44 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:839ccfaa059e49126a938b8850c9df3ec38cf484c0c95f5c14b9eb50fb36a895`  
		Last Modified: Fri, 11 Aug 2023 19:50:46 GMT  
		Size: 51.7 MB (51657455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9543fb2907b72ec5df755f4db825a5ae32f4cbdc749e989965f9d72ee7bcb6`  
		Last Modified: Fri, 11 Aug 2023 19:50:44 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd0eacfced14419234a05f1b1e9e19eccc3865252109121bf0dae89617cff219`  
		Last Modified: Fri, 11 Aug 2023 19:50:44 GMT  
		Size: 2.8 KB (2790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cccdbbaec66df698f6a4bc2707bf638518ab567ee7a7530bf4588bf9eb5b3b45`  
		Last Modified: Fri, 11 Aug 2023 20:50:44 GMT  
		Size: 4.9 MB (4935241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:23-git` - unknown; unknown

```console
$ docker pull docker@sha256:513d96a7dbd54ac24532ceaeb052d7bf47a53386ccea8cb7a281e20baf9baf76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **814.2 KB (814182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae59ba2a28674e14a1f3564e14bee647ebf01c4212543ce18f04dd1e861f24c0`

```dockerfile
```

-	Layers:
	-	`sha256:b85b9d41fde510641bcb1ba814e5636f08b12377573e5f1405cb311d8d0ac750`  
		Last Modified: Fri, 11 Aug 2023 20:50:44 GMT  
		Size: 801.5 KB (801546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffc584ef81418ce781a3bc205d1f7074e3c3be25ce94c1ed266ade93b1962460`  
		Last Modified: Fri, 11 Aug 2023 20:50:44 GMT  
		Size: 12.6 KB (12636 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:23-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:63564662fa78db8c67628dd3002a41d073161edee577ad37a5808bf61a3fdcbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.1 MB (112055028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71f860b3d76384b038376e9a37436f6fff23b676a5868359d8169fe59cdf1169`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 16 May 2023 17:59:38 GMT
ADD file:b2e7eaa7e41f08853dbe08d84439a7f9fd32fc58c3aa1e298f3f60343b2b683a in / 
# Tue, 16 May 2023 17:59:38 GMT
CMD ["/bin/sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_VERSION=23.0.6
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_BUILDX_VERSION=0.11.2
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-amd64'; 			sha256='311568ee69715abc46163fd688e56c77ab0144ff32e116d0f293bfc3470e75b7'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-arm-v6'; 			sha256='c1bab0c7374406d5069f60b291971d71161fbd3c00e8a8fb1b68b9053eda8a4e'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-arm-v7'; 			sha256='4defdf463ca2516d3f58fef69a6f78cbbb8baf16d936cdfc54df4a4be0d48f7f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-arm64'; 			sha256='565e36085a35bba5104f37365ba796c111338eea1a0902b3a7ff42e2e1248815'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-ppc64le'; 			sha256='c5f5cb9957890873a537c7ff5c4eef36132339622baeabb37a4b9b7251ddf836'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-riscv64'; 			sha256='c0adc4b4625f7e3df7dcdec840568f918673f2ed4bcd03ca1e63ea2a5627ca35'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-s390x'; 			sha256='02916c76c3872fd0b3fa57e71403fee92b6be10f350b96a5ff99e7914dd277b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.20.3
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.20.3/docker-compose-linux-x86_64'; 			sha256='f45e4cb687df8b48a57f656097ce7175fa8e8bef70be407b011e29ff663f475f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.20.3/docker-compose-linux-armv6'; 			sha256='e2010f160f5077c6d4d777965d21147328dbfb29894e60a5fbbce716284fd3cf'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.20.3/docker-compose-linux-armv7'; 			sha256='f62e5fb2e1908152c5f3e250faa2057c3d3351207eedd4c042ff540bba5f7575'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.20.3/docker-compose-linux-aarch64'; 			sha256='9d6a6396b7604a390977ffff78379090f7c6910160bbd3b9669e2fcc635633c5'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.20.3/docker-compose-linux-ppc64le'; 			sha256='463d3d220da0fe49c40605a1fc9e4ed7414f47c0ac028c80c55d2e758e99d7ee'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.20.3/docker-compose-linux-riscv64'; 			sha256='03b0ec338482f61593074b62ffab482ae67ecdc5d868eb72bb8fe3f8a7680c91'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.20.3/docker-compose-linux-s390x'; 			sha256='3b24ddd85e859757801a8b9a7e53b96882fa5fd18cc12ee8750770f43b6afa14'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DIND_COMMIT=d58df1fc6c866447ce2cd129af10e5b507705624
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
RUN apk add --no-cache git # buildkit
```

-	Layers:
	-	`sha256:9fda8d8052c61740409c4bea888859c141fd8cc3f58ac61943144ff6d1681b2d`  
		Last Modified: Mon, 07 Aug 2023 19:39:45 GMT  
		Size: 3.3 MB (3330767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6852f3ef0b5f9b77c7c21abf9035ed77c331514fd6aa1498370a5dbd3e2048b5`  
		Last Modified: Mon, 07 Aug 2023 22:18:57 GMT  
		Size: 2.0 MB (2024556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5fa0183f177eef4fbf1985af430c61c77b95421f027eea28f816b0cd1422c2a`  
		Last Modified: Mon, 07 Aug 2023 22:43:59 GMT  
		Size: 15.3 MB (15325086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee7e69ab8affe56e6a48d95a413242bda38be403d58d989c83afd66e5ecddeb`  
		Last Modified: Mon, 07 Aug 2023 22:43:59 GMT  
		Size: 15.8 MB (15768048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8aaebe906561cb42268d9c65693ff93af99196ddf8c1e458f09696236ff61b2`  
		Last Modified: Fri, 11 Aug 2023 19:44:53 GMT  
		Size: 16.2 MB (16233579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b5960a34667065c72697817f35c0319e2e3a2285c87d6537dcffd413d3e9ca`  
		Last Modified: Fri, 11 Aug 2023 19:44:52 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e7e976f07bbb77bd91c3c11c8d031fff6de3f83dfb0c73401fee1586a2e48f`  
		Last Modified: Fri, 11 Aug 2023 19:44:51 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cff4ee2d5ff5467ed15b93f16cf3039f34219c9d12b88c7e0adeae9845d23b9`  
		Last Modified: Fri, 11 Aug 2023 19:44:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17dfbddc9408b8533e30e88b7a207a84eb71e8c74527bb54dab0e1eb3f402c28`  
		Last Modified: Fri, 11 Aug 2023 19:51:45 GMT  
		Size: 7.3 MB (7291228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b8bb9aa52255b29d0e13e7af1ea0e3db87093ac3cf9f5789a06b18795eb754f`  
		Last Modified: Fri, 11 Aug 2023 19:51:44 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c2864d07b59e68e46d0d4a0aa5cf9a61d4535a53e2317e5f01d955ddfbcad3b`  
		Last Modified: Fri, 11 Aug 2023 19:51:48 GMT  
		Size: 47.1 MB (47053371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c68c5a9d5540985902dee670b0adfb318eeea0655db88b38655d2285c82ead`  
		Last Modified: Fri, 11 Aug 2023 19:51:44 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a9821c3135c69ab0e187955879c4bdedd4fbb4b5e4195dede2bd0b87d622ed3`  
		Last Modified: Fri, 11 Aug 2023 19:51:45 GMT  
		Size: 2.8 KB (2795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aca6e8dd0795db0393a03a9de5507574b3cb327ba4731079d8f336b7afb93d58`  
		Last Modified: Fri, 11 Aug 2023 21:05:46 GMT  
		Size: 5.0 MB (5021554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:23-git` - unknown; unknown

```console
$ docker pull docker@sha256:fde913bf7a6f9ddaa9278d70ea67d7192b48e2890149c4e3d464076d9ac9c153
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **812.2 KB (812223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4d18e1d456d2164f10285d9664923cf55705524292dc1f592f18ddf97f829b8`

```dockerfile
```

-	Layers:
	-	`sha256:0e0f55c980c440412b4d738c1c87fd3f1b2a2527a3acff8f17f21fd157e952d0`  
		Last Modified: Fri, 11 Aug 2023 21:05:45 GMT  
		Size: 801.8 KB (801755 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:001037644f5c72972805b8c7e7d37300383174d23de721e8060834cbc1e5e702`  
		Last Modified: Fri, 11 Aug 2023 21:05:45 GMT  
		Size: 10.5 KB (10468 bytes)  
		MIME: application/vnd.in-toto+json
