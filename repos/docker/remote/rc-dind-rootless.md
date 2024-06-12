## `docker:rc-dind-rootless`

```console
$ docker pull docker@sha256:47113ee26006c463b7f7d7492af242c7673c7b70fffdc78eacffc1f1b28e202b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:rc-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:4d06440f0a9a4cc2d9ca7be6960b3f2638ad63d322b29a64b6f05738669f7077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.3 MB (149251274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:966887c7bd59e63cf6ed92def371219d16ed3fa4306059c2b95e60e3ba62fa0d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Wed, 20 Mar 2024 05:04:39 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 20 Mar 2024 05:04:39 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 20 Mar 2024 05:04:39 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 20 Mar 2024 05:04:39 GMT
ENV DOCKER_VERSION=26.0.0-rc3
# Wed, 20 Mar 2024 05:04:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-26.0.0-rc3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-26.0.0-rc3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-26.0.0-rc3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-26.0.0-rc3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 20 Mar 2024 05:04:39 GMT
ENV DOCKER_BUILDX_VERSION=0.13.1
# Wed, 20 Mar 2024 05:04:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-amd64'; 			sha256='3e2bc8ed25a9125d6aeec07df4e0211edea6288e075b524160ef3fd305d3d74c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm-v6'; 			sha256='643063c656098e312533fe5ee3411523fa06cc3926bd2e96b4c6239b9cecbf88'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm-v7'; 			sha256='8d42e7823237e777b121070fda6ad68159539aa6597aedfa7630384643ad6f9a'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm64'; 			sha256='3ba35a5d38361a64b62aeb9d20acc835ff6862a711cb438e610026b29c0ac489'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-ppc64le'; 			sha256='1d16f7b15706d98523889a1ca50e9dfc44bbaec1f736d883a0528805795b9de2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-riscv64'; 			sha256='202221c9b7fb881d092986e8ec2497ee71729f17c4afd912384a086af700e1ad'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-s390x'; 			sha256='71d7c39192b1b07790eb71e46742cc69a559f3eb00a1512f4a8d2ea1067408da'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 20 Mar 2024 05:04:39 GMT
ENV DOCKER_COMPOSE_VERSION=2.25.0
# Wed, 20 Mar 2024 05:04:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-x86_64'; 			sha256='53641b8a28419f947bc58c085e0c39b97a209b6e875a25c585e7fab44ff48576'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-armv6'; 			sha256='a123b79b530a65c7381ca8bb3b29cde7177f4f260984a127d998c9696cae794c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-armv7'; 			sha256='8ea72e93e8da8259d7d5d051f3c65dc14c44a23d5ebc6939394d7d03b147e238'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-aarch64'; 			sha256='b9f303c9f9db75ecf18ea6fc516b3dc54a3e54f3b3d8e7f1a449416522958bc5'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-ppc64le'; 			sha256='dc067ab61239cef3d2e145d37fcd68c1fc2320c6728d77a9a4ec4fb0e6c6dd64'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-riscv64'; 			sha256='a17f07604fa74c661e62d5e27ae358f8a611f42bb9a4a147cec76b8bb591bea4'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-s390x'; 			sha256='9e613275e5fa46cb864d3f2fccb10e3239b879527d075490b03e381df56c397c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 20 Mar 2024 05:04:39 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 20 Mar 2024 05:04:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 05:04:39 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 20 Mar 2024 05:04:39 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 20 Mar 2024 05:04:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 05:04:39 GMT
CMD ["sh"]
# Wed, 20 Mar 2024 05:04:39 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 20 Mar 2024 05:04:39 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 20 Mar 2024 05:04:39 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 20 Mar 2024 05:04:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-26.0.0-rc3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-26.0.0-rc3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-26.0.0-rc3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-26.0.0-rc3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 20 Mar 2024 05:04:39 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 20 Mar 2024 05:04:39 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 20 Mar 2024 05:04:39 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 05:04:39 GMT
VOLUME [/var/lib/docker]
# Wed, 20 Mar 2024 05:04:39 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 20 Mar 2024 05:04:39 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 20 Mar 2024 05:04:39 GMT
CMD []
# Wed, 20 Mar 2024 05:04:39 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Wed, 20 Mar 2024 05:04:39 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 20 Mar 2024 05:04:39 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 20 Mar 2024 05:04:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-26.0.0-rc3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-26.0.0-rc3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 20 Mar 2024 05:04:39 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 20 Mar 2024 05:04:39 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 20 Mar 2024 05:04:39 GMT
USER rootless
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191143df37f970086d287fa40933ddb51174d26d2256c8635a84c36c07fc1e97`  
		Last Modified: Wed, 20 Mar 2024 20:48:33 GMT  
		Size: 2.0 MB (2026152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68f247f5174db76e258cfc0e52123ca51e09482b175fb396f35bf17113c09051`  
		Last Modified: Wed, 20 Mar 2024 20:48:33 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e3cc27c28ae2657280b50026cc2715dc87d824d0f56e6f58bb1bacef28c3d8e`  
		Last Modified: Wed, 20 Mar 2024 20:48:33 GMT  
		Size: 17.0 MB (16973012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:306511527ae1f2d291f0069220e410b44450e3b32ff44d96e5be9254a5aeba22`  
		Last Modified: Wed, 20 Mar 2024 20:48:33 GMT  
		Size: 18.0 MB (17982275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dfc9d2d84a01bc5a89a449c929a5afc0caf3d112f7f3fe092a335cd92ac192e`  
		Last Modified: Wed, 20 Mar 2024 20:48:35 GMT  
		Size: 18.2 MB (18222097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f00efc6ac8f4ee50f39bb1ddb94e33bdf5e681e46d62da699f4ff4f15b195e3`  
		Last Modified: Wed, 20 Mar 2024 20:48:35 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47853701358ab4d2f26ab62afea290be60b545567d07778c08462a26dc1979f0`  
		Last Modified: Wed, 20 Mar 2024 20:48:35 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58cb5780b5227feb52c054302e0f5491f6cacbf0457141dfe87ca7a99195c9a5`  
		Last Modified: Wed, 20 Mar 2024 20:48:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a5f535afbc1f27d6845fc07fb962fca9d77835c6f9d1e3fbcab9de7b7275d66`  
		Last Modified: Wed, 20 Mar 2024 21:50:07 GMT  
		Size: 12.2 MB (12157516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da2f288b8b59ab4b69992f6cbcc3da6ee6e15ffb2d372ef9d9eb1610175a16c`  
		Last Modified: Wed, 20 Mar 2024 21:50:07 GMT  
		Size: 89.1 KB (89122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e62869a44cc160ae672e3f93149e3efa35bb0f8d7deb942b6d353a4ca00fc4d`  
		Last Modified: Wed, 20 Mar 2024 21:50:07 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fa38153f2b48d9b60e7d88cbd14f6e10f98dae0c3e95411ca6f9680f73e9e14`  
		Last Modified: Wed, 20 Mar 2024 21:50:08 GMT  
		Size: 56.4 MB (56414921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a851022dad888d6afd5c24642ecb56a7b724c5df86e2f71cbf7f5314ace18ac5`  
		Last Modified: Wed, 20 Mar 2024 21:50:08 GMT  
		Size: 1.5 KB (1508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39c2061d2e03465672445eb83cf759bbe86a6acef102f7204c6bd6ce5206f459`  
		Last Modified: Wed, 20 Mar 2024 21:50:08 GMT  
		Size: 3.2 KB (3248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b785063d8d9f166fbb6be5e6dac0fb46357eebb3638c0055ff13f860ac60e1e`  
		Last Modified: Wed, 20 Mar 2024 22:49:43 GMT  
		Size: 981.6 KB (981566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9a0559ebce5e8173dd1c57e48147fdba999943188b0e660cd3391d3e88c1e0`  
		Last Modified: Wed, 20 Mar 2024 22:49:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2946da53a0877a9fa8b92848e3e94cfdbd0f796ea7a55006d7c7d666328096c`  
		Last Modified: Wed, 20 Mar 2024 22:49:43 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:155db9dc5e5df349c3cc2068b928a6e748df392b0d8566d7e01725e1ab761591`  
		Last Modified: Wed, 20 Mar 2024 22:49:44 GMT  
		Size: 21.0 MB (20985928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86a1c2d7ad27930c5c922ed196b24d72dc41309594648a778bc49118660f63a`  
		Last Modified: Wed, 20 Mar 2024 22:49:44 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:c953dd265b7c300a1a9034e9ed6ea5661a2652dbf3ebf860da7d4571a552a183
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **923.8 KB (923846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0409560d8af8de5fbaa1f8b5646149669a12553e54562e32e78ba6ecf52c9f22`

```dockerfile
```

-	Layers:
	-	`sha256:8a100157342baee7f90403d87eebde4dc8fa8be7b1a4936ef8e17ed13f46d643`  
		Last Modified: Wed, 20 Mar 2024 22:49:43 GMT  
		Size: 890.9 KB (890852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ead7a93c07215a5de7c234d2dc37a72b02d188e5e837d748225c0ba6e7c020e6`  
		Last Modified: Wed, 20 Mar 2024 22:49:43 GMT  
		Size: 33.0 KB (32994 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:78b52125b862cfcd5abbb90f4375567334864efc2cc236d31794cd2c4a183564
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.9 MB (142910225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:008e841ec0dc8e4456f623bb1c109bdec6a9969a77b7c34373f5e17f00b96378`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Thu, 07 Mar 2024 21:18:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
ENV DOCKER_VERSION=26.0.0-rc2
# Thu, 07 Mar 2024 21:18:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-26.0.0-rc2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-26.0.0-rc2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-26.0.0-rc2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-26.0.0-rc2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
ENV DOCKER_BUILDX_VERSION=0.13.1
# Thu, 07 Mar 2024 21:18:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-amd64'; 			sha256='3e2bc8ed25a9125d6aeec07df4e0211edea6288e075b524160ef3fd305d3d74c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm-v6'; 			sha256='643063c656098e312533fe5ee3411523fa06cc3926bd2e96b4c6239b9cecbf88'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm-v7'; 			sha256='8d42e7823237e777b121070fda6ad68159539aa6597aedfa7630384643ad6f9a'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm64'; 			sha256='3ba35a5d38361a64b62aeb9d20acc835ff6862a711cb438e610026b29c0ac489'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-ppc64le'; 			sha256='1d16f7b15706d98523889a1ca50e9dfc44bbaec1f736d883a0528805795b9de2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-riscv64'; 			sha256='202221c9b7fb881d092986e8ec2497ee71729f17c4afd912384a086af700e1ad'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-s390x'; 			sha256='71d7c39192b1b07790eb71e46742cc69a559f3eb00a1512f4a8d2ea1067408da'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.25.0
# Thu, 07 Mar 2024 21:18:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-x86_64'; 			sha256='53641b8a28419f947bc58c085e0c39b97a209b6e875a25c585e7fab44ff48576'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-armv6'; 			sha256='a123b79b530a65c7381ca8bb3b29cde7177f4f260984a127d998c9696cae794c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-armv7'; 			sha256='8ea72e93e8da8259d7d5d051f3c65dc14c44a23d5ebc6939394d7d03b147e238'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-aarch64'; 			sha256='b9f303c9f9db75ecf18ea6fc516b3dc54a3e54f3b3d8e7f1a449416522958bc5'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-ppc64le'; 			sha256='dc067ab61239cef3d2e145d37fcd68c1fc2320c6728d77a9a4ec4fb0e6c6dd64'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-riscv64'; 			sha256='a17f07604fa74c661e62d5e27ae358f8a611f42bb9a4a147cec76b8bb591bea4'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-s390x'; 			sha256='9e613275e5fa46cb864d3f2fccb10e3239b879527d075490b03e381df56c397c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 07 Mar 2024 21:18:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 Mar 2024 21:18:50 GMT
CMD ["sh"]
# Thu, 07 Mar 2024 21:18:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-26.0.0-rc2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-26.0.0-rc2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-26.0.0-rc2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-26.0.0-rc2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 07 Mar 2024 21:18:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
VOLUME [/var/lib/docker]
# Thu, 07 Mar 2024 21:18:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 07 Mar 2024 21:18:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 07 Mar 2024 21:18:50 GMT
CMD []
# Thu, 07 Mar 2024 21:18:50 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-26.0.0-rc2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-26.0.0-rc2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 07 Mar 2024 21:18:50 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 07 Mar 2024 21:18:50 GMT
USER rootless
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
	-	`sha256:0b1fd8107a0166ec2911f8f43a2a5e067961d5963e722b47e61856820dd946c8`  
		Last Modified: Mon, 18 Mar 2024 22:51:05 GMT  
		Size: 15.9 MB (15936587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7f3e440238097c0c767248819bba9d596e55a79b8eb3e25da8bd16e03ea05e5`  
		Last Modified: Mon, 18 Mar 2024 22:51:06 GMT  
		Size: 16.3 MB (16349514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f677fe87a3f5798ccdc2e06a7e8db90c3afbe88459e3dfd23707f0cc9e47ebb`  
		Last Modified: Mon, 18 Mar 2024 22:51:06 GMT  
		Size: 16.6 MB (16646385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:540ce7efad7a51b0915b014a5e04762666981161df191f26548e78f51be5a318`  
		Last Modified: Mon, 18 Mar 2024 22:51:05 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ad2a99d95baf2767c815ab3a5a825daf12e9d9308d31461a91d1282c5d2375`  
		Last Modified: Mon, 18 Mar 2024 22:51:06 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95dc950dc93070da3a2b5d02565dae19fe24e817c4dd9ea11a52dc68fb132adb`  
		Last Modified: Mon, 18 Mar 2024 22:51:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36d3c5b6288c7755a5c220d0745660053eddee657a09ae16c26b349678e29520`  
		Last Modified: Mon, 18 Mar 2024 23:53:15 GMT  
		Size: 12.6 MB (12626611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6b762eee4ec5328138a4d393a74c84deadbafe675f09aa428a12d695ab1a7a7`  
		Last Modified: Mon, 18 Mar 2024 23:53:15 GMT  
		Size: 98.4 KB (98383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca2721186303e204524ed82419068792431b289fd1ac001f824cbb1ac17acb4`  
		Last Modified: Mon, 18 Mar 2024 23:53:15 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea9e248815d5d13c087a61c67ca6111a7d1d485c01b4240c29a924666a61a7a`  
		Last Modified: Mon, 18 Mar 2024 23:53:17 GMT  
		Size: 52.0 MB (52014239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:733fab59b60d5be26cfad73f827f857b30482d4b6e35d93b1cd721c3c0d447f7`  
		Last Modified: Mon, 18 Mar 2024 23:53:16 GMT  
		Size: 1.5 KB (1509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79857979182097a4617aaf48be183f178d463e80071208d098cc57c68637422f`  
		Last Modified: Mon, 18 Mar 2024 23:53:16 GMT  
		Size: 3.2 KB (3250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ff881fd7be676bf9819ef33c630463b5dfba7c8a2a4c5c81d9d949709f0e0e`  
		Last Modified: Tue, 19 Mar 2024 00:51:09 GMT  
		Size: 1.0 MB (1022483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0911e3b692b5de97896000a29a2bf933d39b6415c8c23b4843b86828856042b`  
		Last Modified: Tue, 19 Mar 2024 00:51:09 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:293455c2a45bf7a0039761f35ecf7243c23c46630c1ae17d2f4dff3753223689`  
		Last Modified: Tue, 19 Mar 2024 00:51:09 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:912a798661e8ab62f4234d9395b437fec55970c722c57c6679537ce91e52a89d`  
		Last Modified: Tue, 19 Mar 2024 00:51:10 GMT  
		Size: 22.8 MB (22838647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2af20a8e84b74e3f2b3bad295a5091db0020b4c44140a0ed9d18cf53ad7c29`  
		Last Modified: Tue, 19 Mar 2024 00:51:10 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:25f44b34ec7584a8f932c70f7d61350d067c4c22438639c148db31c043468d6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **917.0 KB (916962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a287bf4beb3501b10a095121604a03558f048142825bf4c79d56b72c8aed98e`

```dockerfile
```

-	Layers:
	-	`sha256:11a7918a55d06bbd57f05a551dc93005be3eb54d84861725562f80480d48266c`  
		Last Modified: Tue, 19 Mar 2024 00:51:08 GMT  
		Size: 883.9 KB (883906 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f8284a16cca78d536f5d7d16e1bba5cbdfbcf693e5ddc36e5adb394d6e4d4e1`  
		Last Modified: Tue, 19 Mar 2024 00:51:08 GMT  
		Size: 33.1 KB (33056 bytes)  
		MIME: application/vnd.in-toto+json
