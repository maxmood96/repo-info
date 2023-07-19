## `docker:24-dind-rootless`

```console
$ docker pull docker@sha256:b8fa997e8c4ee02ff4375963ba2dd6725fc9eaed7a41b1c4a3af85898c708edb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:24-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:756f99e4701c73d0c0ade59e5d15ee8da94b6226c0a67d19507c347687102747
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.7 MB (142720561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baa1d1e225c20290e93bdd24b8030ebc1dfb541ce7a67228d7ce4d213b4c794f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Wed, 19 Jul 2023 17:05:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 19 Jul 2023 17:05:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 19 Jul 2023 17:05:42 GMT
ENV DOCKER_VERSION=24.0.4
# Wed, 19 Jul 2023 17:05:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 19 Jul 2023 17:05:42 GMT
ENV DOCKER_BUILDX_VERSION=0.11.2
# Wed, 19 Jul 2023 17:05:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-amd64'; 			sha256='311568ee69715abc46163fd688e56c77ab0144ff32e116d0f293bfc3470e75b7'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-arm-v6'; 			sha256='c1bab0c7374406d5069f60b291971d71161fbd3c00e8a8fb1b68b9053eda8a4e'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-arm-v7'; 			sha256='4defdf463ca2516d3f58fef69a6f78cbbb8baf16d936cdfc54df4a4be0d48f7f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-arm64'; 			sha256='565e36085a35bba5104f37365ba796c111338eea1a0902b3a7ff42e2e1248815'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-ppc64le'; 			sha256='c5f5cb9957890873a537c7ff5c4eef36132339622baeabb37a4b9b7251ddf836'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-riscv64'; 			sha256='c0adc4b4625f7e3df7dcdec840568f918673f2ed4bcd03ca1e63ea2a5627ca35'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-s390x'; 			sha256='02916c76c3872fd0b3fa57e71403fee92b6be10f350b96a5ff99e7914dd277b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 19 Jul 2023 17:05:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.20.2
# Wed, 19 Jul 2023 17:05:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.20.2/docker-compose-linux-x86_64'; 			sha256='b9385dabb7931636a3afc0aee94625ebff3bb29584493a87804afb6ebaf2d916'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.20.2/docker-compose-linux-armv6'; 			sha256='39cef332454d1c7a26e12f8d9ee297908d1da9cb71112ede1816c550766ddb8e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.20.2/docker-compose-linux-armv7'; 			sha256='139275f3453761b46f0837a4e4c2a00883b778abee997e299c52e1bcf3d8fc9f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.20.2/docker-compose-linux-aarch64'; 			sha256='e63a24e57d2104a09b37ee6aa04c76f4ae85bdf7a59e1bf79adc6d5f55340a31'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.20.2/docker-compose-linux-ppc64le'; 			sha256='9c08eb875a7ffd4a832a585540a4c9c81da5dcab263ec3e704ab1d62b573636f'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.20.2/docker-compose-linux-riscv64'; 			sha256='5a3bff32ecf0a5a38a83afeb3dc2effd8ca3d52eb2e07ec000334663d493055b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.20.2/docker-compose-linux-s390x'; 			sha256='297be6a0ece070ae95d5caf91a23b89dc1b2563e928db80eee480d7018919ee6'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 19 Jul 2023 17:05:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 19 Jul 2023 17:05:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 19 Jul 2023 17:05:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 19 Jul 2023 17:05:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 19 Jul 2023 17:05:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 19 Jul 2023 17:05:42 GMT
CMD ["sh"]
# Fri, 07 Jul 2023 21:23:59 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Fri, 07 Jul 2023 21:23:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 07 Jul 2023 21:23:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 07 Jul 2023 21:23:59 GMT
ENV DIND_COMMIT=d58df1fc6c866447ce2cd129af10e5b507705624
# Fri, 07 Jul 2023 21:23:59 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 07 Jul 2023 21:23:59 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 07 Jul 2023 21:23:59 GMT
VOLUME [/var/lib/docker]
# Fri, 07 Jul 2023 21:23:59 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 07 Jul 2023 21:23:59 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 07 Jul 2023 21:23:59 GMT
CMD []
# Fri, 07 Jul 2023 21:23:59 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Fri, 07 Jul 2023 21:23:59 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 07 Jul 2023 21:23:59 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 07 Jul 2023 21:23:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-24.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-24.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 07 Jul 2023 21:23:59 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 07 Jul 2023 21:23:59 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 07 Jul 2023 21:23:59 GMT
USER rootless
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7d0e1aee3d7ae6d265ee545cbab734bf74984f2c92ce1e9de99384496437d9`  
		Last Modified: Thu, 15 Jun 2023 05:27:05 GMT  
		Size: 2.0 MB (2014369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:616dc7f2241d214810794d133404c6c0fce720828611e22602fb0509d3b7dc6c`  
		Last Modified: Thu, 15 Jun 2023 05:27:05 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49f83d66c9f2978256f5af482db96fc7c7c0c35e61a85ad5580a2078ea66adf9`  
		Last Modified: Mon, 10 Jul 2023 19:28:02 GMT  
		Size: 16.4 MB (16389603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90bde9fd98629e849be4c1c842a3f6ab622a43952b7b5d4f9ced2dc8c3dd9f00`  
		Last Modified: Wed, 19 Jul 2023 20:22:41 GMT  
		Size: 17.5 MB (17459296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4efa32db2427829573666edca06e2b55de2a58199ee74f32f4926e55c03fa99`  
		Last Modified: Wed, 19 Jul 2023 20:22:41 GMT  
		Size: 18.0 MB (17988797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:065a5d67b5a32047d0ce6dd3048b96752ccb52e577d9214b83dca4e1118b7c4e`  
		Last Modified: Wed, 19 Jul 2023 20:22:38 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0910dd0b8996b622e8eb2a914ebf833079e75d501a1f29551590b074c1e1c6f`  
		Last Modified: Wed, 19 Jul 2023 20:22:38 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a29df90565e359d0707552639e00f12e37fd5a4a0c04fd85e48d42e4ee4606`  
		Last Modified: Wed, 19 Jul 2023 20:22:38 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a4c378ddc5965fd3ba622b2cc663cd0cac4ff81b90dfbfaface41054c905176`  
		Last Modified: Wed, 19 Jul 2023 20:22:59 GMT  
		Size: 9.3 MB (9266776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b79ecdcbdf3b5c1a425caea8972ad9c23f75617ec26dc49f72295dd0b7df85a5`  
		Last Modified: Wed, 19 Jul 2023 20:22:57 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9ff431477f2332da8104ee103875b3d6ec72fa4846b797a56286af56a9cd5f`  
		Last Modified: Wed, 19 Jul 2023 20:23:05 GMT  
		Size: 54.2 MB (54182367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2030f7531c7716c87038e59801646ce93e57e1b14d0152ec28f79bec9865dde`  
		Last Modified: Wed, 19 Jul 2023 20:22:57 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f99062ad67c9fa50f996bbb53460ccca0023e42ce993e8f04fb22875d31f57`  
		Last Modified: Wed, 19 Jul 2023 20:22:57 GMT  
		Size: 2.8 KB (2791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86207ebcf9843c3838c68da5c97e546d682d11f59f7f5f588d7e0bf80ba384bf`  
		Last Modified: Wed, 19 Jul 2023 20:23:33 GMT  
		Size: 1.4 MB (1362401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1c7cacfda991a82f62139d84fc9681785d6297ad7de2bef1bb9e00b6c4068d0`  
		Last Modified: Wed, 19 Jul 2023 20:23:33 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c93327f0fb6847584acbcd81664ce51301a898d386e9bdcc37de0e48087ddfb`  
		Last Modified: Wed, 19 Jul 2023 20:23:32 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:803c27132cd97c96ac7144e16a6bdc4d531989d18d3ee66e91f3dd7a3ad17875`  
		Last Modified: Wed, 19 Jul 2023 20:23:36 GMT  
		Size: 20.7 MB (20650351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51eea0f4288852510cc8fed09c3604b2e5ac3ed917f256e8ff4a409c51102c14`  
		Last Modified: Wed, 19 Jul 2023 20:23:32 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:24-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:022404564ad32458c0276e846bb6cca51add70e26992f5f8e2048ee5e420b7a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135595538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c9c5ef900e99a8f63d43d3997fa774e53e8349de3aace06ef52f2de98a2aacb`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Wed, 19 Jul 2023 17:05:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 19 Jul 2023 17:05:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 19 Jul 2023 17:05:42 GMT
ENV DOCKER_VERSION=24.0.4
# Wed, 19 Jul 2023 17:05:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 19 Jul 2023 17:05:42 GMT
ENV DOCKER_BUILDX_VERSION=0.11.2
# Wed, 19 Jul 2023 17:05:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-amd64'; 			sha256='311568ee69715abc46163fd688e56c77ab0144ff32e116d0f293bfc3470e75b7'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-arm-v6'; 			sha256='c1bab0c7374406d5069f60b291971d71161fbd3c00e8a8fb1b68b9053eda8a4e'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-arm-v7'; 			sha256='4defdf463ca2516d3f58fef69a6f78cbbb8baf16d936cdfc54df4a4be0d48f7f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-arm64'; 			sha256='565e36085a35bba5104f37365ba796c111338eea1a0902b3a7ff42e2e1248815'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-ppc64le'; 			sha256='c5f5cb9957890873a537c7ff5c4eef36132339622baeabb37a4b9b7251ddf836'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-riscv64'; 			sha256='c0adc4b4625f7e3df7dcdec840568f918673f2ed4bcd03ca1e63ea2a5627ca35'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-s390x'; 			sha256='02916c76c3872fd0b3fa57e71403fee92b6be10f350b96a5ff99e7914dd277b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 19 Jul 2023 17:05:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.20.2
# Wed, 19 Jul 2023 17:05:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.20.2/docker-compose-linux-x86_64'; 			sha256='b9385dabb7931636a3afc0aee94625ebff3bb29584493a87804afb6ebaf2d916'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.20.2/docker-compose-linux-armv6'; 			sha256='39cef332454d1c7a26e12f8d9ee297908d1da9cb71112ede1816c550766ddb8e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.20.2/docker-compose-linux-armv7'; 			sha256='139275f3453761b46f0837a4e4c2a00883b778abee997e299c52e1bcf3d8fc9f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.20.2/docker-compose-linux-aarch64'; 			sha256='e63a24e57d2104a09b37ee6aa04c76f4ae85bdf7a59e1bf79adc6d5f55340a31'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.20.2/docker-compose-linux-ppc64le'; 			sha256='9c08eb875a7ffd4a832a585540a4c9c81da5dcab263ec3e704ab1d62b573636f'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.20.2/docker-compose-linux-riscv64'; 			sha256='5a3bff32ecf0a5a38a83afeb3dc2effd8ca3d52eb2e07ec000334663d493055b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.20.2/docker-compose-linux-s390x'; 			sha256='297be6a0ece070ae95d5caf91a23b89dc1b2563e928db80eee480d7018919ee6'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 19 Jul 2023 17:05:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 19 Jul 2023 17:05:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 19 Jul 2023 17:05:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 19 Jul 2023 17:05:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 19 Jul 2023 17:05:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 19 Jul 2023 17:05:42 GMT
CMD ["sh"]
# Fri, 07 Jul 2023 21:23:59 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Fri, 07 Jul 2023 21:23:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 07 Jul 2023 21:23:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 07 Jul 2023 21:23:59 GMT
ENV DIND_COMMIT=d58df1fc6c866447ce2cd129af10e5b507705624
# Fri, 07 Jul 2023 21:23:59 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 07 Jul 2023 21:23:59 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 07 Jul 2023 21:23:59 GMT
VOLUME [/var/lib/docker]
# Fri, 07 Jul 2023 21:23:59 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 07 Jul 2023 21:23:59 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 07 Jul 2023 21:23:59 GMT
CMD []
# Fri, 07 Jul 2023 21:23:59 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Fri, 07 Jul 2023 21:23:59 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 07 Jul 2023 21:23:59 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 07 Jul 2023 21:23:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-24.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-24.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 07 Jul 2023 21:23:59 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 07 Jul 2023 21:23:59 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 07 Jul 2023 21:23:59 GMT
USER rootless
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e640e1526600576ae628fd21f3470e3216d9579d4b14b1032c2ed619de68e53`  
		Last Modified: Wed, 14 Jun 2023 22:40:52 GMT  
		Size: 2.0 MB (2024530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2eba5565b7a07c4d4ea27b5423aca276dfd220175588874377309ecab83ecc`  
		Last Modified: Wed, 14 Jun 2023 22:40:52 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c19aadc22366563d3dabd7151e690b7bfe4b2f1db8f3419a507fb07e013b6f96`  
		Last Modified: Mon, 10 Jul 2023 19:41:27 GMT  
		Size: 15.4 MB (15435078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e70e5ec6da172ec838c790286d3aaa2ebd964b0951a01ed8eb1a4e2b352ce7a`  
		Last Modified: Wed, 19 Jul 2023 20:40:44 GMT  
		Size: 15.8 MB (15768112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d3fbbc691e72b7081573dabb096aa95342bf34ae681d4a622ef7696651a4830`  
		Last Modified: Wed, 19 Jul 2023 20:40:44 GMT  
		Size: 16.3 MB (16320826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49b41b17c20e03697f28f7f7c2e860389b78d7b471fc425016adee114f8293fb`  
		Last Modified: Wed, 19 Jul 2023 20:40:42 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a826f2b3dad06e2444cc9ffde222e2b700967914f722b6887fc549069654bb2d`  
		Last Modified: Wed, 19 Jul 2023 20:40:42 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5531ba243dbfea631cc734f355ea8045ffe2a81893eb9d7567e543b8b2de673`  
		Last Modified: Wed, 19 Jul 2023 20:40:42 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4285121a81bf04cd8bbfdc670745f5e58ec0ce332834294adb8c8a5a6f2eca`  
		Last Modified: Wed, 19 Jul 2023 20:41:01 GMT  
		Size: 9.4 MB (9359452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e8c414b5e5057d0725d185d1e0832ff765c99dac23b0a50df72b0d90a9e1091`  
		Last Modified: Wed, 19 Jul 2023 20:41:00 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:493972f3fddd95f175cd09fd326797252531f413b3eb9c08ed1cb9832c68dfce`  
		Last Modified: Wed, 19 Jul 2023 20:41:05 GMT  
		Size: 49.5 MB (49485562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e508478045931994623c57010a7db7c9d334d609ec693f18bd3031fa0b4e3637`  
		Last Modified: Wed, 19 Jul 2023 20:41:00 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdb3c461dc3d4a930a2cedef4a9af6ba9df0b3e23160f5959ed24febdb6da3bb`  
		Last Modified: Wed, 19 Jul 2023 20:41:00 GMT  
		Size: 2.8 KB (2790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ab9b76efd749ada845e648a7ead0a551bafa4b9f6c164f5d698d3dc14668ba3`  
		Last Modified: Wed, 19 Jul 2023 20:41:33 GMT  
		Size: 1.4 MB (1413226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb6e0c4666889c5df5feae6c7164063c41bf5ffd2ffc0b962aa557bf0af4dfa2`  
		Last Modified: Wed, 19 Jul 2023 20:41:32 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a523e7599e8d0452d8bf374ecf586d965317bd361d89acdf796880a7c39eed73`  
		Last Modified: Wed, 19 Jul 2023 20:41:32 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:724b5b46a5119e78e7397818c5a8f4df04e1104425b400493658f35f8ffab0cb`  
		Last Modified: Wed, 19 Jul 2023 20:41:35 GMT  
		Size: 22.5 MB (22450778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:090bba6460069fdd2827810041059436f6ea34ab4e39e7b9acb84529466fcfa4`  
		Last Modified: Wed, 19 Jul 2023 20:41:32 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
