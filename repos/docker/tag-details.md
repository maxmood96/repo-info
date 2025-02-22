<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `docker`

-	[`docker:28`](#docker28)
-	[`docker:28-cli`](#docker28-cli)
-	[`docker:28-dind`](#docker28-dind)
-	[`docker:28-dind-rootless`](#docker28-dind-rootless)
-	[`docker:28-windowsservercore`](#docker28-windowsservercore)
-	[`docker:28-windowsservercore-1809`](#docker28-windowsservercore-1809)
-	[`docker:28-windowsservercore-ltsc2022`](#docker28-windowsservercore-ltsc2022)
-	[`docker:28-windowsservercore-ltsc2025`](#docker28-windowsservercore-ltsc2025)
-	[`docker:28.0`](#docker280)
-	[`docker:28.0-cli`](#docker280-cli)
-	[`docker:28.0-dind`](#docker280-dind)
-	[`docker:28.0-dind-rootless`](#docker280-dind-rootless)
-	[`docker:28.0-windowsservercore`](#docker280-windowsservercore)
-	[`docker:28.0-windowsservercore-1809`](#docker280-windowsservercore-1809)
-	[`docker:28.0-windowsservercore-ltsc2022`](#docker280-windowsservercore-ltsc2022)
-	[`docker:28.0-windowsservercore-ltsc2025`](#docker280-windowsservercore-ltsc2025)
-	[`docker:28.0.0`](#docker2800)
-	[`docker:28.0.0-alpine3.21`](#docker2800-alpine321)
-	[`docker:28.0.0-cli`](#docker2800-cli)
-	[`docker:28.0.0-cli-alpine3.21`](#docker2800-cli-alpine321)
-	[`docker:28.0.0-dind`](#docker2800-dind)
-	[`docker:28.0.0-dind-alpine3.21`](#docker2800-dind-alpine321)
-	[`docker:28.0.0-dind-rootless`](#docker2800-dind-rootless)
-	[`docker:28.0.0-windowsservercore`](#docker2800-windowsservercore)
-	[`docker:28.0.0-windowsservercore-1809`](#docker2800-windowsservercore-1809)
-	[`docker:28.0.0-windowsservercore-ltsc2022`](#docker2800-windowsservercore-ltsc2022)
-	[`docker:28.0.0-windowsservercore-ltsc2025`](#docker2800-windowsservercore-ltsc2025)
-	[`docker:cli`](#dockercli)
-	[`docker:dind`](#dockerdind)
-	[`docker:dind-rootless`](#dockerdind-rootless)
-	[`docker:latest`](#dockerlatest)
-	[`docker:windowsservercore`](#dockerwindowsservercore)
-	[`docker:windowsservercore-1809`](#dockerwindowsservercore-1809)
-	[`docker:windowsservercore-ltsc2022`](#dockerwindowsservercore-ltsc2022)
-	[`docker:windowsservercore-ltsc2025`](#dockerwindowsservercore-ltsc2025)

## `docker:28`

```console
$ docker pull docker@sha256:0a9c58ebc9f86e5af35e4330f6c738dc64fce3ca2e2574b5becdfb88765b308b
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

### `docker:28` - linux; amd64

```console
$ docker pull docker@sha256:32c276e9aafff90ea7765271afa524c293c9749e880748217b1abedd04af39a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.0 MB (141006353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1da86d0da980dad6c82075b9859478027165e57dba77994a2fe1fa99ed408f3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_VERSION=28.0.0
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-amd64'; 			sha256='7f355525bfaf411302570b705118181b720f18071f4be3f0eaac7b2297d826e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v6'; 			sha256='f841251fd67646e8b6bb4c7e0c2c385f6a1dc7403f5ac6ee7b07c96f0815f7f3'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v7'; 			sha256='81d7040e90e9b69cb0378778f673e1fc2a24ef6dbd47931dc83ab6472fc5809d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm64'; 			sha256='42d5cee287ec7426de5252276a05f3ea565ac2d65d62d052b885a84dd54152d5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-ppc64le'; 			sha256='6a4e6a243f83d80cd46c939f327b2e14cfddd2c6690651cf48d0e208c3345b88'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-riscv64'; 			sha256='eae82aec74a420c3d1734123e6a3bc10b3a2a981aa1d538502373e31c91bf76e'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-s390x'; 			sha256='97b112b3366a471cc375e0f881d65a9a7b07f0962f308834c37f5c3fa75aad08'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 20 Feb 2025 06:04:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD ["sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
VOLUME [/var/lib/docker]
# Thu, 20 Feb 2025 06:04:43 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD []
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fddc498219722db61fe7f7e06295aa8b64f7e48d19d0339176689ea591eea4ca`  
		Last Modified: Sat, 22 Feb 2025 00:27:26 GMT  
		Size: 8.1 MB (8062985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c17b75175e66b76074511db7ebd5bdc56ac19ba269d30e4f58ba4812816ad4`  
		Last Modified: Sat, 22 Feb 2025 00:27:26 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987b6d8519d32209785b3840639a10aa6247ff1e290a651ebcca3d8c33e23dd2`  
		Last Modified: Sat, 22 Feb 2025 00:27:27 GMT  
		Size: 19.5 MB (19492233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7677267af1ddfc39dbdf35dcdca7c20328e83a42b64595f0d5880c62e99a91f`  
		Last Modified: Sat, 22 Feb 2025 00:27:27 GMT  
		Size: 21.8 MB (21829139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9fa9f5140fd1401e5edaa2de6f975bd14f0b79efbafbe0d2497ea0213ecd260`  
		Last Modified: Sat, 22 Feb 2025 00:27:27 GMT  
		Size: 21.0 MB (20958635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124bcf7a51a8a140479ebb1cfd0aea5bf38223d37b7c6ae1deb93bbb1abc0469`  
		Last Modified: Sat, 22 Feb 2025 00:27:28 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3083b3dfd2242fbeb7b498bb2e0d99d55c8e34cad7396573784aa86db3c69355`  
		Last Modified: Sat, 22 Feb 2025 00:27:28 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b255e6bd488c8fb61ba962afb512c02077ecc7e41b50991cb3229aaa7ae94b`  
		Last Modified: Sat, 22 Feb 2025 00:27:28 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42458739bc4b2677f265360a10a2eacffd5133b0242dd313ba8a3dac7a116c4`  
		Last Modified: Sat, 22 Feb 2025 01:08:23 GMT  
		Size: 6.7 MB (6733003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5a7650793a22cfeac45c6610fe2cd3ccd26b6795d33ee5389d66a174c05a65`  
		Last Modified: Sat, 22 Feb 2025 01:08:23 GMT  
		Size: 90.3 KB (90318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03749f129a866bd1cf2e2797db758f883cf177f3cd33ff3c60924ec811728b4f`  
		Last Modified: Sat, 22 Feb 2025 01:08:23 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:769e1c97b1855704d1f74c39b30c2d2bbc890339752b2be542477e64d2529c32`  
		Last Modified: Sat, 22 Feb 2025 01:08:24 GMT  
		Size: 60.2 MB (60189735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e450e39e6d5b103505878dd35ff532dcdfef40450540495b6a666e7bc34e2587`  
		Last Modified: Sat, 22 Feb 2025 01:08:23 GMT  
		Size: 1.6 KB (1637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254862f49c6f0929e44b00f9635661aff98a508d2dc321d6ddc2944f60ac90bb`  
		Last Modified: Sat, 22 Feb 2025 01:08:23 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28` - unknown; unknown

```console
$ docker pull docker@sha256:ba9368fe1da752bf14bb9ed738b656214abfea5e16cb949f4883beeb86cf9408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:658bfc3f8051aceaf851bbf4fdcff3b32c7f8c853b5262abd646f57fbf14bb10`

```dockerfile
```

-	Layers:
	-	`sha256:670c6ce494a80447b9f682d0ac427af5be54978f5f629221274a481ecf2be95e`  
		Last Modified: Sat, 22 Feb 2025 01:08:22 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28` - linux; arm variant v6

```console
$ docker pull docker@sha256:346b1790ac4379efe1ff83735d9d72ded98e8ebcc776f29f190a50d1086d5c63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.7 MB (131676535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e2b568d33d9f4d9da33be6f6a26a6e533f58d6d874c445c67494a71fe99ce8c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_VERSION=28.0.0
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-amd64'; 			sha256='7f355525bfaf411302570b705118181b720f18071f4be3f0eaac7b2297d826e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v6'; 			sha256='f841251fd67646e8b6bb4c7e0c2c385f6a1dc7403f5ac6ee7b07c96f0815f7f3'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v7'; 			sha256='81d7040e90e9b69cb0378778f673e1fc2a24ef6dbd47931dc83ab6472fc5809d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm64'; 			sha256='42d5cee287ec7426de5252276a05f3ea565ac2d65d62d052b885a84dd54152d5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-ppc64le'; 			sha256='6a4e6a243f83d80cd46c939f327b2e14cfddd2c6690651cf48d0e208c3345b88'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-riscv64'; 			sha256='eae82aec74a420c3d1734123e6a3bc10b3a2a981aa1d538502373e31c91bf76e'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-s390x'; 			sha256='97b112b3366a471cc375e0f881d65a9a7b07f0962f308834c37f5c3fa75aad08'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 20 Feb 2025 06:04:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD ["sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
VOLUME [/var/lib/docker]
# Thu, 20 Feb 2025 06:04:43 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD []
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e40b3641449ca47aef50c48f620eb6d3a3bc2292e5cf4ea267f5f03e6c7bc`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 8.0 MB (7978133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df16922f358c97f513c6d0b9457abb36aefc588e45374edd23692381878a7`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21eb60c27f71135d16125d7dcf87a6c0a49fc39428a0a7ecbc83c6bc1087efa9`  
		Last Modified: Thu, 20 Feb 2025 23:28:03 GMT  
		Size: 17.5 MB (17453851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b3b7abf60d98565d245e7aab34cfdec0b3c2c8ff503fb00ebceed21f636a93`  
		Last Modified: Sat, 22 Feb 2025 00:28:48 GMT  
		Size: 20.4 MB (20432003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ced3aebdded979735885d70afdbc8a5f03be15205f1145cd3b2af469eb21175`  
		Last Modified: Sat, 22 Feb 2025 00:28:48 GMT  
		Size: 19.7 MB (19725892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f8d07fba646c3b5ac2a07d053675df2a0422b36b698a824d345ee2447bc8e1`  
		Last Modified: Sat, 22 Feb 2025 00:28:47 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c51a22c8e8f3b4205fde47fd17f66895fad1496f33f46bb6aebdf5938bb94ad`  
		Last Modified: Sat, 22 Feb 2025 00:28:47 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f36ff703ab2a5ebeeeb26f374c59106eb92bf26531f572228024531dcc975f64`  
		Last Modified: Sat, 22 Feb 2025 00:28:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2440995b1488c0fccd4c0a9b3062c58a33404bcc3ca3e8289ae64b6393946c65`  
		Last Modified: Sat, 22 Feb 2025 01:29:31 GMT  
		Size: 7.0 MB (7036904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cce93707f7a9fed88581b5b8e8f49a184ba206f961aae653eef08af3b94987b1`  
		Last Modified: Sat, 22 Feb 2025 01:29:30 GMT  
		Size: 89.8 KB (89849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26cf971d434da3f52513e2595da034274a6fb8c1ef74cddc815339506b7b704a`  
		Last Modified: Sat, 22 Feb 2025 01:29:30 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c3188476c3d7ba720f96be3cdceb222b9a7a6e0693a917966988332f14e8ef`  
		Last Modified: Sat, 22 Feb 2025 01:29:33 GMT  
		Size: 55.6 MB (55587101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c9e4329aff590ce10c6d6613452bf70f9708c4817750614d9a1a68918444a6`  
		Last Modified: Sat, 22 Feb 2025 01:29:31 GMT  
		Size: 1.6 KB (1638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ff2444afd5e703729aeef9ead8d60b8f059c8e5f0b4b82853f021d0f2c24504`  
		Last Modified: Sat, 22 Feb 2025 01:29:31 GMT  
		Size: 3.3 KB (3263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28` - unknown; unknown

```console
$ docker pull docker@sha256:0931cacdc5870a73bd56837c9590fb9801af1b229cbf7ee86dc79c932a51323c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d14b9f57c5e9b67b594f4172c7cfbb95e2442a040e0bb090b09cc95ce2d35a18`

```dockerfile
```

-	Layers:
	-	`sha256:93150d2f1d44b19b0d6d36517e86cddc39cd49f0857f41bdb86a200f7db357e6`  
		Last Modified: Sat, 22 Feb 2025 01:29:30 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28` - linux; arm variant v7

```console
$ docker pull docker@sha256:089424d7adbb66df8dd78e5ce27d9bd9d13cebe072cb5eb79e7478f00c124163
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (130009843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da65fa603f2dc74e8750fbdc3d7173e607ca901a8dfb81fab1136584884d3018`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_VERSION=28.0.0
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-amd64'; 			sha256='7f355525bfaf411302570b705118181b720f18071f4be3f0eaac7b2297d826e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v6'; 			sha256='f841251fd67646e8b6bb4c7e0c2c385f6a1dc7403f5ac6ee7b07c96f0815f7f3'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v7'; 			sha256='81d7040e90e9b69cb0378778f673e1fc2a24ef6dbd47931dc83ab6472fc5809d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm64'; 			sha256='42d5cee287ec7426de5252276a05f3ea565ac2d65d62d052b885a84dd54152d5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-ppc64le'; 			sha256='6a4e6a243f83d80cd46c939f327b2e14cfddd2c6690651cf48d0e208c3345b88'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-riscv64'; 			sha256='eae82aec74a420c3d1734123e6a3bc10b3a2a981aa1d538502373e31c91bf76e'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-s390x'; 			sha256='97b112b3366a471cc375e0f881d65a9a7b07f0962f308834c37f5c3fa75aad08'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 20 Feb 2025 06:04:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD ["sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
VOLUME [/var/lib/docker]
# Thu, 20 Feb 2025 06:04:43 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD []
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b654458a637c48c7f8f46da325ae8f810828e851ed4ab4b406092503eb680f`  
		Last Modified: Sat, 22 Feb 2025 00:28:04 GMT  
		Size: 7.3 MB (7299375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3474560bdd0e71f5972a48abd9e80877e2219f6eacae8272034d8503bcb634b2`  
		Last Modified: Sat, 22 Feb 2025 00:28:03 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ffc820c153872520700f2618e71ee9bea9cfee69fbff7b0ea4acb751a2fee5`  
		Last Modified: Sat, 22 Feb 2025 00:28:04 GMT  
		Size: 17.4 MB (17444426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a39a48e6818f4f7d6e7637cf221cc02da7b2e8ab3ca2643a527024430497175`  
		Last Modified: Sat, 22 Feb 2025 00:28:04 GMT  
		Size: 20.4 MB (20411656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168ce845c02246501347d9ae0d1bb9bb9f55a707c5ef03ba3bb6377e832c28f4`  
		Last Modified: Sat, 22 Feb 2025 00:28:05 GMT  
		Size: 19.7 MB (19708525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d62f1159ab01591fa3510e1ddc7b7e0313d001750472b1eaa0dcfb3a1f097732`  
		Last Modified: Sat, 22 Feb 2025 00:28:05 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ab9b1b4b0f9c261b260d739cd6d593a2c510b9c29045d72d930f2baf5fa78e`  
		Last Modified: Sat, 22 Feb 2025 00:28:05 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d27509dd9fc9bdb19051b5661dce75fc9b53979841bcd49fd03667b1ad6dde`  
		Last Modified: Sat, 22 Feb 2025 00:28:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd0d2a57f389ccbd627e0bca3b813e9397f4a6a55364b1f7cf22df043542cf1a`  
		Last Modified: Sat, 22 Feb 2025 04:54:52 GMT  
		Size: 6.4 MB (6366292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5947e3cbc6a2eb4d8c4ec17605876ea3e3a5cb2c09abac0a58d53cc4d6569f7`  
		Last Modified: Sat, 22 Feb 2025 04:54:51 GMT  
		Size: 86.3 KB (86342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc1fa6b8e4e654268e5dfc6afa5b1e88bfb92da3c33018f231f76ad7e08a59e`  
		Last Modified: Sat, 22 Feb 2025 04:54:51 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f544c5574adf21ca185480beea8b120134f2ed74f3f2418dc0ef564a3891490`  
		Last Modified: Sat, 22 Feb 2025 04:54:53 GMT  
		Size: 55.6 MB (55587054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd1c8be29e89fc14e8cd0778dcda3dae4c641d9ab956b2f9ce8d02df1d7984e`  
		Last Modified: Sat, 22 Feb 2025 04:54:52 GMT  
		Size: 1.6 KB (1636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db5e7511235a55ebe7a92c8825189d27a2b1d951e0f25d22e4e932636abbd466`  
		Last Modified: Sat, 22 Feb 2025 04:54:52 GMT  
		Size: 3.3 KB (3256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28` - unknown; unknown

```console
$ docker pull docker@sha256:1cdaa27022a39a251e498044fefc2f4160913794dc50a3074935741e0d39d28b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:643a439611cab3be1c6fde6e85ec369c205d94c81b88f1c91a627a32a6448b32`

```dockerfile
```

-	Layers:
	-	`sha256:fa998948cfd33a55b2120a90b998117bea32698c81f84e340fc1f9fa359825c4`  
		Last Modified: Sat, 22 Feb 2025 04:54:51 GMT  
		Size: 34.8 KB (34765 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:af92e15294f197a3cc4de0e75e012f4e91a996e4fd58ad96e163208aea7f0be3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.4 MB (132399422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89d922b5c31bca4bc340632485ab5243809aaf557e7aaf377fd956c15f4ad0a6`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_VERSION=28.0.0
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-amd64'; 			sha256='7f355525bfaf411302570b705118181b720f18071f4be3f0eaac7b2297d826e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v6'; 			sha256='f841251fd67646e8b6bb4c7e0c2c385f6a1dc7403f5ac6ee7b07c96f0815f7f3'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v7'; 			sha256='81d7040e90e9b69cb0378778f673e1fc2a24ef6dbd47931dc83ab6472fc5809d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm64'; 			sha256='42d5cee287ec7426de5252276a05f3ea565ac2d65d62d052b885a84dd54152d5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-ppc64le'; 			sha256='6a4e6a243f83d80cd46c939f327b2e14cfddd2c6690651cf48d0e208c3345b88'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-riscv64'; 			sha256='eae82aec74a420c3d1734123e6a3bc10b3a2a981aa1d538502373e31c91bf76e'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-s390x'; 			sha256='97b112b3366a471cc375e0f881d65a9a7b07f0962f308834c37f5c3fa75aad08'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 20 Feb 2025 06:04:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD ["sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
VOLUME [/var/lib/docker]
# Thu, 20 Feb 2025 06:04:43 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD []
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:076f26e7389ad2e79a31e03589b2c6943495faa94ce7fc6ecd800dd0c320c71e`  
		Last Modified: Sat, 22 Feb 2025 00:28:38 GMT  
		Size: 8.1 MB (8076430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54483e7ea72052e991e704ef33b6d45d32f2c9886445d70ae79e50a2dd444147`  
		Last Modified: Sat, 22 Feb 2025 00:28:37 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d747fdfb37d0ca59992c4852cab088ffb4549e3f8ef7632b252452c1c12c7989`  
		Last Modified: Sat, 22 Feb 2025 00:28:38 GMT  
		Size: 18.4 MB (18412791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84912acd39dd03fae2cffdb073ec52df5d17e2700910653a8c844d31a916a7eb`  
		Last Modified: Sat, 22 Feb 2025 00:28:39 GMT  
		Size: 20.0 MB (20041446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49191a7f2e90fd89997d49d48799f225e27d4d811c1ab6a1a5ed18c8b5a9f94`  
		Last Modified: Sat, 22 Feb 2025 00:28:40 GMT  
		Size: 19.2 MB (19222674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7debd3993d0af81423e3290841931e4b162ff882877ebb292b10f3dde6dc5694`  
		Last Modified: Sat, 22 Feb 2025 00:28:39 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855282ceddcfc470897f6e2cb33f2ad4742db7c00f24a0386714c91a31a090fa`  
		Last Modified: Sat, 22 Feb 2025 00:28:40 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fbaf9714c72f8c1c56eb53405de18b5c63f82fcfa89814a71a92c9844e1fb8b`  
		Last Modified: Sat, 22 Feb 2025 00:28:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f1efb7aef297fc62aaca013f0102b13d4fb2bd1eb6e39c858c91c440c973f87`  
		Last Modified: Sat, 22 Feb 2025 02:46:00 GMT  
		Size: 7.0 MB (6978850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d301065fd8bf09964f1efc59488efd3c692d574aae6e2460fefc3dac799912b`  
		Last Modified: Sat, 22 Feb 2025 02:46:00 GMT  
		Size: 99.4 KB (99390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d33e0f749652bb606f1e92e433cb70fa6c8e7a30737050979d975e9f06a132f`  
		Last Modified: Sat, 22 Feb 2025 02:45:59 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a409b11008465c3cb7523e669b4d2a064619125185de982089bf11944cf62502`  
		Last Modified: Sat, 22 Feb 2025 02:46:01 GMT  
		Size: 55.6 MB (55566753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff8cdce63f040e68fff768b8a75d7ebdd3f4cd4e69ed0f85ae0ad620baa9c40`  
		Last Modified: Sat, 22 Feb 2025 02:46:00 GMT  
		Size: 1.6 KB (1636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f72a632b800deed0be1fc7ec78852db28106ae059a841b87a966fed6ec7255f`  
		Last Modified: Sat, 22 Feb 2025 02:46:01 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28` - unknown; unknown

```console
$ docker pull docker@sha256:d6dd49a97960eaef409aa41f89cf8596c02281b55801b3f726b267761031bc90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4105199c766800ff78dca393a5dccdb1435364291ecf731c31deacb4fa6e86a4`

```dockerfile
```

-	Layers:
	-	`sha256:2f7e554767be7baf2d46a3652bbe4405cdcb83972440eb83c19280ab0e991188`  
		Last Modified: Sat, 22 Feb 2025 02:45:59 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28-cli`

```console
$ docker pull docker@sha256:28fb556c1ea1eef2f1d8d70e8c7eb52e38324b2ae04ffcb8df26648a7c2e5dfc
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

### `docker:28-cli` - linux; amd64

```console
$ docker pull docker@sha256:828f4f57525db5dbdb2f52ba47087c383361fd22975c264142bab1ff78ea8587
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73987390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2047a2478c64769a8f8963db4efc714c734b9ec896b1452fb424720a232732d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 21 Feb 2025 18:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_VERSION=28.0.0
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-amd64'; 			sha256='7f355525bfaf411302570b705118181b720f18071f4be3f0eaac7b2297d826e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v6'; 			sha256='f841251fd67646e8b6bb4c7e0c2c385f6a1dc7403f5ac6ee7b07c96f0815f7f3'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v7'; 			sha256='81d7040e90e9b69cb0378778f673e1fc2a24ef6dbd47931dc83ab6472fc5809d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm64'; 			sha256='42d5cee287ec7426de5252276a05f3ea565ac2d65d62d052b885a84dd54152d5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-ppc64le'; 			sha256='6a4e6a243f83d80cd46c939f327b2e14cfddd2c6690651cf48d0e208c3345b88'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-riscv64'; 			sha256='eae82aec74a420c3d1734123e6a3bc10b3a2a981aa1d538502373e31c91bf76e'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-s390x'; 			sha256='97b112b3366a471cc375e0f881d65a9a7b07f0962f308834c37f5c3fa75aad08'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 21 Feb 2025 18:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 18:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fddc498219722db61fe7f7e06295aa8b64f7e48d19d0339176689ea591eea4ca`  
		Last Modified: Sat, 22 Feb 2025 00:27:26 GMT  
		Size: 8.1 MB (8062985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c17b75175e66b76074511db7ebd5bdc56ac19ba269d30e4f58ba4812816ad4`  
		Last Modified: Sat, 22 Feb 2025 00:27:26 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987b6d8519d32209785b3840639a10aa6247ff1e290a651ebcca3d8c33e23dd2`  
		Last Modified: Sat, 22 Feb 2025 00:27:27 GMT  
		Size: 19.5 MB (19492233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7677267af1ddfc39dbdf35dcdca7c20328e83a42b64595f0d5880c62e99a91f`  
		Last Modified: Sat, 22 Feb 2025 00:27:27 GMT  
		Size: 21.8 MB (21829139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9fa9f5140fd1401e5edaa2de6f975bd14f0b79efbafbe0d2497ea0213ecd260`  
		Last Modified: Sat, 22 Feb 2025 00:27:27 GMT  
		Size: 21.0 MB (20958635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124bcf7a51a8a140479ebb1cfd0aea5bf38223d37b7c6ae1deb93bbb1abc0469`  
		Last Modified: Sat, 22 Feb 2025 00:27:28 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3083b3dfd2242fbeb7b498bb2e0d99d55c8e34cad7396573784aa86db3c69355`  
		Last Modified: Sat, 22 Feb 2025 00:27:28 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b255e6bd488c8fb61ba962afb512c02077ecc7e41b50991cb3229aaa7ae94b`  
		Last Modified: Sat, 22 Feb 2025 00:27:28 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:23d0fdad7d91848fe9aefbb31f9ec0f13048b4043d184117ef3506756fb199f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d89ed9762486ccde5720aaa5cfd88b8e5c1bf286c15632485f3c3a9b66385e0`

```dockerfile
```

-	Layers:
	-	`sha256:29c00cb8b559fbda58a54628ef429544bb24356f7620856781c43b802464d245`  
		Last Modified: Sat, 22 Feb 2025 00:27:26 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:563c0b58e54b2cb6649f26c22d8f06f2be7ebb8dead799918f4b22b13dd7d9f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (68956771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eabedade3d89f3eb7ffac6cf1924c31c852c974072b582d14b744e4c9c6993a2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 21 Feb 2025 18:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_VERSION=28.0.0
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-amd64'; 			sha256='7f355525bfaf411302570b705118181b720f18071f4be3f0eaac7b2297d826e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v6'; 			sha256='f841251fd67646e8b6bb4c7e0c2c385f6a1dc7403f5ac6ee7b07c96f0815f7f3'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v7'; 			sha256='81d7040e90e9b69cb0378778f673e1fc2a24ef6dbd47931dc83ab6472fc5809d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm64'; 			sha256='42d5cee287ec7426de5252276a05f3ea565ac2d65d62d052b885a84dd54152d5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-ppc64le'; 			sha256='6a4e6a243f83d80cd46c939f327b2e14cfddd2c6690651cf48d0e208c3345b88'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-riscv64'; 			sha256='eae82aec74a420c3d1734123e6a3bc10b3a2a981aa1d538502373e31c91bf76e'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-s390x'; 			sha256='97b112b3366a471cc375e0f881d65a9a7b07f0962f308834c37f5c3fa75aad08'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 21 Feb 2025 18:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 18:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e40b3641449ca47aef50c48f620eb6d3a3bc2292e5cf4ea267f5f03e6c7bc`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 8.0 MB (7978133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df16922f358c97f513c6d0b9457abb36aefc588e45374edd23692381878a7`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21eb60c27f71135d16125d7dcf87a6c0a49fc39428a0a7ecbc83c6bc1087efa9`  
		Last Modified: Thu, 20 Feb 2025 23:28:03 GMT  
		Size: 17.5 MB (17453851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b3b7abf60d98565d245e7aab34cfdec0b3c2c8ff503fb00ebceed21f636a93`  
		Last Modified: Sat, 22 Feb 2025 00:28:48 GMT  
		Size: 20.4 MB (20432003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ced3aebdded979735885d70afdbc8a5f03be15205f1145cd3b2af469eb21175`  
		Last Modified: Sat, 22 Feb 2025 00:28:48 GMT  
		Size: 19.7 MB (19725892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f8d07fba646c3b5ac2a07d053675df2a0422b36b698a824d345ee2447bc8e1`  
		Last Modified: Sat, 22 Feb 2025 00:28:47 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c51a22c8e8f3b4205fde47fd17f66895fad1496f33f46bb6aebdf5938bb94ad`  
		Last Modified: Sat, 22 Feb 2025 00:28:47 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f36ff703ab2a5ebeeeb26f374c59106eb92bf26531f572228024531dcc975f64`  
		Last Modified: Sat, 22 Feb 2025 00:28:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:19ac4c1b39024c4040fa578e5a4947132dfa561816cb7525547f283ad033cb82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d38b373d00ff94b39de7f66b705b156b58a6c9747a3aa783505be0e6c3ebf00`

```dockerfile
```

-	Layers:
	-	`sha256:65c4a818e540437ada35738cd53dff3f48895979403e4f6d6893ef134b4a0b5e`  
		Last Modified: Sat, 22 Feb 2025 00:28:47 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:6045d4846c59f8ee46c1d168dfe9b4de563a1602ed536f9a75e133d23291dc17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (67964254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ba8f3ae10c4069acc8988e46282e2592d80824e75e262440f1ca87b5b54fa4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 21 Feb 2025 18:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_VERSION=28.0.0
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-amd64'; 			sha256='7f355525bfaf411302570b705118181b720f18071f4be3f0eaac7b2297d826e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v6'; 			sha256='f841251fd67646e8b6bb4c7e0c2c385f6a1dc7403f5ac6ee7b07c96f0815f7f3'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v7'; 			sha256='81d7040e90e9b69cb0378778f673e1fc2a24ef6dbd47931dc83ab6472fc5809d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm64'; 			sha256='42d5cee287ec7426de5252276a05f3ea565ac2d65d62d052b885a84dd54152d5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-ppc64le'; 			sha256='6a4e6a243f83d80cd46c939f327b2e14cfddd2c6690651cf48d0e208c3345b88'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-riscv64'; 			sha256='eae82aec74a420c3d1734123e6a3bc10b3a2a981aa1d538502373e31c91bf76e'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-s390x'; 			sha256='97b112b3366a471cc375e0f881d65a9a7b07f0962f308834c37f5c3fa75aad08'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 21 Feb 2025 18:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 18:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b654458a637c48c7f8f46da325ae8f810828e851ed4ab4b406092503eb680f`  
		Last Modified: Sat, 22 Feb 2025 00:28:04 GMT  
		Size: 7.3 MB (7299375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3474560bdd0e71f5972a48abd9e80877e2219f6eacae8272034d8503bcb634b2`  
		Last Modified: Sat, 22 Feb 2025 00:28:03 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ffc820c153872520700f2618e71ee9bea9cfee69fbff7b0ea4acb751a2fee5`  
		Last Modified: Sat, 22 Feb 2025 00:28:04 GMT  
		Size: 17.4 MB (17444426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a39a48e6818f4f7d6e7637cf221cc02da7b2e8ab3ca2643a527024430497175`  
		Last Modified: Sat, 22 Feb 2025 00:28:04 GMT  
		Size: 20.4 MB (20411656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168ce845c02246501347d9ae0d1bb9bb9f55a707c5ef03ba3bb6377e832c28f4`  
		Last Modified: Sat, 22 Feb 2025 00:28:05 GMT  
		Size: 19.7 MB (19708525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d62f1159ab01591fa3510e1ddc7b7e0313d001750472b1eaa0dcfb3a1f097732`  
		Last Modified: Sat, 22 Feb 2025 00:28:05 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ab9b1b4b0f9c261b260d739cd6d593a2c510b9c29045d72d930f2baf5fa78e`  
		Last Modified: Sat, 22 Feb 2025 00:28:05 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d27509dd9fc9bdb19051b5661dce75fc9b53979841bcd49fd03667b1ad6dde`  
		Last Modified: Sat, 22 Feb 2025 00:28:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:23645fb2cbf9071135cf4f6aa3c2daf2dc3370793a863fef2ee39d5314bc1a81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93af0d5ba0d4eddf4e7d202afc318f1221ed8bb0f4b1ffde83604fd9bd752b41`

```dockerfile
```

-	Layers:
	-	`sha256:c3cccd9b156d9500700d8b30693438b27b91e56bc8149ff0300632ebb0780d36`  
		Last Modified: Sat, 22 Feb 2025 00:28:03 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:11e8dfd68841685653bd4816fc6ab2f95cc84940d099b1e683a4b60a958599df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69748524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af7e01753428f0214a4072134b7c0481b29b9f695ebe735e920d47b6c0302c4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 21 Feb 2025 18:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_VERSION=28.0.0
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-amd64'; 			sha256='7f355525bfaf411302570b705118181b720f18071f4be3f0eaac7b2297d826e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v6'; 			sha256='f841251fd67646e8b6bb4c7e0c2c385f6a1dc7403f5ac6ee7b07c96f0815f7f3'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v7'; 			sha256='81d7040e90e9b69cb0378778f673e1fc2a24ef6dbd47931dc83ab6472fc5809d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm64'; 			sha256='42d5cee287ec7426de5252276a05f3ea565ac2d65d62d052b885a84dd54152d5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-ppc64le'; 			sha256='6a4e6a243f83d80cd46c939f327b2e14cfddd2c6690651cf48d0e208c3345b88'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-riscv64'; 			sha256='eae82aec74a420c3d1734123e6a3bc10b3a2a981aa1d538502373e31c91bf76e'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-s390x'; 			sha256='97b112b3366a471cc375e0f881d65a9a7b07f0962f308834c37f5c3fa75aad08'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 21 Feb 2025 18:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 18:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:076f26e7389ad2e79a31e03589b2c6943495faa94ce7fc6ecd800dd0c320c71e`  
		Last Modified: Sat, 22 Feb 2025 00:28:38 GMT  
		Size: 8.1 MB (8076430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54483e7ea72052e991e704ef33b6d45d32f2c9886445d70ae79e50a2dd444147`  
		Last Modified: Sat, 22 Feb 2025 00:28:37 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d747fdfb37d0ca59992c4852cab088ffb4549e3f8ef7632b252452c1c12c7989`  
		Last Modified: Sat, 22 Feb 2025 00:28:38 GMT  
		Size: 18.4 MB (18412791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84912acd39dd03fae2cffdb073ec52df5d17e2700910653a8c844d31a916a7eb`  
		Last Modified: Sat, 22 Feb 2025 00:28:39 GMT  
		Size: 20.0 MB (20041446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49191a7f2e90fd89997d49d48799f225e27d4d811c1ab6a1a5ed18c8b5a9f94`  
		Last Modified: Sat, 22 Feb 2025 00:28:40 GMT  
		Size: 19.2 MB (19222674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7debd3993d0af81423e3290841931e4b162ff882877ebb292b10f3dde6dc5694`  
		Last Modified: Sat, 22 Feb 2025 00:28:39 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855282ceddcfc470897f6e2cb33f2ad4742db7c00f24a0386714c91a31a090fa`  
		Last Modified: Sat, 22 Feb 2025 00:28:40 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fbaf9714c72f8c1c56eb53405de18b5c63f82fcfa89814a71a92c9844e1fb8b`  
		Last Modified: Sat, 22 Feb 2025 00:28:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:30588165fa8677446217c19a011fa7b5dd4b56689b71068054b1769685612965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:050a79ebe758ee7f1e33b2b06dd06dabf7b2d3ccb381eb495d95c61658b577c3`

```dockerfile
```

-	Layers:
	-	`sha256:eb188e16beab9632a0818b296adc7960adad9c23b87529bf5b8f419eef964844`  
		Last Modified: Sat, 22 Feb 2025 00:28:37 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28-dind`

```console
$ docker pull docker@sha256:0a9c58ebc9f86e5af35e4330f6c738dc64fce3ca2e2574b5becdfb88765b308b
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

### `docker:28-dind` - linux; amd64

```console
$ docker pull docker@sha256:32c276e9aafff90ea7765271afa524c293c9749e880748217b1abedd04af39a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.0 MB (141006353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1da86d0da980dad6c82075b9859478027165e57dba77994a2fe1fa99ed408f3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_VERSION=28.0.0
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-amd64'; 			sha256='7f355525bfaf411302570b705118181b720f18071f4be3f0eaac7b2297d826e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v6'; 			sha256='f841251fd67646e8b6bb4c7e0c2c385f6a1dc7403f5ac6ee7b07c96f0815f7f3'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v7'; 			sha256='81d7040e90e9b69cb0378778f673e1fc2a24ef6dbd47931dc83ab6472fc5809d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm64'; 			sha256='42d5cee287ec7426de5252276a05f3ea565ac2d65d62d052b885a84dd54152d5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-ppc64le'; 			sha256='6a4e6a243f83d80cd46c939f327b2e14cfddd2c6690651cf48d0e208c3345b88'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-riscv64'; 			sha256='eae82aec74a420c3d1734123e6a3bc10b3a2a981aa1d538502373e31c91bf76e'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-s390x'; 			sha256='97b112b3366a471cc375e0f881d65a9a7b07f0962f308834c37f5c3fa75aad08'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 20 Feb 2025 06:04:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD ["sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
VOLUME [/var/lib/docker]
# Thu, 20 Feb 2025 06:04:43 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD []
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fddc498219722db61fe7f7e06295aa8b64f7e48d19d0339176689ea591eea4ca`  
		Last Modified: Sat, 22 Feb 2025 00:27:26 GMT  
		Size: 8.1 MB (8062985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c17b75175e66b76074511db7ebd5bdc56ac19ba269d30e4f58ba4812816ad4`  
		Last Modified: Sat, 22 Feb 2025 00:27:26 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987b6d8519d32209785b3840639a10aa6247ff1e290a651ebcca3d8c33e23dd2`  
		Last Modified: Sat, 22 Feb 2025 00:27:27 GMT  
		Size: 19.5 MB (19492233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7677267af1ddfc39dbdf35dcdca7c20328e83a42b64595f0d5880c62e99a91f`  
		Last Modified: Sat, 22 Feb 2025 00:27:27 GMT  
		Size: 21.8 MB (21829139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9fa9f5140fd1401e5edaa2de6f975bd14f0b79efbafbe0d2497ea0213ecd260`  
		Last Modified: Sat, 22 Feb 2025 00:27:27 GMT  
		Size: 21.0 MB (20958635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124bcf7a51a8a140479ebb1cfd0aea5bf38223d37b7c6ae1deb93bbb1abc0469`  
		Last Modified: Sat, 22 Feb 2025 00:27:28 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3083b3dfd2242fbeb7b498bb2e0d99d55c8e34cad7396573784aa86db3c69355`  
		Last Modified: Sat, 22 Feb 2025 00:27:28 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b255e6bd488c8fb61ba962afb512c02077ecc7e41b50991cb3229aaa7ae94b`  
		Last Modified: Sat, 22 Feb 2025 00:27:28 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42458739bc4b2677f265360a10a2eacffd5133b0242dd313ba8a3dac7a116c4`  
		Last Modified: Sat, 22 Feb 2025 01:08:23 GMT  
		Size: 6.7 MB (6733003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5a7650793a22cfeac45c6610fe2cd3ccd26b6795d33ee5389d66a174c05a65`  
		Last Modified: Sat, 22 Feb 2025 01:08:23 GMT  
		Size: 90.3 KB (90318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03749f129a866bd1cf2e2797db758f883cf177f3cd33ff3c60924ec811728b4f`  
		Last Modified: Sat, 22 Feb 2025 01:08:23 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:769e1c97b1855704d1f74c39b30c2d2bbc890339752b2be542477e64d2529c32`  
		Last Modified: Sat, 22 Feb 2025 01:08:24 GMT  
		Size: 60.2 MB (60189735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e450e39e6d5b103505878dd35ff532dcdfef40450540495b6a666e7bc34e2587`  
		Last Modified: Sat, 22 Feb 2025 01:08:23 GMT  
		Size: 1.6 KB (1637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254862f49c6f0929e44b00f9635661aff98a508d2dc321d6ddc2944f60ac90bb`  
		Last Modified: Sat, 22 Feb 2025 01:08:23 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind` - unknown; unknown

```console
$ docker pull docker@sha256:ba9368fe1da752bf14bb9ed738b656214abfea5e16cb949f4883beeb86cf9408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:658bfc3f8051aceaf851bbf4fdcff3b32c7f8c853b5262abd646f57fbf14bb10`

```dockerfile
```

-	Layers:
	-	`sha256:670c6ce494a80447b9f682d0ac427af5be54978f5f629221274a481ecf2be95e`  
		Last Modified: Sat, 22 Feb 2025 01:08:22 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:346b1790ac4379efe1ff83735d9d72ded98e8ebcc776f29f190a50d1086d5c63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.7 MB (131676535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e2b568d33d9f4d9da33be6f6a26a6e533f58d6d874c445c67494a71fe99ce8c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_VERSION=28.0.0
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-amd64'; 			sha256='7f355525bfaf411302570b705118181b720f18071f4be3f0eaac7b2297d826e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v6'; 			sha256='f841251fd67646e8b6bb4c7e0c2c385f6a1dc7403f5ac6ee7b07c96f0815f7f3'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v7'; 			sha256='81d7040e90e9b69cb0378778f673e1fc2a24ef6dbd47931dc83ab6472fc5809d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm64'; 			sha256='42d5cee287ec7426de5252276a05f3ea565ac2d65d62d052b885a84dd54152d5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-ppc64le'; 			sha256='6a4e6a243f83d80cd46c939f327b2e14cfddd2c6690651cf48d0e208c3345b88'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-riscv64'; 			sha256='eae82aec74a420c3d1734123e6a3bc10b3a2a981aa1d538502373e31c91bf76e'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-s390x'; 			sha256='97b112b3366a471cc375e0f881d65a9a7b07f0962f308834c37f5c3fa75aad08'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 20 Feb 2025 06:04:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD ["sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
VOLUME [/var/lib/docker]
# Thu, 20 Feb 2025 06:04:43 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD []
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e40b3641449ca47aef50c48f620eb6d3a3bc2292e5cf4ea267f5f03e6c7bc`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 8.0 MB (7978133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df16922f358c97f513c6d0b9457abb36aefc588e45374edd23692381878a7`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21eb60c27f71135d16125d7dcf87a6c0a49fc39428a0a7ecbc83c6bc1087efa9`  
		Last Modified: Thu, 20 Feb 2025 23:28:03 GMT  
		Size: 17.5 MB (17453851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b3b7abf60d98565d245e7aab34cfdec0b3c2c8ff503fb00ebceed21f636a93`  
		Last Modified: Sat, 22 Feb 2025 00:28:48 GMT  
		Size: 20.4 MB (20432003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ced3aebdded979735885d70afdbc8a5f03be15205f1145cd3b2af469eb21175`  
		Last Modified: Sat, 22 Feb 2025 00:28:48 GMT  
		Size: 19.7 MB (19725892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f8d07fba646c3b5ac2a07d053675df2a0422b36b698a824d345ee2447bc8e1`  
		Last Modified: Sat, 22 Feb 2025 00:28:47 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c51a22c8e8f3b4205fde47fd17f66895fad1496f33f46bb6aebdf5938bb94ad`  
		Last Modified: Sat, 22 Feb 2025 00:28:47 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f36ff703ab2a5ebeeeb26f374c59106eb92bf26531f572228024531dcc975f64`  
		Last Modified: Sat, 22 Feb 2025 00:28:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2440995b1488c0fccd4c0a9b3062c58a33404bcc3ca3e8289ae64b6393946c65`  
		Last Modified: Sat, 22 Feb 2025 01:29:31 GMT  
		Size: 7.0 MB (7036904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cce93707f7a9fed88581b5b8e8f49a184ba206f961aae653eef08af3b94987b1`  
		Last Modified: Sat, 22 Feb 2025 01:29:30 GMT  
		Size: 89.8 KB (89849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26cf971d434da3f52513e2595da034274a6fb8c1ef74cddc815339506b7b704a`  
		Last Modified: Sat, 22 Feb 2025 01:29:30 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c3188476c3d7ba720f96be3cdceb222b9a7a6e0693a917966988332f14e8ef`  
		Last Modified: Sat, 22 Feb 2025 01:29:33 GMT  
		Size: 55.6 MB (55587101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c9e4329aff590ce10c6d6613452bf70f9708c4817750614d9a1a68918444a6`  
		Last Modified: Sat, 22 Feb 2025 01:29:31 GMT  
		Size: 1.6 KB (1638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ff2444afd5e703729aeef9ead8d60b8f059c8e5f0b4b82853f021d0f2c24504`  
		Last Modified: Sat, 22 Feb 2025 01:29:31 GMT  
		Size: 3.3 KB (3263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind` - unknown; unknown

```console
$ docker pull docker@sha256:0931cacdc5870a73bd56837c9590fb9801af1b229cbf7ee86dc79c932a51323c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d14b9f57c5e9b67b594f4172c7cfbb95e2442a040e0bb090b09cc95ce2d35a18`

```dockerfile
```

-	Layers:
	-	`sha256:93150d2f1d44b19b0d6d36517e86cddc39cd49f0857f41bdb86a200f7db357e6`  
		Last Modified: Sat, 22 Feb 2025 01:29:30 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:089424d7adbb66df8dd78e5ce27d9bd9d13cebe072cb5eb79e7478f00c124163
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (130009843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da65fa603f2dc74e8750fbdc3d7173e607ca901a8dfb81fab1136584884d3018`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_VERSION=28.0.0
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-amd64'; 			sha256='7f355525bfaf411302570b705118181b720f18071f4be3f0eaac7b2297d826e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v6'; 			sha256='f841251fd67646e8b6bb4c7e0c2c385f6a1dc7403f5ac6ee7b07c96f0815f7f3'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v7'; 			sha256='81d7040e90e9b69cb0378778f673e1fc2a24ef6dbd47931dc83ab6472fc5809d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm64'; 			sha256='42d5cee287ec7426de5252276a05f3ea565ac2d65d62d052b885a84dd54152d5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-ppc64le'; 			sha256='6a4e6a243f83d80cd46c939f327b2e14cfddd2c6690651cf48d0e208c3345b88'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-riscv64'; 			sha256='eae82aec74a420c3d1734123e6a3bc10b3a2a981aa1d538502373e31c91bf76e'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-s390x'; 			sha256='97b112b3366a471cc375e0f881d65a9a7b07f0962f308834c37f5c3fa75aad08'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 20 Feb 2025 06:04:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD ["sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
VOLUME [/var/lib/docker]
# Thu, 20 Feb 2025 06:04:43 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD []
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b654458a637c48c7f8f46da325ae8f810828e851ed4ab4b406092503eb680f`  
		Last Modified: Sat, 22 Feb 2025 00:28:04 GMT  
		Size: 7.3 MB (7299375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3474560bdd0e71f5972a48abd9e80877e2219f6eacae8272034d8503bcb634b2`  
		Last Modified: Sat, 22 Feb 2025 00:28:03 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ffc820c153872520700f2618e71ee9bea9cfee69fbff7b0ea4acb751a2fee5`  
		Last Modified: Sat, 22 Feb 2025 00:28:04 GMT  
		Size: 17.4 MB (17444426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a39a48e6818f4f7d6e7637cf221cc02da7b2e8ab3ca2643a527024430497175`  
		Last Modified: Sat, 22 Feb 2025 00:28:04 GMT  
		Size: 20.4 MB (20411656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168ce845c02246501347d9ae0d1bb9bb9f55a707c5ef03ba3bb6377e832c28f4`  
		Last Modified: Sat, 22 Feb 2025 00:28:05 GMT  
		Size: 19.7 MB (19708525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d62f1159ab01591fa3510e1ddc7b7e0313d001750472b1eaa0dcfb3a1f097732`  
		Last Modified: Sat, 22 Feb 2025 00:28:05 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ab9b1b4b0f9c261b260d739cd6d593a2c510b9c29045d72d930f2baf5fa78e`  
		Last Modified: Sat, 22 Feb 2025 00:28:05 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d27509dd9fc9bdb19051b5661dce75fc9b53979841bcd49fd03667b1ad6dde`  
		Last Modified: Sat, 22 Feb 2025 00:28:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd0d2a57f389ccbd627e0bca3b813e9397f4a6a55364b1f7cf22df043542cf1a`  
		Last Modified: Sat, 22 Feb 2025 04:54:52 GMT  
		Size: 6.4 MB (6366292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5947e3cbc6a2eb4d8c4ec17605876ea3e3a5cb2c09abac0a58d53cc4d6569f7`  
		Last Modified: Sat, 22 Feb 2025 04:54:51 GMT  
		Size: 86.3 KB (86342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc1fa6b8e4e654268e5dfc6afa5b1e88bfb92da3c33018f231f76ad7e08a59e`  
		Last Modified: Sat, 22 Feb 2025 04:54:51 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f544c5574adf21ca185480beea8b120134f2ed74f3f2418dc0ef564a3891490`  
		Last Modified: Sat, 22 Feb 2025 04:54:53 GMT  
		Size: 55.6 MB (55587054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd1c8be29e89fc14e8cd0778dcda3dae4c641d9ab956b2f9ce8d02df1d7984e`  
		Last Modified: Sat, 22 Feb 2025 04:54:52 GMT  
		Size: 1.6 KB (1636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db5e7511235a55ebe7a92c8825189d27a2b1d951e0f25d22e4e932636abbd466`  
		Last Modified: Sat, 22 Feb 2025 04:54:52 GMT  
		Size: 3.3 KB (3256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind` - unknown; unknown

```console
$ docker pull docker@sha256:1cdaa27022a39a251e498044fefc2f4160913794dc50a3074935741e0d39d28b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:643a439611cab3be1c6fde6e85ec369c205d94c81b88f1c91a627a32a6448b32`

```dockerfile
```

-	Layers:
	-	`sha256:fa998948cfd33a55b2120a90b998117bea32698c81f84e340fc1f9fa359825c4`  
		Last Modified: Sat, 22 Feb 2025 04:54:51 GMT  
		Size: 34.8 KB (34765 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:af92e15294f197a3cc4de0e75e012f4e91a996e4fd58ad96e163208aea7f0be3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.4 MB (132399422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89d922b5c31bca4bc340632485ab5243809aaf557e7aaf377fd956c15f4ad0a6`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_VERSION=28.0.0
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-amd64'; 			sha256='7f355525bfaf411302570b705118181b720f18071f4be3f0eaac7b2297d826e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v6'; 			sha256='f841251fd67646e8b6bb4c7e0c2c385f6a1dc7403f5ac6ee7b07c96f0815f7f3'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v7'; 			sha256='81d7040e90e9b69cb0378778f673e1fc2a24ef6dbd47931dc83ab6472fc5809d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm64'; 			sha256='42d5cee287ec7426de5252276a05f3ea565ac2d65d62d052b885a84dd54152d5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-ppc64le'; 			sha256='6a4e6a243f83d80cd46c939f327b2e14cfddd2c6690651cf48d0e208c3345b88'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-riscv64'; 			sha256='eae82aec74a420c3d1734123e6a3bc10b3a2a981aa1d538502373e31c91bf76e'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-s390x'; 			sha256='97b112b3366a471cc375e0f881d65a9a7b07f0962f308834c37f5c3fa75aad08'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 20 Feb 2025 06:04:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD ["sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
VOLUME [/var/lib/docker]
# Thu, 20 Feb 2025 06:04:43 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD []
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:076f26e7389ad2e79a31e03589b2c6943495faa94ce7fc6ecd800dd0c320c71e`  
		Last Modified: Sat, 22 Feb 2025 00:28:38 GMT  
		Size: 8.1 MB (8076430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54483e7ea72052e991e704ef33b6d45d32f2c9886445d70ae79e50a2dd444147`  
		Last Modified: Sat, 22 Feb 2025 00:28:37 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d747fdfb37d0ca59992c4852cab088ffb4549e3f8ef7632b252452c1c12c7989`  
		Last Modified: Sat, 22 Feb 2025 00:28:38 GMT  
		Size: 18.4 MB (18412791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84912acd39dd03fae2cffdb073ec52df5d17e2700910653a8c844d31a916a7eb`  
		Last Modified: Sat, 22 Feb 2025 00:28:39 GMT  
		Size: 20.0 MB (20041446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49191a7f2e90fd89997d49d48799f225e27d4d811c1ab6a1a5ed18c8b5a9f94`  
		Last Modified: Sat, 22 Feb 2025 00:28:40 GMT  
		Size: 19.2 MB (19222674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7debd3993d0af81423e3290841931e4b162ff882877ebb292b10f3dde6dc5694`  
		Last Modified: Sat, 22 Feb 2025 00:28:39 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855282ceddcfc470897f6e2cb33f2ad4742db7c00f24a0386714c91a31a090fa`  
		Last Modified: Sat, 22 Feb 2025 00:28:40 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fbaf9714c72f8c1c56eb53405de18b5c63f82fcfa89814a71a92c9844e1fb8b`  
		Last Modified: Sat, 22 Feb 2025 00:28:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f1efb7aef297fc62aaca013f0102b13d4fb2bd1eb6e39c858c91c440c973f87`  
		Last Modified: Sat, 22 Feb 2025 02:46:00 GMT  
		Size: 7.0 MB (6978850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d301065fd8bf09964f1efc59488efd3c692d574aae6e2460fefc3dac799912b`  
		Last Modified: Sat, 22 Feb 2025 02:46:00 GMT  
		Size: 99.4 KB (99390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d33e0f749652bb606f1e92e433cb70fa6c8e7a30737050979d975e9f06a132f`  
		Last Modified: Sat, 22 Feb 2025 02:45:59 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a409b11008465c3cb7523e669b4d2a064619125185de982089bf11944cf62502`  
		Last Modified: Sat, 22 Feb 2025 02:46:01 GMT  
		Size: 55.6 MB (55566753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff8cdce63f040e68fff768b8a75d7ebdd3f4cd4e69ed0f85ae0ad620baa9c40`  
		Last Modified: Sat, 22 Feb 2025 02:46:00 GMT  
		Size: 1.6 KB (1636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f72a632b800deed0be1fc7ec78852db28106ae059a841b87a966fed6ec7255f`  
		Last Modified: Sat, 22 Feb 2025 02:46:01 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind` - unknown; unknown

```console
$ docker pull docker@sha256:d6dd49a97960eaef409aa41f89cf8596c02281b55801b3f726b267761031bc90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4105199c766800ff78dca393a5dccdb1435364291ecf731c31deacb4fa6e86a4`

```dockerfile
```

-	Layers:
	-	`sha256:2f7e554767be7baf2d46a3652bbe4405cdcb83972440eb83c19280ab0e991188`  
		Last Modified: Sat, 22 Feb 2025 02:45:59 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28-dind-rootless`

```console
$ docker pull docker@sha256:f36f8f41d9e38bae8c3d247446a1e31df98bd84d1ccc22d9d8d50fbe6cbafae8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:28-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:16356585ff8acaa68e6bd54dd11f6760ce507fa719fe7e00bc7db05f53c7a074
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.2 MB (159160666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f413ddafbf744ab3b46d57ab5bda7d4b4ed64aa0ac7f3bd49a3055f8aa5c604`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_VERSION=28.0.0
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-amd64'; 			sha256='7f355525bfaf411302570b705118181b720f18071f4be3f0eaac7b2297d826e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v6'; 			sha256='f841251fd67646e8b6bb4c7e0c2c385f6a1dc7403f5ac6ee7b07c96f0815f7f3'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v7'; 			sha256='81d7040e90e9b69cb0378778f673e1fc2a24ef6dbd47931dc83ab6472fc5809d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm64'; 			sha256='42d5cee287ec7426de5252276a05f3ea565ac2d65d62d052b885a84dd54152d5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-ppc64le'; 			sha256='6a4e6a243f83d80cd46c939f327b2e14cfddd2c6690651cf48d0e208c3345b88'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-riscv64'; 			sha256='eae82aec74a420c3d1734123e6a3bc10b3a2a981aa1d538502373e31c91bf76e'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-s390x'; 			sha256='97b112b3366a471cc375e0f881d65a9a7b07f0962f308834c37f5c3fa75aad08'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 20 Feb 2025 06:04:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD ["sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
VOLUME [/var/lib/docker]
# Thu, 20 Feb 2025 06:04:43 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD []
# Thu, 20 Feb 2025 06:04:43 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 20 Feb 2025 06:04:43 GMT
USER rootless
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fddc498219722db61fe7f7e06295aa8b64f7e48d19d0339176689ea591eea4ca`  
		Last Modified: Sat, 22 Feb 2025 00:27:26 GMT  
		Size: 8.1 MB (8062985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c17b75175e66b76074511db7ebd5bdc56ac19ba269d30e4f58ba4812816ad4`  
		Last Modified: Sat, 22 Feb 2025 00:27:26 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987b6d8519d32209785b3840639a10aa6247ff1e290a651ebcca3d8c33e23dd2`  
		Last Modified: Sat, 22 Feb 2025 00:27:27 GMT  
		Size: 19.5 MB (19492233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7677267af1ddfc39dbdf35dcdca7c20328e83a42b64595f0d5880c62e99a91f`  
		Last Modified: Sat, 22 Feb 2025 00:27:27 GMT  
		Size: 21.8 MB (21829139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9fa9f5140fd1401e5edaa2de6f975bd14f0b79efbafbe0d2497ea0213ecd260`  
		Last Modified: Sat, 22 Feb 2025 00:27:27 GMT  
		Size: 21.0 MB (20958635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124bcf7a51a8a140479ebb1cfd0aea5bf38223d37b7c6ae1deb93bbb1abc0469`  
		Last Modified: Sat, 22 Feb 2025 00:27:28 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3083b3dfd2242fbeb7b498bb2e0d99d55c8e34cad7396573784aa86db3c69355`  
		Last Modified: Sat, 22 Feb 2025 00:27:28 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b255e6bd488c8fb61ba962afb512c02077ecc7e41b50991cb3229aaa7ae94b`  
		Last Modified: Sat, 22 Feb 2025 00:27:28 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42458739bc4b2677f265360a10a2eacffd5133b0242dd313ba8a3dac7a116c4`  
		Last Modified: Sat, 22 Feb 2025 01:08:23 GMT  
		Size: 6.7 MB (6733003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5a7650793a22cfeac45c6610fe2cd3ccd26b6795d33ee5389d66a174c05a65`  
		Last Modified: Sat, 22 Feb 2025 01:08:23 GMT  
		Size: 90.3 KB (90318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03749f129a866bd1cf2e2797db758f883cf177f3cd33ff3c60924ec811728b4f`  
		Last Modified: Sat, 22 Feb 2025 01:08:23 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:769e1c97b1855704d1f74c39b30c2d2bbc890339752b2be542477e64d2529c32`  
		Last Modified: Sat, 22 Feb 2025 01:08:24 GMT  
		Size: 60.2 MB (60189735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e450e39e6d5b103505878dd35ff532dcdfef40450540495b6a666e7bc34e2587`  
		Last Modified: Sat, 22 Feb 2025 01:08:23 GMT  
		Size: 1.6 KB (1637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254862f49c6f0929e44b00f9635661aff98a508d2dc321d6ddc2944f60ac90bb`  
		Last Modified: Sat, 22 Feb 2025 01:08:23 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04d666bba697d05e04595251efc48c7cfb46c50934eb5e8b28f9ece93bbaa12f`  
		Last Modified: Sat, 22 Feb 2025 02:08:04 GMT  
		Size: 986.6 KB (986572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9e9040036c95835735c8d16482226c61fd43befb113e4654d11899b4c82c24`  
		Last Modified: Sat, 22 Feb 2025 02:08:04 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c773fc7dad6ddd06fd1b5c0d2b81528878a1c879bcfed7b967fed225ec4346a7`  
		Last Modified: Sat, 22 Feb 2025 02:08:04 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce0abea1fd4caba2bf7cfa1eaab27c1e81060389830353f7de69a562c0d129f3`  
		Last Modified: Sat, 22 Feb 2025 02:08:05 GMT  
		Size: 17.2 MB (17166401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e73037866943973bf1a62ff0acb7da9d1f19cc8ff52edb6c2ddf748fba1507`  
		Last Modified: Sat, 22 Feb 2025 02:08:05 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:788f83bf8b427ca8d5db790b94b5465dd4e729d19870cf23c0a99aa2247419e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:171bb75448d4664abab1f0e5b2859c6858afa3eaf4bbe30c4ff52221ef9588a5`

```dockerfile
```

-	Layers:
	-	`sha256:681e1874c769bcd3cc3a0fe90e1caa86a29f1a172fc7caa3eb5c75bb6e9843e7`  
		Last Modified: Sat, 22 Feb 2025 02:08:03 GMT  
		Size: 30.5 KB (30451 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:73776940d20eac532ae279be7c72ff89ea730517ff9dab5a659516bc00d09dda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.7 MB (152694408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5b89ed4c42e88420300229e316f2cf5c30d71c0341b7ba4039b7887870e259b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_VERSION=28.0.0
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-amd64'; 			sha256='7f355525bfaf411302570b705118181b720f18071f4be3f0eaac7b2297d826e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v6'; 			sha256='f841251fd67646e8b6bb4c7e0c2c385f6a1dc7403f5ac6ee7b07c96f0815f7f3'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v7'; 			sha256='81d7040e90e9b69cb0378778f673e1fc2a24ef6dbd47931dc83ab6472fc5809d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm64'; 			sha256='42d5cee287ec7426de5252276a05f3ea565ac2d65d62d052b885a84dd54152d5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-ppc64le'; 			sha256='6a4e6a243f83d80cd46c939f327b2e14cfddd2c6690651cf48d0e208c3345b88'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-riscv64'; 			sha256='eae82aec74a420c3d1734123e6a3bc10b3a2a981aa1d538502373e31c91bf76e'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-s390x'; 			sha256='97b112b3366a471cc375e0f881d65a9a7b07f0962f308834c37f5c3fa75aad08'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 20 Feb 2025 06:04:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD ["sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
VOLUME [/var/lib/docker]
# Thu, 20 Feb 2025 06:04:43 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD []
# Thu, 20 Feb 2025 06:04:43 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 20 Feb 2025 06:04:43 GMT
USER rootless
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:076f26e7389ad2e79a31e03589b2c6943495faa94ce7fc6ecd800dd0c320c71e`  
		Last Modified: Sat, 22 Feb 2025 00:28:38 GMT  
		Size: 8.1 MB (8076430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54483e7ea72052e991e704ef33b6d45d32f2c9886445d70ae79e50a2dd444147`  
		Last Modified: Sat, 22 Feb 2025 00:28:37 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d747fdfb37d0ca59992c4852cab088ffb4549e3f8ef7632b252452c1c12c7989`  
		Last Modified: Sat, 22 Feb 2025 00:28:38 GMT  
		Size: 18.4 MB (18412791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84912acd39dd03fae2cffdb073ec52df5d17e2700910653a8c844d31a916a7eb`  
		Last Modified: Sat, 22 Feb 2025 00:28:39 GMT  
		Size: 20.0 MB (20041446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49191a7f2e90fd89997d49d48799f225e27d4d811c1ab6a1a5ed18c8b5a9f94`  
		Last Modified: Sat, 22 Feb 2025 00:28:40 GMT  
		Size: 19.2 MB (19222674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7debd3993d0af81423e3290841931e4b162ff882877ebb292b10f3dde6dc5694`  
		Last Modified: Sat, 22 Feb 2025 00:28:39 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855282ceddcfc470897f6e2cb33f2ad4742db7c00f24a0386714c91a31a090fa`  
		Last Modified: Sat, 22 Feb 2025 00:28:40 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fbaf9714c72f8c1c56eb53405de18b5c63f82fcfa89814a71a92c9844e1fb8b`  
		Last Modified: Sat, 22 Feb 2025 00:28:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f1efb7aef297fc62aaca013f0102b13d4fb2bd1eb6e39c858c91c440c973f87`  
		Last Modified: Sat, 22 Feb 2025 02:46:00 GMT  
		Size: 7.0 MB (6978850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d301065fd8bf09964f1efc59488efd3c692d574aae6e2460fefc3dac799912b`  
		Last Modified: Sat, 22 Feb 2025 02:46:00 GMT  
		Size: 99.4 KB (99390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d33e0f749652bb606f1e92e433cb70fa6c8e7a30737050979d975e9f06a132f`  
		Last Modified: Sat, 22 Feb 2025 02:45:59 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a409b11008465c3cb7523e669b4d2a064619125185de982089bf11944cf62502`  
		Last Modified: Sat, 22 Feb 2025 02:46:01 GMT  
		Size: 55.6 MB (55566753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff8cdce63f040e68fff768b8a75d7ebdd3f4cd4e69ed0f85ae0ad620baa9c40`  
		Last Modified: Sat, 22 Feb 2025 02:46:00 GMT  
		Size: 1.6 KB (1636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f72a632b800deed0be1fc7ec78852db28106ae059a841b87a966fed6ec7255f`  
		Last Modified: Sat, 22 Feb 2025 02:46:01 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4468cca51cdd29ea280bb7c9d7dcffc805ae2134d5d10101acabb31403f19c34`  
		Last Modified: Sat, 22 Feb 2025 03:07:17 GMT  
		Size: 1.0 MB (1014200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d43f7cfe0c5e55bc699a2f0f56e6ecd213c0d84783892175a2bbabe01e1ee1`  
		Last Modified: Sat, 22 Feb 2025 03:07:17 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ffc8590ff3cdff71a791e5dd600d08fee46a9a23862330e1c51e7fe2953e3c`  
		Last Modified: Sat, 22 Feb 2025 03:07:17 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b03647ba73f1a14d321c6973445bfedd81d7195d0c270c2a52d81c4bd00241ec`  
		Last Modified: Sat, 22 Feb 2025 03:07:18 GMT  
		Size: 19.3 MB (19279443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42024c25dd02ca9c645e8270327928627cf8b2d1ce95c86e3184f7236d8254b3`  
		Last Modified: Sat, 22 Feb 2025 03:07:18 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:7caef0d171c210bbc06a3c6c5f181d699cdab3868ed8201206157f5ce2b26b41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66ce0dd66d759a7501d703e2bd782cf6c3190278388bb80297dd5fdc65839c39`

```dockerfile
```

-	Layers:
	-	`sha256:f29410d962e3aeed18fdb7f16f7e72ba75bab67d36d78eaa1f5bb9e00bee589a`  
		Last Modified: Sat, 22 Feb 2025 03:07:17 GMT  
		Size: 30.6 KB (30621 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28-windowsservercore`

```console
$ docker pull docker@sha256:8cbb71e3463881e43b4e46000916a151f195288cba0ad77f0eabef966bc5d438
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

### `docker:28-windowsservercore` - windows version 10.0.26100.2894; amd64

```console
$ docker pull docker@sha256:13348bcc4ed6fcd578c6aea25afa087bac0759457ff724c916d2fb3624c804ba
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2565217611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:172682bc22fc40249839b093831f2ccdb06d47eda95530dd64db1bf9bba03ee5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Sat, 22 Feb 2025 00:31:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 22 Feb 2025 00:31:31 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 22 Feb 2025 00:31:31 GMT
ENV DOCKER_VERSION=28.0.0
# Sat, 22 Feb 2025 00:31:32 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.0.zip
# Sat, 22 Feb 2025 00:31:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 22 Feb 2025 00:31:42 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Sat, 22 Feb 2025 00:31:42 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.windows-amd64.exe
# Sat, 22 Feb 2025 00:31:43 GMT
ENV DOCKER_BUILDX_SHA256=ab3eba3acbfa6b6612690af075795254f29762efc8abace5f636b8e7628b1851
# Sat, 22 Feb 2025 00:31:51 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 22 Feb 2025 00:31:52 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Sat, 22 Feb 2025 00:31:53 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-windows-x86_64.exe
# Sat, 22 Feb 2025 00:31:53 GMT
ENV DOCKER_COMPOSE_SHA256=01bce3456228d8e1e4b0ba056f4b9730b7fd2c1a7113c8a985144c0fdee797b0
# Sat, 22 Feb 2025 00:32:02 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Tue, 14 Jan 2025 18:53:06 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b538b630814b004320f0f9ee0a9c3594e03b773b5580fed4105a81f74e7c098f`  
		Last Modified: Sat, 22 Feb 2025 00:32:07 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58e25b87bc1505ec562cf342b28ce02166b0c50e250e5b111cae842bd29224a6`  
		Last Modified: Sat, 22 Feb 2025 00:32:08 GMT  
		Size: 382.4 KB (382390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54dec53b66cd21d806f4ecb36e798d52785171b19a3b94a2886816c4b00fc357`  
		Last Modified: Sat, 22 Feb 2025 00:32:07 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:173311079ab932318629c9bfc59957c46ffef6d9500148722bf57885ab4d912e`  
		Last Modified: Sat, 22 Feb 2025 00:32:07 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5ef5273358e9d6949b1c0c7a006b2fe22a9b45af8454771a753c47f67702fc5`  
		Last Modified: Sat, 22 Feb 2025 00:32:09 GMT  
		Size: 19.8 MB (19841357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6550ae8a0cab9e35d0c0177c6afc594dd1f53008f4c0b85bdca771700fa770c`  
		Last Modified: Sat, 22 Feb 2025 00:32:06 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e430e1223ff0212bf349270e614e999171df037e89b09997ff907efa689e97d`  
		Last Modified: Sat, 22 Feb 2025 00:32:06 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adf1c042512ab6127e6371768343f9e2125e122a97350d29044867620964da29`  
		Last Modified: Sat, 22 Feb 2025 00:32:05 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbcc9f9bc1cf9f00d67c29fcbf84300c45479de6c73cf2f49f1ae660cf73bb07`  
		Last Modified: Sat, 22 Feb 2025 00:32:08 GMT  
		Size: 22.8 MB (22778890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b21becac3572331f658c564c93303ec2f6d01292e600e1b7deab5fea30b05ff6`  
		Last Modified: Sat, 22 Feb 2025 00:32:05 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e856f770850ac4d1cb287a7e7807f001c6f669a135f306ccf2fe6e63129def66`  
		Last Modified: Sat, 22 Feb 2025 00:32:05 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e457e71b003d1ce3d61f1df1c12e7500d728f4b5598604334164ddb533cb2ba`  
		Last Modified: Sat, 22 Feb 2025 00:32:05 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f63f581bda80c595a4087c00b71030e7a4d71012bb05cbc2eb9c139f9679e31`  
		Last Modified: Sat, 22 Feb 2025 00:32:08 GMT  
		Size: 21.9 MB (21925519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28-windowsservercore` - windows version 10.0.20348.3207; amd64

```console
$ docker pull docker@sha256:40cac7c487ab96fd2608d22182da86766f98f6f8726e4a9cc87f61fba1c79f0e
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2328776516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a7dc1af03d6c94095c7be69ba1d7ffcba2c6ddbf201a1901bafc1445c1d7615`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Sat, 22 Feb 2025 00:37:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 22 Feb 2025 00:37:49 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 22 Feb 2025 00:37:49 GMT
ENV DOCKER_VERSION=28.0.0
# Sat, 22 Feb 2025 00:37:50 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.0.zip
# Sat, 22 Feb 2025 00:38:01 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 22 Feb 2025 00:38:01 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Sat, 22 Feb 2025 00:38:02 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.windows-amd64.exe
# Sat, 22 Feb 2025 00:38:02 GMT
ENV DOCKER_BUILDX_SHA256=ab3eba3acbfa6b6612690af075795254f29762efc8abace5f636b8e7628b1851
# Sat, 22 Feb 2025 00:38:11 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 22 Feb 2025 00:38:12 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Sat, 22 Feb 2025 00:38:13 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-windows-x86_64.exe
# Sat, 22 Feb 2025 00:38:13 GMT
ENV DOCKER_COMPOSE_SHA256=01bce3456228d8e1e4b0ba056f4b9730b7fd2c1a7113c8a985144c0fdee797b0
# Sat, 22 Feb 2025 00:38:22 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Tue, 11 Feb 2025 18:38:32 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a513c2ebb5aac6eaccc568c460584aa652a09401a4f865e8b1a9870e4f9826d`  
		Last Modified: Sat, 22 Feb 2025 00:38:28 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f0ea743d1a5ae5f5f7088a7c23ca759ec9b363ca46d674d9e7425aa27739ba`  
		Last Modified: Sat, 22 Feb 2025 00:38:27 GMT  
		Size: 389.0 KB (388984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:401dea1d9556118c14843e687f7eb2f2767205cefe7c534ce370103f7bb4520c`  
		Last Modified: Sat, 22 Feb 2025 00:38:27 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ff218fd9efd93054faba12c9de123bd815f47af0057f0822bebe1980b506039`  
		Last Modified: Sat, 22 Feb 2025 00:38:26 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef9e343cb24c4c76e4c3fbbf11fa22c10da7fea8e22f98be5493a15840e79f6`  
		Last Modified: Sat, 22 Feb 2025 00:38:28 GMT  
		Size: 19.8 MB (19832408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b072185e609fe777fbfd0d1c7e0860cfd307e8d0718c19365cbe22f499636207`  
		Last Modified: Sat, 22 Feb 2025 00:38:26 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a89b4e620aaf525ac2545408e3d49037c7d5b8c99ee26edb1937e8a2a5c181c`  
		Last Modified: Sat, 22 Feb 2025 00:38:25 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7edf322adba1ba7c101c710b53b2f04cb139c273b95e29fcc5d8943f581af167`  
		Last Modified: Sat, 22 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c220811a807867c0315d6291b99472e043388fe4f317d60dcb70cf42963b333`  
		Last Modified: Sat, 22 Feb 2025 00:38:27 GMT  
		Size: 22.8 MB (22770286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a73d03430d6958d170ed89b00d83fa15b1b28a9aa22fbd4ae9018b5671cb08f6`  
		Last Modified: Sat, 22 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:164bc468207a3b25ae55b075dc0b5987de3ca0d425be73ff7f45fe57b49f807f`  
		Last Modified: Sat, 22 Feb 2025 00:38:24 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7307712a7f1b1601e8cf9b306574434f960222e78bb80360573ae2829c165ab9`  
		Last Modified: Sat, 22 Feb 2025 00:38:24 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ff623c1936592d4e22a10ac22c1ba99d55a4c960680df6e5e9da20450cf85d`  
		Last Modified: Sat, 22 Feb 2025 00:38:27 GMT  
		Size: 21.9 MB (21914957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28-windowsservercore` - windows version 10.0.17763.6893; amd64

```console
$ docker pull docker@sha256:575fd688c3bf866a95546fe93e2564fea753d26e5931ebfc1e32ebd9bc411358
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2201693889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47afabbd0d9bf289e87beda973d92a82859b49c2b2f83325e44032f22df554d7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Sat, 22 Feb 2025 00:36:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 22 Feb 2025 00:37:03 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 22 Feb 2025 00:37:04 GMT
ENV DOCKER_VERSION=28.0.0
# Sat, 22 Feb 2025 00:37:05 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.0.zip
# Sat, 22 Feb 2025 00:37:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 22 Feb 2025 00:37:18 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Sat, 22 Feb 2025 00:37:18 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.windows-amd64.exe
# Sat, 22 Feb 2025 00:37:19 GMT
ENV DOCKER_BUILDX_SHA256=ab3eba3acbfa6b6612690af075795254f29762efc8abace5f636b8e7628b1851
# Sat, 22 Feb 2025 00:37:28 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 22 Feb 2025 00:37:29 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Sat, 22 Feb 2025 00:37:30 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-windows-x86_64.exe
# Sat, 22 Feb 2025 00:37:31 GMT
ENV DOCKER_COMPOSE_SHA256=01bce3456228d8e1e4b0ba056f4b9730b7fd2c1a7113c8a985144c0fdee797b0
# Sat, 22 Feb 2025 00:37:39 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 18:49:50 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d662e474d0eebcc45d26c962c3ea2815d5ad421c4abce3dfca970d20d34206`  
		Last Modified: Sat, 22 Feb 2025 00:37:45 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b80c05d72492cc29e69146de42b5cbab7c6912ef3a85c579caaf8ccb3b7eabb9`  
		Last Modified: Sat, 22 Feb 2025 00:37:44 GMT  
		Size: 343.2 KB (343235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df0623e2321e34b1b589a3f2314cdc767fe978372d17c7d621c1b6e40645f0e2`  
		Last Modified: Sat, 22 Feb 2025 00:37:44 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177b2d1a530b8667811479317d9e8ae2eb9cf1e26892e886e4baa298209fcfa4`  
		Last Modified: Sat, 22 Feb 2025 00:37:44 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3834ee7310198b95517a8b510904c8f38cbdb7c49df0b228572059fee55faa4`  
		Last Modified: Sat, 22 Feb 2025 00:37:46 GMT  
		Size: 19.8 MB (19805126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7d9cad94e2d870741143d557fc15084b8f7f0c3f510618f76861f6c020ec0c`  
		Last Modified: Sat, 22 Feb 2025 00:37:43 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73e623554754f1c6df8e43e93e867af1218d203b9111a1b977befbc4542f33e`  
		Last Modified: Sat, 22 Feb 2025 00:37:43 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39746d0ab1fefcec984bb203b47fb43af6294430288792c106045708180cf90f`  
		Last Modified: Sat, 22 Feb 2025 00:37:43 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb7e0de055ddbb75c2d00fd897c8e623d5d164e9da002c14c5d7b16034ddefb2`  
		Last Modified: Sat, 22 Feb 2025 00:37:45 GMT  
		Size: 22.7 MB (22743044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d103e4264cc2326442d2f2c0d9a6f8a6d63672a9e1888b0eb106211fe4c866a8`  
		Last Modified: Sat, 22 Feb 2025 00:37:42 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e7898abd14f1e9f5aaa3850e26c6e47b5af14ccc7727ace668f06058bb6bbbb`  
		Last Modified: Sat, 22 Feb 2025 00:37:42 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac30b7d53b77634caea695af70ca54fad87eec4119c5d63afcd64b762dadee9f`  
		Last Modified: Sat, 22 Feb 2025 00:37:42 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a13d827d5d10e25d56e691281a38fb310acbe73a53d8ecb6c27a3c737305b83d`  
		Last Modified: Sat, 22 Feb 2025 00:37:44 GMT  
		Size: 21.9 MB (21881997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28-windowsservercore-1809`

```console
$ docker pull docker@sha256:8b5e611771751fe8360ccf0f5bb3b6c022a079599c9e8dada6351d3682c645b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `docker:28-windowsservercore-1809` - windows version 10.0.17763.6893; amd64

```console
$ docker pull docker@sha256:575fd688c3bf866a95546fe93e2564fea753d26e5931ebfc1e32ebd9bc411358
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2201693889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47afabbd0d9bf289e87beda973d92a82859b49c2b2f83325e44032f22df554d7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Sat, 22 Feb 2025 00:36:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 22 Feb 2025 00:37:03 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 22 Feb 2025 00:37:04 GMT
ENV DOCKER_VERSION=28.0.0
# Sat, 22 Feb 2025 00:37:05 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.0.zip
# Sat, 22 Feb 2025 00:37:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 22 Feb 2025 00:37:18 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Sat, 22 Feb 2025 00:37:18 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.windows-amd64.exe
# Sat, 22 Feb 2025 00:37:19 GMT
ENV DOCKER_BUILDX_SHA256=ab3eba3acbfa6b6612690af075795254f29762efc8abace5f636b8e7628b1851
# Sat, 22 Feb 2025 00:37:28 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 22 Feb 2025 00:37:29 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Sat, 22 Feb 2025 00:37:30 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-windows-x86_64.exe
# Sat, 22 Feb 2025 00:37:31 GMT
ENV DOCKER_COMPOSE_SHA256=01bce3456228d8e1e4b0ba056f4b9730b7fd2c1a7113c8a985144c0fdee797b0
# Sat, 22 Feb 2025 00:37:39 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 18:49:50 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d662e474d0eebcc45d26c962c3ea2815d5ad421c4abce3dfca970d20d34206`  
		Last Modified: Sat, 22 Feb 2025 00:37:45 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b80c05d72492cc29e69146de42b5cbab7c6912ef3a85c579caaf8ccb3b7eabb9`  
		Last Modified: Sat, 22 Feb 2025 00:37:44 GMT  
		Size: 343.2 KB (343235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df0623e2321e34b1b589a3f2314cdc767fe978372d17c7d621c1b6e40645f0e2`  
		Last Modified: Sat, 22 Feb 2025 00:37:44 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177b2d1a530b8667811479317d9e8ae2eb9cf1e26892e886e4baa298209fcfa4`  
		Last Modified: Sat, 22 Feb 2025 00:37:44 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3834ee7310198b95517a8b510904c8f38cbdb7c49df0b228572059fee55faa4`  
		Last Modified: Sat, 22 Feb 2025 00:37:46 GMT  
		Size: 19.8 MB (19805126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7d9cad94e2d870741143d557fc15084b8f7f0c3f510618f76861f6c020ec0c`  
		Last Modified: Sat, 22 Feb 2025 00:37:43 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73e623554754f1c6df8e43e93e867af1218d203b9111a1b977befbc4542f33e`  
		Last Modified: Sat, 22 Feb 2025 00:37:43 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39746d0ab1fefcec984bb203b47fb43af6294430288792c106045708180cf90f`  
		Last Modified: Sat, 22 Feb 2025 00:37:43 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb7e0de055ddbb75c2d00fd897c8e623d5d164e9da002c14c5d7b16034ddefb2`  
		Last Modified: Sat, 22 Feb 2025 00:37:45 GMT  
		Size: 22.7 MB (22743044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d103e4264cc2326442d2f2c0d9a6f8a6d63672a9e1888b0eb106211fe4c866a8`  
		Last Modified: Sat, 22 Feb 2025 00:37:42 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e7898abd14f1e9f5aaa3850e26c6e47b5af14ccc7727ace668f06058bb6bbbb`  
		Last Modified: Sat, 22 Feb 2025 00:37:42 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac30b7d53b77634caea695af70ca54fad87eec4119c5d63afcd64b762dadee9f`  
		Last Modified: Sat, 22 Feb 2025 00:37:42 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a13d827d5d10e25d56e691281a38fb310acbe73a53d8ecb6c27a3c737305b83d`  
		Last Modified: Sat, 22 Feb 2025 00:37:44 GMT  
		Size: 21.9 MB (21881997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:4a4531319a3d77d264dd66e0056a37a0ce12653a767680d3114dc86e6d50de94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3207; amd64

### `docker:28-windowsservercore-ltsc2022` - windows version 10.0.20348.3207; amd64

```console
$ docker pull docker@sha256:40cac7c487ab96fd2608d22182da86766f98f6f8726e4a9cc87f61fba1c79f0e
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2328776516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a7dc1af03d6c94095c7be69ba1d7ffcba2c6ddbf201a1901bafc1445c1d7615`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Sat, 22 Feb 2025 00:37:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 22 Feb 2025 00:37:49 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 22 Feb 2025 00:37:49 GMT
ENV DOCKER_VERSION=28.0.0
# Sat, 22 Feb 2025 00:37:50 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.0.zip
# Sat, 22 Feb 2025 00:38:01 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 22 Feb 2025 00:38:01 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Sat, 22 Feb 2025 00:38:02 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.windows-amd64.exe
# Sat, 22 Feb 2025 00:38:02 GMT
ENV DOCKER_BUILDX_SHA256=ab3eba3acbfa6b6612690af075795254f29762efc8abace5f636b8e7628b1851
# Sat, 22 Feb 2025 00:38:11 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 22 Feb 2025 00:38:12 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Sat, 22 Feb 2025 00:38:13 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-windows-x86_64.exe
# Sat, 22 Feb 2025 00:38:13 GMT
ENV DOCKER_COMPOSE_SHA256=01bce3456228d8e1e4b0ba056f4b9730b7fd2c1a7113c8a985144c0fdee797b0
# Sat, 22 Feb 2025 00:38:22 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Tue, 11 Feb 2025 18:38:32 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a513c2ebb5aac6eaccc568c460584aa652a09401a4f865e8b1a9870e4f9826d`  
		Last Modified: Sat, 22 Feb 2025 00:38:28 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f0ea743d1a5ae5f5f7088a7c23ca759ec9b363ca46d674d9e7425aa27739ba`  
		Last Modified: Sat, 22 Feb 2025 00:38:27 GMT  
		Size: 389.0 KB (388984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:401dea1d9556118c14843e687f7eb2f2767205cefe7c534ce370103f7bb4520c`  
		Last Modified: Sat, 22 Feb 2025 00:38:27 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ff218fd9efd93054faba12c9de123bd815f47af0057f0822bebe1980b506039`  
		Last Modified: Sat, 22 Feb 2025 00:38:26 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef9e343cb24c4c76e4c3fbbf11fa22c10da7fea8e22f98be5493a15840e79f6`  
		Last Modified: Sat, 22 Feb 2025 00:38:28 GMT  
		Size: 19.8 MB (19832408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b072185e609fe777fbfd0d1c7e0860cfd307e8d0718c19365cbe22f499636207`  
		Last Modified: Sat, 22 Feb 2025 00:38:26 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a89b4e620aaf525ac2545408e3d49037c7d5b8c99ee26edb1937e8a2a5c181c`  
		Last Modified: Sat, 22 Feb 2025 00:38:25 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7edf322adba1ba7c101c710b53b2f04cb139c273b95e29fcc5d8943f581af167`  
		Last Modified: Sat, 22 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c220811a807867c0315d6291b99472e043388fe4f317d60dcb70cf42963b333`  
		Last Modified: Sat, 22 Feb 2025 00:38:27 GMT  
		Size: 22.8 MB (22770286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a73d03430d6958d170ed89b00d83fa15b1b28a9aa22fbd4ae9018b5671cb08f6`  
		Last Modified: Sat, 22 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:164bc468207a3b25ae55b075dc0b5987de3ca0d425be73ff7f45fe57b49f807f`  
		Last Modified: Sat, 22 Feb 2025 00:38:24 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7307712a7f1b1601e8cf9b306574434f960222e78bb80360573ae2829c165ab9`  
		Last Modified: Sat, 22 Feb 2025 00:38:24 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ff623c1936592d4e22a10ac22c1ba99d55a4c960680df6e5e9da20450cf85d`  
		Last Modified: Sat, 22 Feb 2025 00:38:27 GMT  
		Size: 21.9 MB (21914957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:78307f6a713fd34f43a0d89127421c46b2ff65f06362768394f4e6612dc89989
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.2894; amd64

### `docker:28-windowsservercore-ltsc2025` - windows version 10.0.26100.2894; amd64

```console
$ docker pull docker@sha256:13348bcc4ed6fcd578c6aea25afa087bac0759457ff724c916d2fb3624c804ba
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2565217611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:172682bc22fc40249839b093831f2ccdb06d47eda95530dd64db1bf9bba03ee5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Sat, 22 Feb 2025 00:31:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 22 Feb 2025 00:31:31 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 22 Feb 2025 00:31:31 GMT
ENV DOCKER_VERSION=28.0.0
# Sat, 22 Feb 2025 00:31:32 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.0.zip
# Sat, 22 Feb 2025 00:31:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 22 Feb 2025 00:31:42 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Sat, 22 Feb 2025 00:31:42 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.windows-amd64.exe
# Sat, 22 Feb 2025 00:31:43 GMT
ENV DOCKER_BUILDX_SHA256=ab3eba3acbfa6b6612690af075795254f29762efc8abace5f636b8e7628b1851
# Sat, 22 Feb 2025 00:31:51 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 22 Feb 2025 00:31:52 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Sat, 22 Feb 2025 00:31:53 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-windows-x86_64.exe
# Sat, 22 Feb 2025 00:31:53 GMT
ENV DOCKER_COMPOSE_SHA256=01bce3456228d8e1e4b0ba056f4b9730b7fd2c1a7113c8a985144c0fdee797b0
# Sat, 22 Feb 2025 00:32:02 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Tue, 14 Jan 2025 18:53:06 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b538b630814b004320f0f9ee0a9c3594e03b773b5580fed4105a81f74e7c098f`  
		Last Modified: Sat, 22 Feb 2025 00:32:07 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58e25b87bc1505ec562cf342b28ce02166b0c50e250e5b111cae842bd29224a6`  
		Last Modified: Sat, 22 Feb 2025 00:32:08 GMT  
		Size: 382.4 KB (382390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54dec53b66cd21d806f4ecb36e798d52785171b19a3b94a2886816c4b00fc357`  
		Last Modified: Sat, 22 Feb 2025 00:32:07 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:173311079ab932318629c9bfc59957c46ffef6d9500148722bf57885ab4d912e`  
		Last Modified: Sat, 22 Feb 2025 00:32:07 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5ef5273358e9d6949b1c0c7a006b2fe22a9b45af8454771a753c47f67702fc5`  
		Last Modified: Sat, 22 Feb 2025 00:32:09 GMT  
		Size: 19.8 MB (19841357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6550ae8a0cab9e35d0c0177c6afc594dd1f53008f4c0b85bdca771700fa770c`  
		Last Modified: Sat, 22 Feb 2025 00:32:06 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e430e1223ff0212bf349270e614e999171df037e89b09997ff907efa689e97d`  
		Last Modified: Sat, 22 Feb 2025 00:32:06 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adf1c042512ab6127e6371768343f9e2125e122a97350d29044867620964da29`  
		Last Modified: Sat, 22 Feb 2025 00:32:05 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbcc9f9bc1cf9f00d67c29fcbf84300c45479de6c73cf2f49f1ae660cf73bb07`  
		Last Modified: Sat, 22 Feb 2025 00:32:08 GMT  
		Size: 22.8 MB (22778890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b21becac3572331f658c564c93303ec2f6d01292e600e1b7deab5fea30b05ff6`  
		Last Modified: Sat, 22 Feb 2025 00:32:05 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e856f770850ac4d1cb287a7e7807f001c6f669a135f306ccf2fe6e63129def66`  
		Last Modified: Sat, 22 Feb 2025 00:32:05 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e457e71b003d1ce3d61f1df1c12e7500d728f4b5598604334164ddb533cb2ba`  
		Last Modified: Sat, 22 Feb 2025 00:32:05 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f63f581bda80c595a4087c00b71030e7a4d71012bb05cbc2eb9c139f9679e31`  
		Last Modified: Sat, 22 Feb 2025 00:32:08 GMT  
		Size: 21.9 MB (21925519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.0`

```console
$ docker pull docker@sha256:0a9c58ebc9f86e5af35e4330f6c738dc64fce3ca2e2574b5becdfb88765b308b
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

### `docker:28.0` - linux; amd64

```console
$ docker pull docker@sha256:32c276e9aafff90ea7765271afa524c293c9749e880748217b1abedd04af39a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.0 MB (141006353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1da86d0da980dad6c82075b9859478027165e57dba77994a2fe1fa99ed408f3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_VERSION=28.0.0
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-amd64'; 			sha256='7f355525bfaf411302570b705118181b720f18071f4be3f0eaac7b2297d826e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v6'; 			sha256='f841251fd67646e8b6bb4c7e0c2c385f6a1dc7403f5ac6ee7b07c96f0815f7f3'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v7'; 			sha256='81d7040e90e9b69cb0378778f673e1fc2a24ef6dbd47931dc83ab6472fc5809d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm64'; 			sha256='42d5cee287ec7426de5252276a05f3ea565ac2d65d62d052b885a84dd54152d5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-ppc64le'; 			sha256='6a4e6a243f83d80cd46c939f327b2e14cfddd2c6690651cf48d0e208c3345b88'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-riscv64'; 			sha256='eae82aec74a420c3d1734123e6a3bc10b3a2a981aa1d538502373e31c91bf76e'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-s390x'; 			sha256='97b112b3366a471cc375e0f881d65a9a7b07f0962f308834c37f5c3fa75aad08'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 20 Feb 2025 06:04:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD ["sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
VOLUME [/var/lib/docker]
# Thu, 20 Feb 2025 06:04:43 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD []
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fddc498219722db61fe7f7e06295aa8b64f7e48d19d0339176689ea591eea4ca`  
		Last Modified: Sat, 22 Feb 2025 00:27:26 GMT  
		Size: 8.1 MB (8062985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c17b75175e66b76074511db7ebd5bdc56ac19ba269d30e4f58ba4812816ad4`  
		Last Modified: Sat, 22 Feb 2025 00:27:26 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987b6d8519d32209785b3840639a10aa6247ff1e290a651ebcca3d8c33e23dd2`  
		Last Modified: Sat, 22 Feb 2025 00:27:27 GMT  
		Size: 19.5 MB (19492233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7677267af1ddfc39dbdf35dcdca7c20328e83a42b64595f0d5880c62e99a91f`  
		Last Modified: Sat, 22 Feb 2025 00:27:27 GMT  
		Size: 21.8 MB (21829139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9fa9f5140fd1401e5edaa2de6f975bd14f0b79efbafbe0d2497ea0213ecd260`  
		Last Modified: Sat, 22 Feb 2025 00:27:27 GMT  
		Size: 21.0 MB (20958635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124bcf7a51a8a140479ebb1cfd0aea5bf38223d37b7c6ae1deb93bbb1abc0469`  
		Last Modified: Sat, 22 Feb 2025 00:27:28 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3083b3dfd2242fbeb7b498bb2e0d99d55c8e34cad7396573784aa86db3c69355`  
		Last Modified: Sat, 22 Feb 2025 00:27:28 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b255e6bd488c8fb61ba962afb512c02077ecc7e41b50991cb3229aaa7ae94b`  
		Last Modified: Sat, 22 Feb 2025 00:27:28 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42458739bc4b2677f265360a10a2eacffd5133b0242dd313ba8a3dac7a116c4`  
		Last Modified: Sat, 22 Feb 2025 01:08:23 GMT  
		Size: 6.7 MB (6733003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5a7650793a22cfeac45c6610fe2cd3ccd26b6795d33ee5389d66a174c05a65`  
		Last Modified: Sat, 22 Feb 2025 01:08:23 GMT  
		Size: 90.3 KB (90318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03749f129a866bd1cf2e2797db758f883cf177f3cd33ff3c60924ec811728b4f`  
		Last Modified: Sat, 22 Feb 2025 01:08:23 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:769e1c97b1855704d1f74c39b30c2d2bbc890339752b2be542477e64d2529c32`  
		Last Modified: Sat, 22 Feb 2025 01:08:24 GMT  
		Size: 60.2 MB (60189735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e450e39e6d5b103505878dd35ff532dcdfef40450540495b6a666e7bc34e2587`  
		Last Modified: Sat, 22 Feb 2025 01:08:23 GMT  
		Size: 1.6 KB (1637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254862f49c6f0929e44b00f9635661aff98a508d2dc321d6ddc2944f60ac90bb`  
		Last Modified: Sat, 22 Feb 2025 01:08:23 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0` - unknown; unknown

```console
$ docker pull docker@sha256:ba9368fe1da752bf14bb9ed738b656214abfea5e16cb949f4883beeb86cf9408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:658bfc3f8051aceaf851bbf4fdcff3b32c7f8c853b5262abd646f57fbf14bb10`

```dockerfile
```

-	Layers:
	-	`sha256:670c6ce494a80447b9f682d0ac427af5be54978f5f629221274a481ecf2be95e`  
		Last Modified: Sat, 22 Feb 2025 01:08:22 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0` - linux; arm variant v6

```console
$ docker pull docker@sha256:346b1790ac4379efe1ff83735d9d72ded98e8ebcc776f29f190a50d1086d5c63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.7 MB (131676535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e2b568d33d9f4d9da33be6f6a26a6e533f58d6d874c445c67494a71fe99ce8c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_VERSION=28.0.0
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-amd64'; 			sha256='7f355525bfaf411302570b705118181b720f18071f4be3f0eaac7b2297d826e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v6'; 			sha256='f841251fd67646e8b6bb4c7e0c2c385f6a1dc7403f5ac6ee7b07c96f0815f7f3'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v7'; 			sha256='81d7040e90e9b69cb0378778f673e1fc2a24ef6dbd47931dc83ab6472fc5809d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm64'; 			sha256='42d5cee287ec7426de5252276a05f3ea565ac2d65d62d052b885a84dd54152d5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-ppc64le'; 			sha256='6a4e6a243f83d80cd46c939f327b2e14cfddd2c6690651cf48d0e208c3345b88'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-riscv64'; 			sha256='eae82aec74a420c3d1734123e6a3bc10b3a2a981aa1d538502373e31c91bf76e'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-s390x'; 			sha256='97b112b3366a471cc375e0f881d65a9a7b07f0962f308834c37f5c3fa75aad08'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 20 Feb 2025 06:04:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD ["sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
VOLUME [/var/lib/docker]
# Thu, 20 Feb 2025 06:04:43 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD []
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e40b3641449ca47aef50c48f620eb6d3a3bc2292e5cf4ea267f5f03e6c7bc`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 8.0 MB (7978133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df16922f358c97f513c6d0b9457abb36aefc588e45374edd23692381878a7`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21eb60c27f71135d16125d7dcf87a6c0a49fc39428a0a7ecbc83c6bc1087efa9`  
		Last Modified: Thu, 20 Feb 2025 23:28:03 GMT  
		Size: 17.5 MB (17453851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b3b7abf60d98565d245e7aab34cfdec0b3c2c8ff503fb00ebceed21f636a93`  
		Last Modified: Sat, 22 Feb 2025 00:28:48 GMT  
		Size: 20.4 MB (20432003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ced3aebdded979735885d70afdbc8a5f03be15205f1145cd3b2af469eb21175`  
		Last Modified: Sat, 22 Feb 2025 00:28:48 GMT  
		Size: 19.7 MB (19725892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f8d07fba646c3b5ac2a07d053675df2a0422b36b698a824d345ee2447bc8e1`  
		Last Modified: Sat, 22 Feb 2025 00:28:47 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c51a22c8e8f3b4205fde47fd17f66895fad1496f33f46bb6aebdf5938bb94ad`  
		Last Modified: Sat, 22 Feb 2025 00:28:47 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f36ff703ab2a5ebeeeb26f374c59106eb92bf26531f572228024531dcc975f64`  
		Last Modified: Sat, 22 Feb 2025 00:28:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2440995b1488c0fccd4c0a9b3062c58a33404bcc3ca3e8289ae64b6393946c65`  
		Last Modified: Sat, 22 Feb 2025 01:29:31 GMT  
		Size: 7.0 MB (7036904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cce93707f7a9fed88581b5b8e8f49a184ba206f961aae653eef08af3b94987b1`  
		Last Modified: Sat, 22 Feb 2025 01:29:30 GMT  
		Size: 89.8 KB (89849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26cf971d434da3f52513e2595da034274a6fb8c1ef74cddc815339506b7b704a`  
		Last Modified: Sat, 22 Feb 2025 01:29:30 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c3188476c3d7ba720f96be3cdceb222b9a7a6e0693a917966988332f14e8ef`  
		Last Modified: Sat, 22 Feb 2025 01:29:33 GMT  
		Size: 55.6 MB (55587101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c9e4329aff590ce10c6d6613452bf70f9708c4817750614d9a1a68918444a6`  
		Last Modified: Sat, 22 Feb 2025 01:29:31 GMT  
		Size: 1.6 KB (1638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ff2444afd5e703729aeef9ead8d60b8f059c8e5f0b4b82853f021d0f2c24504`  
		Last Modified: Sat, 22 Feb 2025 01:29:31 GMT  
		Size: 3.3 KB (3263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0` - unknown; unknown

```console
$ docker pull docker@sha256:0931cacdc5870a73bd56837c9590fb9801af1b229cbf7ee86dc79c932a51323c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d14b9f57c5e9b67b594f4172c7cfbb95e2442a040e0bb090b09cc95ce2d35a18`

```dockerfile
```

-	Layers:
	-	`sha256:93150d2f1d44b19b0d6d36517e86cddc39cd49f0857f41bdb86a200f7db357e6`  
		Last Modified: Sat, 22 Feb 2025 01:29:30 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0` - linux; arm variant v7

```console
$ docker pull docker@sha256:089424d7adbb66df8dd78e5ce27d9bd9d13cebe072cb5eb79e7478f00c124163
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (130009843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da65fa603f2dc74e8750fbdc3d7173e607ca901a8dfb81fab1136584884d3018`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_VERSION=28.0.0
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-amd64'; 			sha256='7f355525bfaf411302570b705118181b720f18071f4be3f0eaac7b2297d826e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v6'; 			sha256='f841251fd67646e8b6bb4c7e0c2c385f6a1dc7403f5ac6ee7b07c96f0815f7f3'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v7'; 			sha256='81d7040e90e9b69cb0378778f673e1fc2a24ef6dbd47931dc83ab6472fc5809d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm64'; 			sha256='42d5cee287ec7426de5252276a05f3ea565ac2d65d62d052b885a84dd54152d5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-ppc64le'; 			sha256='6a4e6a243f83d80cd46c939f327b2e14cfddd2c6690651cf48d0e208c3345b88'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-riscv64'; 			sha256='eae82aec74a420c3d1734123e6a3bc10b3a2a981aa1d538502373e31c91bf76e'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-s390x'; 			sha256='97b112b3366a471cc375e0f881d65a9a7b07f0962f308834c37f5c3fa75aad08'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 20 Feb 2025 06:04:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD ["sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
VOLUME [/var/lib/docker]
# Thu, 20 Feb 2025 06:04:43 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD []
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b654458a637c48c7f8f46da325ae8f810828e851ed4ab4b406092503eb680f`  
		Last Modified: Sat, 22 Feb 2025 00:28:04 GMT  
		Size: 7.3 MB (7299375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3474560bdd0e71f5972a48abd9e80877e2219f6eacae8272034d8503bcb634b2`  
		Last Modified: Sat, 22 Feb 2025 00:28:03 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ffc820c153872520700f2618e71ee9bea9cfee69fbff7b0ea4acb751a2fee5`  
		Last Modified: Sat, 22 Feb 2025 00:28:04 GMT  
		Size: 17.4 MB (17444426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a39a48e6818f4f7d6e7637cf221cc02da7b2e8ab3ca2643a527024430497175`  
		Last Modified: Sat, 22 Feb 2025 00:28:04 GMT  
		Size: 20.4 MB (20411656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168ce845c02246501347d9ae0d1bb9bb9f55a707c5ef03ba3bb6377e832c28f4`  
		Last Modified: Sat, 22 Feb 2025 00:28:05 GMT  
		Size: 19.7 MB (19708525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d62f1159ab01591fa3510e1ddc7b7e0313d001750472b1eaa0dcfb3a1f097732`  
		Last Modified: Sat, 22 Feb 2025 00:28:05 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ab9b1b4b0f9c261b260d739cd6d593a2c510b9c29045d72d930f2baf5fa78e`  
		Last Modified: Sat, 22 Feb 2025 00:28:05 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d27509dd9fc9bdb19051b5661dce75fc9b53979841bcd49fd03667b1ad6dde`  
		Last Modified: Sat, 22 Feb 2025 00:28:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd0d2a57f389ccbd627e0bca3b813e9397f4a6a55364b1f7cf22df043542cf1a`  
		Last Modified: Sat, 22 Feb 2025 04:54:52 GMT  
		Size: 6.4 MB (6366292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5947e3cbc6a2eb4d8c4ec17605876ea3e3a5cb2c09abac0a58d53cc4d6569f7`  
		Last Modified: Sat, 22 Feb 2025 04:54:51 GMT  
		Size: 86.3 KB (86342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc1fa6b8e4e654268e5dfc6afa5b1e88bfb92da3c33018f231f76ad7e08a59e`  
		Last Modified: Sat, 22 Feb 2025 04:54:51 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f544c5574adf21ca185480beea8b120134f2ed74f3f2418dc0ef564a3891490`  
		Last Modified: Sat, 22 Feb 2025 04:54:53 GMT  
		Size: 55.6 MB (55587054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd1c8be29e89fc14e8cd0778dcda3dae4c641d9ab956b2f9ce8d02df1d7984e`  
		Last Modified: Sat, 22 Feb 2025 04:54:52 GMT  
		Size: 1.6 KB (1636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db5e7511235a55ebe7a92c8825189d27a2b1d951e0f25d22e4e932636abbd466`  
		Last Modified: Sat, 22 Feb 2025 04:54:52 GMT  
		Size: 3.3 KB (3256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0` - unknown; unknown

```console
$ docker pull docker@sha256:1cdaa27022a39a251e498044fefc2f4160913794dc50a3074935741e0d39d28b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:643a439611cab3be1c6fde6e85ec369c205d94c81b88f1c91a627a32a6448b32`

```dockerfile
```

-	Layers:
	-	`sha256:fa998948cfd33a55b2120a90b998117bea32698c81f84e340fc1f9fa359825c4`  
		Last Modified: Sat, 22 Feb 2025 04:54:51 GMT  
		Size: 34.8 KB (34765 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:af92e15294f197a3cc4de0e75e012f4e91a996e4fd58ad96e163208aea7f0be3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.4 MB (132399422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89d922b5c31bca4bc340632485ab5243809aaf557e7aaf377fd956c15f4ad0a6`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_VERSION=28.0.0
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-amd64'; 			sha256='7f355525bfaf411302570b705118181b720f18071f4be3f0eaac7b2297d826e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v6'; 			sha256='f841251fd67646e8b6bb4c7e0c2c385f6a1dc7403f5ac6ee7b07c96f0815f7f3'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v7'; 			sha256='81d7040e90e9b69cb0378778f673e1fc2a24ef6dbd47931dc83ab6472fc5809d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm64'; 			sha256='42d5cee287ec7426de5252276a05f3ea565ac2d65d62d052b885a84dd54152d5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-ppc64le'; 			sha256='6a4e6a243f83d80cd46c939f327b2e14cfddd2c6690651cf48d0e208c3345b88'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-riscv64'; 			sha256='eae82aec74a420c3d1734123e6a3bc10b3a2a981aa1d538502373e31c91bf76e'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-s390x'; 			sha256='97b112b3366a471cc375e0f881d65a9a7b07f0962f308834c37f5c3fa75aad08'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 20 Feb 2025 06:04:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD ["sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
VOLUME [/var/lib/docker]
# Thu, 20 Feb 2025 06:04:43 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD []
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:076f26e7389ad2e79a31e03589b2c6943495faa94ce7fc6ecd800dd0c320c71e`  
		Last Modified: Sat, 22 Feb 2025 00:28:38 GMT  
		Size: 8.1 MB (8076430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54483e7ea72052e991e704ef33b6d45d32f2c9886445d70ae79e50a2dd444147`  
		Last Modified: Sat, 22 Feb 2025 00:28:37 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d747fdfb37d0ca59992c4852cab088ffb4549e3f8ef7632b252452c1c12c7989`  
		Last Modified: Sat, 22 Feb 2025 00:28:38 GMT  
		Size: 18.4 MB (18412791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84912acd39dd03fae2cffdb073ec52df5d17e2700910653a8c844d31a916a7eb`  
		Last Modified: Sat, 22 Feb 2025 00:28:39 GMT  
		Size: 20.0 MB (20041446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49191a7f2e90fd89997d49d48799f225e27d4d811c1ab6a1a5ed18c8b5a9f94`  
		Last Modified: Sat, 22 Feb 2025 00:28:40 GMT  
		Size: 19.2 MB (19222674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7debd3993d0af81423e3290841931e4b162ff882877ebb292b10f3dde6dc5694`  
		Last Modified: Sat, 22 Feb 2025 00:28:39 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855282ceddcfc470897f6e2cb33f2ad4742db7c00f24a0386714c91a31a090fa`  
		Last Modified: Sat, 22 Feb 2025 00:28:40 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fbaf9714c72f8c1c56eb53405de18b5c63f82fcfa89814a71a92c9844e1fb8b`  
		Last Modified: Sat, 22 Feb 2025 00:28:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f1efb7aef297fc62aaca013f0102b13d4fb2bd1eb6e39c858c91c440c973f87`  
		Last Modified: Sat, 22 Feb 2025 02:46:00 GMT  
		Size: 7.0 MB (6978850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d301065fd8bf09964f1efc59488efd3c692d574aae6e2460fefc3dac799912b`  
		Last Modified: Sat, 22 Feb 2025 02:46:00 GMT  
		Size: 99.4 KB (99390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d33e0f749652bb606f1e92e433cb70fa6c8e7a30737050979d975e9f06a132f`  
		Last Modified: Sat, 22 Feb 2025 02:45:59 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a409b11008465c3cb7523e669b4d2a064619125185de982089bf11944cf62502`  
		Last Modified: Sat, 22 Feb 2025 02:46:01 GMT  
		Size: 55.6 MB (55566753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff8cdce63f040e68fff768b8a75d7ebdd3f4cd4e69ed0f85ae0ad620baa9c40`  
		Last Modified: Sat, 22 Feb 2025 02:46:00 GMT  
		Size: 1.6 KB (1636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f72a632b800deed0be1fc7ec78852db28106ae059a841b87a966fed6ec7255f`  
		Last Modified: Sat, 22 Feb 2025 02:46:01 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0` - unknown; unknown

```console
$ docker pull docker@sha256:d6dd49a97960eaef409aa41f89cf8596c02281b55801b3f726b267761031bc90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4105199c766800ff78dca393a5dccdb1435364291ecf731c31deacb4fa6e86a4`

```dockerfile
```

-	Layers:
	-	`sha256:2f7e554767be7baf2d46a3652bbe4405cdcb83972440eb83c19280ab0e991188`  
		Last Modified: Sat, 22 Feb 2025 02:45:59 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.0-cli`

```console
$ docker pull docker@sha256:28fb556c1ea1eef2f1d8d70e8c7eb52e38324b2ae04ffcb8df26648a7c2e5dfc
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

### `docker:28.0-cli` - linux; amd64

```console
$ docker pull docker@sha256:828f4f57525db5dbdb2f52ba47087c383361fd22975c264142bab1ff78ea8587
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73987390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2047a2478c64769a8f8963db4efc714c734b9ec896b1452fb424720a232732d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 21 Feb 2025 18:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_VERSION=28.0.0
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-amd64'; 			sha256='7f355525bfaf411302570b705118181b720f18071f4be3f0eaac7b2297d826e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v6'; 			sha256='f841251fd67646e8b6bb4c7e0c2c385f6a1dc7403f5ac6ee7b07c96f0815f7f3'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v7'; 			sha256='81d7040e90e9b69cb0378778f673e1fc2a24ef6dbd47931dc83ab6472fc5809d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm64'; 			sha256='42d5cee287ec7426de5252276a05f3ea565ac2d65d62d052b885a84dd54152d5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-ppc64le'; 			sha256='6a4e6a243f83d80cd46c939f327b2e14cfddd2c6690651cf48d0e208c3345b88'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-riscv64'; 			sha256='eae82aec74a420c3d1734123e6a3bc10b3a2a981aa1d538502373e31c91bf76e'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-s390x'; 			sha256='97b112b3366a471cc375e0f881d65a9a7b07f0962f308834c37f5c3fa75aad08'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 21 Feb 2025 18:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 18:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fddc498219722db61fe7f7e06295aa8b64f7e48d19d0339176689ea591eea4ca`  
		Last Modified: Sat, 22 Feb 2025 00:27:26 GMT  
		Size: 8.1 MB (8062985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c17b75175e66b76074511db7ebd5bdc56ac19ba269d30e4f58ba4812816ad4`  
		Last Modified: Sat, 22 Feb 2025 00:27:26 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987b6d8519d32209785b3840639a10aa6247ff1e290a651ebcca3d8c33e23dd2`  
		Last Modified: Sat, 22 Feb 2025 00:27:27 GMT  
		Size: 19.5 MB (19492233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7677267af1ddfc39dbdf35dcdca7c20328e83a42b64595f0d5880c62e99a91f`  
		Last Modified: Sat, 22 Feb 2025 00:27:27 GMT  
		Size: 21.8 MB (21829139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9fa9f5140fd1401e5edaa2de6f975bd14f0b79efbafbe0d2497ea0213ecd260`  
		Last Modified: Sat, 22 Feb 2025 00:27:27 GMT  
		Size: 21.0 MB (20958635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124bcf7a51a8a140479ebb1cfd0aea5bf38223d37b7c6ae1deb93bbb1abc0469`  
		Last Modified: Sat, 22 Feb 2025 00:27:28 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3083b3dfd2242fbeb7b498bb2e0d99d55c8e34cad7396573784aa86db3c69355`  
		Last Modified: Sat, 22 Feb 2025 00:27:28 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b255e6bd488c8fb61ba962afb512c02077ecc7e41b50991cb3229aaa7ae94b`  
		Last Modified: Sat, 22 Feb 2025 00:27:28 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:23d0fdad7d91848fe9aefbb31f9ec0f13048b4043d184117ef3506756fb199f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d89ed9762486ccde5720aaa5cfd88b8e5c1bf286c15632485f3c3a9b66385e0`

```dockerfile
```

-	Layers:
	-	`sha256:29c00cb8b559fbda58a54628ef429544bb24356f7620856781c43b802464d245`  
		Last Modified: Sat, 22 Feb 2025 00:27:26 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:563c0b58e54b2cb6649f26c22d8f06f2be7ebb8dead799918f4b22b13dd7d9f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (68956771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eabedade3d89f3eb7ffac6cf1924c31c852c974072b582d14b744e4c9c6993a2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 21 Feb 2025 18:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_VERSION=28.0.0
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-amd64'; 			sha256='7f355525bfaf411302570b705118181b720f18071f4be3f0eaac7b2297d826e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v6'; 			sha256='f841251fd67646e8b6bb4c7e0c2c385f6a1dc7403f5ac6ee7b07c96f0815f7f3'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v7'; 			sha256='81d7040e90e9b69cb0378778f673e1fc2a24ef6dbd47931dc83ab6472fc5809d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm64'; 			sha256='42d5cee287ec7426de5252276a05f3ea565ac2d65d62d052b885a84dd54152d5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-ppc64le'; 			sha256='6a4e6a243f83d80cd46c939f327b2e14cfddd2c6690651cf48d0e208c3345b88'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-riscv64'; 			sha256='eae82aec74a420c3d1734123e6a3bc10b3a2a981aa1d538502373e31c91bf76e'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-s390x'; 			sha256='97b112b3366a471cc375e0f881d65a9a7b07f0962f308834c37f5c3fa75aad08'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 21 Feb 2025 18:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 18:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e40b3641449ca47aef50c48f620eb6d3a3bc2292e5cf4ea267f5f03e6c7bc`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 8.0 MB (7978133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df16922f358c97f513c6d0b9457abb36aefc588e45374edd23692381878a7`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21eb60c27f71135d16125d7dcf87a6c0a49fc39428a0a7ecbc83c6bc1087efa9`  
		Last Modified: Thu, 20 Feb 2025 23:28:03 GMT  
		Size: 17.5 MB (17453851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b3b7abf60d98565d245e7aab34cfdec0b3c2c8ff503fb00ebceed21f636a93`  
		Last Modified: Sat, 22 Feb 2025 00:28:48 GMT  
		Size: 20.4 MB (20432003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ced3aebdded979735885d70afdbc8a5f03be15205f1145cd3b2af469eb21175`  
		Last Modified: Sat, 22 Feb 2025 00:28:48 GMT  
		Size: 19.7 MB (19725892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f8d07fba646c3b5ac2a07d053675df2a0422b36b698a824d345ee2447bc8e1`  
		Last Modified: Sat, 22 Feb 2025 00:28:47 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c51a22c8e8f3b4205fde47fd17f66895fad1496f33f46bb6aebdf5938bb94ad`  
		Last Modified: Sat, 22 Feb 2025 00:28:47 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f36ff703ab2a5ebeeeb26f374c59106eb92bf26531f572228024531dcc975f64`  
		Last Modified: Sat, 22 Feb 2025 00:28:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:19ac4c1b39024c4040fa578e5a4947132dfa561816cb7525547f283ad033cb82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d38b373d00ff94b39de7f66b705b156b58a6c9747a3aa783505be0e6c3ebf00`

```dockerfile
```

-	Layers:
	-	`sha256:65c4a818e540437ada35738cd53dff3f48895979403e4f6d6893ef134b4a0b5e`  
		Last Modified: Sat, 22 Feb 2025 00:28:47 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:6045d4846c59f8ee46c1d168dfe9b4de563a1602ed536f9a75e133d23291dc17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (67964254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ba8f3ae10c4069acc8988e46282e2592d80824e75e262440f1ca87b5b54fa4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 21 Feb 2025 18:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_VERSION=28.0.0
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-amd64'; 			sha256='7f355525bfaf411302570b705118181b720f18071f4be3f0eaac7b2297d826e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v6'; 			sha256='f841251fd67646e8b6bb4c7e0c2c385f6a1dc7403f5ac6ee7b07c96f0815f7f3'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v7'; 			sha256='81d7040e90e9b69cb0378778f673e1fc2a24ef6dbd47931dc83ab6472fc5809d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm64'; 			sha256='42d5cee287ec7426de5252276a05f3ea565ac2d65d62d052b885a84dd54152d5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-ppc64le'; 			sha256='6a4e6a243f83d80cd46c939f327b2e14cfddd2c6690651cf48d0e208c3345b88'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-riscv64'; 			sha256='eae82aec74a420c3d1734123e6a3bc10b3a2a981aa1d538502373e31c91bf76e'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-s390x'; 			sha256='97b112b3366a471cc375e0f881d65a9a7b07f0962f308834c37f5c3fa75aad08'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 21 Feb 2025 18:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 18:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b654458a637c48c7f8f46da325ae8f810828e851ed4ab4b406092503eb680f`  
		Last Modified: Sat, 22 Feb 2025 00:28:04 GMT  
		Size: 7.3 MB (7299375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3474560bdd0e71f5972a48abd9e80877e2219f6eacae8272034d8503bcb634b2`  
		Last Modified: Sat, 22 Feb 2025 00:28:03 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ffc820c153872520700f2618e71ee9bea9cfee69fbff7b0ea4acb751a2fee5`  
		Last Modified: Sat, 22 Feb 2025 00:28:04 GMT  
		Size: 17.4 MB (17444426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a39a48e6818f4f7d6e7637cf221cc02da7b2e8ab3ca2643a527024430497175`  
		Last Modified: Sat, 22 Feb 2025 00:28:04 GMT  
		Size: 20.4 MB (20411656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168ce845c02246501347d9ae0d1bb9bb9f55a707c5ef03ba3bb6377e832c28f4`  
		Last Modified: Sat, 22 Feb 2025 00:28:05 GMT  
		Size: 19.7 MB (19708525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d62f1159ab01591fa3510e1ddc7b7e0313d001750472b1eaa0dcfb3a1f097732`  
		Last Modified: Sat, 22 Feb 2025 00:28:05 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ab9b1b4b0f9c261b260d739cd6d593a2c510b9c29045d72d930f2baf5fa78e`  
		Last Modified: Sat, 22 Feb 2025 00:28:05 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d27509dd9fc9bdb19051b5661dce75fc9b53979841bcd49fd03667b1ad6dde`  
		Last Modified: Sat, 22 Feb 2025 00:28:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:23645fb2cbf9071135cf4f6aa3c2daf2dc3370793a863fef2ee39d5314bc1a81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93af0d5ba0d4eddf4e7d202afc318f1221ed8bb0f4b1ffde83604fd9bd752b41`

```dockerfile
```

-	Layers:
	-	`sha256:c3cccd9b156d9500700d8b30693438b27b91e56bc8149ff0300632ebb0780d36`  
		Last Modified: Sat, 22 Feb 2025 00:28:03 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:11e8dfd68841685653bd4816fc6ab2f95cc84940d099b1e683a4b60a958599df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69748524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af7e01753428f0214a4072134b7c0481b29b9f695ebe735e920d47b6c0302c4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 21 Feb 2025 18:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_VERSION=28.0.0
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-amd64'; 			sha256='7f355525bfaf411302570b705118181b720f18071f4be3f0eaac7b2297d826e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v6'; 			sha256='f841251fd67646e8b6bb4c7e0c2c385f6a1dc7403f5ac6ee7b07c96f0815f7f3'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v7'; 			sha256='81d7040e90e9b69cb0378778f673e1fc2a24ef6dbd47931dc83ab6472fc5809d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm64'; 			sha256='42d5cee287ec7426de5252276a05f3ea565ac2d65d62d052b885a84dd54152d5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-ppc64le'; 			sha256='6a4e6a243f83d80cd46c939f327b2e14cfddd2c6690651cf48d0e208c3345b88'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-riscv64'; 			sha256='eae82aec74a420c3d1734123e6a3bc10b3a2a981aa1d538502373e31c91bf76e'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-s390x'; 			sha256='97b112b3366a471cc375e0f881d65a9a7b07f0962f308834c37f5c3fa75aad08'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 21 Feb 2025 18:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 18:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:076f26e7389ad2e79a31e03589b2c6943495faa94ce7fc6ecd800dd0c320c71e`  
		Last Modified: Sat, 22 Feb 2025 00:28:38 GMT  
		Size: 8.1 MB (8076430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54483e7ea72052e991e704ef33b6d45d32f2c9886445d70ae79e50a2dd444147`  
		Last Modified: Sat, 22 Feb 2025 00:28:37 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d747fdfb37d0ca59992c4852cab088ffb4549e3f8ef7632b252452c1c12c7989`  
		Last Modified: Sat, 22 Feb 2025 00:28:38 GMT  
		Size: 18.4 MB (18412791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84912acd39dd03fae2cffdb073ec52df5d17e2700910653a8c844d31a916a7eb`  
		Last Modified: Sat, 22 Feb 2025 00:28:39 GMT  
		Size: 20.0 MB (20041446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49191a7f2e90fd89997d49d48799f225e27d4d811c1ab6a1a5ed18c8b5a9f94`  
		Last Modified: Sat, 22 Feb 2025 00:28:40 GMT  
		Size: 19.2 MB (19222674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7debd3993d0af81423e3290841931e4b162ff882877ebb292b10f3dde6dc5694`  
		Last Modified: Sat, 22 Feb 2025 00:28:39 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855282ceddcfc470897f6e2cb33f2ad4742db7c00f24a0386714c91a31a090fa`  
		Last Modified: Sat, 22 Feb 2025 00:28:40 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fbaf9714c72f8c1c56eb53405de18b5c63f82fcfa89814a71a92c9844e1fb8b`  
		Last Modified: Sat, 22 Feb 2025 00:28:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:30588165fa8677446217c19a011fa7b5dd4b56689b71068054b1769685612965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:050a79ebe758ee7f1e33b2b06dd06dabf7b2d3ccb381eb495d95c61658b577c3`

```dockerfile
```

-	Layers:
	-	`sha256:eb188e16beab9632a0818b296adc7960adad9c23b87529bf5b8f419eef964844`  
		Last Modified: Sat, 22 Feb 2025 00:28:37 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.0-dind`

```console
$ docker pull docker@sha256:0a9c58ebc9f86e5af35e4330f6c738dc64fce3ca2e2574b5becdfb88765b308b
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

### `docker:28.0-dind` - linux; amd64

```console
$ docker pull docker@sha256:32c276e9aafff90ea7765271afa524c293c9749e880748217b1abedd04af39a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.0 MB (141006353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1da86d0da980dad6c82075b9859478027165e57dba77994a2fe1fa99ed408f3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_VERSION=28.0.0
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-amd64'; 			sha256='7f355525bfaf411302570b705118181b720f18071f4be3f0eaac7b2297d826e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v6'; 			sha256='f841251fd67646e8b6bb4c7e0c2c385f6a1dc7403f5ac6ee7b07c96f0815f7f3'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v7'; 			sha256='81d7040e90e9b69cb0378778f673e1fc2a24ef6dbd47931dc83ab6472fc5809d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm64'; 			sha256='42d5cee287ec7426de5252276a05f3ea565ac2d65d62d052b885a84dd54152d5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-ppc64le'; 			sha256='6a4e6a243f83d80cd46c939f327b2e14cfddd2c6690651cf48d0e208c3345b88'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-riscv64'; 			sha256='eae82aec74a420c3d1734123e6a3bc10b3a2a981aa1d538502373e31c91bf76e'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-s390x'; 			sha256='97b112b3366a471cc375e0f881d65a9a7b07f0962f308834c37f5c3fa75aad08'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 20 Feb 2025 06:04:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD ["sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
VOLUME [/var/lib/docker]
# Thu, 20 Feb 2025 06:04:43 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD []
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fddc498219722db61fe7f7e06295aa8b64f7e48d19d0339176689ea591eea4ca`  
		Last Modified: Sat, 22 Feb 2025 00:27:26 GMT  
		Size: 8.1 MB (8062985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c17b75175e66b76074511db7ebd5bdc56ac19ba269d30e4f58ba4812816ad4`  
		Last Modified: Sat, 22 Feb 2025 00:27:26 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987b6d8519d32209785b3840639a10aa6247ff1e290a651ebcca3d8c33e23dd2`  
		Last Modified: Sat, 22 Feb 2025 00:27:27 GMT  
		Size: 19.5 MB (19492233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7677267af1ddfc39dbdf35dcdca7c20328e83a42b64595f0d5880c62e99a91f`  
		Last Modified: Sat, 22 Feb 2025 00:27:27 GMT  
		Size: 21.8 MB (21829139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9fa9f5140fd1401e5edaa2de6f975bd14f0b79efbafbe0d2497ea0213ecd260`  
		Last Modified: Sat, 22 Feb 2025 00:27:27 GMT  
		Size: 21.0 MB (20958635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124bcf7a51a8a140479ebb1cfd0aea5bf38223d37b7c6ae1deb93bbb1abc0469`  
		Last Modified: Sat, 22 Feb 2025 00:27:28 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3083b3dfd2242fbeb7b498bb2e0d99d55c8e34cad7396573784aa86db3c69355`  
		Last Modified: Sat, 22 Feb 2025 00:27:28 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b255e6bd488c8fb61ba962afb512c02077ecc7e41b50991cb3229aaa7ae94b`  
		Last Modified: Sat, 22 Feb 2025 00:27:28 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42458739bc4b2677f265360a10a2eacffd5133b0242dd313ba8a3dac7a116c4`  
		Last Modified: Sat, 22 Feb 2025 01:08:23 GMT  
		Size: 6.7 MB (6733003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5a7650793a22cfeac45c6610fe2cd3ccd26b6795d33ee5389d66a174c05a65`  
		Last Modified: Sat, 22 Feb 2025 01:08:23 GMT  
		Size: 90.3 KB (90318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03749f129a866bd1cf2e2797db758f883cf177f3cd33ff3c60924ec811728b4f`  
		Last Modified: Sat, 22 Feb 2025 01:08:23 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:769e1c97b1855704d1f74c39b30c2d2bbc890339752b2be542477e64d2529c32`  
		Last Modified: Sat, 22 Feb 2025 01:08:24 GMT  
		Size: 60.2 MB (60189735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e450e39e6d5b103505878dd35ff532dcdfef40450540495b6a666e7bc34e2587`  
		Last Modified: Sat, 22 Feb 2025 01:08:23 GMT  
		Size: 1.6 KB (1637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254862f49c6f0929e44b00f9635661aff98a508d2dc321d6ddc2944f60ac90bb`  
		Last Modified: Sat, 22 Feb 2025 01:08:23 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0-dind` - unknown; unknown

```console
$ docker pull docker@sha256:ba9368fe1da752bf14bb9ed738b656214abfea5e16cb949f4883beeb86cf9408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:658bfc3f8051aceaf851bbf4fdcff3b32c7f8c853b5262abd646f57fbf14bb10`

```dockerfile
```

-	Layers:
	-	`sha256:670c6ce494a80447b9f682d0ac427af5be54978f5f629221274a481ecf2be95e`  
		Last Modified: Sat, 22 Feb 2025 01:08:22 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:346b1790ac4379efe1ff83735d9d72ded98e8ebcc776f29f190a50d1086d5c63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.7 MB (131676535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e2b568d33d9f4d9da33be6f6a26a6e533f58d6d874c445c67494a71fe99ce8c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_VERSION=28.0.0
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-amd64'; 			sha256='7f355525bfaf411302570b705118181b720f18071f4be3f0eaac7b2297d826e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v6'; 			sha256='f841251fd67646e8b6bb4c7e0c2c385f6a1dc7403f5ac6ee7b07c96f0815f7f3'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v7'; 			sha256='81d7040e90e9b69cb0378778f673e1fc2a24ef6dbd47931dc83ab6472fc5809d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm64'; 			sha256='42d5cee287ec7426de5252276a05f3ea565ac2d65d62d052b885a84dd54152d5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-ppc64le'; 			sha256='6a4e6a243f83d80cd46c939f327b2e14cfddd2c6690651cf48d0e208c3345b88'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-riscv64'; 			sha256='eae82aec74a420c3d1734123e6a3bc10b3a2a981aa1d538502373e31c91bf76e'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-s390x'; 			sha256='97b112b3366a471cc375e0f881d65a9a7b07f0962f308834c37f5c3fa75aad08'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 20 Feb 2025 06:04:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD ["sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
VOLUME [/var/lib/docker]
# Thu, 20 Feb 2025 06:04:43 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD []
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e40b3641449ca47aef50c48f620eb6d3a3bc2292e5cf4ea267f5f03e6c7bc`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 8.0 MB (7978133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df16922f358c97f513c6d0b9457abb36aefc588e45374edd23692381878a7`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21eb60c27f71135d16125d7dcf87a6c0a49fc39428a0a7ecbc83c6bc1087efa9`  
		Last Modified: Thu, 20 Feb 2025 23:28:03 GMT  
		Size: 17.5 MB (17453851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b3b7abf60d98565d245e7aab34cfdec0b3c2c8ff503fb00ebceed21f636a93`  
		Last Modified: Sat, 22 Feb 2025 00:28:48 GMT  
		Size: 20.4 MB (20432003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ced3aebdded979735885d70afdbc8a5f03be15205f1145cd3b2af469eb21175`  
		Last Modified: Sat, 22 Feb 2025 00:28:48 GMT  
		Size: 19.7 MB (19725892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f8d07fba646c3b5ac2a07d053675df2a0422b36b698a824d345ee2447bc8e1`  
		Last Modified: Sat, 22 Feb 2025 00:28:47 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c51a22c8e8f3b4205fde47fd17f66895fad1496f33f46bb6aebdf5938bb94ad`  
		Last Modified: Sat, 22 Feb 2025 00:28:47 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f36ff703ab2a5ebeeeb26f374c59106eb92bf26531f572228024531dcc975f64`  
		Last Modified: Sat, 22 Feb 2025 00:28:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2440995b1488c0fccd4c0a9b3062c58a33404bcc3ca3e8289ae64b6393946c65`  
		Last Modified: Sat, 22 Feb 2025 01:29:31 GMT  
		Size: 7.0 MB (7036904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cce93707f7a9fed88581b5b8e8f49a184ba206f961aae653eef08af3b94987b1`  
		Last Modified: Sat, 22 Feb 2025 01:29:30 GMT  
		Size: 89.8 KB (89849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26cf971d434da3f52513e2595da034274a6fb8c1ef74cddc815339506b7b704a`  
		Last Modified: Sat, 22 Feb 2025 01:29:30 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c3188476c3d7ba720f96be3cdceb222b9a7a6e0693a917966988332f14e8ef`  
		Last Modified: Sat, 22 Feb 2025 01:29:33 GMT  
		Size: 55.6 MB (55587101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c9e4329aff590ce10c6d6613452bf70f9708c4817750614d9a1a68918444a6`  
		Last Modified: Sat, 22 Feb 2025 01:29:31 GMT  
		Size: 1.6 KB (1638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ff2444afd5e703729aeef9ead8d60b8f059c8e5f0b4b82853f021d0f2c24504`  
		Last Modified: Sat, 22 Feb 2025 01:29:31 GMT  
		Size: 3.3 KB (3263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0-dind` - unknown; unknown

```console
$ docker pull docker@sha256:0931cacdc5870a73bd56837c9590fb9801af1b229cbf7ee86dc79c932a51323c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d14b9f57c5e9b67b594f4172c7cfbb95e2442a040e0bb090b09cc95ce2d35a18`

```dockerfile
```

-	Layers:
	-	`sha256:93150d2f1d44b19b0d6d36517e86cddc39cd49f0857f41bdb86a200f7db357e6`  
		Last Modified: Sat, 22 Feb 2025 01:29:30 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:089424d7adbb66df8dd78e5ce27d9bd9d13cebe072cb5eb79e7478f00c124163
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (130009843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da65fa603f2dc74e8750fbdc3d7173e607ca901a8dfb81fab1136584884d3018`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_VERSION=28.0.0
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-amd64'; 			sha256='7f355525bfaf411302570b705118181b720f18071f4be3f0eaac7b2297d826e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v6'; 			sha256='f841251fd67646e8b6bb4c7e0c2c385f6a1dc7403f5ac6ee7b07c96f0815f7f3'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v7'; 			sha256='81d7040e90e9b69cb0378778f673e1fc2a24ef6dbd47931dc83ab6472fc5809d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm64'; 			sha256='42d5cee287ec7426de5252276a05f3ea565ac2d65d62d052b885a84dd54152d5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-ppc64le'; 			sha256='6a4e6a243f83d80cd46c939f327b2e14cfddd2c6690651cf48d0e208c3345b88'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-riscv64'; 			sha256='eae82aec74a420c3d1734123e6a3bc10b3a2a981aa1d538502373e31c91bf76e'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-s390x'; 			sha256='97b112b3366a471cc375e0f881d65a9a7b07f0962f308834c37f5c3fa75aad08'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 20 Feb 2025 06:04:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD ["sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
VOLUME [/var/lib/docker]
# Thu, 20 Feb 2025 06:04:43 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD []
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b654458a637c48c7f8f46da325ae8f810828e851ed4ab4b406092503eb680f`  
		Last Modified: Sat, 22 Feb 2025 00:28:04 GMT  
		Size: 7.3 MB (7299375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3474560bdd0e71f5972a48abd9e80877e2219f6eacae8272034d8503bcb634b2`  
		Last Modified: Sat, 22 Feb 2025 00:28:03 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ffc820c153872520700f2618e71ee9bea9cfee69fbff7b0ea4acb751a2fee5`  
		Last Modified: Sat, 22 Feb 2025 00:28:04 GMT  
		Size: 17.4 MB (17444426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a39a48e6818f4f7d6e7637cf221cc02da7b2e8ab3ca2643a527024430497175`  
		Last Modified: Sat, 22 Feb 2025 00:28:04 GMT  
		Size: 20.4 MB (20411656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168ce845c02246501347d9ae0d1bb9bb9f55a707c5ef03ba3bb6377e832c28f4`  
		Last Modified: Sat, 22 Feb 2025 00:28:05 GMT  
		Size: 19.7 MB (19708525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d62f1159ab01591fa3510e1ddc7b7e0313d001750472b1eaa0dcfb3a1f097732`  
		Last Modified: Sat, 22 Feb 2025 00:28:05 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ab9b1b4b0f9c261b260d739cd6d593a2c510b9c29045d72d930f2baf5fa78e`  
		Last Modified: Sat, 22 Feb 2025 00:28:05 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d27509dd9fc9bdb19051b5661dce75fc9b53979841bcd49fd03667b1ad6dde`  
		Last Modified: Sat, 22 Feb 2025 00:28:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd0d2a57f389ccbd627e0bca3b813e9397f4a6a55364b1f7cf22df043542cf1a`  
		Last Modified: Sat, 22 Feb 2025 04:54:52 GMT  
		Size: 6.4 MB (6366292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5947e3cbc6a2eb4d8c4ec17605876ea3e3a5cb2c09abac0a58d53cc4d6569f7`  
		Last Modified: Sat, 22 Feb 2025 04:54:51 GMT  
		Size: 86.3 KB (86342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc1fa6b8e4e654268e5dfc6afa5b1e88bfb92da3c33018f231f76ad7e08a59e`  
		Last Modified: Sat, 22 Feb 2025 04:54:51 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f544c5574adf21ca185480beea8b120134f2ed74f3f2418dc0ef564a3891490`  
		Last Modified: Sat, 22 Feb 2025 04:54:53 GMT  
		Size: 55.6 MB (55587054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd1c8be29e89fc14e8cd0778dcda3dae4c641d9ab956b2f9ce8d02df1d7984e`  
		Last Modified: Sat, 22 Feb 2025 04:54:52 GMT  
		Size: 1.6 KB (1636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db5e7511235a55ebe7a92c8825189d27a2b1d951e0f25d22e4e932636abbd466`  
		Last Modified: Sat, 22 Feb 2025 04:54:52 GMT  
		Size: 3.3 KB (3256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0-dind` - unknown; unknown

```console
$ docker pull docker@sha256:1cdaa27022a39a251e498044fefc2f4160913794dc50a3074935741e0d39d28b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:643a439611cab3be1c6fde6e85ec369c205d94c81b88f1c91a627a32a6448b32`

```dockerfile
```

-	Layers:
	-	`sha256:fa998948cfd33a55b2120a90b998117bea32698c81f84e340fc1f9fa359825c4`  
		Last Modified: Sat, 22 Feb 2025 04:54:51 GMT  
		Size: 34.8 KB (34765 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:af92e15294f197a3cc4de0e75e012f4e91a996e4fd58ad96e163208aea7f0be3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.4 MB (132399422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89d922b5c31bca4bc340632485ab5243809aaf557e7aaf377fd956c15f4ad0a6`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_VERSION=28.0.0
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-amd64'; 			sha256='7f355525bfaf411302570b705118181b720f18071f4be3f0eaac7b2297d826e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v6'; 			sha256='f841251fd67646e8b6bb4c7e0c2c385f6a1dc7403f5ac6ee7b07c96f0815f7f3'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v7'; 			sha256='81d7040e90e9b69cb0378778f673e1fc2a24ef6dbd47931dc83ab6472fc5809d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm64'; 			sha256='42d5cee287ec7426de5252276a05f3ea565ac2d65d62d052b885a84dd54152d5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-ppc64le'; 			sha256='6a4e6a243f83d80cd46c939f327b2e14cfddd2c6690651cf48d0e208c3345b88'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-riscv64'; 			sha256='eae82aec74a420c3d1734123e6a3bc10b3a2a981aa1d538502373e31c91bf76e'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-s390x'; 			sha256='97b112b3366a471cc375e0f881d65a9a7b07f0962f308834c37f5c3fa75aad08'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 20 Feb 2025 06:04:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD ["sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
VOLUME [/var/lib/docker]
# Thu, 20 Feb 2025 06:04:43 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD []
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:076f26e7389ad2e79a31e03589b2c6943495faa94ce7fc6ecd800dd0c320c71e`  
		Last Modified: Sat, 22 Feb 2025 00:28:38 GMT  
		Size: 8.1 MB (8076430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54483e7ea72052e991e704ef33b6d45d32f2c9886445d70ae79e50a2dd444147`  
		Last Modified: Sat, 22 Feb 2025 00:28:37 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d747fdfb37d0ca59992c4852cab088ffb4549e3f8ef7632b252452c1c12c7989`  
		Last Modified: Sat, 22 Feb 2025 00:28:38 GMT  
		Size: 18.4 MB (18412791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84912acd39dd03fae2cffdb073ec52df5d17e2700910653a8c844d31a916a7eb`  
		Last Modified: Sat, 22 Feb 2025 00:28:39 GMT  
		Size: 20.0 MB (20041446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49191a7f2e90fd89997d49d48799f225e27d4d811c1ab6a1a5ed18c8b5a9f94`  
		Last Modified: Sat, 22 Feb 2025 00:28:40 GMT  
		Size: 19.2 MB (19222674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7debd3993d0af81423e3290841931e4b162ff882877ebb292b10f3dde6dc5694`  
		Last Modified: Sat, 22 Feb 2025 00:28:39 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855282ceddcfc470897f6e2cb33f2ad4742db7c00f24a0386714c91a31a090fa`  
		Last Modified: Sat, 22 Feb 2025 00:28:40 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fbaf9714c72f8c1c56eb53405de18b5c63f82fcfa89814a71a92c9844e1fb8b`  
		Last Modified: Sat, 22 Feb 2025 00:28:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f1efb7aef297fc62aaca013f0102b13d4fb2bd1eb6e39c858c91c440c973f87`  
		Last Modified: Sat, 22 Feb 2025 02:46:00 GMT  
		Size: 7.0 MB (6978850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d301065fd8bf09964f1efc59488efd3c692d574aae6e2460fefc3dac799912b`  
		Last Modified: Sat, 22 Feb 2025 02:46:00 GMT  
		Size: 99.4 KB (99390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d33e0f749652bb606f1e92e433cb70fa6c8e7a30737050979d975e9f06a132f`  
		Last Modified: Sat, 22 Feb 2025 02:45:59 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a409b11008465c3cb7523e669b4d2a064619125185de982089bf11944cf62502`  
		Last Modified: Sat, 22 Feb 2025 02:46:01 GMT  
		Size: 55.6 MB (55566753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff8cdce63f040e68fff768b8a75d7ebdd3f4cd4e69ed0f85ae0ad620baa9c40`  
		Last Modified: Sat, 22 Feb 2025 02:46:00 GMT  
		Size: 1.6 KB (1636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f72a632b800deed0be1fc7ec78852db28106ae059a841b87a966fed6ec7255f`  
		Last Modified: Sat, 22 Feb 2025 02:46:01 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0-dind` - unknown; unknown

```console
$ docker pull docker@sha256:d6dd49a97960eaef409aa41f89cf8596c02281b55801b3f726b267761031bc90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4105199c766800ff78dca393a5dccdb1435364291ecf731c31deacb4fa6e86a4`

```dockerfile
```

-	Layers:
	-	`sha256:2f7e554767be7baf2d46a3652bbe4405cdcb83972440eb83c19280ab0e991188`  
		Last Modified: Sat, 22 Feb 2025 02:45:59 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.0-dind-rootless`

```console
$ docker pull docker@sha256:f36f8f41d9e38bae8c3d247446a1e31df98bd84d1ccc22d9d8d50fbe6cbafae8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:28.0-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:16356585ff8acaa68e6bd54dd11f6760ce507fa719fe7e00bc7db05f53c7a074
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.2 MB (159160666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f413ddafbf744ab3b46d57ab5bda7d4b4ed64aa0ac7f3bd49a3055f8aa5c604`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_VERSION=28.0.0
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-amd64'; 			sha256='7f355525bfaf411302570b705118181b720f18071f4be3f0eaac7b2297d826e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v6'; 			sha256='f841251fd67646e8b6bb4c7e0c2c385f6a1dc7403f5ac6ee7b07c96f0815f7f3'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v7'; 			sha256='81d7040e90e9b69cb0378778f673e1fc2a24ef6dbd47931dc83ab6472fc5809d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm64'; 			sha256='42d5cee287ec7426de5252276a05f3ea565ac2d65d62d052b885a84dd54152d5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-ppc64le'; 			sha256='6a4e6a243f83d80cd46c939f327b2e14cfddd2c6690651cf48d0e208c3345b88'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-riscv64'; 			sha256='eae82aec74a420c3d1734123e6a3bc10b3a2a981aa1d538502373e31c91bf76e'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-s390x'; 			sha256='97b112b3366a471cc375e0f881d65a9a7b07f0962f308834c37f5c3fa75aad08'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 20 Feb 2025 06:04:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD ["sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
VOLUME [/var/lib/docker]
# Thu, 20 Feb 2025 06:04:43 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD []
# Thu, 20 Feb 2025 06:04:43 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 20 Feb 2025 06:04:43 GMT
USER rootless
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fddc498219722db61fe7f7e06295aa8b64f7e48d19d0339176689ea591eea4ca`  
		Last Modified: Sat, 22 Feb 2025 00:27:26 GMT  
		Size: 8.1 MB (8062985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c17b75175e66b76074511db7ebd5bdc56ac19ba269d30e4f58ba4812816ad4`  
		Last Modified: Sat, 22 Feb 2025 00:27:26 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987b6d8519d32209785b3840639a10aa6247ff1e290a651ebcca3d8c33e23dd2`  
		Last Modified: Sat, 22 Feb 2025 00:27:27 GMT  
		Size: 19.5 MB (19492233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7677267af1ddfc39dbdf35dcdca7c20328e83a42b64595f0d5880c62e99a91f`  
		Last Modified: Sat, 22 Feb 2025 00:27:27 GMT  
		Size: 21.8 MB (21829139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9fa9f5140fd1401e5edaa2de6f975bd14f0b79efbafbe0d2497ea0213ecd260`  
		Last Modified: Sat, 22 Feb 2025 00:27:27 GMT  
		Size: 21.0 MB (20958635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124bcf7a51a8a140479ebb1cfd0aea5bf38223d37b7c6ae1deb93bbb1abc0469`  
		Last Modified: Sat, 22 Feb 2025 00:27:28 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3083b3dfd2242fbeb7b498bb2e0d99d55c8e34cad7396573784aa86db3c69355`  
		Last Modified: Sat, 22 Feb 2025 00:27:28 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b255e6bd488c8fb61ba962afb512c02077ecc7e41b50991cb3229aaa7ae94b`  
		Last Modified: Sat, 22 Feb 2025 00:27:28 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42458739bc4b2677f265360a10a2eacffd5133b0242dd313ba8a3dac7a116c4`  
		Last Modified: Sat, 22 Feb 2025 01:08:23 GMT  
		Size: 6.7 MB (6733003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5a7650793a22cfeac45c6610fe2cd3ccd26b6795d33ee5389d66a174c05a65`  
		Last Modified: Sat, 22 Feb 2025 01:08:23 GMT  
		Size: 90.3 KB (90318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03749f129a866bd1cf2e2797db758f883cf177f3cd33ff3c60924ec811728b4f`  
		Last Modified: Sat, 22 Feb 2025 01:08:23 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:769e1c97b1855704d1f74c39b30c2d2bbc890339752b2be542477e64d2529c32`  
		Last Modified: Sat, 22 Feb 2025 01:08:24 GMT  
		Size: 60.2 MB (60189735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e450e39e6d5b103505878dd35ff532dcdfef40450540495b6a666e7bc34e2587`  
		Last Modified: Sat, 22 Feb 2025 01:08:23 GMT  
		Size: 1.6 KB (1637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254862f49c6f0929e44b00f9635661aff98a508d2dc321d6ddc2944f60ac90bb`  
		Last Modified: Sat, 22 Feb 2025 01:08:23 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04d666bba697d05e04595251efc48c7cfb46c50934eb5e8b28f9ece93bbaa12f`  
		Last Modified: Sat, 22 Feb 2025 02:08:04 GMT  
		Size: 986.6 KB (986572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9e9040036c95835735c8d16482226c61fd43befb113e4654d11899b4c82c24`  
		Last Modified: Sat, 22 Feb 2025 02:08:04 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c773fc7dad6ddd06fd1b5c0d2b81528878a1c879bcfed7b967fed225ec4346a7`  
		Last Modified: Sat, 22 Feb 2025 02:08:04 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce0abea1fd4caba2bf7cfa1eaab27c1e81060389830353f7de69a562c0d129f3`  
		Last Modified: Sat, 22 Feb 2025 02:08:05 GMT  
		Size: 17.2 MB (17166401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e73037866943973bf1a62ff0acb7da9d1f19cc8ff52edb6c2ddf748fba1507`  
		Last Modified: Sat, 22 Feb 2025 02:08:05 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:788f83bf8b427ca8d5db790b94b5465dd4e729d19870cf23c0a99aa2247419e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:171bb75448d4664abab1f0e5b2859c6858afa3eaf4bbe30c4ff52221ef9588a5`

```dockerfile
```

-	Layers:
	-	`sha256:681e1874c769bcd3cc3a0fe90e1caa86a29f1a172fc7caa3eb5c75bb6e9843e7`  
		Last Modified: Sat, 22 Feb 2025 02:08:03 GMT  
		Size: 30.5 KB (30451 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:73776940d20eac532ae279be7c72ff89ea730517ff9dab5a659516bc00d09dda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.7 MB (152694408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5b89ed4c42e88420300229e316f2cf5c30d71c0341b7ba4039b7887870e259b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_VERSION=28.0.0
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-amd64'; 			sha256='7f355525bfaf411302570b705118181b720f18071f4be3f0eaac7b2297d826e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v6'; 			sha256='f841251fd67646e8b6bb4c7e0c2c385f6a1dc7403f5ac6ee7b07c96f0815f7f3'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v7'; 			sha256='81d7040e90e9b69cb0378778f673e1fc2a24ef6dbd47931dc83ab6472fc5809d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm64'; 			sha256='42d5cee287ec7426de5252276a05f3ea565ac2d65d62d052b885a84dd54152d5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-ppc64le'; 			sha256='6a4e6a243f83d80cd46c939f327b2e14cfddd2c6690651cf48d0e208c3345b88'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-riscv64'; 			sha256='eae82aec74a420c3d1734123e6a3bc10b3a2a981aa1d538502373e31c91bf76e'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-s390x'; 			sha256='97b112b3366a471cc375e0f881d65a9a7b07f0962f308834c37f5c3fa75aad08'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 20 Feb 2025 06:04:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD ["sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
VOLUME [/var/lib/docker]
# Thu, 20 Feb 2025 06:04:43 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD []
# Thu, 20 Feb 2025 06:04:43 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 20 Feb 2025 06:04:43 GMT
USER rootless
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:076f26e7389ad2e79a31e03589b2c6943495faa94ce7fc6ecd800dd0c320c71e`  
		Last Modified: Sat, 22 Feb 2025 00:28:38 GMT  
		Size: 8.1 MB (8076430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54483e7ea72052e991e704ef33b6d45d32f2c9886445d70ae79e50a2dd444147`  
		Last Modified: Sat, 22 Feb 2025 00:28:37 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d747fdfb37d0ca59992c4852cab088ffb4549e3f8ef7632b252452c1c12c7989`  
		Last Modified: Sat, 22 Feb 2025 00:28:38 GMT  
		Size: 18.4 MB (18412791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84912acd39dd03fae2cffdb073ec52df5d17e2700910653a8c844d31a916a7eb`  
		Last Modified: Sat, 22 Feb 2025 00:28:39 GMT  
		Size: 20.0 MB (20041446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49191a7f2e90fd89997d49d48799f225e27d4d811c1ab6a1a5ed18c8b5a9f94`  
		Last Modified: Sat, 22 Feb 2025 00:28:40 GMT  
		Size: 19.2 MB (19222674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7debd3993d0af81423e3290841931e4b162ff882877ebb292b10f3dde6dc5694`  
		Last Modified: Sat, 22 Feb 2025 00:28:39 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855282ceddcfc470897f6e2cb33f2ad4742db7c00f24a0386714c91a31a090fa`  
		Last Modified: Sat, 22 Feb 2025 00:28:40 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fbaf9714c72f8c1c56eb53405de18b5c63f82fcfa89814a71a92c9844e1fb8b`  
		Last Modified: Sat, 22 Feb 2025 00:28:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f1efb7aef297fc62aaca013f0102b13d4fb2bd1eb6e39c858c91c440c973f87`  
		Last Modified: Sat, 22 Feb 2025 02:46:00 GMT  
		Size: 7.0 MB (6978850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d301065fd8bf09964f1efc59488efd3c692d574aae6e2460fefc3dac799912b`  
		Last Modified: Sat, 22 Feb 2025 02:46:00 GMT  
		Size: 99.4 KB (99390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d33e0f749652bb606f1e92e433cb70fa6c8e7a30737050979d975e9f06a132f`  
		Last Modified: Sat, 22 Feb 2025 02:45:59 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a409b11008465c3cb7523e669b4d2a064619125185de982089bf11944cf62502`  
		Last Modified: Sat, 22 Feb 2025 02:46:01 GMT  
		Size: 55.6 MB (55566753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff8cdce63f040e68fff768b8a75d7ebdd3f4cd4e69ed0f85ae0ad620baa9c40`  
		Last Modified: Sat, 22 Feb 2025 02:46:00 GMT  
		Size: 1.6 KB (1636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f72a632b800deed0be1fc7ec78852db28106ae059a841b87a966fed6ec7255f`  
		Last Modified: Sat, 22 Feb 2025 02:46:01 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4468cca51cdd29ea280bb7c9d7dcffc805ae2134d5d10101acabb31403f19c34`  
		Last Modified: Sat, 22 Feb 2025 03:07:17 GMT  
		Size: 1.0 MB (1014200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d43f7cfe0c5e55bc699a2f0f56e6ecd213c0d84783892175a2bbabe01e1ee1`  
		Last Modified: Sat, 22 Feb 2025 03:07:17 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ffc8590ff3cdff71a791e5dd600d08fee46a9a23862330e1c51e7fe2953e3c`  
		Last Modified: Sat, 22 Feb 2025 03:07:17 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b03647ba73f1a14d321c6973445bfedd81d7195d0c270c2a52d81c4bd00241ec`  
		Last Modified: Sat, 22 Feb 2025 03:07:18 GMT  
		Size: 19.3 MB (19279443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42024c25dd02ca9c645e8270327928627cf8b2d1ce95c86e3184f7236d8254b3`  
		Last Modified: Sat, 22 Feb 2025 03:07:18 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:7caef0d171c210bbc06a3c6c5f181d699cdab3868ed8201206157f5ce2b26b41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66ce0dd66d759a7501d703e2bd782cf6c3190278388bb80297dd5fdc65839c39`

```dockerfile
```

-	Layers:
	-	`sha256:f29410d962e3aeed18fdb7f16f7e72ba75bab67d36d78eaa1f5bb9e00bee589a`  
		Last Modified: Sat, 22 Feb 2025 03:07:17 GMT  
		Size: 30.6 KB (30621 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.0-windowsservercore`

```console
$ docker pull docker@sha256:8cbb71e3463881e43b4e46000916a151f195288cba0ad77f0eabef966bc5d438
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

### `docker:28.0-windowsservercore` - windows version 10.0.26100.2894; amd64

```console
$ docker pull docker@sha256:13348bcc4ed6fcd578c6aea25afa087bac0759457ff724c916d2fb3624c804ba
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2565217611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:172682bc22fc40249839b093831f2ccdb06d47eda95530dd64db1bf9bba03ee5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Sat, 22 Feb 2025 00:31:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 22 Feb 2025 00:31:31 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 22 Feb 2025 00:31:31 GMT
ENV DOCKER_VERSION=28.0.0
# Sat, 22 Feb 2025 00:31:32 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.0.zip
# Sat, 22 Feb 2025 00:31:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 22 Feb 2025 00:31:42 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Sat, 22 Feb 2025 00:31:42 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.windows-amd64.exe
# Sat, 22 Feb 2025 00:31:43 GMT
ENV DOCKER_BUILDX_SHA256=ab3eba3acbfa6b6612690af075795254f29762efc8abace5f636b8e7628b1851
# Sat, 22 Feb 2025 00:31:51 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 22 Feb 2025 00:31:52 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Sat, 22 Feb 2025 00:31:53 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-windows-x86_64.exe
# Sat, 22 Feb 2025 00:31:53 GMT
ENV DOCKER_COMPOSE_SHA256=01bce3456228d8e1e4b0ba056f4b9730b7fd2c1a7113c8a985144c0fdee797b0
# Sat, 22 Feb 2025 00:32:02 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Tue, 14 Jan 2025 18:53:06 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b538b630814b004320f0f9ee0a9c3594e03b773b5580fed4105a81f74e7c098f`  
		Last Modified: Sat, 22 Feb 2025 00:32:07 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58e25b87bc1505ec562cf342b28ce02166b0c50e250e5b111cae842bd29224a6`  
		Last Modified: Sat, 22 Feb 2025 00:32:08 GMT  
		Size: 382.4 KB (382390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54dec53b66cd21d806f4ecb36e798d52785171b19a3b94a2886816c4b00fc357`  
		Last Modified: Sat, 22 Feb 2025 00:32:07 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:173311079ab932318629c9bfc59957c46ffef6d9500148722bf57885ab4d912e`  
		Last Modified: Sat, 22 Feb 2025 00:32:07 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5ef5273358e9d6949b1c0c7a006b2fe22a9b45af8454771a753c47f67702fc5`  
		Last Modified: Sat, 22 Feb 2025 00:32:09 GMT  
		Size: 19.8 MB (19841357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6550ae8a0cab9e35d0c0177c6afc594dd1f53008f4c0b85bdca771700fa770c`  
		Last Modified: Sat, 22 Feb 2025 00:32:06 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e430e1223ff0212bf349270e614e999171df037e89b09997ff907efa689e97d`  
		Last Modified: Sat, 22 Feb 2025 00:32:06 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adf1c042512ab6127e6371768343f9e2125e122a97350d29044867620964da29`  
		Last Modified: Sat, 22 Feb 2025 00:32:05 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbcc9f9bc1cf9f00d67c29fcbf84300c45479de6c73cf2f49f1ae660cf73bb07`  
		Last Modified: Sat, 22 Feb 2025 00:32:08 GMT  
		Size: 22.8 MB (22778890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b21becac3572331f658c564c93303ec2f6d01292e600e1b7deab5fea30b05ff6`  
		Last Modified: Sat, 22 Feb 2025 00:32:05 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e856f770850ac4d1cb287a7e7807f001c6f669a135f306ccf2fe6e63129def66`  
		Last Modified: Sat, 22 Feb 2025 00:32:05 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e457e71b003d1ce3d61f1df1c12e7500d728f4b5598604334164ddb533cb2ba`  
		Last Modified: Sat, 22 Feb 2025 00:32:05 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f63f581bda80c595a4087c00b71030e7a4d71012bb05cbc2eb9c139f9679e31`  
		Last Modified: Sat, 22 Feb 2025 00:32:08 GMT  
		Size: 21.9 MB (21925519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28.0-windowsservercore` - windows version 10.0.20348.3207; amd64

```console
$ docker pull docker@sha256:40cac7c487ab96fd2608d22182da86766f98f6f8726e4a9cc87f61fba1c79f0e
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2328776516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a7dc1af03d6c94095c7be69ba1d7ffcba2c6ddbf201a1901bafc1445c1d7615`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Sat, 22 Feb 2025 00:37:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 22 Feb 2025 00:37:49 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 22 Feb 2025 00:37:49 GMT
ENV DOCKER_VERSION=28.0.0
# Sat, 22 Feb 2025 00:37:50 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.0.zip
# Sat, 22 Feb 2025 00:38:01 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 22 Feb 2025 00:38:01 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Sat, 22 Feb 2025 00:38:02 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.windows-amd64.exe
# Sat, 22 Feb 2025 00:38:02 GMT
ENV DOCKER_BUILDX_SHA256=ab3eba3acbfa6b6612690af075795254f29762efc8abace5f636b8e7628b1851
# Sat, 22 Feb 2025 00:38:11 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 22 Feb 2025 00:38:12 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Sat, 22 Feb 2025 00:38:13 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-windows-x86_64.exe
# Sat, 22 Feb 2025 00:38:13 GMT
ENV DOCKER_COMPOSE_SHA256=01bce3456228d8e1e4b0ba056f4b9730b7fd2c1a7113c8a985144c0fdee797b0
# Sat, 22 Feb 2025 00:38:22 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Tue, 11 Feb 2025 18:38:32 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a513c2ebb5aac6eaccc568c460584aa652a09401a4f865e8b1a9870e4f9826d`  
		Last Modified: Sat, 22 Feb 2025 00:38:28 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f0ea743d1a5ae5f5f7088a7c23ca759ec9b363ca46d674d9e7425aa27739ba`  
		Last Modified: Sat, 22 Feb 2025 00:38:27 GMT  
		Size: 389.0 KB (388984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:401dea1d9556118c14843e687f7eb2f2767205cefe7c534ce370103f7bb4520c`  
		Last Modified: Sat, 22 Feb 2025 00:38:27 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ff218fd9efd93054faba12c9de123bd815f47af0057f0822bebe1980b506039`  
		Last Modified: Sat, 22 Feb 2025 00:38:26 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef9e343cb24c4c76e4c3fbbf11fa22c10da7fea8e22f98be5493a15840e79f6`  
		Last Modified: Sat, 22 Feb 2025 00:38:28 GMT  
		Size: 19.8 MB (19832408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b072185e609fe777fbfd0d1c7e0860cfd307e8d0718c19365cbe22f499636207`  
		Last Modified: Sat, 22 Feb 2025 00:38:26 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a89b4e620aaf525ac2545408e3d49037c7d5b8c99ee26edb1937e8a2a5c181c`  
		Last Modified: Sat, 22 Feb 2025 00:38:25 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7edf322adba1ba7c101c710b53b2f04cb139c273b95e29fcc5d8943f581af167`  
		Last Modified: Sat, 22 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c220811a807867c0315d6291b99472e043388fe4f317d60dcb70cf42963b333`  
		Last Modified: Sat, 22 Feb 2025 00:38:27 GMT  
		Size: 22.8 MB (22770286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a73d03430d6958d170ed89b00d83fa15b1b28a9aa22fbd4ae9018b5671cb08f6`  
		Last Modified: Sat, 22 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:164bc468207a3b25ae55b075dc0b5987de3ca0d425be73ff7f45fe57b49f807f`  
		Last Modified: Sat, 22 Feb 2025 00:38:24 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7307712a7f1b1601e8cf9b306574434f960222e78bb80360573ae2829c165ab9`  
		Last Modified: Sat, 22 Feb 2025 00:38:24 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ff623c1936592d4e22a10ac22c1ba99d55a4c960680df6e5e9da20450cf85d`  
		Last Modified: Sat, 22 Feb 2025 00:38:27 GMT  
		Size: 21.9 MB (21914957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28.0-windowsservercore` - windows version 10.0.17763.6893; amd64

```console
$ docker pull docker@sha256:575fd688c3bf866a95546fe93e2564fea753d26e5931ebfc1e32ebd9bc411358
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2201693889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47afabbd0d9bf289e87beda973d92a82859b49c2b2f83325e44032f22df554d7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Sat, 22 Feb 2025 00:36:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 22 Feb 2025 00:37:03 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 22 Feb 2025 00:37:04 GMT
ENV DOCKER_VERSION=28.0.0
# Sat, 22 Feb 2025 00:37:05 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.0.zip
# Sat, 22 Feb 2025 00:37:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 22 Feb 2025 00:37:18 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Sat, 22 Feb 2025 00:37:18 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.windows-amd64.exe
# Sat, 22 Feb 2025 00:37:19 GMT
ENV DOCKER_BUILDX_SHA256=ab3eba3acbfa6b6612690af075795254f29762efc8abace5f636b8e7628b1851
# Sat, 22 Feb 2025 00:37:28 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 22 Feb 2025 00:37:29 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Sat, 22 Feb 2025 00:37:30 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-windows-x86_64.exe
# Sat, 22 Feb 2025 00:37:31 GMT
ENV DOCKER_COMPOSE_SHA256=01bce3456228d8e1e4b0ba056f4b9730b7fd2c1a7113c8a985144c0fdee797b0
# Sat, 22 Feb 2025 00:37:39 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 18:49:50 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d662e474d0eebcc45d26c962c3ea2815d5ad421c4abce3dfca970d20d34206`  
		Last Modified: Sat, 22 Feb 2025 00:37:45 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b80c05d72492cc29e69146de42b5cbab7c6912ef3a85c579caaf8ccb3b7eabb9`  
		Last Modified: Sat, 22 Feb 2025 00:37:44 GMT  
		Size: 343.2 KB (343235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df0623e2321e34b1b589a3f2314cdc767fe978372d17c7d621c1b6e40645f0e2`  
		Last Modified: Sat, 22 Feb 2025 00:37:44 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177b2d1a530b8667811479317d9e8ae2eb9cf1e26892e886e4baa298209fcfa4`  
		Last Modified: Sat, 22 Feb 2025 00:37:44 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3834ee7310198b95517a8b510904c8f38cbdb7c49df0b228572059fee55faa4`  
		Last Modified: Sat, 22 Feb 2025 00:37:46 GMT  
		Size: 19.8 MB (19805126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7d9cad94e2d870741143d557fc15084b8f7f0c3f510618f76861f6c020ec0c`  
		Last Modified: Sat, 22 Feb 2025 00:37:43 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73e623554754f1c6df8e43e93e867af1218d203b9111a1b977befbc4542f33e`  
		Last Modified: Sat, 22 Feb 2025 00:37:43 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39746d0ab1fefcec984bb203b47fb43af6294430288792c106045708180cf90f`  
		Last Modified: Sat, 22 Feb 2025 00:37:43 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb7e0de055ddbb75c2d00fd897c8e623d5d164e9da002c14c5d7b16034ddefb2`  
		Last Modified: Sat, 22 Feb 2025 00:37:45 GMT  
		Size: 22.7 MB (22743044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d103e4264cc2326442d2f2c0d9a6f8a6d63672a9e1888b0eb106211fe4c866a8`  
		Last Modified: Sat, 22 Feb 2025 00:37:42 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e7898abd14f1e9f5aaa3850e26c6e47b5af14ccc7727ace668f06058bb6bbbb`  
		Last Modified: Sat, 22 Feb 2025 00:37:42 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac30b7d53b77634caea695af70ca54fad87eec4119c5d63afcd64b762dadee9f`  
		Last Modified: Sat, 22 Feb 2025 00:37:42 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a13d827d5d10e25d56e691281a38fb310acbe73a53d8ecb6c27a3c737305b83d`  
		Last Modified: Sat, 22 Feb 2025 00:37:44 GMT  
		Size: 21.9 MB (21881997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.0-windowsservercore-1809`

```console
$ docker pull docker@sha256:8b5e611771751fe8360ccf0f5bb3b6c022a079599c9e8dada6351d3682c645b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `docker:28.0-windowsservercore-1809` - windows version 10.0.17763.6893; amd64

```console
$ docker pull docker@sha256:575fd688c3bf866a95546fe93e2564fea753d26e5931ebfc1e32ebd9bc411358
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2201693889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47afabbd0d9bf289e87beda973d92a82859b49c2b2f83325e44032f22df554d7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Sat, 22 Feb 2025 00:36:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 22 Feb 2025 00:37:03 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 22 Feb 2025 00:37:04 GMT
ENV DOCKER_VERSION=28.0.0
# Sat, 22 Feb 2025 00:37:05 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.0.zip
# Sat, 22 Feb 2025 00:37:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 22 Feb 2025 00:37:18 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Sat, 22 Feb 2025 00:37:18 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.windows-amd64.exe
# Sat, 22 Feb 2025 00:37:19 GMT
ENV DOCKER_BUILDX_SHA256=ab3eba3acbfa6b6612690af075795254f29762efc8abace5f636b8e7628b1851
# Sat, 22 Feb 2025 00:37:28 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 22 Feb 2025 00:37:29 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Sat, 22 Feb 2025 00:37:30 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-windows-x86_64.exe
# Sat, 22 Feb 2025 00:37:31 GMT
ENV DOCKER_COMPOSE_SHA256=01bce3456228d8e1e4b0ba056f4b9730b7fd2c1a7113c8a985144c0fdee797b0
# Sat, 22 Feb 2025 00:37:39 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 18:49:50 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d662e474d0eebcc45d26c962c3ea2815d5ad421c4abce3dfca970d20d34206`  
		Last Modified: Sat, 22 Feb 2025 00:37:45 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b80c05d72492cc29e69146de42b5cbab7c6912ef3a85c579caaf8ccb3b7eabb9`  
		Last Modified: Sat, 22 Feb 2025 00:37:44 GMT  
		Size: 343.2 KB (343235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df0623e2321e34b1b589a3f2314cdc767fe978372d17c7d621c1b6e40645f0e2`  
		Last Modified: Sat, 22 Feb 2025 00:37:44 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177b2d1a530b8667811479317d9e8ae2eb9cf1e26892e886e4baa298209fcfa4`  
		Last Modified: Sat, 22 Feb 2025 00:37:44 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3834ee7310198b95517a8b510904c8f38cbdb7c49df0b228572059fee55faa4`  
		Last Modified: Sat, 22 Feb 2025 00:37:46 GMT  
		Size: 19.8 MB (19805126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7d9cad94e2d870741143d557fc15084b8f7f0c3f510618f76861f6c020ec0c`  
		Last Modified: Sat, 22 Feb 2025 00:37:43 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73e623554754f1c6df8e43e93e867af1218d203b9111a1b977befbc4542f33e`  
		Last Modified: Sat, 22 Feb 2025 00:37:43 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39746d0ab1fefcec984bb203b47fb43af6294430288792c106045708180cf90f`  
		Last Modified: Sat, 22 Feb 2025 00:37:43 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb7e0de055ddbb75c2d00fd897c8e623d5d164e9da002c14c5d7b16034ddefb2`  
		Last Modified: Sat, 22 Feb 2025 00:37:45 GMT  
		Size: 22.7 MB (22743044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d103e4264cc2326442d2f2c0d9a6f8a6d63672a9e1888b0eb106211fe4c866a8`  
		Last Modified: Sat, 22 Feb 2025 00:37:42 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e7898abd14f1e9f5aaa3850e26c6e47b5af14ccc7727ace668f06058bb6bbbb`  
		Last Modified: Sat, 22 Feb 2025 00:37:42 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac30b7d53b77634caea695af70ca54fad87eec4119c5d63afcd64b762dadee9f`  
		Last Modified: Sat, 22 Feb 2025 00:37:42 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a13d827d5d10e25d56e691281a38fb310acbe73a53d8ecb6c27a3c737305b83d`  
		Last Modified: Sat, 22 Feb 2025 00:37:44 GMT  
		Size: 21.9 MB (21881997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.0-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:4a4531319a3d77d264dd66e0056a37a0ce12653a767680d3114dc86e6d50de94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3207; amd64

### `docker:28.0-windowsservercore-ltsc2022` - windows version 10.0.20348.3207; amd64

```console
$ docker pull docker@sha256:40cac7c487ab96fd2608d22182da86766f98f6f8726e4a9cc87f61fba1c79f0e
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2328776516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a7dc1af03d6c94095c7be69ba1d7ffcba2c6ddbf201a1901bafc1445c1d7615`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Sat, 22 Feb 2025 00:37:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 22 Feb 2025 00:37:49 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 22 Feb 2025 00:37:49 GMT
ENV DOCKER_VERSION=28.0.0
# Sat, 22 Feb 2025 00:37:50 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.0.zip
# Sat, 22 Feb 2025 00:38:01 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 22 Feb 2025 00:38:01 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Sat, 22 Feb 2025 00:38:02 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.windows-amd64.exe
# Sat, 22 Feb 2025 00:38:02 GMT
ENV DOCKER_BUILDX_SHA256=ab3eba3acbfa6b6612690af075795254f29762efc8abace5f636b8e7628b1851
# Sat, 22 Feb 2025 00:38:11 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 22 Feb 2025 00:38:12 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Sat, 22 Feb 2025 00:38:13 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-windows-x86_64.exe
# Sat, 22 Feb 2025 00:38:13 GMT
ENV DOCKER_COMPOSE_SHA256=01bce3456228d8e1e4b0ba056f4b9730b7fd2c1a7113c8a985144c0fdee797b0
# Sat, 22 Feb 2025 00:38:22 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Tue, 11 Feb 2025 18:38:32 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a513c2ebb5aac6eaccc568c460584aa652a09401a4f865e8b1a9870e4f9826d`  
		Last Modified: Sat, 22 Feb 2025 00:38:28 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f0ea743d1a5ae5f5f7088a7c23ca759ec9b363ca46d674d9e7425aa27739ba`  
		Last Modified: Sat, 22 Feb 2025 00:38:27 GMT  
		Size: 389.0 KB (388984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:401dea1d9556118c14843e687f7eb2f2767205cefe7c534ce370103f7bb4520c`  
		Last Modified: Sat, 22 Feb 2025 00:38:27 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ff218fd9efd93054faba12c9de123bd815f47af0057f0822bebe1980b506039`  
		Last Modified: Sat, 22 Feb 2025 00:38:26 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef9e343cb24c4c76e4c3fbbf11fa22c10da7fea8e22f98be5493a15840e79f6`  
		Last Modified: Sat, 22 Feb 2025 00:38:28 GMT  
		Size: 19.8 MB (19832408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b072185e609fe777fbfd0d1c7e0860cfd307e8d0718c19365cbe22f499636207`  
		Last Modified: Sat, 22 Feb 2025 00:38:26 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a89b4e620aaf525ac2545408e3d49037c7d5b8c99ee26edb1937e8a2a5c181c`  
		Last Modified: Sat, 22 Feb 2025 00:38:25 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7edf322adba1ba7c101c710b53b2f04cb139c273b95e29fcc5d8943f581af167`  
		Last Modified: Sat, 22 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c220811a807867c0315d6291b99472e043388fe4f317d60dcb70cf42963b333`  
		Last Modified: Sat, 22 Feb 2025 00:38:27 GMT  
		Size: 22.8 MB (22770286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a73d03430d6958d170ed89b00d83fa15b1b28a9aa22fbd4ae9018b5671cb08f6`  
		Last Modified: Sat, 22 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:164bc468207a3b25ae55b075dc0b5987de3ca0d425be73ff7f45fe57b49f807f`  
		Last Modified: Sat, 22 Feb 2025 00:38:24 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7307712a7f1b1601e8cf9b306574434f960222e78bb80360573ae2829c165ab9`  
		Last Modified: Sat, 22 Feb 2025 00:38:24 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ff623c1936592d4e22a10ac22c1ba99d55a4c960680df6e5e9da20450cf85d`  
		Last Modified: Sat, 22 Feb 2025 00:38:27 GMT  
		Size: 21.9 MB (21914957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.0-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:78307f6a713fd34f43a0d89127421c46b2ff65f06362768394f4e6612dc89989
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.2894; amd64

### `docker:28.0-windowsservercore-ltsc2025` - windows version 10.0.26100.2894; amd64

```console
$ docker pull docker@sha256:13348bcc4ed6fcd578c6aea25afa087bac0759457ff724c916d2fb3624c804ba
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2565217611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:172682bc22fc40249839b093831f2ccdb06d47eda95530dd64db1bf9bba03ee5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Sat, 22 Feb 2025 00:31:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 22 Feb 2025 00:31:31 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 22 Feb 2025 00:31:31 GMT
ENV DOCKER_VERSION=28.0.0
# Sat, 22 Feb 2025 00:31:32 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.0.zip
# Sat, 22 Feb 2025 00:31:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 22 Feb 2025 00:31:42 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Sat, 22 Feb 2025 00:31:42 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.windows-amd64.exe
# Sat, 22 Feb 2025 00:31:43 GMT
ENV DOCKER_BUILDX_SHA256=ab3eba3acbfa6b6612690af075795254f29762efc8abace5f636b8e7628b1851
# Sat, 22 Feb 2025 00:31:51 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 22 Feb 2025 00:31:52 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Sat, 22 Feb 2025 00:31:53 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-windows-x86_64.exe
# Sat, 22 Feb 2025 00:31:53 GMT
ENV DOCKER_COMPOSE_SHA256=01bce3456228d8e1e4b0ba056f4b9730b7fd2c1a7113c8a985144c0fdee797b0
# Sat, 22 Feb 2025 00:32:02 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Tue, 14 Jan 2025 18:53:06 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b538b630814b004320f0f9ee0a9c3594e03b773b5580fed4105a81f74e7c098f`  
		Last Modified: Sat, 22 Feb 2025 00:32:07 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58e25b87bc1505ec562cf342b28ce02166b0c50e250e5b111cae842bd29224a6`  
		Last Modified: Sat, 22 Feb 2025 00:32:08 GMT  
		Size: 382.4 KB (382390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54dec53b66cd21d806f4ecb36e798d52785171b19a3b94a2886816c4b00fc357`  
		Last Modified: Sat, 22 Feb 2025 00:32:07 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:173311079ab932318629c9bfc59957c46ffef6d9500148722bf57885ab4d912e`  
		Last Modified: Sat, 22 Feb 2025 00:32:07 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5ef5273358e9d6949b1c0c7a006b2fe22a9b45af8454771a753c47f67702fc5`  
		Last Modified: Sat, 22 Feb 2025 00:32:09 GMT  
		Size: 19.8 MB (19841357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6550ae8a0cab9e35d0c0177c6afc594dd1f53008f4c0b85bdca771700fa770c`  
		Last Modified: Sat, 22 Feb 2025 00:32:06 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e430e1223ff0212bf349270e614e999171df037e89b09997ff907efa689e97d`  
		Last Modified: Sat, 22 Feb 2025 00:32:06 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adf1c042512ab6127e6371768343f9e2125e122a97350d29044867620964da29`  
		Last Modified: Sat, 22 Feb 2025 00:32:05 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbcc9f9bc1cf9f00d67c29fcbf84300c45479de6c73cf2f49f1ae660cf73bb07`  
		Last Modified: Sat, 22 Feb 2025 00:32:08 GMT  
		Size: 22.8 MB (22778890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b21becac3572331f658c564c93303ec2f6d01292e600e1b7deab5fea30b05ff6`  
		Last Modified: Sat, 22 Feb 2025 00:32:05 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e856f770850ac4d1cb287a7e7807f001c6f669a135f306ccf2fe6e63129def66`  
		Last Modified: Sat, 22 Feb 2025 00:32:05 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e457e71b003d1ce3d61f1df1c12e7500d728f4b5598604334164ddb533cb2ba`  
		Last Modified: Sat, 22 Feb 2025 00:32:05 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f63f581bda80c595a4087c00b71030e7a4d71012bb05cbc2eb9c139f9679e31`  
		Last Modified: Sat, 22 Feb 2025 00:32:08 GMT  
		Size: 21.9 MB (21925519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.0.0`

```console
$ docker pull docker@sha256:0a9c58ebc9f86e5af35e4330f6c738dc64fce3ca2e2574b5becdfb88765b308b
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

### `docker:28.0.0` - linux; amd64

```console
$ docker pull docker@sha256:32c276e9aafff90ea7765271afa524c293c9749e880748217b1abedd04af39a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.0 MB (141006353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1da86d0da980dad6c82075b9859478027165e57dba77994a2fe1fa99ed408f3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_VERSION=28.0.0
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-amd64'; 			sha256='7f355525bfaf411302570b705118181b720f18071f4be3f0eaac7b2297d826e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v6'; 			sha256='f841251fd67646e8b6bb4c7e0c2c385f6a1dc7403f5ac6ee7b07c96f0815f7f3'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v7'; 			sha256='81d7040e90e9b69cb0378778f673e1fc2a24ef6dbd47931dc83ab6472fc5809d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm64'; 			sha256='42d5cee287ec7426de5252276a05f3ea565ac2d65d62d052b885a84dd54152d5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-ppc64le'; 			sha256='6a4e6a243f83d80cd46c939f327b2e14cfddd2c6690651cf48d0e208c3345b88'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-riscv64'; 			sha256='eae82aec74a420c3d1734123e6a3bc10b3a2a981aa1d538502373e31c91bf76e'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-s390x'; 			sha256='97b112b3366a471cc375e0f881d65a9a7b07f0962f308834c37f5c3fa75aad08'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 20 Feb 2025 06:04:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD ["sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
VOLUME [/var/lib/docker]
# Thu, 20 Feb 2025 06:04:43 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD []
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fddc498219722db61fe7f7e06295aa8b64f7e48d19d0339176689ea591eea4ca`  
		Last Modified: Sat, 22 Feb 2025 00:27:26 GMT  
		Size: 8.1 MB (8062985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c17b75175e66b76074511db7ebd5bdc56ac19ba269d30e4f58ba4812816ad4`  
		Last Modified: Sat, 22 Feb 2025 00:27:26 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987b6d8519d32209785b3840639a10aa6247ff1e290a651ebcca3d8c33e23dd2`  
		Last Modified: Sat, 22 Feb 2025 00:27:27 GMT  
		Size: 19.5 MB (19492233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7677267af1ddfc39dbdf35dcdca7c20328e83a42b64595f0d5880c62e99a91f`  
		Last Modified: Sat, 22 Feb 2025 00:27:27 GMT  
		Size: 21.8 MB (21829139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9fa9f5140fd1401e5edaa2de6f975bd14f0b79efbafbe0d2497ea0213ecd260`  
		Last Modified: Sat, 22 Feb 2025 00:27:27 GMT  
		Size: 21.0 MB (20958635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124bcf7a51a8a140479ebb1cfd0aea5bf38223d37b7c6ae1deb93bbb1abc0469`  
		Last Modified: Sat, 22 Feb 2025 00:27:28 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3083b3dfd2242fbeb7b498bb2e0d99d55c8e34cad7396573784aa86db3c69355`  
		Last Modified: Sat, 22 Feb 2025 00:27:28 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b255e6bd488c8fb61ba962afb512c02077ecc7e41b50991cb3229aaa7ae94b`  
		Last Modified: Sat, 22 Feb 2025 00:27:28 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42458739bc4b2677f265360a10a2eacffd5133b0242dd313ba8a3dac7a116c4`  
		Last Modified: Sat, 22 Feb 2025 01:08:23 GMT  
		Size: 6.7 MB (6733003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5a7650793a22cfeac45c6610fe2cd3ccd26b6795d33ee5389d66a174c05a65`  
		Last Modified: Sat, 22 Feb 2025 01:08:23 GMT  
		Size: 90.3 KB (90318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03749f129a866bd1cf2e2797db758f883cf177f3cd33ff3c60924ec811728b4f`  
		Last Modified: Sat, 22 Feb 2025 01:08:23 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:769e1c97b1855704d1f74c39b30c2d2bbc890339752b2be542477e64d2529c32`  
		Last Modified: Sat, 22 Feb 2025 01:08:24 GMT  
		Size: 60.2 MB (60189735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e450e39e6d5b103505878dd35ff532dcdfef40450540495b6a666e7bc34e2587`  
		Last Modified: Sat, 22 Feb 2025 01:08:23 GMT  
		Size: 1.6 KB (1637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254862f49c6f0929e44b00f9635661aff98a508d2dc321d6ddc2944f60ac90bb`  
		Last Modified: Sat, 22 Feb 2025 01:08:23 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.0` - unknown; unknown

```console
$ docker pull docker@sha256:ba9368fe1da752bf14bb9ed738b656214abfea5e16cb949f4883beeb86cf9408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:658bfc3f8051aceaf851bbf4fdcff3b32c7f8c853b5262abd646f57fbf14bb10`

```dockerfile
```

-	Layers:
	-	`sha256:670c6ce494a80447b9f682d0ac427af5be54978f5f629221274a481ecf2be95e`  
		Last Modified: Sat, 22 Feb 2025 01:08:22 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.0` - linux; arm variant v6

```console
$ docker pull docker@sha256:346b1790ac4379efe1ff83735d9d72ded98e8ebcc776f29f190a50d1086d5c63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.7 MB (131676535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e2b568d33d9f4d9da33be6f6a26a6e533f58d6d874c445c67494a71fe99ce8c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_VERSION=28.0.0
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-amd64'; 			sha256='7f355525bfaf411302570b705118181b720f18071f4be3f0eaac7b2297d826e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v6'; 			sha256='f841251fd67646e8b6bb4c7e0c2c385f6a1dc7403f5ac6ee7b07c96f0815f7f3'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v7'; 			sha256='81d7040e90e9b69cb0378778f673e1fc2a24ef6dbd47931dc83ab6472fc5809d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm64'; 			sha256='42d5cee287ec7426de5252276a05f3ea565ac2d65d62d052b885a84dd54152d5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-ppc64le'; 			sha256='6a4e6a243f83d80cd46c939f327b2e14cfddd2c6690651cf48d0e208c3345b88'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-riscv64'; 			sha256='eae82aec74a420c3d1734123e6a3bc10b3a2a981aa1d538502373e31c91bf76e'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-s390x'; 			sha256='97b112b3366a471cc375e0f881d65a9a7b07f0962f308834c37f5c3fa75aad08'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 20 Feb 2025 06:04:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD ["sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
VOLUME [/var/lib/docker]
# Thu, 20 Feb 2025 06:04:43 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD []
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e40b3641449ca47aef50c48f620eb6d3a3bc2292e5cf4ea267f5f03e6c7bc`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 8.0 MB (7978133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df16922f358c97f513c6d0b9457abb36aefc588e45374edd23692381878a7`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21eb60c27f71135d16125d7dcf87a6c0a49fc39428a0a7ecbc83c6bc1087efa9`  
		Last Modified: Thu, 20 Feb 2025 23:28:03 GMT  
		Size: 17.5 MB (17453851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b3b7abf60d98565d245e7aab34cfdec0b3c2c8ff503fb00ebceed21f636a93`  
		Last Modified: Sat, 22 Feb 2025 00:28:48 GMT  
		Size: 20.4 MB (20432003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ced3aebdded979735885d70afdbc8a5f03be15205f1145cd3b2af469eb21175`  
		Last Modified: Sat, 22 Feb 2025 00:28:48 GMT  
		Size: 19.7 MB (19725892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f8d07fba646c3b5ac2a07d053675df2a0422b36b698a824d345ee2447bc8e1`  
		Last Modified: Sat, 22 Feb 2025 00:28:47 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c51a22c8e8f3b4205fde47fd17f66895fad1496f33f46bb6aebdf5938bb94ad`  
		Last Modified: Sat, 22 Feb 2025 00:28:47 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f36ff703ab2a5ebeeeb26f374c59106eb92bf26531f572228024531dcc975f64`  
		Last Modified: Sat, 22 Feb 2025 00:28:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2440995b1488c0fccd4c0a9b3062c58a33404bcc3ca3e8289ae64b6393946c65`  
		Last Modified: Sat, 22 Feb 2025 01:29:31 GMT  
		Size: 7.0 MB (7036904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cce93707f7a9fed88581b5b8e8f49a184ba206f961aae653eef08af3b94987b1`  
		Last Modified: Sat, 22 Feb 2025 01:29:30 GMT  
		Size: 89.8 KB (89849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26cf971d434da3f52513e2595da034274a6fb8c1ef74cddc815339506b7b704a`  
		Last Modified: Sat, 22 Feb 2025 01:29:30 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c3188476c3d7ba720f96be3cdceb222b9a7a6e0693a917966988332f14e8ef`  
		Last Modified: Sat, 22 Feb 2025 01:29:33 GMT  
		Size: 55.6 MB (55587101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c9e4329aff590ce10c6d6613452bf70f9708c4817750614d9a1a68918444a6`  
		Last Modified: Sat, 22 Feb 2025 01:29:31 GMT  
		Size: 1.6 KB (1638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ff2444afd5e703729aeef9ead8d60b8f059c8e5f0b4b82853f021d0f2c24504`  
		Last Modified: Sat, 22 Feb 2025 01:29:31 GMT  
		Size: 3.3 KB (3263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.0` - unknown; unknown

```console
$ docker pull docker@sha256:0931cacdc5870a73bd56837c9590fb9801af1b229cbf7ee86dc79c932a51323c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d14b9f57c5e9b67b594f4172c7cfbb95e2442a040e0bb090b09cc95ce2d35a18`

```dockerfile
```

-	Layers:
	-	`sha256:93150d2f1d44b19b0d6d36517e86cddc39cd49f0857f41bdb86a200f7db357e6`  
		Last Modified: Sat, 22 Feb 2025 01:29:30 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.0` - linux; arm variant v7

```console
$ docker pull docker@sha256:089424d7adbb66df8dd78e5ce27d9bd9d13cebe072cb5eb79e7478f00c124163
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (130009843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da65fa603f2dc74e8750fbdc3d7173e607ca901a8dfb81fab1136584884d3018`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_VERSION=28.0.0
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-amd64'; 			sha256='7f355525bfaf411302570b705118181b720f18071f4be3f0eaac7b2297d826e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v6'; 			sha256='f841251fd67646e8b6bb4c7e0c2c385f6a1dc7403f5ac6ee7b07c96f0815f7f3'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v7'; 			sha256='81d7040e90e9b69cb0378778f673e1fc2a24ef6dbd47931dc83ab6472fc5809d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm64'; 			sha256='42d5cee287ec7426de5252276a05f3ea565ac2d65d62d052b885a84dd54152d5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-ppc64le'; 			sha256='6a4e6a243f83d80cd46c939f327b2e14cfddd2c6690651cf48d0e208c3345b88'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-riscv64'; 			sha256='eae82aec74a420c3d1734123e6a3bc10b3a2a981aa1d538502373e31c91bf76e'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-s390x'; 			sha256='97b112b3366a471cc375e0f881d65a9a7b07f0962f308834c37f5c3fa75aad08'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 20 Feb 2025 06:04:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD ["sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
VOLUME [/var/lib/docker]
# Thu, 20 Feb 2025 06:04:43 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD []
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b654458a637c48c7f8f46da325ae8f810828e851ed4ab4b406092503eb680f`  
		Last Modified: Sat, 22 Feb 2025 00:28:04 GMT  
		Size: 7.3 MB (7299375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3474560bdd0e71f5972a48abd9e80877e2219f6eacae8272034d8503bcb634b2`  
		Last Modified: Sat, 22 Feb 2025 00:28:03 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ffc820c153872520700f2618e71ee9bea9cfee69fbff7b0ea4acb751a2fee5`  
		Last Modified: Sat, 22 Feb 2025 00:28:04 GMT  
		Size: 17.4 MB (17444426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a39a48e6818f4f7d6e7637cf221cc02da7b2e8ab3ca2643a527024430497175`  
		Last Modified: Sat, 22 Feb 2025 00:28:04 GMT  
		Size: 20.4 MB (20411656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168ce845c02246501347d9ae0d1bb9bb9f55a707c5ef03ba3bb6377e832c28f4`  
		Last Modified: Sat, 22 Feb 2025 00:28:05 GMT  
		Size: 19.7 MB (19708525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d62f1159ab01591fa3510e1ddc7b7e0313d001750472b1eaa0dcfb3a1f097732`  
		Last Modified: Sat, 22 Feb 2025 00:28:05 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ab9b1b4b0f9c261b260d739cd6d593a2c510b9c29045d72d930f2baf5fa78e`  
		Last Modified: Sat, 22 Feb 2025 00:28:05 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d27509dd9fc9bdb19051b5661dce75fc9b53979841bcd49fd03667b1ad6dde`  
		Last Modified: Sat, 22 Feb 2025 00:28:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd0d2a57f389ccbd627e0bca3b813e9397f4a6a55364b1f7cf22df043542cf1a`  
		Last Modified: Sat, 22 Feb 2025 04:54:52 GMT  
		Size: 6.4 MB (6366292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5947e3cbc6a2eb4d8c4ec17605876ea3e3a5cb2c09abac0a58d53cc4d6569f7`  
		Last Modified: Sat, 22 Feb 2025 04:54:51 GMT  
		Size: 86.3 KB (86342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc1fa6b8e4e654268e5dfc6afa5b1e88bfb92da3c33018f231f76ad7e08a59e`  
		Last Modified: Sat, 22 Feb 2025 04:54:51 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f544c5574adf21ca185480beea8b120134f2ed74f3f2418dc0ef564a3891490`  
		Last Modified: Sat, 22 Feb 2025 04:54:53 GMT  
		Size: 55.6 MB (55587054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd1c8be29e89fc14e8cd0778dcda3dae4c641d9ab956b2f9ce8d02df1d7984e`  
		Last Modified: Sat, 22 Feb 2025 04:54:52 GMT  
		Size: 1.6 KB (1636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db5e7511235a55ebe7a92c8825189d27a2b1d951e0f25d22e4e932636abbd466`  
		Last Modified: Sat, 22 Feb 2025 04:54:52 GMT  
		Size: 3.3 KB (3256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.0` - unknown; unknown

```console
$ docker pull docker@sha256:1cdaa27022a39a251e498044fefc2f4160913794dc50a3074935741e0d39d28b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:643a439611cab3be1c6fde6e85ec369c205d94c81b88f1c91a627a32a6448b32`

```dockerfile
```

-	Layers:
	-	`sha256:fa998948cfd33a55b2120a90b998117bea32698c81f84e340fc1f9fa359825c4`  
		Last Modified: Sat, 22 Feb 2025 04:54:51 GMT  
		Size: 34.8 KB (34765 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.0` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:af92e15294f197a3cc4de0e75e012f4e91a996e4fd58ad96e163208aea7f0be3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.4 MB (132399422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89d922b5c31bca4bc340632485ab5243809aaf557e7aaf377fd956c15f4ad0a6`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_VERSION=28.0.0
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-amd64'; 			sha256='7f355525bfaf411302570b705118181b720f18071f4be3f0eaac7b2297d826e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v6'; 			sha256='f841251fd67646e8b6bb4c7e0c2c385f6a1dc7403f5ac6ee7b07c96f0815f7f3'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v7'; 			sha256='81d7040e90e9b69cb0378778f673e1fc2a24ef6dbd47931dc83ab6472fc5809d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm64'; 			sha256='42d5cee287ec7426de5252276a05f3ea565ac2d65d62d052b885a84dd54152d5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-ppc64le'; 			sha256='6a4e6a243f83d80cd46c939f327b2e14cfddd2c6690651cf48d0e208c3345b88'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-riscv64'; 			sha256='eae82aec74a420c3d1734123e6a3bc10b3a2a981aa1d538502373e31c91bf76e'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-s390x'; 			sha256='97b112b3366a471cc375e0f881d65a9a7b07f0962f308834c37f5c3fa75aad08'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 20 Feb 2025 06:04:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD ["sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
VOLUME [/var/lib/docker]
# Thu, 20 Feb 2025 06:04:43 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD []
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:076f26e7389ad2e79a31e03589b2c6943495faa94ce7fc6ecd800dd0c320c71e`  
		Last Modified: Sat, 22 Feb 2025 00:28:38 GMT  
		Size: 8.1 MB (8076430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54483e7ea72052e991e704ef33b6d45d32f2c9886445d70ae79e50a2dd444147`  
		Last Modified: Sat, 22 Feb 2025 00:28:37 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d747fdfb37d0ca59992c4852cab088ffb4549e3f8ef7632b252452c1c12c7989`  
		Last Modified: Sat, 22 Feb 2025 00:28:38 GMT  
		Size: 18.4 MB (18412791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84912acd39dd03fae2cffdb073ec52df5d17e2700910653a8c844d31a916a7eb`  
		Last Modified: Sat, 22 Feb 2025 00:28:39 GMT  
		Size: 20.0 MB (20041446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49191a7f2e90fd89997d49d48799f225e27d4d811c1ab6a1a5ed18c8b5a9f94`  
		Last Modified: Sat, 22 Feb 2025 00:28:40 GMT  
		Size: 19.2 MB (19222674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7debd3993d0af81423e3290841931e4b162ff882877ebb292b10f3dde6dc5694`  
		Last Modified: Sat, 22 Feb 2025 00:28:39 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855282ceddcfc470897f6e2cb33f2ad4742db7c00f24a0386714c91a31a090fa`  
		Last Modified: Sat, 22 Feb 2025 00:28:40 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fbaf9714c72f8c1c56eb53405de18b5c63f82fcfa89814a71a92c9844e1fb8b`  
		Last Modified: Sat, 22 Feb 2025 00:28:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f1efb7aef297fc62aaca013f0102b13d4fb2bd1eb6e39c858c91c440c973f87`  
		Last Modified: Sat, 22 Feb 2025 02:46:00 GMT  
		Size: 7.0 MB (6978850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d301065fd8bf09964f1efc59488efd3c692d574aae6e2460fefc3dac799912b`  
		Last Modified: Sat, 22 Feb 2025 02:46:00 GMT  
		Size: 99.4 KB (99390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d33e0f749652bb606f1e92e433cb70fa6c8e7a30737050979d975e9f06a132f`  
		Last Modified: Sat, 22 Feb 2025 02:45:59 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a409b11008465c3cb7523e669b4d2a064619125185de982089bf11944cf62502`  
		Last Modified: Sat, 22 Feb 2025 02:46:01 GMT  
		Size: 55.6 MB (55566753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff8cdce63f040e68fff768b8a75d7ebdd3f4cd4e69ed0f85ae0ad620baa9c40`  
		Last Modified: Sat, 22 Feb 2025 02:46:00 GMT  
		Size: 1.6 KB (1636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f72a632b800deed0be1fc7ec78852db28106ae059a841b87a966fed6ec7255f`  
		Last Modified: Sat, 22 Feb 2025 02:46:01 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.0` - unknown; unknown

```console
$ docker pull docker@sha256:d6dd49a97960eaef409aa41f89cf8596c02281b55801b3f726b267761031bc90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4105199c766800ff78dca393a5dccdb1435364291ecf731c31deacb4fa6e86a4`

```dockerfile
```

-	Layers:
	-	`sha256:2f7e554767be7baf2d46a3652bbe4405cdcb83972440eb83c19280ab0e991188`  
		Last Modified: Sat, 22 Feb 2025 02:45:59 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.0.0-alpine3.21`

```console
$ docker pull docker@sha256:0a9c58ebc9f86e5af35e4330f6c738dc64fce3ca2e2574b5becdfb88765b308b
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

### `docker:28.0.0-alpine3.21` - linux; amd64

```console
$ docker pull docker@sha256:32c276e9aafff90ea7765271afa524c293c9749e880748217b1abedd04af39a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.0 MB (141006353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1da86d0da980dad6c82075b9859478027165e57dba77994a2fe1fa99ed408f3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_VERSION=28.0.0
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-amd64'; 			sha256='7f355525bfaf411302570b705118181b720f18071f4be3f0eaac7b2297d826e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v6'; 			sha256='f841251fd67646e8b6bb4c7e0c2c385f6a1dc7403f5ac6ee7b07c96f0815f7f3'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v7'; 			sha256='81d7040e90e9b69cb0378778f673e1fc2a24ef6dbd47931dc83ab6472fc5809d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm64'; 			sha256='42d5cee287ec7426de5252276a05f3ea565ac2d65d62d052b885a84dd54152d5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-ppc64le'; 			sha256='6a4e6a243f83d80cd46c939f327b2e14cfddd2c6690651cf48d0e208c3345b88'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-riscv64'; 			sha256='eae82aec74a420c3d1734123e6a3bc10b3a2a981aa1d538502373e31c91bf76e'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-s390x'; 			sha256='97b112b3366a471cc375e0f881d65a9a7b07f0962f308834c37f5c3fa75aad08'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 20 Feb 2025 06:04:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD ["sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
VOLUME [/var/lib/docker]
# Thu, 20 Feb 2025 06:04:43 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD []
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fddc498219722db61fe7f7e06295aa8b64f7e48d19d0339176689ea591eea4ca`  
		Last Modified: Sat, 22 Feb 2025 00:27:26 GMT  
		Size: 8.1 MB (8062985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c17b75175e66b76074511db7ebd5bdc56ac19ba269d30e4f58ba4812816ad4`  
		Last Modified: Sat, 22 Feb 2025 00:27:26 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987b6d8519d32209785b3840639a10aa6247ff1e290a651ebcca3d8c33e23dd2`  
		Last Modified: Sat, 22 Feb 2025 00:27:27 GMT  
		Size: 19.5 MB (19492233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7677267af1ddfc39dbdf35dcdca7c20328e83a42b64595f0d5880c62e99a91f`  
		Last Modified: Sat, 22 Feb 2025 00:27:27 GMT  
		Size: 21.8 MB (21829139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9fa9f5140fd1401e5edaa2de6f975bd14f0b79efbafbe0d2497ea0213ecd260`  
		Last Modified: Sat, 22 Feb 2025 00:27:27 GMT  
		Size: 21.0 MB (20958635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124bcf7a51a8a140479ebb1cfd0aea5bf38223d37b7c6ae1deb93bbb1abc0469`  
		Last Modified: Sat, 22 Feb 2025 00:27:28 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3083b3dfd2242fbeb7b498bb2e0d99d55c8e34cad7396573784aa86db3c69355`  
		Last Modified: Sat, 22 Feb 2025 00:27:28 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b255e6bd488c8fb61ba962afb512c02077ecc7e41b50991cb3229aaa7ae94b`  
		Last Modified: Sat, 22 Feb 2025 00:27:28 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42458739bc4b2677f265360a10a2eacffd5133b0242dd313ba8a3dac7a116c4`  
		Last Modified: Sat, 22 Feb 2025 01:08:23 GMT  
		Size: 6.7 MB (6733003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5a7650793a22cfeac45c6610fe2cd3ccd26b6795d33ee5389d66a174c05a65`  
		Last Modified: Sat, 22 Feb 2025 01:08:23 GMT  
		Size: 90.3 KB (90318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03749f129a866bd1cf2e2797db758f883cf177f3cd33ff3c60924ec811728b4f`  
		Last Modified: Sat, 22 Feb 2025 01:08:23 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:769e1c97b1855704d1f74c39b30c2d2bbc890339752b2be542477e64d2529c32`  
		Last Modified: Sat, 22 Feb 2025 01:08:24 GMT  
		Size: 60.2 MB (60189735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e450e39e6d5b103505878dd35ff532dcdfef40450540495b6a666e7bc34e2587`  
		Last Modified: Sat, 22 Feb 2025 01:08:23 GMT  
		Size: 1.6 KB (1637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254862f49c6f0929e44b00f9635661aff98a508d2dc321d6ddc2944f60ac90bb`  
		Last Modified: Sat, 22 Feb 2025 01:08:23 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.0-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:ba9368fe1da752bf14bb9ed738b656214abfea5e16cb949f4883beeb86cf9408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:658bfc3f8051aceaf851bbf4fdcff3b32c7f8c853b5262abd646f57fbf14bb10`

```dockerfile
```

-	Layers:
	-	`sha256:670c6ce494a80447b9f682d0ac427af5be54978f5f629221274a481ecf2be95e`  
		Last Modified: Sat, 22 Feb 2025 01:08:22 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.0-alpine3.21` - linux; arm variant v6

```console
$ docker pull docker@sha256:346b1790ac4379efe1ff83735d9d72ded98e8ebcc776f29f190a50d1086d5c63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.7 MB (131676535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e2b568d33d9f4d9da33be6f6a26a6e533f58d6d874c445c67494a71fe99ce8c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_VERSION=28.0.0
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-amd64'; 			sha256='7f355525bfaf411302570b705118181b720f18071f4be3f0eaac7b2297d826e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v6'; 			sha256='f841251fd67646e8b6bb4c7e0c2c385f6a1dc7403f5ac6ee7b07c96f0815f7f3'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v7'; 			sha256='81d7040e90e9b69cb0378778f673e1fc2a24ef6dbd47931dc83ab6472fc5809d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm64'; 			sha256='42d5cee287ec7426de5252276a05f3ea565ac2d65d62d052b885a84dd54152d5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-ppc64le'; 			sha256='6a4e6a243f83d80cd46c939f327b2e14cfddd2c6690651cf48d0e208c3345b88'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-riscv64'; 			sha256='eae82aec74a420c3d1734123e6a3bc10b3a2a981aa1d538502373e31c91bf76e'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-s390x'; 			sha256='97b112b3366a471cc375e0f881d65a9a7b07f0962f308834c37f5c3fa75aad08'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 20 Feb 2025 06:04:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD ["sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
VOLUME [/var/lib/docker]
# Thu, 20 Feb 2025 06:04:43 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD []
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e40b3641449ca47aef50c48f620eb6d3a3bc2292e5cf4ea267f5f03e6c7bc`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 8.0 MB (7978133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df16922f358c97f513c6d0b9457abb36aefc588e45374edd23692381878a7`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21eb60c27f71135d16125d7dcf87a6c0a49fc39428a0a7ecbc83c6bc1087efa9`  
		Last Modified: Thu, 20 Feb 2025 23:28:03 GMT  
		Size: 17.5 MB (17453851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b3b7abf60d98565d245e7aab34cfdec0b3c2c8ff503fb00ebceed21f636a93`  
		Last Modified: Sat, 22 Feb 2025 00:28:48 GMT  
		Size: 20.4 MB (20432003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ced3aebdded979735885d70afdbc8a5f03be15205f1145cd3b2af469eb21175`  
		Last Modified: Sat, 22 Feb 2025 00:28:48 GMT  
		Size: 19.7 MB (19725892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f8d07fba646c3b5ac2a07d053675df2a0422b36b698a824d345ee2447bc8e1`  
		Last Modified: Sat, 22 Feb 2025 00:28:47 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c51a22c8e8f3b4205fde47fd17f66895fad1496f33f46bb6aebdf5938bb94ad`  
		Last Modified: Sat, 22 Feb 2025 00:28:47 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f36ff703ab2a5ebeeeb26f374c59106eb92bf26531f572228024531dcc975f64`  
		Last Modified: Sat, 22 Feb 2025 00:28:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2440995b1488c0fccd4c0a9b3062c58a33404bcc3ca3e8289ae64b6393946c65`  
		Last Modified: Sat, 22 Feb 2025 01:29:31 GMT  
		Size: 7.0 MB (7036904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cce93707f7a9fed88581b5b8e8f49a184ba206f961aae653eef08af3b94987b1`  
		Last Modified: Sat, 22 Feb 2025 01:29:30 GMT  
		Size: 89.8 KB (89849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26cf971d434da3f52513e2595da034274a6fb8c1ef74cddc815339506b7b704a`  
		Last Modified: Sat, 22 Feb 2025 01:29:30 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c3188476c3d7ba720f96be3cdceb222b9a7a6e0693a917966988332f14e8ef`  
		Last Modified: Sat, 22 Feb 2025 01:29:33 GMT  
		Size: 55.6 MB (55587101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c9e4329aff590ce10c6d6613452bf70f9708c4817750614d9a1a68918444a6`  
		Last Modified: Sat, 22 Feb 2025 01:29:31 GMT  
		Size: 1.6 KB (1638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ff2444afd5e703729aeef9ead8d60b8f059c8e5f0b4b82853f021d0f2c24504`  
		Last Modified: Sat, 22 Feb 2025 01:29:31 GMT  
		Size: 3.3 KB (3263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.0-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:0931cacdc5870a73bd56837c9590fb9801af1b229cbf7ee86dc79c932a51323c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d14b9f57c5e9b67b594f4172c7cfbb95e2442a040e0bb090b09cc95ce2d35a18`

```dockerfile
```

-	Layers:
	-	`sha256:93150d2f1d44b19b0d6d36517e86cddc39cd49f0857f41bdb86a200f7db357e6`  
		Last Modified: Sat, 22 Feb 2025 01:29:30 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.0-alpine3.21` - linux; arm variant v7

```console
$ docker pull docker@sha256:089424d7adbb66df8dd78e5ce27d9bd9d13cebe072cb5eb79e7478f00c124163
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (130009843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da65fa603f2dc74e8750fbdc3d7173e607ca901a8dfb81fab1136584884d3018`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_VERSION=28.0.0
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-amd64'; 			sha256='7f355525bfaf411302570b705118181b720f18071f4be3f0eaac7b2297d826e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v6'; 			sha256='f841251fd67646e8b6bb4c7e0c2c385f6a1dc7403f5ac6ee7b07c96f0815f7f3'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v7'; 			sha256='81d7040e90e9b69cb0378778f673e1fc2a24ef6dbd47931dc83ab6472fc5809d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm64'; 			sha256='42d5cee287ec7426de5252276a05f3ea565ac2d65d62d052b885a84dd54152d5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-ppc64le'; 			sha256='6a4e6a243f83d80cd46c939f327b2e14cfddd2c6690651cf48d0e208c3345b88'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-riscv64'; 			sha256='eae82aec74a420c3d1734123e6a3bc10b3a2a981aa1d538502373e31c91bf76e'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-s390x'; 			sha256='97b112b3366a471cc375e0f881d65a9a7b07f0962f308834c37f5c3fa75aad08'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 20 Feb 2025 06:04:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD ["sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
VOLUME [/var/lib/docker]
# Thu, 20 Feb 2025 06:04:43 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD []
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b654458a637c48c7f8f46da325ae8f810828e851ed4ab4b406092503eb680f`  
		Last Modified: Sat, 22 Feb 2025 00:28:04 GMT  
		Size: 7.3 MB (7299375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3474560bdd0e71f5972a48abd9e80877e2219f6eacae8272034d8503bcb634b2`  
		Last Modified: Sat, 22 Feb 2025 00:28:03 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ffc820c153872520700f2618e71ee9bea9cfee69fbff7b0ea4acb751a2fee5`  
		Last Modified: Sat, 22 Feb 2025 00:28:04 GMT  
		Size: 17.4 MB (17444426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a39a48e6818f4f7d6e7637cf221cc02da7b2e8ab3ca2643a527024430497175`  
		Last Modified: Sat, 22 Feb 2025 00:28:04 GMT  
		Size: 20.4 MB (20411656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168ce845c02246501347d9ae0d1bb9bb9f55a707c5ef03ba3bb6377e832c28f4`  
		Last Modified: Sat, 22 Feb 2025 00:28:05 GMT  
		Size: 19.7 MB (19708525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d62f1159ab01591fa3510e1ddc7b7e0313d001750472b1eaa0dcfb3a1f097732`  
		Last Modified: Sat, 22 Feb 2025 00:28:05 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ab9b1b4b0f9c261b260d739cd6d593a2c510b9c29045d72d930f2baf5fa78e`  
		Last Modified: Sat, 22 Feb 2025 00:28:05 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d27509dd9fc9bdb19051b5661dce75fc9b53979841bcd49fd03667b1ad6dde`  
		Last Modified: Sat, 22 Feb 2025 00:28:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd0d2a57f389ccbd627e0bca3b813e9397f4a6a55364b1f7cf22df043542cf1a`  
		Last Modified: Sat, 22 Feb 2025 04:54:52 GMT  
		Size: 6.4 MB (6366292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5947e3cbc6a2eb4d8c4ec17605876ea3e3a5cb2c09abac0a58d53cc4d6569f7`  
		Last Modified: Sat, 22 Feb 2025 04:54:51 GMT  
		Size: 86.3 KB (86342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc1fa6b8e4e654268e5dfc6afa5b1e88bfb92da3c33018f231f76ad7e08a59e`  
		Last Modified: Sat, 22 Feb 2025 04:54:51 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f544c5574adf21ca185480beea8b120134f2ed74f3f2418dc0ef564a3891490`  
		Last Modified: Sat, 22 Feb 2025 04:54:53 GMT  
		Size: 55.6 MB (55587054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd1c8be29e89fc14e8cd0778dcda3dae4c641d9ab956b2f9ce8d02df1d7984e`  
		Last Modified: Sat, 22 Feb 2025 04:54:52 GMT  
		Size: 1.6 KB (1636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db5e7511235a55ebe7a92c8825189d27a2b1d951e0f25d22e4e932636abbd466`  
		Last Modified: Sat, 22 Feb 2025 04:54:52 GMT  
		Size: 3.3 KB (3256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.0-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:1cdaa27022a39a251e498044fefc2f4160913794dc50a3074935741e0d39d28b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:643a439611cab3be1c6fde6e85ec369c205d94c81b88f1c91a627a32a6448b32`

```dockerfile
```

-	Layers:
	-	`sha256:fa998948cfd33a55b2120a90b998117bea32698c81f84e340fc1f9fa359825c4`  
		Last Modified: Sat, 22 Feb 2025 04:54:51 GMT  
		Size: 34.8 KB (34765 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.0-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:af92e15294f197a3cc4de0e75e012f4e91a996e4fd58ad96e163208aea7f0be3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.4 MB (132399422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89d922b5c31bca4bc340632485ab5243809aaf557e7aaf377fd956c15f4ad0a6`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_VERSION=28.0.0
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-amd64'; 			sha256='7f355525bfaf411302570b705118181b720f18071f4be3f0eaac7b2297d826e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v6'; 			sha256='f841251fd67646e8b6bb4c7e0c2c385f6a1dc7403f5ac6ee7b07c96f0815f7f3'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v7'; 			sha256='81d7040e90e9b69cb0378778f673e1fc2a24ef6dbd47931dc83ab6472fc5809d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm64'; 			sha256='42d5cee287ec7426de5252276a05f3ea565ac2d65d62d052b885a84dd54152d5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-ppc64le'; 			sha256='6a4e6a243f83d80cd46c939f327b2e14cfddd2c6690651cf48d0e208c3345b88'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-riscv64'; 			sha256='eae82aec74a420c3d1734123e6a3bc10b3a2a981aa1d538502373e31c91bf76e'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-s390x'; 			sha256='97b112b3366a471cc375e0f881d65a9a7b07f0962f308834c37f5c3fa75aad08'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 20 Feb 2025 06:04:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD ["sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
VOLUME [/var/lib/docker]
# Thu, 20 Feb 2025 06:04:43 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD []
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:076f26e7389ad2e79a31e03589b2c6943495faa94ce7fc6ecd800dd0c320c71e`  
		Last Modified: Sat, 22 Feb 2025 00:28:38 GMT  
		Size: 8.1 MB (8076430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54483e7ea72052e991e704ef33b6d45d32f2c9886445d70ae79e50a2dd444147`  
		Last Modified: Sat, 22 Feb 2025 00:28:37 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d747fdfb37d0ca59992c4852cab088ffb4549e3f8ef7632b252452c1c12c7989`  
		Last Modified: Sat, 22 Feb 2025 00:28:38 GMT  
		Size: 18.4 MB (18412791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84912acd39dd03fae2cffdb073ec52df5d17e2700910653a8c844d31a916a7eb`  
		Last Modified: Sat, 22 Feb 2025 00:28:39 GMT  
		Size: 20.0 MB (20041446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49191a7f2e90fd89997d49d48799f225e27d4d811c1ab6a1a5ed18c8b5a9f94`  
		Last Modified: Sat, 22 Feb 2025 00:28:40 GMT  
		Size: 19.2 MB (19222674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7debd3993d0af81423e3290841931e4b162ff882877ebb292b10f3dde6dc5694`  
		Last Modified: Sat, 22 Feb 2025 00:28:39 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855282ceddcfc470897f6e2cb33f2ad4742db7c00f24a0386714c91a31a090fa`  
		Last Modified: Sat, 22 Feb 2025 00:28:40 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fbaf9714c72f8c1c56eb53405de18b5c63f82fcfa89814a71a92c9844e1fb8b`  
		Last Modified: Sat, 22 Feb 2025 00:28:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f1efb7aef297fc62aaca013f0102b13d4fb2bd1eb6e39c858c91c440c973f87`  
		Last Modified: Sat, 22 Feb 2025 02:46:00 GMT  
		Size: 7.0 MB (6978850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d301065fd8bf09964f1efc59488efd3c692d574aae6e2460fefc3dac799912b`  
		Last Modified: Sat, 22 Feb 2025 02:46:00 GMT  
		Size: 99.4 KB (99390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d33e0f749652bb606f1e92e433cb70fa6c8e7a30737050979d975e9f06a132f`  
		Last Modified: Sat, 22 Feb 2025 02:45:59 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a409b11008465c3cb7523e669b4d2a064619125185de982089bf11944cf62502`  
		Last Modified: Sat, 22 Feb 2025 02:46:01 GMT  
		Size: 55.6 MB (55566753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff8cdce63f040e68fff768b8a75d7ebdd3f4cd4e69ed0f85ae0ad620baa9c40`  
		Last Modified: Sat, 22 Feb 2025 02:46:00 GMT  
		Size: 1.6 KB (1636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f72a632b800deed0be1fc7ec78852db28106ae059a841b87a966fed6ec7255f`  
		Last Modified: Sat, 22 Feb 2025 02:46:01 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.0-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:d6dd49a97960eaef409aa41f89cf8596c02281b55801b3f726b267761031bc90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4105199c766800ff78dca393a5dccdb1435364291ecf731c31deacb4fa6e86a4`

```dockerfile
```

-	Layers:
	-	`sha256:2f7e554767be7baf2d46a3652bbe4405cdcb83972440eb83c19280ab0e991188`  
		Last Modified: Sat, 22 Feb 2025 02:45:59 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.0.0-cli`

```console
$ docker pull docker@sha256:28fb556c1ea1eef2f1d8d70e8c7eb52e38324b2ae04ffcb8df26648a7c2e5dfc
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

### `docker:28.0.0-cli` - linux; amd64

```console
$ docker pull docker@sha256:828f4f57525db5dbdb2f52ba47087c383361fd22975c264142bab1ff78ea8587
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73987390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2047a2478c64769a8f8963db4efc714c734b9ec896b1452fb424720a232732d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 21 Feb 2025 18:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_VERSION=28.0.0
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-amd64'; 			sha256='7f355525bfaf411302570b705118181b720f18071f4be3f0eaac7b2297d826e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v6'; 			sha256='f841251fd67646e8b6bb4c7e0c2c385f6a1dc7403f5ac6ee7b07c96f0815f7f3'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v7'; 			sha256='81d7040e90e9b69cb0378778f673e1fc2a24ef6dbd47931dc83ab6472fc5809d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm64'; 			sha256='42d5cee287ec7426de5252276a05f3ea565ac2d65d62d052b885a84dd54152d5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-ppc64le'; 			sha256='6a4e6a243f83d80cd46c939f327b2e14cfddd2c6690651cf48d0e208c3345b88'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-riscv64'; 			sha256='eae82aec74a420c3d1734123e6a3bc10b3a2a981aa1d538502373e31c91bf76e'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-s390x'; 			sha256='97b112b3366a471cc375e0f881d65a9a7b07f0962f308834c37f5c3fa75aad08'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 21 Feb 2025 18:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 18:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fddc498219722db61fe7f7e06295aa8b64f7e48d19d0339176689ea591eea4ca`  
		Last Modified: Sat, 22 Feb 2025 00:27:26 GMT  
		Size: 8.1 MB (8062985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c17b75175e66b76074511db7ebd5bdc56ac19ba269d30e4f58ba4812816ad4`  
		Last Modified: Sat, 22 Feb 2025 00:27:26 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987b6d8519d32209785b3840639a10aa6247ff1e290a651ebcca3d8c33e23dd2`  
		Last Modified: Sat, 22 Feb 2025 00:27:27 GMT  
		Size: 19.5 MB (19492233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7677267af1ddfc39dbdf35dcdca7c20328e83a42b64595f0d5880c62e99a91f`  
		Last Modified: Sat, 22 Feb 2025 00:27:27 GMT  
		Size: 21.8 MB (21829139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9fa9f5140fd1401e5edaa2de6f975bd14f0b79efbafbe0d2497ea0213ecd260`  
		Last Modified: Sat, 22 Feb 2025 00:27:27 GMT  
		Size: 21.0 MB (20958635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124bcf7a51a8a140479ebb1cfd0aea5bf38223d37b7c6ae1deb93bbb1abc0469`  
		Last Modified: Sat, 22 Feb 2025 00:27:28 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3083b3dfd2242fbeb7b498bb2e0d99d55c8e34cad7396573784aa86db3c69355`  
		Last Modified: Sat, 22 Feb 2025 00:27:28 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b255e6bd488c8fb61ba962afb512c02077ecc7e41b50991cb3229aaa7ae94b`  
		Last Modified: Sat, 22 Feb 2025 00:27:28 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:23d0fdad7d91848fe9aefbb31f9ec0f13048b4043d184117ef3506756fb199f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d89ed9762486ccde5720aaa5cfd88b8e5c1bf286c15632485f3c3a9b66385e0`

```dockerfile
```

-	Layers:
	-	`sha256:29c00cb8b559fbda58a54628ef429544bb24356f7620856781c43b802464d245`  
		Last Modified: Sat, 22 Feb 2025 00:27:26 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.0-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:563c0b58e54b2cb6649f26c22d8f06f2be7ebb8dead799918f4b22b13dd7d9f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (68956771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eabedade3d89f3eb7ffac6cf1924c31c852c974072b582d14b744e4c9c6993a2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 21 Feb 2025 18:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_VERSION=28.0.0
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-amd64'; 			sha256='7f355525bfaf411302570b705118181b720f18071f4be3f0eaac7b2297d826e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v6'; 			sha256='f841251fd67646e8b6bb4c7e0c2c385f6a1dc7403f5ac6ee7b07c96f0815f7f3'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v7'; 			sha256='81d7040e90e9b69cb0378778f673e1fc2a24ef6dbd47931dc83ab6472fc5809d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm64'; 			sha256='42d5cee287ec7426de5252276a05f3ea565ac2d65d62d052b885a84dd54152d5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-ppc64le'; 			sha256='6a4e6a243f83d80cd46c939f327b2e14cfddd2c6690651cf48d0e208c3345b88'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-riscv64'; 			sha256='eae82aec74a420c3d1734123e6a3bc10b3a2a981aa1d538502373e31c91bf76e'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-s390x'; 			sha256='97b112b3366a471cc375e0f881d65a9a7b07f0962f308834c37f5c3fa75aad08'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 21 Feb 2025 18:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 18:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e40b3641449ca47aef50c48f620eb6d3a3bc2292e5cf4ea267f5f03e6c7bc`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 8.0 MB (7978133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df16922f358c97f513c6d0b9457abb36aefc588e45374edd23692381878a7`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21eb60c27f71135d16125d7dcf87a6c0a49fc39428a0a7ecbc83c6bc1087efa9`  
		Last Modified: Thu, 20 Feb 2025 23:28:03 GMT  
		Size: 17.5 MB (17453851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b3b7abf60d98565d245e7aab34cfdec0b3c2c8ff503fb00ebceed21f636a93`  
		Last Modified: Sat, 22 Feb 2025 00:28:48 GMT  
		Size: 20.4 MB (20432003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ced3aebdded979735885d70afdbc8a5f03be15205f1145cd3b2af469eb21175`  
		Last Modified: Sat, 22 Feb 2025 00:28:48 GMT  
		Size: 19.7 MB (19725892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f8d07fba646c3b5ac2a07d053675df2a0422b36b698a824d345ee2447bc8e1`  
		Last Modified: Sat, 22 Feb 2025 00:28:47 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c51a22c8e8f3b4205fde47fd17f66895fad1496f33f46bb6aebdf5938bb94ad`  
		Last Modified: Sat, 22 Feb 2025 00:28:47 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f36ff703ab2a5ebeeeb26f374c59106eb92bf26531f572228024531dcc975f64`  
		Last Modified: Sat, 22 Feb 2025 00:28:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:19ac4c1b39024c4040fa578e5a4947132dfa561816cb7525547f283ad033cb82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d38b373d00ff94b39de7f66b705b156b58a6c9747a3aa783505be0e6c3ebf00`

```dockerfile
```

-	Layers:
	-	`sha256:65c4a818e540437ada35738cd53dff3f48895979403e4f6d6893ef134b4a0b5e`  
		Last Modified: Sat, 22 Feb 2025 00:28:47 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.0-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:6045d4846c59f8ee46c1d168dfe9b4de563a1602ed536f9a75e133d23291dc17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (67964254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ba8f3ae10c4069acc8988e46282e2592d80824e75e262440f1ca87b5b54fa4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 21 Feb 2025 18:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_VERSION=28.0.0
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-amd64'; 			sha256='7f355525bfaf411302570b705118181b720f18071f4be3f0eaac7b2297d826e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v6'; 			sha256='f841251fd67646e8b6bb4c7e0c2c385f6a1dc7403f5ac6ee7b07c96f0815f7f3'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v7'; 			sha256='81d7040e90e9b69cb0378778f673e1fc2a24ef6dbd47931dc83ab6472fc5809d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm64'; 			sha256='42d5cee287ec7426de5252276a05f3ea565ac2d65d62d052b885a84dd54152d5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-ppc64le'; 			sha256='6a4e6a243f83d80cd46c939f327b2e14cfddd2c6690651cf48d0e208c3345b88'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-riscv64'; 			sha256='eae82aec74a420c3d1734123e6a3bc10b3a2a981aa1d538502373e31c91bf76e'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-s390x'; 			sha256='97b112b3366a471cc375e0f881d65a9a7b07f0962f308834c37f5c3fa75aad08'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 21 Feb 2025 18:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 18:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b654458a637c48c7f8f46da325ae8f810828e851ed4ab4b406092503eb680f`  
		Last Modified: Sat, 22 Feb 2025 00:28:04 GMT  
		Size: 7.3 MB (7299375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3474560bdd0e71f5972a48abd9e80877e2219f6eacae8272034d8503bcb634b2`  
		Last Modified: Sat, 22 Feb 2025 00:28:03 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ffc820c153872520700f2618e71ee9bea9cfee69fbff7b0ea4acb751a2fee5`  
		Last Modified: Sat, 22 Feb 2025 00:28:04 GMT  
		Size: 17.4 MB (17444426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a39a48e6818f4f7d6e7637cf221cc02da7b2e8ab3ca2643a527024430497175`  
		Last Modified: Sat, 22 Feb 2025 00:28:04 GMT  
		Size: 20.4 MB (20411656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168ce845c02246501347d9ae0d1bb9bb9f55a707c5ef03ba3bb6377e832c28f4`  
		Last Modified: Sat, 22 Feb 2025 00:28:05 GMT  
		Size: 19.7 MB (19708525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d62f1159ab01591fa3510e1ddc7b7e0313d001750472b1eaa0dcfb3a1f097732`  
		Last Modified: Sat, 22 Feb 2025 00:28:05 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ab9b1b4b0f9c261b260d739cd6d593a2c510b9c29045d72d930f2baf5fa78e`  
		Last Modified: Sat, 22 Feb 2025 00:28:05 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d27509dd9fc9bdb19051b5661dce75fc9b53979841bcd49fd03667b1ad6dde`  
		Last Modified: Sat, 22 Feb 2025 00:28:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:23645fb2cbf9071135cf4f6aa3c2daf2dc3370793a863fef2ee39d5314bc1a81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93af0d5ba0d4eddf4e7d202afc318f1221ed8bb0f4b1ffde83604fd9bd752b41`

```dockerfile
```

-	Layers:
	-	`sha256:c3cccd9b156d9500700d8b30693438b27b91e56bc8149ff0300632ebb0780d36`  
		Last Modified: Sat, 22 Feb 2025 00:28:03 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.0-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:11e8dfd68841685653bd4816fc6ab2f95cc84940d099b1e683a4b60a958599df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69748524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af7e01753428f0214a4072134b7c0481b29b9f695ebe735e920d47b6c0302c4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 21 Feb 2025 18:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_VERSION=28.0.0
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-amd64'; 			sha256='7f355525bfaf411302570b705118181b720f18071f4be3f0eaac7b2297d826e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v6'; 			sha256='f841251fd67646e8b6bb4c7e0c2c385f6a1dc7403f5ac6ee7b07c96f0815f7f3'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v7'; 			sha256='81d7040e90e9b69cb0378778f673e1fc2a24ef6dbd47931dc83ab6472fc5809d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm64'; 			sha256='42d5cee287ec7426de5252276a05f3ea565ac2d65d62d052b885a84dd54152d5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-ppc64le'; 			sha256='6a4e6a243f83d80cd46c939f327b2e14cfddd2c6690651cf48d0e208c3345b88'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-riscv64'; 			sha256='eae82aec74a420c3d1734123e6a3bc10b3a2a981aa1d538502373e31c91bf76e'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-s390x'; 			sha256='97b112b3366a471cc375e0f881d65a9a7b07f0962f308834c37f5c3fa75aad08'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 21 Feb 2025 18:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 18:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:076f26e7389ad2e79a31e03589b2c6943495faa94ce7fc6ecd800dd0c320c71e`  
		Last Modified: Sat, 22 Feb 2025 00:28:38 GMT  
		Size: 8.1 MB (8076430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54483e7ea72052e991e704ef33b6d45d32f2c9886445d70ae79e50a2dd444147`  
		Last Modified: Sat, 22 Feb 2025 00:28:37 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d747fdfb37d0ca59992c4852cab088ffb4549e3f8ef7632b252452c1c12c7989`  
		Last Modified: Sat, 22 Feb 2025 00:28:38 GMT  
		Size: 18.4 MB (18412791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84912acd39dd03fae2cffdb073ec52df5d17e2700910653a8c844d31a916a7eb`  
		Last Modified: Sat, 22 Feb 2025 00:28:39 GMT  
		Size: 20.0 MB (20041446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49191a7f2e90fd89997d49d48799f225e27d4d811c1ab6a1a5ed18c8b5a9f94`  
		Last Modified: Sat, 22 Feb 2025 00:28:40 GMT  
		Size: 19.2 MB (19222674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7debd3993d0af81423e3290841931e4b162ff882877ebb292b10f3dde6dc5694`  
		Last Modified: Sat, 22 Feb 2025 00:28:39 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855282ceddcfc470897f6e2cb33f2ad4742db7c00f24a0386714c91a31a090fa`  
		Last Modified: Sat, 22 Feb 2025 00:28:40 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fbaf9714c72f8c1c56eb53405de18b5c63f82fcfa89814a71a92c9844e1fb8b`  
		Last Modified: Sat, 22 Feb 2025 00:28:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:30588165fa8677446217c19a011fa7b5dd4b56689b71068054b1769685612965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:050a79ebe758ee7f1e33b2b06dd06dabf7b2d3ccb381eb495d95c61658b577c3`

```dockerfile
```

-	Layers:
	-	`sha256:eb188e16beab9632a0818b296adc7960adad9c23b87529bf5b8f419eef964844`  
		Last Modified: Sat, 22 Feb 2025 00:28:37 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.0.0-cli-alpine3.21`

```console
$ docker pull docker@sha256:28fb556c1ea1eef2f1d8d70e8c7eb52e38324b2ae04ffcb8df26648a7c2e5dfc
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

### `docker:28.0.0-cli-alpine3.21` - linux; amd64

```console
$ docker pull docker@sha256:828f4f57525db5dbdb2f52ba47087c383361fd22975c264142bab1ff78ea8587
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73987390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2047a2478c64769a8f8963db4efc714c734b9ec896b1452fb424720a232732d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 21 Feb 2025 18:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_VERSION=28.0.0
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-amd64'; 			sha256='7f355525bfaf411302570b705118181b720f18071f4be3f0eaac7b2297d826e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v6'; 			sha256='f841251fd67646e8b6bb4c7e0c2c385f6a1dc7403f5ac6ee7b07c96f0815f7f3'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v7'; 			sha256='81d7040e90e9b69cb0378778f673e1fc2a24ef6dbd47931dc83ab6472fc5809d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm64'; 			sha256='42d5cee287ec7426de5252276a05f3ea565ac2d65d62d052b885a84dd54152d5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-ppc64le'; 			sha256='6a4e6a243f83d80cd46c939f327b2e14cfddd2c6690651cf48d0e208c3345b88'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-riscv64'; 			sha256='eae82aec74a420c3d1734123e6a3bc10b3a2a981aa1d538502373e31c91bf76e'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-s390x'; 			sha256='97b112b3366a471cc375e0f881d65a9a7b07f0962f308834c37f5c3fa75aad08'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 21 Feb 2025 18:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 18:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fddc498219722db61fe7f7e06295aa8b64f7e48d19d0339176689ea591eea4ca`  
		Last Modified: Sat, 22 Feb 2025 00:27:26 GMT  
		Size: 8.1 MB (8062985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c17b75175e66b76074511db7ebd5bdc56ac19ba269d30e4f58ba4812816ad4`  
		Last Modified: Sat, 22 Feb 2025 00:27:26 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987b6d8519d32209785b3840639a10aa6247ff1e290a651ebcca3d8c33e23dd2`  
		Last Modified: Sat, 22 Feb 2025 00:27:27 GMT  
		Size: 19.5 MB (19492233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7677267af1ddfc39dbdf35dcdca7c20328e83a42b64595f0d5880c62e99a91f`  
		Last Modified: Sat, 22 Feb 2025 00:27:27 GMT  
		Size: 21.8 MB (21829139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9fa9f5140fd1401e5edaa2de6f975bd14f0b79efbafbe0d2497ea0213ecd260`  
		Last Modified: Sat, 22 Feb 2025 00:27:27 GMT  
		Size: 21.0 MB (20958635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124bcf7a51a8a140479ebb1cfd0aea5bf38223d37b7c6ae1deb93bbb1abc0469`  
		Last Modified: Sat, 22 Feb 2025 00:27:28 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3083b3dfd2242fbeb7b498bb2e0d99d55c8e34cad7396573784aa86db3c69355`  
		Last Modified: Sat, 22 Feb 2025 00:27:28 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b255e6bd488c8fb61ba962afb512c02077ecc7e41b50991cb3229aaa7ae94b`  
		Last Modified: Sat, 22 Feb 2025 00:27:28 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.0-cli-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:23d0fdad7d91848fe9aefbb31f9ec0f13048b4043d184117ef3506756fb199f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d89ed9762486ccde5720aaa5cfd88b8e5c1bf286c15632485f3c3a9b66385e0`

```dockerfile
```

-	Layers:
	-	`sha256:29c00cb8b559fbda58a54628ef429544bb24356f7620856781c43b802464d245`  
		Last Modified: Sat, 22 Feb 2025 00:27:26 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.0-cli-alpine3.21` - linux; arm variant v6

```console
$ docker pull docker@sha256:563c0b58e54b2cb6649f26c22d8f06f2be7ebb8dead799918f4b22b13dd7d9f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (68956771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eabedade3d89f3eb7ffac6cf1924c31c852c974072b582d14b744e4c9c6993a2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 21 Feb 2025 18:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_VERSION=28.0.0
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-amd64'; 			sha256='7f355525bfaf411302570b705118181b720f18071f4be3f0eaac7b2297d826e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v6'; 			sha256='f841251fd67646e8b6bb4c7e0c2c385f6a1dc7403f5ac6ee7b07c96f0815f7f3'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v7'; 			sha256='81d7040e90e9b69cb0378778f673e1fc2a24ef6dbd47931dc83ab6472fc5809d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm64'; 			sha256='42d5cee287ec7426de5252276a05f3ea565ac2d65d62d052b885a84dd54152d5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-ppc64le'; 			sha256='6a4e6a243f83d80cd46c939f327b2e14cfddd2c6690651cf48d0e208c3345b88'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-riscv64'; 			sha256='eae82aec74a420c3d1734123e6a3bc10b3a2a981aa1d538502373e31c91bf76e'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-s390x'; 			sha256='97b112b3366a471cc375e0f881d65a9a7b07f0962f308834c37f5c3fa75aad08'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 21 Feb 2025 18:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 18:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e40b3641449ca47aef50c48f620eb6d3a3bc2292e5cf4ea267f5f03e6c7bc`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 8.0 MB (7978133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df16922f358c97f513c6d0b9457abb36aefc588e45374edd23692381878a7`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21eb60c27f71135d16125d7dcf87a6c0a49fc39428a0a7ecbc83c6bc1087efa9`  
		Last Modified: Thu, 20 Feb 2025 23:28:03 GMT  
		Size: 17.5 MB (17453851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b3b7abf60d98565d245e7aab34cfdec0b3c2c8ff503fb00ebceed21f636a93`  
		Last Modified: Sat, 22 Feb 2025 00:28:48 GMT  
		Size: 20.4 MB (20432003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ced3aebdded979735885d70afdbc8a5f03be15205f1145cd3b2af469eb21175`  
		Last Modified: Sat, 22 Feb 2025 00:28:48 GMT  
		Size: 19.7 MB (19725892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f8d07fba646c3b5ac2a07d053675df2a0422b36b698a824d345ee2447bc8e1`  
		Last Modified: Sat, 22 Feb 2025 00:28:47 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c51a22c8e8f3b4205fde47fd17f66895fad1496f33f46bb6aebdf5938bb94ad`  
		Last Modified: Sat, 22 Feb 2025 00:28:47 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f36ff703ab2a5ebeeeb26f374c59106eb92bf26531f572228024531dcc975f64`  
		Last Modified: Sat, 22 Feb 2025 00:28:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.0-cli-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:19ac4c1b39024c4040fa578e5a4947132dfa561816cb7525547f283ad033cb82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d38b373d00ff94b39de7f66b705b156b58a6c9747a3aa783505be0e6c3ebf00`

```dockerfile
```

-	Layers:
	-	`sha256:65c4a818e540437ada35738cd53dff3f48895979403e4f6d6893ef134b4a0b5e`  
		Last Modified: Sat, 22 Feb 2025 00:28:47 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.0-cli-alpine3.21` - linux; arm variant v7

```console
$ docker pull docker@sha256:6045d4846c59f8ee46c1d168dfe9b4de563a1602ed536f9a75e133d23291dc17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (67964254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ba8f3ae10c4069acc8988e46282e2592d80824e75e262440f1ca87b5b54fa4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 21 Feb 2025 18:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_VERSION=28.0.0
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-amd64'; 			sha256='7f355525bfaf411302570b705118181b720f18071f4be3f0eaac7b2297d826e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v6'; 			sha256='f841251fd67646e8b6bb4c7e0c2c385f6a1dc7403f5ac6ee7b07c96f0815f7f3'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v7'; 			sha256='81d7040e90e9b69cb0378778f673e1fc2a24ef6dbd47931dc83ab6472fc5809d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm64'; 			sha256='42d5cee287ec7426de5252276a05f3ea565ac2d65d62d052b885a84dd54152d5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-ppc64le'; 			sha256='6a4e6a243f83d80cd46c939f327b2e14cfddd2c6690651cf48d0e208c3345b88'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-riscv64'; 			sha256='eae82aec74a420c3d1734123e6a3bc10b3a2a981aa1d538502373e31c91bf76e'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-s390x'; 			sha256='97b112b3366a471cc375e0f881d65a9a7b07f0962f308834c37f5c3fa75aad08'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 21 Feb 2025 18:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 18:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b654458a637c48c7f8f46da325ae8f810828e851ed4ab4b406092503eb680f`  
		Last Modified: Sat, 22 Feb 2025 00:28:04 GMT  
		Size: 7.3 MB (7299375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3474560bdd0e71f5972a48abd9e80877e2219f6eacae8272034d8503bcb634b2`  
		Last Modified: Sat, 22 Feb 2025 00:28:03 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ffc820c153872520700f2618e71ee9bea9cfee69fbff7b0ea4acb751a2fee5`  
		Last Modified: Sat, 22 Feb 2025 00:28:04 GMT  
		Size: 17.4 MB (17444426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a39a48e6818f4f7d6e7637cf221cc02da7b2e8ab3ca2643a527024430497175`  
		Last Modified: Sat, 22 Feb 2025 00:28:04 GMT  
		Size: 20.4 MB (20411656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168ce845c02246501347d9ae0d1bb9bb9f55a707c5ef03ba3bb6377e832c28f4`  
		Last Modified: Sat, 22 Feb 2025 00:28:05 GMT  
		Size: 19.7 MB (19708525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d62f1159ab01591fa3510e1ddc7b7e0313d001750472b1eaa0dcfb3a1f097732`  
		Last Modified: Sat, 22 Feb 2025 00:28:05 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ab9b1b4b0f9c261b260d739cd6d593a2c510b9c29045d72d930f2baf5fa78e`  
		Last Modified: Sat, 22 Feb 2025 00:28:05 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d27509dd9fc9bdb19051b5661dce75fc9b53979841bcd49fd03667b1ad6dde`  
		Last Modified: Sat, 22 Feb 2025 00:28:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.0-cli-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:23645fb2cbf9071135cf4f6aa3c2daf2dc3370793a863fef2ee39d5314bc1a81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93af0d5ba0d4eddf4e7d202afc318f1221ed8bb0f4b1ffde83604fd9bd752b41`

```dockerfile
```

-	Layers:
	-	`sha256:c3cccd9b156d9500700d8b30693438b27b91e56bc8149ff0300632ebb0780d36`  
		Last Modified: Sat, 22 Feb 2025 00:28:03 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.0-cli-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:11e8dfd68841685653bd4816fc6ab2f95cc84940d099b1e683a4b60a958599df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69748524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af7e01753428f0214a4072134b7c0481b29b9f695ebe735e920d47b6c0302c4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 21 Feb 2025 18:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_VERSION=28.0.0
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-amd64'; 			sha256='7f355525bfaf411302570b705118181b720f18071f4be3f0eaac7b2297d826e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v6'; 			sha256='f841251fd67646e8b6bb4c7e0c2c385f6a1dc7403f5ac6ee7b07c96f0815f7f3'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v7'; 			sha256='81d7040e90e9b69cb0378778f673e1fc2a24ef6dbd47931dc83ab6472fc5809d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm64'; 			sha256='42d5cee287ec7426de5252276a05f3ea565ac2d65d62d052b885a84dd54152d5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-ppc64le'; 			sha256='6a4e6a243f83d80cd46c939f327b2e14cfddd2c6690651cf48d0e208c3345b88'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-riscv64'; 			sha256='eae82aec74a420c3d1734123e6a3bc10b3a2a981aa1d538502373e31c91bf76e'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-s390x'; 			sha256='97b112b3366a471cc375e0f881d65a9a7b07f0962f308834c37f5c3fa75aad08'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 21 Feb 2025 18:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 18:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:076f26e7389ad2e79a31e03589b2c6943495faa94ce7fc6ecd800dd0c320c71e`  
		Last Modified: Sat, 22 Feb 2025 00:28:38 GMT  
		Size: 8.1 MB (8076430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54483e7ea72052e991e704ef33b6d45d32f2c9886445d70ae79e50a2dd444147`  
		Last Modified: Sat, 22 Feb 2025 00:28:37 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d747fdfb37d0ca59992c4852cab088ffb4549e3f8ef7632b252452c1c12c7989`  
		Last Modified: Sat, 22 Feb 2025 00:28:38 GMT  
		Size: 18.4 MB (18412791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84912acd39dd03fae2cffdb073ec52df5d17e2700910653a8c844d31a916a7eb`  
		Last Modified: Sat, 22 Feb 2025 00:28:39 GMT  
		Size: 20.0 MB (20041446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49191a7f2e90fd89997d49d48799f225e27d4d811c1ab6a1a5ed18c8b5a9f94`  
		Last Modified: Sat, 22 Feb 2025 00:28:40 GMT  
		Size: 19.2 MB (19222674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7debd3993d0af81423e3290841931e4b162ff882877ebb292b10f3dde6dc5694`  
		Last Modified: Sat, 22 Feb 2025 00:28:39 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855282ceddcfc470897f6e2cb33f2ad4742db7c00f24a0386714c91a31a090fa`  
		Last Modified: Sat, 22 Feb 2025 00:28:40 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fbaf9714c72f8c1c56eb53405de18b5c63f82fcfa89814a71a92c9844e1fb8b`  
		Last Modified: Sat, 22 Feb 2025 00:28:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.0-cli-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:30588165fa8677446217c19a011fa7b5dd4b56689b71068054b1769685612965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:050a79ebe758ee7f1e33b2b06dd06dabf7b2d3ccb381eb495d95c61658b577c3`

```dockerfile
```

-	Layers:
	-	`sha256:eb188e16beab9632a0818b296adc7960adad9c23b87529bf5b8f419eef964844`  
		Last Modified: Sat, 22 Feb 2025 00:28:37 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.0.0-dind`

```console
$ docker pull docker@sha256:0a9c58ebc9f86e5af35e4330f6c738dc64fce3ca2e2574b5becdfb88765b308b
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

### `docker:28.0.0-dind` - linux; amd64

```console
$ docker pull docker@sha256:32c276e9aafff90ea7765271afa524c293c9749e880748217b1abedd04af39a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.0 MB (141006353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1da86d0da980dad6c82075b9859478027165e57dba77994a2fe1fa99ed408f3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_VERSION=28.0.0
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-amd64'; 			sha256='7f355525bfaf411302570b705118181b720f18071f4be3f0eaac7b2297d826e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v6'; 			sha256='f841251fd67646e8b6bb4c7e0c2c385f6a1dc7403f5ac6ee7b07c96f0815f7f3'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v7'; 			sha256='81d7040e90e9b69cb0378778f673e1fc2a24ef6dbd47931dc83ab6472fc5809d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm64'; 			sha256='42d5cee287ec7426de5252276a05f3ea565ac2d65d62d052b885a84dd54152d5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-ppc64le'; 			sha256='6a4e6a243f83d80cd46c939f327b2e14cfddd2c6690651cf48d0e208c3345b88'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-riscv64'; 			sha256='eae82aec74a420c3d1734123e6a3bc10b3a2a981aa1d538502373e31c91bf76e'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-s390x'; 			sha256='97b112b3366a471cc375e0f881d65a9a7b07f0962f308834c37f5c3fa75aad08'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 20 Feb 2025 06:04:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD ["sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
VOLUME [/var/lib/docker]
# Thu, 20 Feb 2025 06:04:43 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD []
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fddc498219722db61fe7f7e06295aa8b64f7e48d19d0339176689ea591eea4ca`  
		Last Modified: Sat, 22 Feb 2025 00:27:26 GMT  
		Size: 8.1 MB (8062985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c17b75175e66b76074511db7ebd5bdc56ac19ba269d30e4f58ba4812816ad4`  
		Last Modified: Sat, 22 Feb 2025 00:27:26 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987b6d8519d32209785b3840639a10aa6247ff1e290a651ebcca3d8c33e23dd2`  
		Last Modified: Sat, 22 Feb 2025 00:27:27 GMT  
		Size: 19.5 MB (19492233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7677267af1ddfc39dbdf35dcdca7c20328e83a42b64595f0d5880c62e99a91f`  
		Last Modified: Sat, 22 Feb 2025 00:27:27 GMT  
		Size: 21.8 MB (21829139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9fa9f5140fd1401e5edaa2de6f975bd14f0b79efbafbe0d2497ea0213ecd260`  
		Last Modified: Sat, 22 Feb 2025 00:27:27 GMT  
		Size: 21.0 MB (20958635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124bcf7a51a8a140479ebb1cfd0aea5bf38223d37b7c6ae1deb93bbb1abc0469`  
		Last Modified: Sat, 22 Feb 2025 00:27:28 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3083b3dfd2242fbeb7b498bb2e0d99d55c8e34cad7396573784aa86db3c69355`  
		Last Modified: Sat, 22 Feb 2025 00:27:28 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b255e6bd488c8fb61ba962afb512c02077ecc7e41b50991cb3229aaa7ae94b`  
		Last Modified: Sat, 22 Feb 2025 00:27:28 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42458739bc4b2677f265360a10a2eacffd5133b0242dd313ba8a3dac7a116c4`  
		Last Modified: Sat, 22 Feb 2025 01:08:23 GMT  
		Size: 6.7 MB (6733003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5a7650793a22cfeac45c6610fe2cd3ccd26b6795d33ee5389d66a174c05a65`  
		Last Modified: Sat, 22 Feb 2025 01:08:23 GMT  
		Size: 90.3 KB (90318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03749f129a866bd1cf2e2797db758f883cf177f3cd33ff3c60924ec811728b4f`  
		Last Modified: Sat, 22 Feb 2025 01:08:23 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:769e1c97b1855704d1f74c39b30c2d2bbc890339752b2be542477e64d2529c32`  
		Last Modified: Sat, 22 Feb 2025 01:08:24 GMT  
		Size: 60.2 MB (60189735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e450e39e6d5b103505878dd35ff532dcdfef40450540495b6a666e7bc34e2587`  
		Last Modified: Sat, 22 Feb 2025 01:08:23 GMT  
		Size: 1.6 KB (1637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254862f49c6f0929e44b00f9635661aff98a508d2dc321d6ddc2944f60ac90bb`  
		Last Modified: Sat, 22 Feb 2025 01:08:23 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.0-dind` - unknown; unknown

```console
$ docker pull docker@sha256:ba9368fe1da752bf14bb9ed738b656214abfea5e16cb949f4883beeb86cf9408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:658bfc3f8051aceaf851bbf4fdcff3b32c7f8c853b5262abd646f57fbf14bb10`

```dockerfile
```

-	Layers:
	-	`sha256:670c6ce494a80447b9f682d0ac427af5be54978f5f629221274a481ecf2be95e`  
		Last Modified: Sat, 22 Feb 2025 01:08:22 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.0-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:346b1790ac4379efe1ff83735d9d72ded98e8ebcc776f29f190a50d1086d5c63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.7 MB (131676535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e2b568d33d9f4d9da33be6f6a26a6e533f58d6d874c445c67494a71fe99ce8c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_VERSION=28.0.0
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-amd64'; 			sha256='7f355525bfaf411302570b705118181b720f18071f4be3f0eaac7b2297d826e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v6'; 			sha256='f841251fd67646e8b6bb4c7e0c2c385f6a1dc7403f5ac6ee7b07c96f0815f7f3'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v7'; 			sha256='81d7040e90e9b69cb0378778f673e1fc2a24ef6dbd47931dc83ab6472fc5809d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm64'; 			sha256='42d5cee287ec7426de5252276a05f3ea565ac2d65d62d052b885a84dd54152d5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-ppc64le'; 			sha256='6a4e6a243f83d80cd46c939f327b2e14cfddd2c6690651cf48d0e208c3345b88'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-riscv64'; 			sha256='eae82aec74a420c3d1734123e6a3bc10b3a2a981aa1d538502373e31c91bf76e'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-s390x'; 			sha256='97b112b3366a471cc375e0f881d65a9a7b07f0962f308834c37f5c3fa75aad08'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 20 Feb 2025 06:04:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD ["sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
VOLUME [/var/lib/docker]
# Thu, 20 Feb 2025 06:04:43 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD []
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e40b3641449ca47aef50c48f620eb6d3a3bc2292e5cf4ea267f5f03e6c7bc`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 8.0 MB (7978133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df16922f358c97f513c6d0b9457abb36aefc588e45374edd23692381878a7`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21eb60c27f71135d16125d7dcf87a6c0a49fc39428a0a7ecbc83c6bc1087efa9`  
		Last Modified: Thu, 20 Feb 2025 23:28:03 GMT  
		Size: 17.5 MB (17453851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b3b7abf60d98565d245e7aab34cfdec0b3c2c8ff503fb00ebceed21f636a93`  
		Last Modified: Sat, 22 Feb 2025 00:28:48 GMT  
		Size: 20.4 MB (20432003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ced3aebdded979735885d70afdbc8a5f03be15205f1145cd3b2af469eb21175`  
		Last Modified: Sat, 22 Feb 2025 00:28:48 GMT  
		Size: 19.7 MB (19725892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f8d07fba646c3b5ac2a07d053675df2a0422b36b698a824d345ee2447bc8e1`  
		Last Modified: Sat, 22 Feb 2025 00:28:47 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c51a22c8e8f3b4205fde47fd17f66895fad1496f33f46bb6aebdf5938bb94ad`  
		Last Modified: Sat, 22 Feb 2025 00:28:47 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f36ff703ab2a5ebeeeb26f374c59106eb92bf26531f572228024531dcc975f64`  
		Last Modified: Sat, 22 Feb 2025 00:28:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2440995b1488c0fccd4c0a9b3062c58a33404bcc3ca3e8289ae64b6393946c65`  
		Last Modified: Sat, 22 Feb 2025 01:29:31 GMT  
		Size: 7.0 MB (7036904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cce93707f7a9fed88581b5b8e8f49a184ba206f961aae653eef08af3b94987b1`  
		Last Modified: Sat, 22 Feb 2025 01:29:30 GMT  
		Size: 89.8 KB (89849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26cf971d434da3f52513e2595da034274a6fb8c1ef74cddc815339506b7b704a`  
		Last Modified: Sat, 22 Feb 2025 01:29:30 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c3188476c3d7ba720f96be3cdceb222b9a7a6e0693a917966988332f14e8ef`  
		Last Modified: Sat, 22 Feb 2025 01:29:33 GMT  
		Size: 55.6 MB (55587101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c9e4329aff590ce10c6d6613452bf70f9708c4817750614d9a1a68918444a6`  
		Last Modified: Sat, 22 Feb 2025 01:29:31 GMT  
		Size: 1.6 KB (1638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ff2444afd5e703729aeef9ead8d60b8f059c8e5f0b4b82853f021d0f2c24504`  
		Last Modified: Sat, 22 Feb 2025 01:29:31 GMT  
		Size: 3.3 KB (3263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.0-dind` - unknown; unknown

```console
$ docker pull docker@sha256:0931cacdc5870a73bd56837c9590fb9801af1b229cbf7ee86dc79c932a51323c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d14b9f57c5e9b67b594f4172c7cfbb95e2442a040e0bb090b09cc95ce2d35a18`

```dockerfile
```

-	Layers:
	-	`sha256:93150d2f1d44b19b0d6d36517e86cddc39cd49f0857f41bdb86a200f7db357e6`  
		Last Modified: Sat, 22 Feb 2025 01:29:30 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.0-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:089424d7adbb66df8dd78e5ce27d9bd9d13cebe072cb5eb79e7478f00c124163
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (130009843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da65fa603f2dc74e8750fbdc3d7173e607ca901a8dfb81fab1136584884d3018`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_VERSION=28.0.0
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-amd64'; 			sha256='7f355525bfaf411302570b705118181b720f18071f4be3f0eaac7b2297d826e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v6'; 			sha256='f841251fd67646e8b6bb4c7e0c2c385f6a1dc7403f5ac6ee7b07c96f0815f7f3'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v7'; 			sha256='81d7040e90e9b69cb0378778f673e1fc2a24ef6dbd47931dc83ab6472fc5809d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm64'; 			sha256='42d5cee287ec7426de5252276a05f3ea565ac2d65d62d052b885a84dd54152d5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-ppc64le'; 			sha256='6a4e6a243f83d80cd46c939f327b2e14cfddd2c6690651cf48d0e208c3345b88'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-riscv64'; 			sha256='eae82aec74a420c3d1734123e6a3bc10b3a2a981aa1d538502373e31c91bf76e'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-s390x'; 			sha256='97b112b3366a471cc375e0f881d65a9a7b07f0962f308834c37f5c3fa75aad08'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 20 Feb 2025 06:04:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD ["sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
VOLUME [/var/lib/docker]
# Thu, 20 Feb 2025 06:04:43 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD []
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b654458a637c48c7f8f46da325ae8f810828e851ed4ab4b406092503eb680f`  
		Last Modified: Sat, 22 Feb 2025 00:28:04 GMT  
		Size: 7.3 MB (7299375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3474560bdd0e71f5972a48abd9e80877e2219f6eacae8272034d8503bcb634b2`  
		Last Modified: Sat, 22 Feb 2025 00:28:03 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ffc820c153872520700f2618e71ee9bea9cfee69fbff7b0ea4acb751a2fee5`  
		Last Modified: Sat, 22 Feb 2025 00:28:04 GMT  
		Size: 17.4 MB (17444426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a39a48e6818f4f7d6e7637cf221cc02da7b2e8ab3ca2643a527024430497175`  
		Last Modified: Sat, 22 Feb 2025 00:28:04 GMT  
		Size: 20.4 MB (20411656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168ce845c02246501347d9ae0d1bb9bb9f55a707c5ef03ba3bb6377e832c28f4`  
		Last Modified: Sat, 22 Feb 2025 00:28:05 GMT  
		Size: 19.7 MB (19708525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d62f1159ab01591fa3510e1ddc7b7e0313d001750472b1eaa0dcfb3a1f097732`  
		Last Modified: Sat, 22 Feb 2025 00:28:05 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ab9b1b4b0f9c261b260d739cd6d593a2c510b9c29045d72d930f2baf5fa78e`  
		Last Modified: Sat, 22 Feb 2025 00:28:05 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d27509dd9fc9bdb19051b5661dce75fc9b53979841bcd49fd03667b1ad6dde`  
		Last Modified: Sat, 22 Feb 2025 00:28:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd0d2a57f389ccbd627e0bca3b813e9397f4a6a55364b1f7cf22df043542cf1a`  
		Last Modified: Sat, 22 Feb 2025 04:54:52 GMT  
		Size: 6.4 MB (6366292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5947e3cbc6a2eb4d8c4ec17605876ea3e3a5cb2c09abac0a58d53cc4d6569f7`  
		Last Modified: Sat, 22 Feb 2025 04:54:51 GMT  
		Size: 86.3 KB (86342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc1fa6b8e4e654268e5dfc6afa5b1e88bfb92da3c33018f231f76ad7e08a59e`  
		Last Modified: Sat, 22 Feb 2025 04:54:51 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f544c5574adf21ca185480beea8b120134f2ed74f3f2418dc0ef564a3891490`  
		Last Modified: Sat, 22 Feb 2025 04:54:53 GMT  
		Size: 55.6 MB (55587054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd1c8be29e89fc14e8cd0778dcda3dae4c641d9ab956b2f9ce8d02df1d7984e`  
		Last Modified: Sat, 22 Feb 2025 04:54:52 GMT  
		Size: 1.6 KB (1636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db5e7511235a55ebe7a92c8825189d27a2b1d951e0f25d22e4e932636abbd466`  
		Last Modified: Sat, 22 Feb 2025 04:54:52 GMT  
		Size: 3.3 KB (3256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.0-dind` - unknown; unknown

```console
$ docker pull docker@sha256:1cdaa27022a39a251e498044fefc2f4160913794dc50a3074935741e0d39d28b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:643a439611cab3be1c6fde6e85ec369c205d94c81b88f1c91a627a32a6448b32`

```dockerfile
```

-	Layers:
	-	`sha256:fa998948cfd33a55b2120a90b998117bea32698c81f84e340fc1f9fa359825c4`  
		Last Modified: Sat, 22 Feb 2025 04:54:51 GMT  
		Size: 34.8 KB (34765 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.0-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:af92e15294f197a3cc4de0e75e012f4e91a996e4fd58ad96e163208aea7f0be3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.4 MB (132399422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89d922b5c31bca4bc340632485ab5243809aaf557e7aaf377fd956c15f4ad0a6`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_VERSION=28.0.0
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-amd64'; 			sha256='7f355525bfaf411302570b705118181b720f18071f4be3f0eaac7b2297d826e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v6'; 			sha256='f841251fd67646e8b6bb4c7e0c2c385f6a1dc7403f5ac6ee7b07c96f0815f7f3'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v7'; 			sha256='81d7040e90e9b69cb0378778f673e1fc2a24ef6dbd47931dc83ab6472fc5809d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm64'; 			sha256='42d5cee287ec7426de5252276a05f3ea565ac2d65d62d052b885a84dd54152d5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-ppc64le'; 			sha256='6a4e6a243f83d80cd46c939f327b2e14cfddd2c6690651cf48d0e208c3345b88'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-riscv64'; 			sha256='eae82aec74a420c3d1734123e6a3bc10b3a2a981aa1d538502373e31c91bf76e'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-s390x'; 			sha256='97b112b3366a471cc375e0f881d65a9a7b07f0962f308834c37f5c3fa75aad08'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 20 Feb 2025 06:04:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD ["sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
VOLUME [/var/lib/docker]
# Thu, 20 Feb 2025 06:04:43 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD []
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:076f26e7389ad2e79a31e03589b2c6943495faa94ce7fc6ecd800dd0c320c71e`  
		Last Modified: Sat, 22 Feb 2025 00:28:38 GMT  
		Size: 8.1 MB (8076430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54483e7ea72052e991e704ef33b6d45d32f2c9886445d70ae79e50a2dd444147`  
		Last Modified: Sat, 22 Feb 2025 00:28:37 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d747fdfb37d0ca59992c4852cab088ffb4549e3f8ef7632b252452c1c12c7989`  
		Last Modified: Sat, 22 Feb 2025 00:28:38 GMT  
		Size: 18.4 MB (18412791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84912acd39dd03fae2cffdb073ec52df5d17e2700910653a8c844d31a916a7eb`  
		Last Modified: Sat, 22 Feb 2025 00:28:39 GMT  
		Size: 20.0 MB (20041446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49191a7f2e90fd89997d49d48799f225e27d4d811c1ab6a1a5ed18c8b5a9f94`  
		Last Modified: Sat, 22 Feb 2025 00:28:40 GMT  
		Size: 19.2 MB (19222674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7debd3993d0af81423e3290841931e4b162ff882877ebb292b10f3dde6dc5694`  
		Last Modified: Sat, 22 Feb 2025 00:28:39 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855282ceddcfc470897f6e2cb33f2ad4742db7c00f24a0386714c91a31a090fa`  
		Last Modified: Sat, 22 Feb 2025 00:28:40 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fbaf9714c72f8c1c56eb53405de18b5c63f82fcfa89814a71a92c9844e1fb8b`  
		Last Modified: Sat, 22 Feb 2025 00:28:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f1efb7aef297fc62aaca013f0102b13d4fb2bd1eb6e39c858c91c440c973f87`  
		Last Modified: Sat, 22 Feb 2025 02:46:00 GMT  
		Size: 7.0 MB (6978850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d301065fd8bf09964f1efc59488efd3c692d574aae6e2460fefc3dac799912b`  
		Last Modified: Sat, 22 Feb 2025 02:46:00 GMT  
		Size: 99.4 KB (99390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d33e0f749652bb606f1e92e433cb70fa6c8e7a30737050979d975e9f06a132f`  
		Last Modified: Sat, 22 Feb 2025 02:45:59 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a409b11008465c3cb7523e669b4d2a064619125185de982089bf11944cf62502`  
		Last Modified: Sat, 22 Feb 2025 02:46:01 GMT  
		Size: 55.6 MB (55566753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff8cdce63f040e68fff768b8a75d7ebdd3f4cd4e69ed0f85ae0ad620baa9c40`  
		Last Modified: Sat, 22 Feb 2025 02:46:00 GMT  
		Size: 1.6 KB (1636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f72a632b800deed0be1fc7ec78852db28106ae059a841b87a966fed6ec7255f`  
		Last Modified: Sat, 22 Feb 2025 02:46:01 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.0-dind` - unknown; unknown

```console
$ docker pull docker@sha256:d6dd49a97960eaef409aa41f89cf8596c02281b55801b3f726b267761031bc90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4105199c766800ff78dca393a5dccdb1435364291ecf731c31deacb4fa6e86a4`

```dockerfile
```

-	Layers:
	-	`sha256:2f7e554767be7baf2d46a3652bbe4405cdcb83972440eb83c19280ab0e991188`  
		Last Modified: Sat, 22 Feb 2025 02:45:59 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.0.0-dind-alpine3.21`

```console
$ docker pull docker@sha256:0a9c58ebc9f86e5af35e4330f6c738dc64fce3ca2e2574b5becdfb88765b308b
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

### `docker:28.0.0-dind-alpine3.21` - linux; amd64

```console
$ docker pull docker@sha256:32c276e9aafff90ea7765271afa524c293c9749e880748217b1abedd04af39a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.0 MB (141006353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1da86d0da980dad6c82075b9859478027165e57dba77994a2fe1fa99ed408f3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_VERSION=28.0.0
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-amd64'; 			sha256='7f355525bfaf411302570b705118181b720f18071f4be3f0eaac7b2297d826e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v6'; 			sha256='f841251fd67646e8b6bb4c7e0c2c385f6a1dc7403f5ac6ee7b07c96f0815f7f3'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v7'; 			sha256='81d7040e90e9b69cb0378778f673e1fc2a24ef6dbd47931dc83ab6472fc5809d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm64'; 			sha256='42d5cee287ec7426de5252276a05f3ea565ac2d65d62d052b885a84dd54152d5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-ppc64le'; 			sha256='6a4e6a243f83d80cd46c939f327b2e14cfddd2c6690651cf48d0e208c3345b88'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-riscv64'; 			sha256='eae82aec74a420c3d1734123e6a3bc10b3a2a981aa1d538502373e31c91bf76e'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-s390x'; 			sha256='97b112b3366a471cc375e0f881d65a9a7b07f0962f308834c37f5c3fa75aad08'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 20 Feb 2025 06:04:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD ["sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
VOLUME [/var/lib/docker]
# Thu, 20 Feb 2025 06:04:43 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD []
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fddc498219722db61fe7f7e06295aa8b64f7e48d19d0339176689ea591eea4ca`  
		Last Modified: Sat, 22 Feb 2025 00:27:26 GMT  
		Size: 8.1 MB (8062985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c17b75175e66b76074511db7ebd5bdc56ac19ba269d30e4f58ba4812816ad4`  
		Last Modified: Sat, 22 Feb 2025 00:27:26 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987b6d8519d32209785b3840639a10aa6247ff1e290a651ebcca3d8c33e23dd2`  
		Last Modified: Sat, 22 Feb 2025 00:27:27 GMT  
		Size: 19.5 MB (19492233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7677267af1ddfc39dbdf35dcdca7c20328e83a42b64595f0d5880c62e99a91f`  
		Last Modified: Sat, 22 Feb 2025 00:27:27 GMT  
		Size: 21.8 MB (21829139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9fa9f5140fd1401e5edaa2de6f975bd14f0b79efbafbe0d2497ea0213ecd260`  
		Last Modified: Sat, 22 Feb 2025 00:27:27 GMT  
		Size: 21.0 MB (20958635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124bcf7a51a8a140479ebb1cfd0aea5bf38223d37b7c6ae1deb93bbb1abc0469`  
		Last Modified: Sat, 22 Feb 2025 00:27:28 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3083b3dfd2242fbeb7b498bb2e0d99d55c8e34cad7396573784aa86db3c69355`  
		Last Modified: Sat, 22 Feb 2025 00:27:28 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b255e6bd488c8fb61ba962afb512c02077ecc7e41b50991cb3229aaa7ae94b`  
		Last Modified: Sat, 22 Feb 2025 00:27:28 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42458739bc4b2677f265360a10a2eacffd5133b0242dd313ba8a3dac7a116c4`  
		Last Modified: Sat, 22 Feb 2025 01:08:23 GMT  
		Size: 6.7 MB (6733003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5a7650793a22cfeac45c6610fe2cd3ccd26b6795d33ee5389d66a174c05a65`  
		Last Modified: Sat, 22 Feb 2025 01:08:23 GMT  
		Size: 90.3 KB (90318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03749f129a866bd1cf2e2797db758f883cf177f3cd33ff3c60924ec811728b4f`  
		Last Modified: Sat, 22 Feb 2025 01:08:23 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:769e1c97b1855704d1f74c39b30c2d2bbc890339752b2be542477e64d2529c32`  
		Last Modified: Sat, 22 Feb 2025 01:08:24 GMT  
		Size: 60.2 MB (60189735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e450e39e6d5b103505878dd35ff532dcdfef40450540495b6a666e7bc34e2587`  
		Last Modified: Sat, 22 Feb 2025 01:08:23 GMT  
		Size: 1.6 KB (1637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254862f49c6f0929e44b00f9635661aff98a508d2dc321d6ddc2944f60ac90bb`  
		Last Modified: Sat, 22 Feb 2025 01:08:23 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.0-dind-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:ba9368fe1da752bf14bb9ed738b656214abfea5e16cb949f4883beeb86cf9408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:658bfc3f8051aceaf851bbf4fdcff3b32c7f8c853b5262abd646f57fbf14bb10`

```dockerfile
```

-	Layers:
	-	`sha256:670c6ce494a80447b9f682d0ac427af5be54978f5f629221274a481ecf2be95e`  
		Last Modified: Sat, 22 Feb 2025 01:08:22 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.0-dind-alpine3.21` - linux; arm variant v6

```console
$ docker pull docker@sha256:346b1790ac4379efe1ff83735d9d72ded98e8ebcc776f29f190a50d1086d5c63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.7 MB (131676535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e2b568d33d9f4d9da33be6f6a26a6e533f58d6d874c445c67494a71fe99ce8c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_VERSION=28.0.0
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-amd64'; 			sha256='7f355525bfaf411302570b705118181b720f18071f4be3f0eaac7b2297d826e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v6'; 			sha256='f841251fd67646e8b6bb4c7e0c2c385f6a1dc7403f5ac6ee7b07c96f0815f7f3'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v7'; 			sha256='81d7040e90e9b69cb0378778f673e1fc2a24ef6dbd47931dc83ab6472fc5809d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm64'; 			sha256='42d5cee287ec7426de5252276a05f3ea565ac2d65d62d052b885a84dd54152d5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-ppc64le'; 			sha256='6a4e6a243f83d80cd46c939f327b2e14cfddd2c6690651cf48d0e208c3345b88'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-riscv64'; 			sha256='eae82aec74a420c3d1734123e6a3bc10b3a2a981aa1d538502373e31c91bf76e'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-s390x'; 			sha256='97b112b3366a471cc375e0f881d65a9a7b07f0962f308834c37f5c3fa75aad08'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 20 Feb 2025 06:04:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD ["sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
VOLUME [/var/lib/docker]
# Thu, 20 Feb 2025 06:04:43 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD []
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e40b3641449ca47aef50c48f620eb6d3a3bc2292e5cf4ea267f5f03e6c7bc`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 8.0 MB (7978133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df16922f358c97f513c6d0b9457abb36aefc588e45374edd23692381878a7`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21eb60c27f71135d16125d7dcf87a6c0a49fc39428a0a7ecbc83c6bc1087efa9`  
		Last Modified: Thu, 20 Feb 2025 23:28:03 GMT  
		Size: 17.5 MB (17453851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b3b7abf60d98565d245e7aab34cfdec0b3c2c8ff503fb00ebceed21f636a93`  
		Last Modified: Sat, 22 Feb 2025 00:28:48 GMT  
		Size: 20.4 MB (20432003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ced3aebdded979735885d70afdbc8a5f03be15205f1145cd3b2af469eb21175`  
		Last Modified: Sat, 22 Feb 2025 00:28:48 GMT  
		Size: 19.7 MB (19725892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f8d07fba646c3b5ac2a07d053675df2a0422b36b698a824d345ee2447bc8e1`  
		Last Modified: Sat, 22 Feb 2025 00:28:47 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c51a22c8e8f3b4205fde47fd17f66895fad1496f33f46bb6aebdf5938bb94ad`  
		Last Modified: Sat, 22 Feb 2025 00:28:47 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f36ff703ab2a5ebeeeb26f374c59106eb92bf26531f572228024531dcc975f64`  
		Last Modified: Sat, 22 Feb 2025 00:28:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2440995b1488c0fccd4c0a9b3062c58a33404bcc3ca3e8289ae64b6393946c65`  
		Last Modified: Sat, 22 Feb 2025 01:29:31 GMT  
		Size: 7.0 MB (7036904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cce93707f7a9fed88581b5b8e8f49a184ba206f961aae653eef08af3b94987b1`  
		Last Modified: Sat, 22 Feb 2025 01:29:30 GMT  
		Size: 89.8 KB (89849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26cf971d434da3f52513e2595da034274a6fb8c1ef74cddc815339506b7b704a`  
		Last Modified: Sat, 22 Feb 2025 01:29:30 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c3188476c3d7ba720f96be3cdceb222b9a7a6e0693a917966988332f14e8ef`  
		Last Modified: Sat, 22 Feb 2025 01:29:33 GMT  
		Size: 55.6 MB (55587101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c9e4329aff590ce10c6d6613452bf70f9708c4817750614d9a1a68918444a6`  
		Last Modified: Sat, 22 Feb 2025 01:29:31 GMT  
		Size: 1.6 KB (1638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ff2444afd5e703729aeef9ead8d60b8f059c8e5f0b4b82853f021d0f2c24504`  
		Last Modified: Sat, 22 Feb 2025 01:29:31 GMT  
		Size: 3.3 KB (3263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.0-dind-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:0931cacdc5870a73bd56837c9590fb9801af1b229cbf7ee86dc79c932a51323c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d14b9f57c5e9b67b594f4172c7cfbb95e2442a040e0bb090b09cc95ce2d35a18`

```dockerfile
```

-	Layers:
	-	`sha256:93150d2f1d44b19b0d6d36517e86cddc39cd49f0857f41bdb86a200f7db357e6`  
		Last Modified: Sat, 22 Feb 2025 01:29:30 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.0-dind-alpine3.21` - linux; arm variant v7

```console
$ docker pull docker@sha256:089424d7adbb66df8dd78e5ce27d9bd9d13cebe072cb5eb79e7478f00c124163
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (130009843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da65fa603f2dc74e8750fbdc3d7173e607ca901a8dfb81fab1136584884d3018`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_VERSION=28.0.0
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-amd64'; 			sha256='7f355525bfaf411302570b705118181b720f18071f4be3f0eaac7b2297d826e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v6'; 			sha256='f841251fd67646e8b6bb4c7e0c2c385f6a1dc7403f5ac6ee7b07c96f0815f7f3'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v7'; 			sha256='81d7040e90e9b69cb0378778f673e1fc2a24ef6dbd47931dc83ab6472fc5809d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm64'; 			sha256='42d5cee287ec7426de5252276a05f3ea565ac2d65d62d052b885a84dd54152d5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-ppc64le'; 			sha256='6a4e6a243f83d80cd46c939f327b2e14cfddd2c6690651cf48d0e208c3345b88'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-riscv64'; 			sha256='eae82aec74a420c3d1734123e6a3bc10b3a2a981aa1d538502373e31c91bf76e'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-s390x'; 			sha256='97b112b3366a471cc375e0f881d65a9a7b07f0962f308834c37f5c3fa75aad08'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 20 Feb 2025 06:04:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD ["sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
VOLUME [/var/lib/docker]
# Thu, 20 Feb 2025 06:04:43 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD []
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b654458a637c48c7f8f46da325ae8f810828e851ed4ab4b406092503eb680f`  
		Last Modified: Sat, 22 Feb 2025 00:28:04 GMT  
		Size: 7.3 MB (7299375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3474560bdd0e71f5972a48abd9e80877e2219f6eacae8272034d8503bcb634b2`  
		Last Modified: Sat, 22 Feb 2025 00:28:03 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ffc820c153872520700f2618e71ee9bea9cfee69fbff7b0ea4acb751a2fee5`  
		Last Modified: Sat, 22 Feb 2025 00:28:04 GMT  
		Size: 17.4 MB (17444426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a39a48e6818f4f7d6e7637cf221cc02da7b2e8ab3ca2643a527024430497175`  
		Last Modified: Sat, 22 Feb 2025 00:28:04 GMT  
		Size: 20.4 MB (20411656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168ce845c02246501347d9ae0d1bb9bb9f55a707c5ef03ba3bb6377e832c28f4`  
		Last Modified: Sat, 22 Feb 2025 00:28:05 GMT  
		Size: 19.7 MB (19708525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d62f1159ab01591fa3510e1ddc7b7e0313d001750472b1eaa0dcfb3a1f097732`  
		Last Modified: Sat, 22 Feb 2025 00:28:05 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ab9b1b4b0f9c261b260d739cd6d593a2c510b9c29045d72d930f2baf5fa78e`  
		Last Modified: Sat, 22 Feb 2025 00:28:05 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d27509dd9fc9bdb19051b5661dce75fc9b53979841bcd49fd03667b1ad6dde`  
		Last Modified: Sat, 22 Feb 2025 00:28:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd0d2a57f389ccbd627e0bca3b813e9397f4a6a55364b1f7cf22df043542cf1a`  
		Last Modified: Sat, 22 Feb 2025 04:54:52 GMT  
		Size: 6.4 MB (6366292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5947e3cbc6a2eb4d8c4ec17605876ea3e3a5cb2c09abac0a58d53cc4d6569f7`  
		Last Modified: Sat, 22 Feb 2025 04:54:51 GMT  
		Size: 86.3 KB (86342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc1fa6b8e4e654268e5dfc6afa5b1e88bfb92da3c33018f231f76ad7e08a59e`  
		Last Modified: Sat, 22 Feb 2025 04:54:51 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f544c5574adf21ca185480beea8b120134f2ed74f3f2418dc0ef564a3891490`  
		Last Modified: Sat, 22 Feb 2025 04:54:53 GMT  
		Size: 55.6 MB (55587054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd1c8be29e89fc14e8cd0778dcda3dae4c641d9ab956b2f9ce8d02df1d7984e`  
		Last Modified: Sat, 22 Feb 2025 04:54:52 GMT  
		Size: 1.6 KB (1636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db5e7511235a55ebe7a92c8825189d27a2b1d951e0f25d22e4e932636abbd466`  
		Last Modified: Sat, 22 Feb 2025 04:54:52 GMT  
		Size: 3.3 KB (3256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.0-dind-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:1cdaa27022a39a251e498044fefc2f4160913794dc50a3074935741e0d39d28b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:643a439611cab3be1c6fde6e85ec369c205d94c81b88f1c91a627a32a6448b32`

```dockerfile
```

-	Layers:
	-	`sha256:fa998948cfd33a55b2120a90b998117bea32698c81f84e340fc1f9fa359825c4`  
		Last Modified: Sat, 22 Feb 2025 04:54:51 GMT  
		Size: 34.8 KB (34765 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.0-dind-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:af92e15294f197a3cc4de0e75e012f4e91a996e4fd58ad96e163208aea7f0be3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.4 MB (132399422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89d922b5c31bca4bc340632485ab5243809aaf557e7aaf377fd956c15f4ad0a6`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_VERSION=28.0.0
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-amd64'; 			sha256='7f355525bfaf411302570b705118181b720f18071f4be3f0eaac7b2297d826e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v6'; 			sha256='f841251fd67646e8b6bb4c7e0c2c385f6a1dc7403f5ac6ee7b07c96f0815f7f3'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v7'; 			sha256='81d7040e90e9b69cb0378778f673e1fc2a24ef6dbd47931dc83ab6472fc5809d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm64'; 			sha256='42d5cee287ec7426de5252276a05f3ea565ac2d65d62d052b885a84dd54152d5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-ppc64le'; 			sha256='6a4e6a243f83d80cd46c939f327b2e14cfddd2c6690651cf48d0e208c3345b88'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-riscv64'; 			sha256='eae82aec74a420c3d1734123e6a3bc10b3a2a981aa1d538502373e31c91bf76e'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-s390x'; 			sha256='97b112b3366a471cc375e0f881d65a9a7b07f0962f308834c37f5c3fa75aad08'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 20 Feb 2025 06:04:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD ["sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
VOLUME [/var/lib/docker]
# Thu, 20 Feb 2025 06:04:43 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD []
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:076f26e7389ad2e79a31e03589b2c6943495faa94ce7fc6ecd800dd0c320c71e`  
		Last Modified: Sat, 22 Feb 2025 00:28:38 GMT  
		Size: 8.1 MB (8076430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54483e7ea72052e991e704ef33b6d45d32f2c9886445d70ae79e50a2dd444147`  
		Last Modified: Sat, 22 Feb 2025 00:28:37 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d747fdfb37d0ca59992c4852cab088ffb4549e3f8ef7632b252452c1c12c7989`  
		Last Modified: Sat, 22 Feb 2025 00:28:38 GMT  
		Size: 18.4 MB (18412791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84912acd39dd03fae2cffdb073ec52df5d17e2700910653a8c844d31a916a7eb`  
		Last Modified: Sat, 22 Feb 2025 00:28:39 GMT  
		Size: 20.0 MB (20041446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49191a7f2e90fd89997d49d48799f225e27d4d811c1ab6a1a5ed18c8b5a9f94`  
		Last Modified: Sat, 22 Feb 2025 00:28:40 GMT  
		Size: 19.2 MB (19222674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7debd3993d0af81423e3290841931e4b162ff882877ebb292b10f3dde6dc5694`  
		Last Modified: Sat, 22 Feb 2025 00:28:39 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855282ceddcfc470897f6e2cb33f2ad4742db7c00f24a0386714c91a31a090fa`  
		Last Modified: Sat, 22 Feb 2025 00:28:40 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fbaf9714c72f8c1c56eb53405de18b5c63f82fcfa89814a71a92c9844e1fb8b`  
		Last Modified: Sat, 22 Feb 2025 00:28:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f1efb7aef297fc62aaca013f0102b13d4fb2bd1eb6e39c858c91c440c973f87`  
		Last Modified: Sat, 22 Feb 2025 02:46:00 GMT  
		Size: 7.0 MB (6978850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d301065fd8bf09964f1efc59488efd3c692d574aae6e2460fefc3dac799912b`  
		Last Modified: Sat, 22 Feb 2025 02:46:00 GMT  
		Size: 99.4 KB (99390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d33e0f749652bb606f1e92e433cb70fa6c8e7a30737050979d975e9f06a132f`  
		Last Modified: Sat, 22 Feb 2025 02:45:59 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a409b11008465c3cb7523e669b4d2a064619125185de982089bf11944cf62502`  
		Last Modified: Sat, 22 Feb 2025 02:46:01 GMT  
		Size: 55.6 MB (55566753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff8cdce63f040e68fff768b8a75d7ebdd3f4cd4e69ed0f85ae0ad620baa9c40`  
		Last Modified: Sat, 22 Feb 2025 02:46:00 GMT  
		Size: 1.6 KB (1636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f72a632b800deed0be1fc7ec78852db28106ae059a841b87a966fed6ec7255f`  
		Last Modified: Sat, 22 Feb 2025 02:46:01 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.0-dind-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:d6dd49a97960eaef409aa41f89cf8596c02281b55801b3f726b267761031bc90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4105199c766800ff78dca393a5dccdb1435364291ecf731c31deacb4fa6e86a4`

```dockerfile
```

-	Layers:
	-	`sha256:2f7e554767be7baf2d46a3652bbe4405cdcb83972440eb83c19280ab0e991188`  
		Last Modified: Sat, 22 Feb 2025 02:45:59 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.0.0-dind-rootless`

```console
$ docker pull docker@sha256:f36f8f41d9e38bae8c3d247446a1e31df98bd84d1ccc22d9d8d50fbe6cbafae8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:28.0.0-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:16356585ff8acaa68e6bd54dd11f6760ce507fa719fe7e00bc7db05f53c7a074
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.2 MB (159160666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f413ddafbf744ab3b46d57ab5bda7d4b4ed64aa0ac7f3bd49a3055f8aa5c604`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_VERSION=28.0.0
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-amd64'; 			sha256='7f355525bfaf411302570b705118181b720f18071f4be3f0eaac7b2297d826e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v6'; 			sha256='f841251fd67646e8b6bb4c7e0c2c385f6a1dc7403f5ac6ee7b07c96f0815f7f3'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v7'; 			sha256='81d7040e90e9b69cb0378778f673e1fc2a24ef6dbd47931dc83ab6472fc5809d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm64'; 			sha256='42d5cee287ec7426de5252276a05f3ea565ac2d65d62d052b885a84dd54152d5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-ppc64le'; 			sha256='6a4e6a243f83d80cd46c939f327b2e14cfddd2c6690651cf48d0e208c3345b88'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-riscv64'; 			sha256='eae82aec74a420c3d1734123e6a3bc10b3a2a981aa1d538502373e31c91bf76e'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-s390x'; 			sha256='97b112b3366a471cc375e0f881d65a9a7b07f0962f308834c37f5c3fa75aad08'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 20 Feb 2025 06:04:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD ["sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
VOLUME [/var/lib/docker]
# Thu, 20 Feb 2025 06:04:43 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD []
# Thu, 20 Feb 2025 06:04:43 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 20 Feb 2025 06:04:43 GMT
USER rootless
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fddc498219722db61fe7f7e06295aa8b64f7e48d19d0339176689ea591eea4ca`  
		Last Modified: Sat, 22 Feb 2025 00:27:26 GMT  
		Size: 8.1 MB (8062985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c17b75175e66b76074511db7ebd5bdc56ac19ba269d30e4f58ba4812816ad4`  
		Last Modified: Sat, 22 Feb 2025 00:27:26 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987b6d8519d32209785b3840639a10aa6247ff1e290a651ebcca3d8c33e23dd2`  
		Last Modified: Sat, 22 Feb 2025 00:27:27 GMT  
		Size: 19.5 MB (19492233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7677267af1ddfc39dbdf35dcdca7c20328e83a42b64595f0d5880c62e99a91f`  
		Last Modified: Sat, 22 Feb 2025 00:27:27 GMT  
		Size: 21.8 MB (21829139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9fa9f5140fd1401e5edaa2de6f975bd14f0b79efbafbe0d2497ea0213ecd260`  
		Last Modified: Sat, 22 Feb 2025 00:27:27 GMT  
		Size: 21.0 MB (20958635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124bcf7a51a8a140479ebb1cfd0aea5bf38223d37b7c6ae1deb93bbb1abc0469`  
		Last Modified: Sat, 22 Feb 2025 00:27:28 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3083b3dfd2242fbeb7b498bb2e0d99d55c8e34cad7396573784aa86db3c69355`  
		Last Modified: Sat, 22 Feb 2025 00:27:28 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b255e6bd488c8fb61ba962afb512c02077ecc7e41b50991cb3229aaa7ae94b`  
		Last Modified: Sat, 22 Feb 2025 00:27:28 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42458739bc4b2677f265360a10a2eacffd5133b0242dd313ba8a3dac7a116c4`  
		Last Modified: Sat, 22 Feb 2025 01:08:23 GMT  
		Size: 6.7 MB (6733003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5a7650793a22cfeac45c6610fe2cd3ccd26b6795d33ee5389d66a174c05a65`  
		Last Modified: Sat, 22 Feb 2025 01:08:23 GMT  
		Size: 90.3 KB (90318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03749f129a866bd1cf2e2797db758f883cf177f3cd33ff3c60924ec811728b4f`  
		Last Modified: Sat, 22 Feb 2025 01:08:23 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:769e1c97b1855704d1f74c39b30c2d2bbc890339752b2be542477e64d2529c32`  
		Last Modified: Sat, 22 Feb 2025 01:08:24 GMT  
		Size: 60.2 MB (60189735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e450e39e6d5b103505878dd35ff532dcdfef40450540495b6a666e7bc34e2587`  
		Last Modified: Sat, 22 Feb 2025 01:08:23 GMT  
		Size: 1.6 KB (1637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254862f49c6f0929e44b00f9635661aff98a508d2dc321d6ddc2944f60ac90bb`  
		Last Modified: Sat, 22 Feb 2025 01:08:23 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04d666bba697d05e04595251efc48c7cfb46c50934eb5e8b28f9ece93bbaa12f`  
		Last Modified: Sat, 22 Feb 2025 02:08:04 GMT  
		Size: 986.6 KB (986572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9e9040036c95835735c8d16482226c61fd43befb113e4654d11899b4c82c24`  
		Last Modified: Sat, 22 Feb 2025 02:08:04 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c773fc7dad6ddd06fd1b5c0d2b81528878a1c879bcfed7b967fed225ec4346a7`  
		Last Modified: Sat, 22 Feb 2025 02:08:04 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce0abea1fd4caba2bf7cfa1eaab27c1e81060389830353f7de69a562c0d129f3`  
		Last Modified: Sat, 22 Feb 2025 02:08:05 GMT  
		Size: 17.2 MB (17166401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e73037866943973bf1a62ff0acb7da9d1f19cc8ff52edb6c2ddf748fba1507`  
		Last Modified: Sat, 22 Feb 2025 02:08:05 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.0-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:788f83bf8b427ca8d5db790b94b5465dd4e729d19870cf23c0a99aa2247419e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:171bb75448d4664abab1f0e5b2859c6858afa3eaf4bbe30c4ff52221ef9588a5`

```dockerfile
```

-	Layers:
	-	`sha256:681e1874c769bcd3cc3a0fe90e1caa86a29f1a172fc7caa3eb5c75bb6e9843e7`  
		Last Modified: Sat, 22 Feb 2025 02:08:03 GMT  
		Size: 30.5 KB (30451 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.0-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:73776940d20eac532ae279be7c72ff89ea730517ff9dab5a659516bc00d09dda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.7 MB (152694408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5b89ed4c42e88420300229e316f2cf5c30d71c0341b7ba4039b7887870e259b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_VERSION=28.0.0
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-amd64'; 			sha256='7f355525bfaf411302570b705118181b720f18071f4be3f0eaac7b2297d826e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v6'; 			sha256='f841251fd67646e8b6bb4c7e0c2c385f6a1dc7403f5ac6ee7b07c96f0815f7f3'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v7'; 			sha256='81d7040e90e9b69cb0378778f673e1fc2a24ef6dbd47931dc83ab6472fc5809d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm64'; 			sha256='42d5cee287ec7426de5252276a05f3ea565ac2d65d62d052b885a84dd54152d5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-ppc64le'; 			sha256='6a4e6a243f83d80cd46c939f327b2e14cfddd2c6690651cf48d0e208c3345b88'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-riscv64'; 			sha256='eae82aec74a420c3d1734123e6a3bc10b3a2a981aa1d538502373e31c91bf76e'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-s390x'; 			sha256='97b112b3366a471cc375e0f881d65a9a7b07f0962f308834c37f5c3fa75aad08'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 20 Feb 2025 06:04:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD ["sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
VOLUME [/var/lib/docker]
# Thu, 20 Feb 2025 06:04:43 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD []
# Thu, 20 Feb 2025 06:04:43 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 20 Feb 2025 06:04:43 GMT
USER rootless
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:076f26e7389ad2e79a31e03589b2c6943495faa94ce7fc6ecd800dd0c320c71e`  
		Last Modified: Sat, 22 Feb 2025 00:28:38 GMT  
		Size: 8.1 MB (8076430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54483e7ea72052e991e704ef33b6d45d32f2c9886445d70ae79e50a2dd444147`  
		Last Modified: Sat, 22 Feb 2025 00:28:37 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d747fdfb37d0ca59992c4852cab088ffb4549e3f8ef7632b252452c1c12c7989`  
		Last Modified: Sat, 22 Feb 2025 00:28:38 GMT  
		Size: 18.4 MB (18412791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84912acd39dd03fae2cffdb073ec52df5d17e2700910653a8c844d31a916a7eb`  
		Last Modified: Sat, 22 Feb 2025 00:28:39 GMT  
		Size: 20.0 MB (20041446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49191a7f2e90fd89997d49d48799f225e27d4d811c1ab6a1a5ed18c8b5a9f94`  
		Last Modified: Sat, 22 Feb 2025 00:28:40 GMT  
		Size: 19.2 MB (19222674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7debd3993d0af81423e3290841931e4b162ff882877ebb292b10f3dde6dc5694`  
		Last Modified: Sat, 22 Feb 2025 00:28:39 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855282ceddcfc470897f6e2cb33f2ad4742db7c00f24a0386714c91a31a090fa`  
		Last Modified: Sat, 22 Feb 2025 00:28:40 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fbaf9714c72f8c1c56eb53405de18b5c63f82fcfa89814a71a92c9844e1fb8b`  
		Last Modified: Sat, 22 Feb 2025 00:28:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f1efb7aef297fc62aaca013f0102b13d4fb2bd1eb6e39c858c91c440c973f87`  
		Last Modified: Sat, 22 Feb 2025 02:46:00 GMT  
		Size: 7.0 MB (6978850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d301065fd8bf09964f1efc59488efd3c692d574aae6e2460fefc3dac799912b`  
		Last Modified: Sat, 22 Feb 2025 02:46:00 GMT  
		Size: 99.4 KB (99390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d33e0f749652bb606f1e92e433cb70fa6c8e7a30737050979d975e9f06a132f`  
		Last Modified: Sat, 22 Feb 2025 02:45:59 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a409b11008465c3cb7523e669b4d2a064619125185de982089bf11944cf62502`  
		Last Modified: Sat, 22 Feb 2025 02:46:01 GMT  
		Size: 55.6 MB (55566753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff8cdce63f040e68fff768b8a75d7ebdd3f4cd4e69ed0f85ae0ad620baa9c40`  
		Last Modified: Sat, 22 Feb 2025 02:46:00 GMT  
		Size: 1.6 KB (1636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f72a632b800deed0be1fc7ec78852db28106ae059a841b87a966fed6ec7255f`  
		Last Modified: Sat, 22 Feb 2025 02:46:01 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4468cca51cdd29ea280bb7c9d7dcffc805ae2134d5d10101acabb31403f19c34`  
		Last Modified: Sat, 22 Feb 2025 03:07:17 GMT  
		Size: 1.0 MB (1014200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d43f7cfe0c5e55bc699a2f0f56e6ecd213c0d84783892175a2bbabe01e1ee1`  
		Last Modified: Sat, 22 Feb 2025 03:07:17 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ffc8590ff3cdff71a791e5dd600d08fee46a9a23862330e1c51e7fe2953e3c`  
		Last Modified: Sat, 22 Feb 2025 03:07:17 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b03647ba73f1a14d321c6973445bfedd81d7195d0c270c2a52d81c4bd00241ec`  
		Last Modified: Sat, 22 Feb 2025 03:07:18 GMT  
		Size: 19.3 MB (19279443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42024c25dd02ca9c645e8270327928627cf8b2d1ce95c86e3184f7236d8254b3`  
		Last Modified: Sat, 22 Feb 2025 03:07:18 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.0-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:7caef0d171c210bbc06a3c6c5f181d699cdab3868ed8201206157f5ce2b26b41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66ce0dd66d759a7501d703e2bd782cf6c3190278388bb80297dd5fdc65839c39`

```dockerfile
```

-	Layers:
	-	`sha256:f29410d962e3aeed18fdb7f16f7e72ba75bab67d36d78eaa1f5bb9e00bee589a`  
		Last Modified: Sat, 22 Feb 2025 03:07:17 GMT  
		Size: 30.6 KB (30621 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.0.0-windowsservercore`

```console
$ docker pull docker@sha256:8cbb71e3463881e43b4e46000916a151f195288cba0ad77f0eabef966bc5d438
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

### `docker:28.0.0-windowsservercore` - windows version 10.0.26100.2894; amd64

```console
$ docker pull docker@sha256:13348bcc4ed6fcd578c6aea25afa087bac0759457ff724c916d2fb3624c804ba
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2565217611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:172682bc22fc40249839b093831f2ccdb06d47eda95530dd64db1bf9bba03ee5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Sat, 22 Feb 2025 00:31:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 22 Feb 2025 00:31:31 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 22 Feb 2025 00:31:31 GMT
ENV DOCKER_VERSION=28.0.0
# Sat, 22 Feb 2025 00:31:32 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.0.zip
# Sat, 22 Feb 2025 00:31:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 22 Feb 2025 00:31:42 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Sat, 22 Feb 2025 00:31:42 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.windows-amd64.exe
# Sat, 22 Feb 2025 00:31:43 GMT
ENV DOCKER_BUILDX_SHA256=ab3eba3acbfa6b6612690af075795254f29762efc8abace5f636b8e7628b1851
# Sat, 22 Feb 2025 00:31:51 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 22 Feb 2025 00:31:52 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Sat, 22 Feb 2025 00:31:53 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-windows-x86_64.exe
# Sat, 22 Feb 2025 00:31:53 GMT
ENV DOCKER_COMPOSE_SHA256=01bce3456228d8e1e4b0ba056f4b9730b7fd2c1a7113c8a985144c0fdee797b0
# Sat, 22 Feb 2025 00:32:02 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Tue, 14 Jan 2025 18:53:06 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b538b630814b004320f0f9ee0a9c3594e03b773b5580fed4105a81f74e7c098f`  
		Last Modified: Sat, 22 Feb 2025 00:32:07 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58e25b87bc1505ec562cf342b28ce02166b0c50e250e5b111cae842bd29224a6`  
		Last Modified: Sat, 22 Feb 2025 00:32:08 GMT  
		Size: 382.4 KB (382390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54dec53b66cd21d806f4ecb36e798d52785171b19a3b94a2886816c4b00fc357`  
		Last Modified: Sat, 22 Feb 2025 00:32:07 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:173311079ab932318629c9bfc59957c46ffef6d9500148722bf57885ab4d912e`  
		Last Modified: Sat, 22 Feb 2025 00:32:07 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5ef5273358e9d6949b1c0c7a006b2fe22a9b45af8454771a753c47f67702fc5`  
		Last Modified: Sat, 22 Feb 2025 00:32:09 GMT  
		Size: 19.8 MB (19841357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6550ae8a0cab9e35d0c0177c6afc594dd1f53008f4c0b85bdca771700fa770c`  
		Last Modified: Sat, 22 Feb 2025 00:32:06 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e430e1223ff0212bf349270e614e999171df037e89b09997ff907efa689e97d`  
		Last Modified: Sat, 22 Feb 2025 00:32:06 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adf1c042512ab6127e6371768343f9e2125e122a97350d29044867620964da29`  
		Last Modified: Sat, 22 Feb 2025 00:32:05 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbcc9f9bc1cf9f00d67c29fcbf84300c45479de6c73cf2f49f1ae660cf73bb07`  
		Last Modified: Sat, 22 Feb 2025 00:32:08 GMT  
		Size: 22.8 MB (22778890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b21becac3572331f658c564c93303ec2f6d01292e600e1b7deab5fea30b05ff6`  
		Last Modified: Sat, 22 Feb 2025 00:32:05 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e856f770850ac4d1cb287a7e7807f001c6f669a135f306ccf2fe6e63129def66`  
		Last Modified: Sat, 22 Feb 2025 00:32:05 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e457e71b003d1ce3d61f1df1c12e7500d728f4b5598604334164ddb533cb2ba`  
		Last Modified: Sat, 22 Feb 2025 00:32:05 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f63f581bda80c595a4087c00b71030e7a4d71012bb05cbc2eb9c139f9679e31`  
		Last Modified: Sat, 22 Feb 2025 00:32:08 GMT  
		Size: 21.9 MB (21925519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28.0.0-windowsservercore` - windows version 10.0.20348.3207; amd64

```console
$ docker pull docker@sha256:40cac7c487ab96fd2608d22182da86766f98f6f8726e4a9cc87f61fba1c79f0e
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2328776516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a7dc1af03d6c94095c7be69ba1d7ffcba2c6ddbf201a1901bafc1445c1d7615`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Sat, 22 Feb 2025 00:37:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 22 Feb 2025 00:37:49 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 22 Feb 2025 00:37:49 GMT
ENV DOCKER_VERSION=28.0.0
# Sat, 22 Feb 2025 00:37:50 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.0.zip
# Sat, 22 Feb 2025 00:38:01 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 22 Feb 2025 00:38:01 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Sat, 22 Feb 2025 00:38:02 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.windows-amd64.exe
# Sat, 22 Feb 2025 00:38:02 GMT
ENV DOCKER_BUILDX_SHA256=ab3eba3acbfa6b6612690af075795254f29762efc8abace5f636b8e7628b1851
# Sat, 22 Feb 2025 00:38:11 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 22 Feb 2025 00:38:12 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Sat, 22 Feb 2025 00:38:13 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-windows-x86_64.exe
# Sat, 22 Feb 2025 00:38:13 GMT
ENV DOCKER_COMPOSE_SHA256=01bce3456228d8e1e4b0ba056f4b9730b7fd2c1a7113c8a985144c0fdee797b0
# Sat, 22 Feb 2025 00:38:22 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Tue, 11 Feb 2025 18:38:32 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a513c2ebb5aac6eaccc568c460584aa652a09401a4f865e8b1a9870e4f9826d`  
		Last Modified: Sat, 22 Feb 2025 00:38:28 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f0ea743d1a5ae5f5f7088a7c23ca759ec9b363ca46d674d9e7425aa27739ba`  
		Last Modified: Sat, 22 Feb 2025 00:38:27 GMT  
		Size: 389.0 KB (388984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:401dea1d9556118c14843e687f7eb2f2767205cefe7c534ce370103f7bb4520c`  
		Last Modified: Sat, 22 Feb 2025 00:38:27 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ff218fd9efd93054faba12c9de123bd815f47af0057f0822bebe1980b506039`  
		Last Modified: Sat, 22 Feb 2025 00:38:26 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef9e343cb24c4c76e4c3fbbf11fa22c10da7fea8e22f98be5493a15840e79f6`  
		Last Modified: Sat, 22 Feb 2025 00:38:28 GMT  
		Size: 19.8 MB (19832408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b072185e609fe777fbfd0d1c7e0860cfd307e8d0718c19365cbe22f499636207`  
		Last Modified: Sat, 22 Feb 2025 00:38:26 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a89b4e620aaf525ac2545408e3d49037c7d5b8c99ee26edb1937e8a2a5c181c`  
		Last Modified: Sat, 22 Feb 2025 00:38:25 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7edf322adba1ba7c101c710b53b2f04cb139c273b95e29fcc5d8943f581af167`  
		Last Modified: Sat, 22 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c220811a807867c0315d6291b99472e043388fe4f317d60dcb70cf42963b333`  
		Last Modified: Sat, 22 Feb 2025 00:38:27 GMT  
		Size: 22.8 MB (22770286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a73d03430d6958d170ed89b00d83fa15b1b28a9aa22fbd4ae9018b5671cb08f6`  
		Last Modified: Sat, 22 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:164bc468207a3b25ae55b075dc0b5987de3ca0d425be73ff7f45fe57b49f807f`  
		Last Modified: Sat, 22 Feb 2025 00:38:24 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7307712a7f1b1601e8cf9b306574434f960222e78bb80360573ae2829c165ab9`  
		Last Modified: Sat, 22 Feb 2025 00:38:24 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ff623c1936592d4e22a10ac22c1ba99d55a4c960680df6e5e9da20450cf85d`  
		Last Modified: Sat, 22 Feb 2025 00:38:27 GMT  
		Size: 21.9 MB (21914957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28.0.0-windowsservercore` - windows version 10.0.17763.6893; amd64

```console
$ docker pull docker@sha256:575fd688c3bf866a95546fe93e2564fea753d26e5931ebfc1e32ebd9bc411358
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2201693889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47afabbd0d9bf289e87beda973d92a82859b49c2b2f83325e44032f22df554d7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Sat, 22 Feb 2025 00:36:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 22 Feb 2025 00:37:03 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 22 Feb 2025 00:37:04 GMT
ENV DOCKER_VERSION=28.0.0
# Sat, 22 Feb 2025 00:37:05 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.0.zip
# Sat, 22 Feb 2025 00:37:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 22 Feb 2025 00:37:18 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Sat, 22 Feb 2025 00:37:18 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.windows-amd64.exe
# Sat, 22 Feb 2025 00:37:19 GMT
ENV DOCKER_BUILDX_SHA256=ab3eba3acbfa6b6612690af075795254f29762efc8abace5f636b8e7628b1851
# Sat, 22 Feb 2025 00:37:28 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 22 Feb 2025 00:37:29 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Sat, 22 Feb 2025 00:37:30 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-windows-x86_64.exe
# Sat, 22 Feb 2025 00:37:31 GMT
ENV DOCKER_COMPOSE_SHA256=01bce3456228d8e1e4b0ba056f4b9730b7fd2c1a7113c8a985144c0fdee797b0
# Sat, 22 Feb 2025 00:37:39 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 18:49:50 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d662e474d0eebcc45d26c962c3ea2815d5ad421c4abce3dfca970d20d34206`  
		Last Modified: Sat, 22 Feb 2025 00:37:45 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b80c05d72492cc29e69146de42b5cbab7c6912ef3a85c579caaf8ccb3b7eabb9`  
		Last Modified: Sat, 22 Feb 2025 00:37:44 GMT  
		Size: 343.2 KB (343235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df0623e2321e34b1b589a3f2314cdc767fe978372d17c7d621c1b6e40645f0e2`  
		Last Modified: Sat, 22 Feb 2025 00:37:44 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177b2d1a530b8667811479317d9e8ae2eb9cf1e26892e886e4baa298209fcfa4`  
		Last Modified: Sat, 22 Feb 2025 00:37:44 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3834ee7310198b95517a8b510904c8f38cbdb7c49df0b228572059fee55faa4`  
		Last Modified: Sat, 22 Feb 2025 00:37:46 GMT  
		Size: 19.8 MB (19805126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7d9cad94e2d870741143d557fc15084b8f7f0c3f510618f76861f6c020ec0c`  
		Last Modified: Sat, 22 Feb 2025 00:37:43 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73e623554754f1c6df8e43e93e867af1218d203b9111a1b977befbc4542f33e`  
		Last Modified: Sat, 22 Feb 2025 00:37:43 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39746d0ab1fefcec984bb203b47fb43af6294430288792c106045708180cf90f`  
		Last Modified: Sat, 22 Feb 2025 00:37:43 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb7e0de055ddbb75c2d00fd897c8e623d5d164e9da002c14c5d7b16034ddefb2`  
		Last Modified: Sat, 22 Feb 2025 00:37:45 GMT  
		Size: 22.7 MB (22743044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d103e4264cc2326442d2f2c0d9a6f8a6d63672a9e1888b0eb106211fe4c866a8`  
		Last Modified: Sat, 22 Feb 2025 00:37:42 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e7898abd14f1e9f5aaa3850e26c6e47b5af14ccc7727ace668f06058bb6bbbb`  
		Last Modified: Sat, 22 Feb 2025 00:37:42 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac30b7d53b77634caea695af70ca54fad87eec4119c5d63afcd64b762dadee9f`  
		Last Modified: Sat, 22 Feb 2025 00:37:42 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a13d827d5d10e25d56e691281a38fb310acbe73a53d8ecb6c27a3c737305b83d`  
		Last Modified: Sat, 22 Feb 2025 00:37:44 GMT  
		Size: 21.9 MB (21881997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.0.0-windowsservercore-1809`

```console
$ docker pull docker@sha256:8b5e611771751fe8360ccf0f5bb3b6c022a079599c9e8dada6351d3682c645b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `docker:28.0.0-windowsservercore-1809` - windows version 10.0.17763.6893; amd64

```console
$ docker pull docker@sha256:575fd688c3bf866a95546fe93e2564fea753d26e5931ebfc1e32ebd9bc411358
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2201693889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47afabbd0d9bf289e87beda973d92a82859b49c2b2f83325e44032f22df554d7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Sat, 22 Feb 2025 00:36:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 22 Feb 2025 00:37:03 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 22 Feb 2025 00:37:04 GMT
ENV DOCKER_VERSION=28.0.0
# Sat, 22 Feb 2025 00:37:05 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.0.zip
# Sat, 22 Feb 2025 00:37:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 22 Feb 2025 00:37:18 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Sat, 22 Feb 2025 00:37:18 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.windows-amd64.exe
# Sat, 22 Feb 2025 00:37:19 GMT
ENV DOCKER_BUILDX_SHA256=ab3eba3acbfa6b6612690af075795254f29762efc8abace5f636b8e7628b1851
# Sat, 22 Feb 2025 00:37:28 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 22 Feb 2025 00:37:29 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Sat, 22 Feb 2025 00:37:30 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-windows-x86_64.exe
# Sat, 22 Feb 2025 00:37:31 GMT
ENV DOCKER_COMPOSE_SHA256=01bce3456228d8e1e4b0ba056f4b9730b7fd2c1a7113c8a985144c0fdee797b0
# Sat, 22 Feb 2025 00:37:39 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 18:49:50 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d662e474d0eebcc45d26c962c3ea2815d5ad421c4abce3dfca970d20d34206`  
		Last Modified: Sat, 22 Feb 2025 00:37:45 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b80c05d72492cc29e69146de42b5cbab7c6912ef3a85c579caaf8ccb3b7eabb9`  
		Last Modified: Sat, 22 Feb 2025 00:37:44 GMT  
		Size: 343.2 KB (343235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df0623e2321e34b1b589a3f2314cdc767fe978372d17c7d621c1b6e40645f0e2`  
		Last Modified: Sat, 22 Feb 2025 00:37:44 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177b2d1a530b8667811479317d9e8ae2eb9cf1e26892e886e4baa298209fcfa4`  
		Last Modified: Sat, 22 Feb 2025 00:37:44 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3834ee7310198b95517a8b510904c8f38cbdb7c49df0b228572059fee55faa4`  
		Last Modified: Sat, 22 Feb 2025 00:37:46 GMT  
		Size: 19.8 MB (19805126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7d9cad94e2d870741143d557fc15084b8f7f0c3f510618f76861f6c020ec0c`  
		Last Modified: Sat, 22 Feb 2025 00:37:43 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73e623554754f1c6df8e43e93e867af1218d203b9111a1b977befbc4542f33e`  
		Last Modified: Sat, 22 Feb 2025 00:37:43 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39746d0ab1fefcec984bb203b47fb43af6294430288792c106045708180cf90f`  
		Last Modified: Sat, 22 Feb 2025 00:37:43 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb7e0de055ddbb75c2d00fd897c8e623d5d164e9da002c14c5d7b16034ddefb2`  
		Last Modified: Sat, 22 Feb 2025 00:37:45 GMT  
		Size: 22.7 MB (22743044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d103e4264cc2326442d2f2c0d9a6f8a6d63672a9e1888b0eb106211fe4c866a8`  
		Last Modified: Sat, 22 Feb 2025 00:37:42 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e7898abd14f1e9f5aaa3850e26c6e47b5af14ccc7727ace668f06058bb6bbbb`  
		Last Modified: Sat, 22 Feb 2025 00:37:42 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac30b7d53b77634caea695af70ca54fad87eec4119c5d63afcd64b762dadee9f`  
		Last Modified: Sat, 22 Feb 2025 00:37:42 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a13d827d5d10e25d56e691281a38fb310acbe73a53d8ecb6c27a3c737305b83d`  
		Last Modified: Sat, 22 Feb 2025 00:37:44 GMT  
		Size: 21.9 MB (21881997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.0.0-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:4a4531319a3d77d264dd66e0056a37a0ce12653a767680d3114dc86e6d50de94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3207; amd64

### `docker:28.0.0-windowsservercore-ltsc2022` - windows version 10.0.20348.3207; amd64

```console
$ docker pull docker@sha256:40cac7c487ab96fd2608d22182da86766f98f6f8726e4a9cc87f61fba1c79f0e
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2328776516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a7dc1af03d6c94095c7be69ba1d7ffcba2c6ddbf201a1901bafc1445c1d7615`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Sat, 22 Feb 2025 00:37:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 22 Feb 2025 00:37:49 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 22 Feb 2025 00:37:49 GMT
ENV DOCKER_VERSION=28.0.0
# Sat, 22 Feb 2025 00:37:50 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.0.zip
# Sat, 22 Feb 2025 00:38:01 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 22 Feb 2025 00:38:01 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Sat, 22 Feb 2025 00:38:02 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.windows-amd64.exe
# Sat, 22 Feb 2025 00:38:02 GMT
ENV DOCKER_BUILDX_SHA256=ab3eba3acbfa6b6612690af075795254f29762efc8abace5f636b8e7628b1851
# Sat, 22 Feb 2025 00:38:11 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 22 Feb 2025 00:38:12 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Sat, 22 Feb 2025 00:38:13 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-windows-x86_64.exe
# Sat, 22 Feb 2025 00:38:13 GMT
ENV DOCKER_COMPOSE_SHA256=01bce3456228d8e1e4b0ba056f4b9730b7fd2c1a7113c8a985144c0fdee797b0
# Sat, 22 Feb 2025 00:38:22 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Tue, 11 Feb 2025 18:38:32 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a513c2ebb5aac6eaccc568c460584aa652a09401a4f865e8b1a9870e4f9826d`  
		Last Modified: Sat, 22 Feb 2025 00:38:28 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f0ea743d1a5ae5f5f7088a7c23ca759ec9b363ca46d674d9e7425aa27739ba`  
		Last Modified: Sat, 22 Feb 2025 00:38:27 GMT  
		Size: 389.0 KB (388984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:401dea1d9556118c14843e687f7eb2f2767205cefe7c534ce370103f7bb4520c`  
		Last Modified: Sat, 22 Feb 2025 00:38:27 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ff218fd9efd93054faba12c9de123bd815f47af0057f0822bebe1980b506039`  
		Last Modified: Sat, 22 Feb 2025 00:38:26 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef9e343cb24c4c76e4c3fbbf11fa22c10da7fea8e22f98be5493a15840e79f6`  
		Last Modified: Sat, 22 Feb 2025 00:38:28 GMT  
		Size: 19.8 MB (19832408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b072185e609fe777fbfd0d1c7e0860cfd307e8d0718c19365cbe22f499636207`  
		Last Modified: Sat, 22 Feb 2025 00:38:26 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a89b4e620aaf525ac2545408e3d49037c7d5b8c99ee26edb1937e8a2a5c181c`  
		Last Modified: Sat, 22 Feb 2025 00:38:25 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7edf322adba1ba7c101c710b53b2f04cb139c273b95e29fcc5d8943f581af167`  
		Last Modified: Sat, 22 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c220811a807867c0315d6291b99472e043388fe4f317d60dcb70cf42963b333`  
		Last Modified: Sat, 22 Feb 2025 00:38:27 GMT  
		Size: 22.8 MB (22770286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a73d03430d6958d170ed89b00d83fa15b1b28a9aa22fbd4ae9018b5671cb08f6`  
		Last Modified: Sat, 22 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:164bc468207a3b25ae55b075dc0b5987de3ca0d425be73ff7f45fe57b49f807f`  
		Last Modified: Sat, 22 Feb 2025 00:38:24 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7307712a7f1b1601e8cf9b306574434f960222e78bb80360573ae2829c165ab9`  
		Last Modified: Sat, 22 Feb 2025 00:38:24 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ff623c1936592d4e22a10ac22c1ba99d55a4c960680df6e5e9da20450cf85d`  
		Last Modified: Sat, 22 Feb 2025 00:38:27 GMT  
		Size: 21.9 MB (21914957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.0.0-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:78307f6a713fd34f43a0d89127421c46b2ff65f06362768394f4e6612dc89989
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.2894; amd64

### `docker:28.0.0-windowsservercore-ltsc2025` - windows version 10.0.26100.2894; amd64

```console
$ docker pull docker@sha256:13348bcc4ed6fcd578c6aea25afa087bac0759457ff724c916d2fb3624c804ba
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2565217611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:172682bc22fc40249839b093831f2ccdb06d47eda95530dd64db1bf9bba03ee5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Sat, 22 Feb 2025 00:31:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 22 Feb 2025 00:31:31 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 22 Feb 2025 00:31:31 GMT
ENV DOCKER_VERSION=28.0.0
# Sat, 22 Feb 2025 00:31:32 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.0.zip
# Sat, 22 Feb 2025 00:31:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 22 Feb 2025 00:31:42 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Sat, 22 Feb 2025 00:31:42 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.windows-amd64.exe
# Sat, 22 Feb 2025 00:31:43 GMT
ENV DOCKER_BUILDX_SHA256=ab3eba3acbfa6b6612690af075795254f29762efc8abace5f636b8e7628b1851
# Sat, 22 Feb 2025 00:31:51 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 22 Feb 2025 00:31:52 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Sat, 22 Feb 2025 00:31:53 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-windows-x86_64.exe
# Sat, 22 Feb 2025 00:31:53 GMT
ENV DOCKER_COMPOSE_SHA256=01bce3456228d8e1e4b0ba056f4b9730b7fd2c1a7113c8a985144c0fdee797b0
# Sat, 22 Feb 2025 00:32:02 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Tue, 14 Jan 2025 18:53:06 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b538b630814b004320f0f9ee0a9c3594e03b773b5580fed4105a81f74e7c098f`  
		Last Modified: Sat, 22 Feb 2025 00:32:07 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58e25b87bc1505ec562cf342b28ce02166b0c50e250e5b111cae842bd29224a6`  
		Last Modified: Sat, 22 Feb 2025 00:32:08 GMT  
		Size: 382.4 KB (382390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54dec53b66cd21d806f4ecb36e798d52785171b19a3b94a2886816c4b00fc357`  
		Last Modified: Sat, 22 Feb 2025 00:32:07 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:173311079ab932318629c9bfc59957c46ffef6d9500148722bf57885ab4d912e`  
		Last Modified: Sat, 22 Feb 2025 00:32:07 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5ef5273358e9d6949b1c0c7a006b2fe22a9b45af8454771a753c47f67702fc5`  
		Last Modified: Sat, 22 Feb 2025 00:32:09 GMT  
		Size: 19.8 MB (19841357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6550ae8a0cab9e35d0c0177c6afc594dd1f53008f4c0b85bdca771700fa770c`  
		Last Modified: Sat, 22 Feb 2025 00:32:06 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e430e1223ff0212bf349270e614e999171df037e89b09997ff907efa689e97d`  
		Last Modified: Sat, 22 Feb 2025 00:32:06 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adf1c042512ab6127e6371768343f9e2125e122a97350d29044867620964da29`  
		Last Modified: Sat, 22 Feb 2025 00:32:05 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbcc9f9bc1cf9f00d67c29fcbf84300c45479de6c73cf2f49f1ae660cf73bb07`  
		Last Modified: Sat, 22 Feb 2025 00:32:08 GMT  
		Size: 22.8 MB (22778890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b21becac3572331f658c564c93303ec2f6d01292e600e1b7deab5fea30b05ff6`  
		Last Modified: Sat, 22 Feb 2025 00:32:05 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e856f770850ac4d1cb287a7e7807f001c6f669a135f306ccf2fe6e63129def66`  
		Last Modified: Sat, 22 Feb 2025 00:32:05 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e457e71b003d1ce3d61f1df1c12e7500d728f4b5598604334164ddb533cb2ba`  
		Last Modified: Sat, 22 Feb 2025 00:32:05 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f63f581bda80c595a4087c00b71030e7a4d71012bb05cbc2eb9c139f9679e31`  
		Last Modified: Sat, 22 Feb 2025 00:32:08 GMT  
		Size: 21.9 MB (21925519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:cli`

```console
$ docker pull docker@sha256:28fb556c1ea1eef2f1d8d70e8c7eb52e38324b2ae04ffcb8df26648a7c2e5dfc
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

### `docker:cli` - linux; amd64

```console
$ docker pull docker@sha256:828f4f57525db5dbdb2f52ba47087c383361fd22975c264142bab1ff78ea8587
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73987390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2047a2478c64769a8f8963db4efc714c734b9ec896b1452fb424720a232732d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 21 Feb 2025 18:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_VERSION=28.0.0
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-amd64'; 			sha256='7f355525bfaf411302570b705118181b720f18071f4be3f0eaac7b2297d826e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v6'; 			sha256='f841251fd67646e8b6bb4c7e0c2c385f6a1dc7403f5ac6ee7b07c96f0815f7f3'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v7'; 			sha256='81d7040e90e9b69cb0378778f673e1fc2a24ef6dbd47931dc83ab6472fc5809d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm64'; 			sha256='42d5cee287ec7426de5252276a05f3ea565ac2d65d62d052b885a84dd54152d5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-ppc64le'; 			sha256='6a4e6a243f83d80cd46c939f327b2e14cfddd2c6690651cf48d0e208c3345b88'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-riscv64'; 			sha256='eae82aec74a420c3d1734123e6a3bc10b3a2a981aa1d538502373e31c91bf76e'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-s390x'; 			sha256='97b112b3366a471cc375e0f881d65a9a7b07f0962f308834c37f5c3fa75aad08'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 21 Feb 2025 18:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 18:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fddc498219722db61fe7f7e06295aa8b64f7e48d19d0339176689ea591eea4ca`  
		Last Modified: Sat, 22 Feb 2025 00:27:26 GMT  
		Size: 8.1 MB (8062985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c17b75175e66b76074511db7ebd5bdc56ac19ba269d30e4f58ba4812816ad4`  
		Last Modified: Sat, 22 Feb 2025 00:27:26 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987b6d8519d32209785b3840639a10aa6247ff1e290a651ebcca3d8c33e23dd2`  
		Last Modified: Sat, 22 Feb 2025 00:27:27 GMT  
		Size: 19.5 MB (19492233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7677267af1ddfc39dbdf35dcdca7c20328e83a42b64595f0d5880c62e99a91f`  
		Last Modified: Sat, 22 Feb 2025 00:27:27 GMT  
		Size: 21.8 MB (21829139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9fa9f5140fd1401e5edaa2de6f975bd14f0b79efbafbe0d2497ea0213ecd260`  
		Last Modified: Sat, 22 Feb 2025 00:27:27 GMT  
		Size: 21.0 MB (20958635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124bcf7a51a8a140479ebb1cfd0aea5bf38223d37b7c6ae1deb93bbb1abc0469`  
		Last Modified: Sat, 22 Feb 2025 00:27:28 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3083b3dfd2242fbeb7b498bb2e0d99d55c8e34cad7396573784aa86db3c69355`  
		Last Modified: Sat, 22 Feb 2025 00:27:28 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b255e6bd488c8fb61ba962afb512c02077ecc7e41b50991cb3229aaa7ae94b`  
		Last Modified: Sat, 22 Feb 2025 00:27:28 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:23d0fdad7d91848fe9aefbb31f9ec0f13048b4043d184117ef3506756fb199f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d89ed9762486ccde5720aaa5cfd88b8e5c1bf286c15632485f3c3a9b66385e0`

```dockerfile
```

-	Layers:
	-	`sha256:29c00cb8b559fbda58a54628ef429544bb24356f7620856781c43b802464d245`  
		Last Modified: Sat, 22 Feb 2025 00:27:26 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:563c0b58e54b2cb6649f26c22d8f06f2be7ebb8dead799918f4b22b13dd7d9f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (68956771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eabedade3d89f3eb7ffac6cf1924c31c852c974072b582d14b744e4c9c6993a2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 21 Feb 2025 18:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_VERSION=28.0.0
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-amd64'; 			sha256='7f355525bfaf411302570b705118181b720f18071f4be3f0eaac7b2297d826e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v6'; 			sha256='f841251fd67646e8b6bb4c7e0c2c385f6a1dc7403f5ac6ee7b07c96f0815f7f3'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v7'; 			sha256='81d7040e90e9b69cb0378778f673e1fc2a24ef6dbd47931dc83ab6472fc5809d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm64'; 			sha256='42d5cee287ec7426de5252276a05f3ea565ac2d65d62d052b885a84dd54152d5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-ppc64le'; 			sha256='6a4e6a243f83d80cd46c939f327b2e14cfddd2c6690651cf48d0e208c3345b88'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-riscv64'; 			sha256='eae82aec74a420c3d1734123e6a3bc10b3a2a981aa1d538502373e31c91bf76e'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-s390x'; 			sha256='97b112b3366a471cc375e0f881d65a9a7b07f0962f308834c37f5c3fa75aad08'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 21 Feb 2025 18:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 18:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e40b3641449ca47aef50c48f620eb6d3a3bc2292e5cf4ea267f5f03e6c7bc`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 8.0 MB (7978133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df16922f358c97f513c6d0b9457abb36aefc588e45374edd23692381878a7`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21eb60c27f71135d16125d7dcf87a6c0a49fc39428a0a7ecbc83c6bc1087efa9`  
		Last Modified: Thu, 20 Feb 2025 23:28:03 GMT  
		Size: 17.5 MB (17453851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b3b7abf60d98565d245e7aab34cfdec0b3c2c8ff503fb00ebceed21f636a93`  
		Last Modified: Sat, 22 Feb 2025 00:28:48 GMT  
		Size: 20.4 MB (20432003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ced3aebdded979735885d70afdbc8a5f03be15205f1145cd3b2af469eb21175`  
		Last Modified: Sat, 22 Feb 2025 00:28:48 GMT  
		Size: 19.7 MB (19725892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f8d07fba646c3b5ac2a07d053675df2a0422b36b698a824d345ee2447bc8e1`  
		Last Modified: Sat, 22 Feb 2025 00:28:47 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c51a22c8e8f3b4205fde47fd17f66895fad1496f33f46bb6aebdf5938bb94ad`  
		Last Modified: Sat, 22 Feb 2025 00:28:47 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f36ff703ab2a5ebeeeb26f374c59106eb92bf26531f572228024531dcc975f64`  
		Last Modified: Sat, 22 Feb 2025 00:28:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:19ac4c1b39024c4040fa578e5a4947132dfa561816cb7525547f283ad033cb82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d38b373d00ff94b39de7f66b705b156b58a6c9747a3aa783505be0e6c3ebf00`

```dockerfile
```

-	Layers:
	-	`sha256:65c4a818e540437ada35738cd53dff3f48895979403e4f6d6893ef134b4a0b5e`  
		Last Modified: Sat, 22 Feb 2025 00:28:47 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:6045d4846c59f8ee46c1d168dfe9b4de563a1602ed536f9a75e133d23291dc17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (67964254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ba8f3ae10c4069acc8988e46282e2592d80824e75e262440f1ca87b5b54fa4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 21 Feb 2025 18:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_VERSION=28.0.0
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-amd64'; 			sha256='7f355525bfaf411302570b705118181b720f18071f4be3f0eaac7b2297d826e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v6'; 			sha256='f841251fd67646e8b6bb4c7e0c2c385f6a1dc7403f5ac6ee7b07c96f0815f7f3'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v7'; 			sha256='81d7040e90e9b69cb0378778f673e1fc2a24ef6dbd47931dc83ab6472fc5809d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm64'; 			sha256='42d5cee287ec7426de5252276a05f3ea565ac2d65d62d052b885a84dd54152d5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-ppc64le'; 			sha256='6a4e6a243f83d80cd46c939f327b2e14cfddd2c6690651cf48d0e208c3345b88'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-riscv64'; 			sha256='eae82aec74a420c3d1734123e6a3bc10b3a2a981aa1d538502373e31c91bf76e'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-s390x'; 			sha256='97b112b3366a471cc375e0f881d65a9a7b07f0962f308834c37f5c3fa75aad08'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 21 Feb 2025 18:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 18:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b654458a637c48c7f8f46da325ae8f810828e851ed4ab4b406092503eb680f`  
		Last Modified: Sat, 22 Feb 2025 00:28:04 GMT  
		Size: 7.3 MB (7299375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3474560bdd0e71f5972a48abd9e80877e2219f6eacae8272034d8503bcb634b2`  
		Last Modified: Sat, 22 Feb 2025 00:28:03 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ffc820c153872520700f2618e71ee9bea9cfee69fbff7b0ea4acb751a2fee5`  
		Last Modified: Sat, 22 Feb 2025 00:28:04 GMT  
		Size: 17.4 MB (17444426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a39a48e6818f4f7d6e7637cf221cc02da7b2e8ab3ca2643a527024430497175`  
		Last Modified: Sat, 22 Feb 2025 00:28:04 GMT  
		Size: 20.4 MB (20411656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168ce845c02246501347d9ae0d1bb9bb9f55a707c5ef03ba3bb6377e832c28f4`  
		Last Modified: Sat, 22 Feb 2025 00:28:05 GMT  
		Size: 19.7 MB (19708525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d62f1159ab01591fa3510e1ddc7b7e0313d001750472b1eaa0dcfb3a1f097732`  
		Last Modified: Sat, 22 Feb 2025 00:28:05 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ab9b1b4b0f9c261b260d739cd6d593a2c510b9c29045d72d930f2baf5fa78e`  
		Last Modified: Sat, 22 Feb 2025 00:28:05 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d27509dd9fc9bdb19051b5661dce75fc9b53979841bcd49fd03667b1ad6dde`  
		Last Modified: Sat, 22 Feb 2025 00:28:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:23645fb2cbf9071135cf4f6aa3c2daf2dc3370793a863fef2ee39d5314bc1a81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93af0d5ba0d4eddf4e7d202afc318f1221ed8bb0f4b1ffde83604fd9bd752b41`

```dockerfile
```

-	Layers:
	-	`sha256:c3cccd9b156d9500700d8b30693438b27b91e56bc8149ff0300632ebb0780d36`  
		Last Modified: Sat, 22 Feb 2025 00:28:03 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:11e8dfd68841685653bd4816fc6ab2f95cc84940d099b1e683a4b60a958599df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69748524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af7e01753428f0214a4072134b7c0481b29b9f695ebe735e920d47b6c0302c4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 21 Feb 2025 18:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_VERSION=28.0.0
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-amd64'; 			sha256='7f355525bfaf411302570b705118181b720f18071f4be3f0eaac7b2297d826e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v6'; 			sha256='f841251fd67646e8b6bb4c7e0c2c385f6a1dc7403f5ac6ee7b07c96f0815f7f3'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v7'; 			sha256='81d7040e90e9b69cb0378778f673e1fc2a24ef6dbd47931dc83ab6472fc5809d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm64'; 			sha256='42d5cee287ec7426de5252276a05f3ea565ac2d65d62d052b885a84dd54152d5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-ppc64le'; 			sha256='6a4e6a243f83d80cd46c939f327b2e14cfddd2c6690651cf48d0e208c3345b88'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-riscv64'; 			sha256='eae82aec74a420c3d1734123e6a3bc10b3a2a981aa1d538502373e31c91bf76e'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-s390x'; 			sha256='97b112b3366a471cc375e0f881d65a9a7b07f0962f308834c37f5c3fa75aad08'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Fri, 21 Feb 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 21 Feb 2025 18:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 21 Feb 2025 18:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 18:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:076f26e7389ad2e79a31e03589b2c6943495faa94ce7fc6ecd800dd0c320c71e`  
		Last Modified: Sat, 22 Feb 2025 00:28:38 GMT  
		Size: 8.1 MB (8076430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54483e7ea72052e991e704ef33b6d45d32f2c9886445d70ae79e50a2dd444147`  
		Last Modified: Sat, 22 Feb 2025 00:28:37 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d747fdfb37d0ca59992c4852cab088ffb4549e3f8ef7632b252452c1c12c7989`  
		Last Modified: Sat, 22 Feb 2025 00:28:38 GMT  
		Size: 18.4 MB (18412791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84912acd39dd03fae2cffdb073ec52df5d17e2700910653a8c844d31a916a7eb`  
		Last Modified: Sat, 22 Feb 2025 00:28:39 GMT  
		Size: 20.0 MB (20041446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49191a7f2e90fd89997d49d48799f225e27d4d811c1ab6a1a5ed18c8b5a9f94`  
		Last Modified: Sat, 22 Feb 2025 00:28:40 GMT  
		Size: 19.2 MB (19222674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7debd3993d0af81423e3290841931e4b162ff882877ebb292b10f3dde6dc5694`  
		Last Modified: Sat, 22 Feb 2025 00:28:39 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855282ceddcfc470897f6e2cb33f2ad4742db7c00f24a0386714c91a31a090fa`  
		Last Modified: Sat, 22 Feb 2025 00:28:40 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fbaf9714c72f8c1c56eb53405de18b5c63f82fcfa89814a71a92c9844e1fb8b`  
		Last Modified: Sat, 22 Feb 2025 00:28:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:30588165fa8677446217c19a011fa7b5dd4b56689b71068054b1769685612965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:050a79ebe758ee7f1e33b2b06dd06dabf7b2d3ccb381eb495d95c61658b577c3`

```dockerfile
```

-	Layers:
	-	`sha256:eb188e16beab9632a0818b296adc7960adad9c23b87529bf5b8f419eef964844`  
		Last Modified: Sat, 22 Feb 2025 00:28:37 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind`

```console
$ docker pull docker@sha256:0a9c58ebc9f86e5af35e4330f6c738dc64fce3ca2e2574b5becdfb88765b308b
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
$ docker pull docker@sha256:32c276e9aafff90ea7765271afa524c293c9749e880748217b1abedd04af39a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.0 MB (141006353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1da86d0da980dad6c82075b9859478027165e57dba77994a2fe1fa99ed408f3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_VERSION=28.0.0
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-amd64'; 			sha256='7f355525bfaf411302570b705118181b720f18071f4be3f0eaac7b2297d826e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v6'; 			sha256='f841251fd67646e8b6bb4c7e0c2c385f6a1dc7403f5ac6ee7b07c96f0815f7f3'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v7'; 			sha256='81d7040e90e9b69cb0378778f673e1fc2a24ef6dbd47931dc83ab6472fc5809d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm64'; 			sha256='42d5cee287ec7426de5252276a05f3ea565ac2d65d62d052b885a84dd54152d5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-ppc64le'; 			sha256='6a4e6a243f83d80cd46c939f327b2e14cfddd2c6690651cf48d0e208c3345b88'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-riscv64'; 			sha256='eae82aec74a420c3d1734123e6a3bc10b3a2a981aa1d538502373e31c91bf76e'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-s390x'; 			sha256='97b112b3366a471cc375e0f881d65a9a7b07f0962f308834c37f5c3fa75aad08'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 20 Feb 2025 06:04:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD ["sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
VOLUME [/var/lib/docker]
# Thu, 20 Feb 2025 06:04:43 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD []
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fddc498219722db61fe7f7e06295aa8b64f7e48d19d0339176689ea591eea4ca`  
		Last Modified: Sat, 22 Feb 2025 00:27:26 GMT  
		Size: 8.1 MB (8062985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c17b75175e66b76074511db7ebd5bdc56ac19ba269d30e4f58ba4812816ad4`  
		Last Modified: Sat, 22 Feb 2025 00:27:26 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987b6d8519d32209785b3840639a10aa6247ff1e290a651ebcca3d8c33e23dd2`  
		Last Modified: Sat, 22 Feb 2025 00:27:27 GMT  
		Size: 19.5 MB (19492233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7677267af1ddfc39dbdf35dcdca7c20328e83a42b64595f0d5880c62e99a91f`  
		Last Modified: Sat, 22 Feb 2025 00:27:27 GMT  
		Size: 21.8 MB (21829139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9fa9f5140fd1401e5edaa2de6f975bd14f0b79efbafbe0d2497ea0213ecd260`  
		Last Modified: Sat, 22 Feb 2025 00:27:27 GMT  
		Size: 21.0 MB (20958635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124bcf7a51a8a140479ebb1cfd0aea5bf38223d37b7c6ae1deb93bbb1abc0469`  
		Last Modified: Sat, 22 Feb 2025 00:27:28 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3083b3dfd2242fbeb7b498bb2e0d99d55c8e34cad7396573784aa86db3c69355`  
		Last Modified: Sat, 22 Feb 2025 00:27:28 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b255e6bd488c8fb61ba962afb512c02077ecc7e41b50991cb3229aaa7ae94b`  
		Last Modified: Sat, 22 Feb 2025 00:27:28 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42458739bc4b2677f265360a10a2eacffd5133b0242dd313ba8a3dac7a116c4`  
		Last Modified: Sat, 22 Feb 2025 01:08:23 GMT  
		Size: 6.7 MB (6733003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5a7650793a22cfeac45c6610fe2cd3ccd26b6795d33ee5389d66a174c05a65`  
		Last Modified: Sat, 22 Feb 2025 01:08:23 GMT  
		Size: 90.3 KB (90318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03749f129a866bd1cf2e2797db758f883cf177f3cd33ff3c60924ec811728b4f`  
		Last Modified: Sat, 22 Feb 2025 01:08:23 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:769e1c97b1855704d1f74c39b30c2d2bbc890339752b2be542477e64d2529c32`  
		Last Modified: Sat, 22 Feb 2025 01:08:24 GMT  
		Size: 60.2 MB (60189735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e450e39e6d5b103505878dd35ff532dcdfef40450540495b6a666e7bc34e2587`  
		Last Modified: Sat, 22 Feb 2025 01:08:23 GMT  
		Size: 1.6 KB (1637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254862f49c6f0929e44b00f9635661aff98a508d2dc321d6ddc2944f60ac90bb`  
		Last Modified: Sat, 22 Feb 2025 01:08:23 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:ba9368fe1da752bf14bb9ed738b656214abfea5e16cb949f4883beeb86cf9408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:658bfc3f8051aceaf851bbf4fdcff3b32c7f8c853b5262abd646f57fbf14bb10`

```dockerfile
```

-	Layers:
	-	`sha256:670c6ce494a80447b9f682d0ac427af5be54978f5f629221274a481ecf2be95e`  
		Last Modified: Sat, 22 Feb 2025 01:08:22 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:346b1790ac4379efe1ff83735d9d72ded98e8ebcc776f29f190a50d1086d5c63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.7 MB (131676535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e2b568d33d9f4d9da33be6f6a26a6e533f58d6d874c445c67494a71fe99ce8c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_VERSION=28.0.0
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-amd64'; 			sha256='7f355525bfaf411302570b705118181b720f18071f4be3f0eaac7b2297d826e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v6'; 			sha256='f841251fd67646e8b6bb4c7e0c2c385f6a1dc7403f5ac6ee7b07c96f0815f7f3'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v7'; 			sha256='81d7040e90e9b69cb0378778f673e1fc2a24ef6dbd47931dc83ab6472fc5809d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm64'; 			sha256='42d5cee287ec7426de5252276a05f3ea565ac2d65d62d052b885a84dd54152d5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-ppc64le'; 			sha256='6a4e6a243f83d80cd46c939f327b2e14cfddd2c6690651cf48d0e208c3345b88'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-riscv64'; 			sha256='eae82aec74a420c3d1734123e6a3bc10b3a2a981aa1d538502373e31c91bf76e'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-s390x'; 			sha256='97b112b3366a471cc375e0f881d65a9a7b07f0962f308834c37f5c3fa75aad08'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 20 Feb 2025 06:04:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD ["sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
VOLUME [/var/lib/docker]
# Thu, 20 Feb 2025 06:04:43 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD []
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e40b3641449ca47aef50c48f620eb6d3a3bc2292e5cf4ea267f5f03e6c7bc`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 8.0 MB (7978133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df16922f358c97f513c6d0b9457abb36aefc588e45374edd23692381878a7`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21eb60c27f71135d16125d7dcf87a6c0a49fc39428a0a7ecbc83c6bc1087efa9`  
		Last Modified: Thu, 20 Feb 2025 23:28:03 GMT  
		Size: 17.5 MB (17453851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b3b7abf60d98565d245e7aab34cfdec0b3c2c8ff503fb00ebceed21f636a93`  
		Last Modified: Sat, 22 Feb 2025 00:28:48 GMT  
		Size: 20.4 MB (20432003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ced3aebdded979735885d70afdbc8a5f03be15205f1145cd3b2af469eb21175`  
		Last Modified: Sat, 22 Feb 2025 00:28:48 GMT  
		Size: 19.7 MB (19725892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f8d07fba646c3b5ac2a07d053675df2a0422b36b698a824d345ee2447bc8e1`  
		Last Modified: Sat, 22 Feb 2025 00:28:47 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c51a22c8e8f3b4205fde47fd17f66895fad1496f33f46bb6aebdf5938bb94ad`  
		Last Modified: Sat, 22 Feb 2025 00:28:47 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f36ff703ab2a5ebeeeb26f374c59106eb92bf26531f572228024531dcc975f64`  
		Last Modified: Sat, 22 Feb 2025 00:28:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2440995b1488c0fccd4c0a9b3062c58a33404bcc3ca3e8289ae64b6393946c65`  
		Last Modified: Sat, 22 Feb 2025 01:29:31 GMT  
		Size: 7.0 MB (7036904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cce93707f7a9fed88581b5b8e8f49a184ba206f961aae653eef08af3b94987b1`  
		Last Modified: Sat, 22 Feb 2025 01:29:30 GMT  
		Size: 89.8 KB (89849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26cf971d434da3f52513e2595da034274a6fb8c1ef74cddc815339506b7b704a`  
		Last Modified: Sat, 22 Feb 2025 01:29:30 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c3188476c3d7ba720f96be3cdceb222b9a7a6e0693a917966988332f14e8ef`  
		Last Modified: Sat, 22 Feb 2025 01:29:33 GMT  
		Size: 55.6 MB (55587101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c9e4329aff590ce10c6d6613452bf70f9708c4817750614d9a1a68918444a6`  
		Last Modified: Sat, 22 Feb 2025 01:29:31 GMT  
		Size: 1.6 KB (1638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ff2444afd5e703729aeef9ead8d60b8f059c8e5f0b4b82853f021d0f2c24504`  
		Last Modified: Sat, 22 Feb 2025 01:29:31 GMT  
		Size: 3.3 KB (3263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:0931cacdc5870a73bd56837c9590fb9801af1b229cbf7ee86dc79c932a51323c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d14b9f57c5e9b67b594f4172c7cfbb95e2442a040e0bb090b09cc95ce2d35a18`

```dockerfile
```

-	Layers:
	-	`sha256:93150d2f1d44b19b0d6d36517e86cddc39cd49f0857f41bdb86a200f7db357e6`  
		Last Modified: Sat, 22 Feb 2025 01:29:30 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:089424d7adbb66df8dd78e5ce27d9bd9d13cebe072cb5eb79e7478f00c124163
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (130009843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da65fa603f2dc74e8750fbdc3d7173e607ca901a8dfb81fab1136584884d3018`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_VERSION=28.0.0
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-amd64'; 			sha256='7f355525bfaf411302570b705118181b720f18071f4be3f0eaac7b2297d826e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v6'; 			sha256='f841251fd67646e8b6bb4c7e0c2c385f6a1dc7403f5ac6ee7b07c96f0815f7f3'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v7'; 			sha256='81d7040e90e9b69cb0378778f673e1fc2a24ef6dbd47931dc83ab6472fc5809d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm64'; 			sha256='42d5cee287ec7426de5252276a05f3ea565ac2d65d62d052b885a84dd54152d5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-ppc64le'; 			sha256='6a4e6a243f83d80cd46c939f327b2e14cfddd2c6690651cf48d0e208c3345b88'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-riscv64'; 			sha256='eae82aec74a420c3d1734123e6a3bc10b3a2a981aa1d538502373e31c91bf76e'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-s390x'; 			sha256='97b112b3366a471cc375e0f881d65a9a7b07f0962f308834c37f5c3fa75aad08'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 20 Feb 2025 06:04:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD ["sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
VOLUME [/var/lib/docker]
# Thu, 20 Feb 2025 06:04:43 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD []
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b654458a637c48c7f8f46da325ae8f810828e851ed4ab4b406092503eb680f`  
		Last Modified: Sat, 22 Feb 2025 00:28:04 GMT  
		Size: 7.3 MB (7299375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3474560bdd0e71f5972a48abd9e80877e2219f6eacae8272034d8503bcb634b2`  
		Last Modified: Sat, 22 Feb 2025 00:28:03 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ffc820c153872520700f2618e71ee9bea9cfee69fbff7b0ea4acb751a2fee5`  
		Last Modified: Sat, 22 Feb 2025 00:28:04 GMT  
		Size: 17.4 MB (17444426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a39a48e6818f4f7d6e7637cf221cc02da7b2e8ab3ca2643a527024430497175`  
		Last Modified: Sat, 22 Feb 2025 00:28:04 GMT  
		Size: 20.4 MB (20411656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168ce845c02246501347d9ae0d1bb9bb9f55a707c5ef03ba3bb6377e832c28f4`  
		Last Modified: Sat, 22 Feb 2025 00:28:05 GMT  
		Size: 19.7 MB (19708525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d62f1159ab01591fa3510e1ddc7b7e0313d001750472b1eaa0dcfb3a1f097732`  
		Last Modified: Sat, 22 Feb 2025 00:28:05 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ab9b1b4b0f9c261b260d739cd6d593a2c510b9c29045d72d930f2baf5fa78e`  
		Last Modified: Sat, 22 Feb 2025 00:28:05 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d27509dd9fc9bdb19051b5661dce75fc9b53979841bcd49fd03667b1ad6dde`  
		Last Modified: Sat, 22 Feb 2025 00:28:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd0d2a57f389ccbd627e0bca3b813e9397f4a6a55364b1f7cf22df043542cf1a`  
		Last Modified: Sat, 22 Feb 2025 04:54:52 GMT  
		Size: 6.4 MB (6366292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5947e3cbc6a2eb4d8c4ec17605876ea3e3a5cb2c09abac0a58d53cc4d6569f7`  
		Last Modified: Sat, 22 Feb 2025 04:54:51 GMT  
		Size: 86.3 KB (86342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc1fa6b8e4e654268e5dfc6afa5b1e88bfb92da3c33018f231f76ad7e08a59e`  
		Last Modified: Sat, 22 Feb 2025 04:54:51 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f544c5574adf21ca185480beea8b120134f2ed74f3f2418dc0ef564a3891490`  
		Last Modified: Sat, 22 Feb 2025 04:54:53 GMT  
		Size: 55.6 MB (55587054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd1c8be29e89fc14e8cd0778dcda3dae4c641d9ab956b2f9ce8d02df1d7984e`  
		Last Modified: Sat, 22 Feb 2025 04:54:52 GMT  
		Size: 1.6 KB (1636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db5e7511235a55ebe7a92c8825189d27a2b1d951e0f25d22e4e932636abbd466`  
		Last Modified: Sat, 22 Feb 2025 04:54:52 GMT  
		Size: 3.3 KB (3256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:1cdaa27022a39a251e498044fefc2f4160913794dc50a3074935741e0d39d28b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:643a439611cab3be1c6fde6e85ec369c205d94c81b88f1c91a627a32a6448b32`

```dockerfile
```

-	Layers:
	-	`sha256:fa998948cfd33a55b2120a90b998117bea32698c81f84e340fc1f9fa359825c4`  
		Last Modified: Sat, 22 Feb 2025 04:54:51 GMT  
		Size: 34.8 KB (34765 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:af92e15294f197a3cc4de0e75e012f4e91a996e4fd58ad96e163208aea7f0be3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.4 MB (132399422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89d922b5c31bca4bc340632485ab5243809aaf557e7aaf377fd956c15f4ad0a6`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_VERSION=28.0.0
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-amd64'; 			sha256='7f355525bfaf411302570b705118181b720f18071f4be3f0eaac7b2297d826e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v6'; 			sha256='f841251fd67646e8b6bb4c7e0c2c385f6a1dc7403f5ac6ee7b07c96f0815f7f3'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v7'; 			sha256='81d7040e90e9b69cb0378778f673e1fc2a24ef6dbd47931dc83ab6472fc5809d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm64'; 			sha256='42d5cee287ec7426de5252276a05f3ea565ac2d65d62d052b885a84dd54152d5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-ppc64le'; 			sha256='6a4e6a243f83d80cd46c939f327b2e14cfddd2c6690651cf48d0e208c3345b88'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-riscv64'; 			sha256='eae82aec74a420c3d1734123e6a3bc10b3a2a981aa1d538502373e31c91bf76e'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-s390x'; 			sha256='97b112b3366a471cc375e0f881d65a9a7b07f0962f308834c37f5c3fa75aad08'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 20 Feb 2025 06:04:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD ["sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
VOLUME [/var/lib/docker]
# Thu, 20 Feb 2025 06:04:43 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD []
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:076f26e7389ad2e79a31e03589b2c6943495faa94ce7fc6ecd800dd0c320c71e`  
		Last Modified: Sat, 22 Feb 2025 00:28:38 GMT  
		Size: 8.1 MB (8076430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54483e7ea72052e991e704ef33b6d45d32f2c9886445d70ae79e50a2dd444147`  
		Last Modified: Sat, 22 Feb 2025 00:28:37 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d747fdfb37d0ca59992c4852cab088ffb4549e3f8ef7632b252452c1c12c7989`  
		Last Modified: Sat, 22 Feb 2025 00:28:38 GMT  
		Size: 18.4 MB (18412791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84912acd39dd03fae2cffdb073ec52df5d17e2700910653a8c844d31a916a7eb`  
		Last Modified: Sat, 22 Feb 2025 00:28:39 GMT  
		Size: 20.0 MB (20041446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49191a7f2e90fd89997d49d48799f225e27d4d811c1ab6a1a5ed18c8b5a9f94`  
		Last Modified: Sat, 22 Feb 2025 00:28:40 GMT  
		Size: 19.2 MB (19222674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7debd3993d0af81423e3290841931e4b162ff882877ebb292b10f3dde6dc5694`  
		Last Modified: Sat, 22 Feb 2025 00:28:39 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855282ceddcfc470897f6e2cb33f2ad4742db7c00f24a0386714c91a31a090fa`  
		Last Modified: Sat, 22 Feb 2025 00:28:40 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fbaf9714c72f8c1c56eb53405de18b5c63f82fcfa89814a71a92c9844e1fb8b`  
		Last Modified: Sat, 22 Feb 2025 00:28:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f1efb7aef297fc62aaca013f0102b13d4fb2bd1eb6e39c858c91c440c973f87`  
		Last Modified: Sat, 22 Feb 2025 02:46:00 GMT  
		Size: 7.0 MB (6978850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d301065fd8bf09964f1efc59488efd3c692d574aae6e2460fefc3dac799912b`  
		Last Modified: Sat, 22 Feb 2025 02:46:00 GMT  
		Size: 99.4 KB (99390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d33e0f749652bb606f1e92e433cb70fa6c8e7a30737050979d975e9f06a132f`  
		Last Modified: Sat, 22 Feb 2025 02:45:59 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a409b11008465c3cb7523e669b4d2a064619125185de982089bf11944cf62502`  
		Last Modified: Sat, 22 Feb 2025 02:46:01 GMT  
		Size: 55.6 MB (55566753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff8cdce63f040e68fff768b8a75d7ebdd3f4cd4e69ed0f85ae0ad620baa9c40`  
		Last Modified: Sat, 22 Feb 2025 02:46:00 GMT  
		Size: 1.6 KB (1636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f72a632b800deed0be1fc7ec78852db28106ae059a841b87a966fed6ec7255f`  
		Last Modified: Sat, 22 Feb 2025 02:46:01 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:d6dd49a97960eaef409aa41f89cf8596c02281b55801b3f726b267761031bc90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4105199c766800ff78dca393a5dccdb1435364291ecf731c31deacb4fa6e86a4`

```dockerfile
```

-	Layers:
	-	`sha256:2f7e554767be7baf2d46a3652bbe4405cdcb83972440eb83c19280ab0e991188`  
		Last Modified: Sat, 22 Feb 2025 02:45:59 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind-rootless`

```console
$ docker pull docker@sha256:f36f8f41d9e38bae8c3d247446a1e31df98bd84d1ccc22d9d8d50fbe6cbafae8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:16356585ff8acaa68e6bd54dd11f6760ce507fa719fe7e00bc7db05f53c7a074
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.2 MB (159160666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f413ddafbf744ab3b46d57ab5bda7d4b4ed64aa0ac7f3bd49a3055f8aa5c604`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_VERSION=28.0.0
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-amd64'; 			sha256='7f355525bfaf411302570b705118181b720f18071f4be3f0eaac7b2297d826e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v6'; 			sha256='f841251fd67646e8b6bb4c7e0c2c385f6a1dc7403f5ac6ee7b07c96f0815f7f3'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v7'; 			sha256='81d7040e90e9b69cb0378778f673e1fc2a24ef6dbd47931dc83ab6472fc5809d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm64'; 			sha256='42d5cee287ec7426de5252276a05f3ea565ac2d65d62d052b885a84dd54152d5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-ppc64le'; 			sha256='6a4e6a243f83d80cd46c939f327b2e14cfddd2c6690651cf48d0e208c3345b88'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-riscv64'; 			sha256='eae82aec74a420c3d1734123e6a3bc10b3a2a981aa1d538502373e31c91bf76e'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-s390x'; 			sha256='97b112b3366a471cc375e0f881d65a9a7b07f0962f308834c37f5c3fa75aad08'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 20 Feb 2025 06:04:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD ["sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
VOLUME [/var/lib/docker]
# Thu, 20 Feb 2025 06:04:43 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD []
# Thu, 20 Feb 2025 06:04:43 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 20 Feb 2025 06:04:43 GMT
USER rootless
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fddc498219722db61fe7f7e06295aa8b64f7e48d19d0339176689ea591eea4ca`  
		Last Modified: Sat, 22 Feb 2025 00:27:26 GMT  
		Size: 8.1 MB (8062985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c17b75175e66b76074511db7ebd5bdc56ac19ba269d30e4f58ba4812816ad4`  
		Last Modified: Sat, 22 Feb 2025 00:27:26 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987b6d8519d32209785b3840639a10aa6247ff1e290a651ebcca3d8c33e23dd2`  
		Last Modified: Sat, 22 Feb 2025 00:27:27 GMT  
		Size: 19.5 MB (19492233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7677267af1ddfc39dbdf35dcdca7c20328e83a42b64595f0d5880c62e99a91f`  
		Last Modified: Sat, 22 Feb 2025 00:27:27 GMT  
		Size: 21.8 MB (21829139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9fa9f5140fd1401e5edaa2de6f975bd14f0b79efbafbe0d2497ea0213ecd260`  
		Last Modified: Sat, 22 Feb 2025 00:27:27 GMT  
		Size: 21.0 MB (20958635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124bcf7a51a8a140479ebb1cfd0aea5bf38223d37b7c6ae1deb93bbb1abc0469`  
		Last Modified: Sat, 22 Feb 2025 00:27:28 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3083b3dfd2242fbeb7b498bb2e0d99d55c8e34cad7396573784aa86db3c69355`  
		Last Modified: Sat, 22 Feb 2025 00:27:28 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b255e6bd488c8fb61ba962afb512c02077ecc7e41b50991cb3229aaa7ae94b`  
		Last Modified: Sat, 22 Feb 2025 00:27:28 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42458739bc4b2677f265360a10a2eacffd5133b0242dd313ba8a3dac7a116c4`  
		Last Modified: Sat, 22 Feb 2025 01:08:23 GMT  
		Size: 6.7 MB (6733003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5a7650793a22cfeac45c6610fe2cd3ccd26b6795d33ee5389d66a174c05a65`  
		Last Modified: Sat, 22 Feb 2025 01:08:23 GMT  
		Size: 90.3 KB (90318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03749f129a866bd1cf2e2797db758f883cf177f3cd33ff3c60924ec811728b4f`  
		Last Modified: Sat, 22 Feb 2025 01:08:23 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:769e1c97b1855704d1f74c39b30c2d2bbc890339752b2be542477e64d2529c32`  
		Last Modified: Sat, 22 Feb 2025 01:08:24 GMT  
		Size: 60.2 MB (60189735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e450e39e6d5b103505878dd35ff532dcdfef40450540495b6a666e7bc34e2587`  
		Last Modified: Sat, 22 Feb 2025 01:08:23 GMT  
		Size: 1.6 KB (1637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254862f49c6f0929e44b00f9635661aff98a508d2dc321d6ddc2944f60ac90bb`  
		Last Modified: Sat, 22 Feb 2025 01:08:23 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04d666bba697d05e04595251efc48c7cfb46c50934eb5e8b28f9ece93bbaa12f`  
		Last Modified: Sat, 22 Feb 2025 02:08:04 GMT  
		Size: 986.6 KB (986572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9e9040036c95835735c8d16482226c61fd43befb113e4654d11899b4c82c24`  
		Last Modified: Sat, 22 Feb 2025 02:08:04 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c773fc7dad6ddd06fd1b5c0d2b81528878a1c879bcfed7b967fed225ec4346a7`  
		Last Modified: Sat, 22 Feb 2025 02:08:04 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce0abea1fd4caba2bf7cfa1eaab27c1e81060389830353f7de69a562c0d129f3`  
		Last Modified: Sat, 22 Feb 2025 02:08:05 GMT  
		Size: 17.2 MB (17166401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e73037866943973bf1a62ff0acb7da9d1f19cc8ff52edb6c2ddf748fba1507`  
		Last Modified: Sat, 22 Feb 2025 02:08:05 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:788f83bf8b427ca8d5db790b94b5465dd4e729d19870cf23c0a99aa2247419e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:171bb75448d4664abab1f0e5b2859c6858afa3eaf4bbe30c4ff52221ef9588a5`

```dockerfile
```

-	Layers:
	-	`sha256:681e1874c769bcd3cc3a0fe90e1caa86a29f1a172fc7caa3eb5c75bb6e9843e7`  
		Last Modified: Sat, 22 Feb 2025 02:08:03 GMT  
		Size: 30.5 KB (30451 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:73776940d20eac532ae279be7c72ff89ea730517ff9dab5a659516bc00d09dda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.7 MB (152694408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5b89ed4c42e88420300229e316f2cf5c30d71c0341b7ba4039b7887870e259b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_VERSION=28.0.0
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-amd64'; 			sha256='7f355525bfaf411302570b705118181b720f18071f4be3f0eaac7b2297d826e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v6'; 			sha256='f841251fd67646e8b6bb4c7e0c2c385f6a1dc7403f5ac6ee7b07c96f0815f7f3'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v7'; 			sha256='81d7040e90e9b69cb0378778f673e1fc2a24ef6dbd47931dc83ab6472fc5809d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm64'; 			sha256='42d5cee287ec7426de5252276a05f3ea565ac2d65d62d052b885a84dd54152d5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-ppc64le'; 			sha256='6a4e6a243f83d80cd46c939f327b2e14cfddd2c6690651cf48d0e208c3345b88'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-riscv64'; 			sha256='eae82aec74a420c3d1734123e6a3bc10b3a2a981aa1d538502373e31c91bf76e'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-s390x'; 			sha256='97b112b3366a471cc375e0f881d65a9a7b07f0962f308834c37f5c3fa75aad08'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 20 Feb 2025 06:04:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD ["sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
VOLUME [/var/lib/docker]
# Thu, 20 Feb 2025 06:04:43 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD []
# Thu, 20 Feb 2025 06:04:43 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 20 Feb 2025 06:04:43 GMT
USER rootless
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:076f26e7389ad2e79a31e03589b2c6943495faa94ce7fc6ecd800dd0c320c71e`  
		Last Modified: Sat, 22 Feb 2025 00:28:38 GMT  
		Size: 8.1 MB (8076430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54483e7ea72052e991e704ef33b6d45d32f2c9886445d70ae79e50a2dd444147`  
		Last Modified: Sat, 22 Feb 2025 00:28:37 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d747fdfb37d0ca59992c4852cab088ffb4549e3f8ef7632b252452c1c12c7989`  
		Last Modified: Sat, 22 Feb 2025 00:28:38 GMT  
		Size: 18.4 MB (18412791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84912acd39dd03fae2cffdb073ec52df5d17e2700910653a8c844d31a916a7eb`  
		Last Modified: Sat, 22 Feb 2025 00:28:39 GMT  
		Size: 20.0 MB (20041446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49191a7f2e90fd89997d49d48799f225e27d4d811c1ab6a1a5ed18c8b5a9f94`  
		Last Modified: Sat, 22 Feb 2025 00:28:40 GMT  
		Size: 19.2 MB (19222674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7debd3993d0af81423e3290841931e4b162ff882877ebb292b10f3dde6dc5694`  
		Last Modified: Sat, 22 Feb 2025 00:28:39 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855282ceddcfc470897f6e2cb33f2ad4742db7c00f24a0386714c91a31a090fa`  
		Last Modified: Sat, 22 Feb 2025 00:28:40 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fbaf9714c72f8c1c56eb53405de18b5c63f82fcfa89814a71a92c9844e1fb8b`  
		Last Modified: Sat, 22 Feb 2025 00:28:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f1efb7aef297fc62aaca013f0102b13d4fb2bd1eb6e39c858c91c440c973f87`  
		Last Modified: Sat, 22 Feb 2025 02:46:00 GMT  
		Size: 7.0 MB (6978850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d301065fd8bf09964f1efc59488efd3c692d574aae6e2460fefc3dac799912b`  
		Last Modified: Sat, 22 Feb 2025 02:46:00 GMT  
		Size: 99.4 KB (99390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d33e0f749652bb606f1e92e433cb70fa6c8e7a30737050979d975e9f06a132f`  
		Last Modified: Sat, 22 Feb 2025 02:45:59 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a409b11008465c3cb7523e669b4d2a064619125185de982089bf11944cf62502`  
		Last Modified: Sat, 22 Feb 2025 02:46:01 GMT  
		Size: 55.6 MB (55566753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff8cdce63f040e68fff768b8a75d7ebdd3f4cd4e69ed0f85ae0ad620baa9c40`  
		Last Modified: Sat, 22 Feb 2025 02:46:00 GMT  
		Size: 1.6 KB (1636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f72a632b800deed0be1fc7ec78852db28106ae059a841b87a966fed6ec7255f`  
		Last Modified: Sat, 22 Feb 2025 02:46:01 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4468cca51cdd29ea280bb7c9d7dcffc805ae2134d5d10101acabb31403f19c34`  
		Last Modified: Sat, 22 Feb 2025 03:07:17 GMT  
		Size: 1.0 MB (1014200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d43f7cfe0c5e55bc699a2f0f56e6ecd213c0d84783892175a2bbabe01e1ee1`  
		Last Modified: Sat, 22 Feb 2025 03:07:17 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ffc8590ff3cdff71a791e5dd600d08fee46a9a23862330e1c51e7fe2953e3c`  
		Last Modified: Sat, 22 Feb 2025 03:07:17 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b03647ba73f1a14d321c6973445bfedd81d7195d0c270c2a52d81c4bd00241ec`  
		Last Modified: Sat, 22 Feb 2025 03:07:18 GMT  
		Size: 19.3 MB (19279443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42024c25dd02ca9c645e8270327928627cf8b2d1ce95c86e3184f7236d8254b3`  
		Last Modified: Sat, 22 Feb 2025 03:07:18 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:7caef0d171c210bbc06a3c6c5f181d699cdab3868ed8201206157f5ce2b26b41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66ce0dd66d759a7501d703e2bd782cf6c3190278388bb80297dd5fdc65839c39`

```dockerfile
```

-	Layers:
	-	`sha256:f29410d962e3aeed18fdb7f16f7e72ba75bab67d36d78eaa1f5bb9e00bee589a`  
		Last Modified: Sat, 22 Feb 2025 03:07:17 GMT  
		Size: 30.6 KB (30621 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:latest`

```console
$ docker pull docker@sha256:0a9c58ebc9f86e5af35e4330f6c738dc64fce3ca2e2574b5becdfb88765b308b
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

### `docker:latest` - linux; amd64

```console
$ docker pull docker@sha256:32c276e9aafff90ea7765271afa524c293c9749e880748217b1abedd04af39a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.0 MB (141006353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1da86d0da980dad6c82075b9859478027165e57dba77994a2fe1fa99ed408f3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_VERSION=28.0.0
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-amd64'; 			sha256='7f355525bfaf411302570b705118181b720f18071f4be3f0eaac7b2297d826e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v6'; 			sha256='f841251fd67646e8b6bb4c7e0c2c385f6a1dc7403f5ac6ee7b07c96f0815f7f3'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v7'; 			sha256='81d7040e90e9b69cb0378778f673e1fc2a24ef6dbd47931dc83ab6472fc5809d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm64'; 			sha256='42d5cee287ec7426de5252276a05f3ea565ac2d65d62d052b885a84dd54152d5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-ppc64le'; 			sha256='6a4e6a243f83d80cd46c939f327b2e14cfddd2c6690651cf48d0e208c3345b88'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-riscv64'; 			sha256='eae82aec74a420c3d1734123e6a3bc10b3a2a981aa1d538502373e31c91bf76e'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-s390x'; 			sha256='97b112b3366a471cc375e0f881d65a9a7b07f0962f308834c37f5c3fa75aad08'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 20 Feb 2025 06:04:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD ["sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
VOLUME [/var/lib/docker]
# Thu, 20 Feb 2025 06:04:43 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD []
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fddc498219722db61fe7f7e06295aa8b64f7e48d19d0339176689ea591eea4ca`  
		Last Modified: Sat, 22 Feb 2025 00:27:26 GMT  
		Size: 8.1 MB (8062985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c17b75175e66b76074511db7ebd5bdc56ac19ba269d30e4f58ba4812816ad4`  
		Last Modified: Sat, 22 Feb 2025 00:27:26 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987b6d8519d32209785b3840639a10aa6247ff1e290a651ebcca3d8c33e23dd2`  
		Last Modified: Sat, 22 Feb 2025 00:27:27 GMT  
		Size: 19.5 MB (19492233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7677267af1ddfc39dbdf35dcdca7c20328e83a42b64595f0d5880c62e99a91f`  
		Last Modified: Sat, 22 Feb 2025 00:27:27 GMT  
		Size: 21.8 MB (21829139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9fa9f5140fd1401e5edaa2de6f975bd14f0b79efbafbe0d2497ea0213ecd260`  
		Last Modified: Sat, 22 Feb 2025 00:27:27 GMT  
		Size: 21.0 MB (20958635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124bcf7a51a8a140479ebb1cfd0aea5bf38223d37b7c6ae1deb93bbb1abc0469`  
		Last Modified: Sat, 22 Feb 2025 00:27:28 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3083b3dfd2242fbeb7b498bb2e0d99d55c8e34cad7396573784aa86db3c69355`  
		Last Modified: Sat, 22 Feb 2025 00:27:28 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b255e6bd488c8fb61ba962afb512c02077ecc7e41b50991cb3229aaa7ae94b`  
		Last Modified: Sat, 22 Feb 2025 00:27:28 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42458739bc4b2677f265360a10a2eacffd5133b0242dd313ba8a3dac7a116c4`  
		Last Modified: Sat, 22 Feb 2025 01:08:23 GMT  
		Size: 6.7 MB (6733003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5a7650793a22cfeac45c6610fe2cd3ccd26b6795d33ee5389d66a174c05a65`  
		Last Modified: Sat, 22 Feb 2025 01:08:23 GMT  
		Size: 90.3 KB (90318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03749f129a866bd1cf2e2797db758f883cf177f3cd33ff3c60924ec811728b4f`  
		Last Modified: Sat, 22 Feb 2025 01:08:23 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:769e1c97b1855704d1f74c39b30c2d2bbc890339752b2be542477e64d2529c32`  
		Last Modified: Sat, 22 Feb 2025 01:08:24 GMT  
		Size: 60.2 MB (60189735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e450e39e6d5b103505878dd35ff532dcdfef40450540495b6a666e7bc34e2587`  
		Last Modified: Sat, 22 Feb 2025 01:08:23 GMT  
		Size: 1.6 KB (1637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254862f49c6f0929e44b00f9635661aff98a508d2dc321d6ddc2944f60ac90bb`  
		Last Modified: Sat, 22 Feb 2025 01:08:23 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:ba9368fe1da752bf14bb9ed738b656214abfea5e16cb949f4883beeb86cf9408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:658bfc3f8051aceaf851bbf4fdcff3b32c7f8c853b5262abd646f57fbf14bb10`

```dockerfile
```

-	Layers:
	-	`sha256:670c6ce494a80447b9f682d0ac427af5be54978f5f629221274a481ecf2be95e`  
		Last Modified: Sat, 22 Feb 2025 01:08:22 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v6

```console
$ docker pull docker@sha256:346b1790ac4379efe1ff83735d9d72ded98e8ebcc776f29f190a50d1086d5c63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.7 MB (131676535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e2b568d33d9f4d9da33be6f6a26a6e533f58d6d874c445c67494a71fe99ce8c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_VERSION=28.0.0
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-amd64'; 			sha256='7f355525bfaf411302570b705118181b720f18071f4be3f0eaac7b2297d826e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v6'; 			sha256='f841251fd67646e8b6bb4c7e0c2c385f6a1dc7403f5ac6ee7b07c96f0815f7f3'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v7'; 			sha256='81d7040e90e9b69cb0378778f673e1fc2a24ef6dbd47931dc83ab6472fc5809d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm64'; 			sha256='42d5cee287ec7426de5252276a05f3ea565ac2d65d62d052b885a84dd54152d5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-ppc64le'; 			sha256='6a4e6a243f83d80cd46c939f327b2e14cfddd2c6690651cf48d0e208c3345b88'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-riscv64'; 			sha256='eae82aec74a420c3d1734123e6a3bc10b3a2a981aa1d538502373e31c91bf76e'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-s390x'; 			sha256='97b112b3366a471cc375e0f881d65a9a7b07f0962f308834c37f5c3fa75aad08'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 20 Feb 2025 06:04:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD ["sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
VOLUME [/var/lib/docker]
# Thu, 20 Feb 2025 06:04:43 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD []
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e40b3641449ca47aef50c48f620eb6d3a3bc2292e5cf4ea267f5f03e6c7bc`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 8.0 MB (7978133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df16922f358c97f513c6d0b9457abb36aefc588e45374edd23692381878a7`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21eb60c27f71135d16125d7dcf87a6c0a49fc39428a0a7ecbc83c6bc1087efa9`  
		Last Modified: Thu, 20 Feb 2025 23:28:03 GMT  
		Size: 17.5 MB (17453851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b3b7abf60d98565d245e7aab34cfdec0b3c2c8ff503fb00ebceed21f636a93`  
		Last Modified: Sat, 22 Feb 2025 00:28:48 GMT  
		Size: 20.4 MB (20432003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ced3aebdded979735885d70afdbc8a5f03be15205f1145cd3b2af469eb21175`  
		Last Modified: Sat, 22 Feb 2025 00:28:48 GMT  
		Size: 19.7 MB (19725892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f8d07fba646c3b5ac2a07d053675df2a0422b36b698a824d345ee2447bc8e1`  
		Last Modified: Sat, 22 Feb 2025 00:28:47 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c51a22c8e8f3b4205fde47fd17f66895fad1496f33f46bb6aebdf5938bb94ad`  
		Last Modified: Sat, 22 Feb 2025 00:28:47 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f36ff703ab2a5ebeeeb26f374c59106eb92bf26531f572228024531dcc975f64`  
		Last Modified: Sat, 22 Feb 2025 00:28:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2440995b1488c0fccd4c0a9b3062c58a33404bcc3ca3e8289ae64b6393946c65`  
		Last Modified: Sat, 22 Feb 2025 01:29:31 GMT  
		Size: 7.0 MB (7036904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cce93707f7a9fed88581b5b8e8f49a184ba206f961aae653eef08af3b94987b1`  
		Last Modified: Sat, 22 Feb 2025 01:29:30 GMT  
		Size: 89.8 KB (89849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26cf971d434da3f52513e2595da034274a6fb8c1ef74cddc815339506b7b704a`  
		Last Modified: Sat, 22 Feb 2025 01:29:30 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c3188476c3d7ba720f96be3cdceb222b9a7a6e0693a917966988332f14e8ef`  
		Last Modified: Sat, 22 Feb 2025 01:29:33 GMT  
		Size: 55.6 MB (55587101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c9e4329aff590ce10c6d6613452bf70f9708c4817750614d9a1a68918444a6`  
		Last Modified: Sat, 22 Feb 2025 01:29:31 GMT  
		Size: 1.6 KB (1638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ff2444afd5e703729aeef9ead8d60b8f059c8e5f0b4b82853f021d0f2c24504`  
		Last Modified: Sat, 22 Feb 2025 01:29:31 GMT  
		Size: 3.3 KB (3263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:0931cacdc5870a73bd56837c9590fb9801af1b229cbf7ee86dc79c932a51323c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d14b9f57c5e9b67b594f4172c7cfbb95e2442a040e0bb090b09cc95ce2d35a18`

```dockerfile
```

-	Layers:
	-	`sha256:93150d2f1d44b19b0d6d36517e86cddc39cd49f0857f41bdb86a200f7db357e6`  
		Last Modified: Sat, 22 Feb 2025 01:29:30 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v7

```console
$ docker pull docker@sha256:089424d7adbb66df8dd78e5ce27d9bd9d13cebe072cb5eb79e7478f00c124163
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (130009843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da65fa603f2dc74e8750fbdc3d7173e607ca901a8dfb81fab1136584884d3018`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_VERSION=28.0.0
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-amd64'; 			sha256='7f355525bfaf411302570b705118181b720f18071f4be3f0eaac7b2297d826e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v6'; 			sha256='f841251fd67646e8b6bb4c7e0c2c385f6a1dc7403f5ac6ee7b07c96f0815f7f3'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v7'; 			sha256='81d7040e90e9b69cb0378778f673e1fc2a24ef6dbd47931dc83ab6472fc5809d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm64'; 			sha256='42d5cee287ec7426de5252276a05f3ea565ac2d65d62d052b885a84dd54152d5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-ppc64le'; 			sha256='6a4e6a243f83d80cd46c939f327b2e14cfddd2c6690651cf48d0e208c3345b88'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-riscv64'; 			sha256='eae82aec74a420c3d1734123e6a3bc10b3a2a981aa1d538502373e31c91bf76e'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-s390x'; 			sha256='97b112b3366a471cc375e0f881d65a9a7b07f0962f308834c37f5c3fa75aad08'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 20 Feb 2025 06:04:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD ["sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
VOLUME [/var/lib/docker]
# Thu, 20 Feb 2025 06:04:43 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD []
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b654458a637c48c7f8f46da325ae8f810828e851ed4ab4b406092503eb680f`  
		Last Modified: Sat, 22 Feb 2025 00:28:04 GMT  
		Size: 7.3 MB (7299375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3474560bdd0e71f5972a48abd9e80877e2219f6eacae8272034d8503bcb634b2`  
		Last Modified: Sat, 22 Feb 2025 00:28:03 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ffc820c153872520700f2618e71ee9bea9cfee69fbff7b0ea4acb751a2fee5`  
		Last Modified: Sat, 22 Feb 2025 00:28:04 GMT  
		Size: 17.4 MB (17444426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a39a48e6818f4f7d6e7637cf221cc02da7b2e8ab3ca2643a527024430497175`  
		Last Modified: Sat, 22 Feb 2025 00:28:04 GMT  
		Size: 20.4 MB (20411656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168ce845c02246501347d9ae0d1bb9bb9f55a707c5ef03ba3bb6377e832c28f4`  
		Last Modified: Sat, 22 Feb 2025 00:28:05 GMT  
		Size: 19.7 MB (19708525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d62f1159ab01591fa3510e1ddc7b7e0313d001750472b1eaa0dcfb3a1f097732`  
		Last Modified: Sat, 22 Feb 2025 00:28:05 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ab9b1b4b0f9c261b260d739cd6d593a2c510b9c29045d72d930f2baf5fa78e`  
		Last Modified: Sat, 22 Feb 2025 00:28:05 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d27509dd9fc9bdb19051b5661dce75fc9b53979841bcd49fd03667b1ad6dde`  
		Last Modified: Sat, 22 Feb 2025 00:28:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd0d2a57f389ccbd627e0bca3b813e9397f4a6a55364b1f7cf22df043542cf1a`  
		Last Modified: Sat, 22 Feb 2025 04:54:52 GMT  
		Size: 6.4 MB (6366292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5947e3cbc6a2eb4d8c4ec17605876ea3e3a5cb2c09abac0a58d53cc4d6569f7`  
		Last Modified: Sat, 22 Feb 2025 04:54:51 GMT  
		Size: 86.3 KB (86342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc1fa6b8e4e654268e5dfc6afa5b1e88bfb92da3c33018f231f76ad7e08a59e`  
		Last Modified: Sat, 22 Feb 2025 04:54:51 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f544c5574adf21ca185480beea8b120134f2ed74f3f2418dc0ef564a3891490`  
		Last Modified: Sat, 22 Feb 2025 04:54:53 GMT  
		Size: 55.6 MB (55587054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd1c8be29e89fc14e8cd0778dcda3dae4c641d9ab956b2f9ce8d02df1d7984e`  
		Last Modified: Sat, 22 Feb 2025 04:54:52 GMT  
		Size: 1.6 KB (1636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db5e7511235a55ebe7a92c8825189d27a2b1d951e0f25d22e4e932636abbd466`  
		Last Modified: Sat, 22 Feb 2025 04:54:52 GMT  
		Size: 3.3 KB (3256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:1cdaa27022a39a251e498044fefc2f4160913794dc50a3074935741e0d39d28b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:643a439611cab3be1c6fde6e85ec369c205d94c81b88f1c91a627a32a6448b32`

```dockerfile
```

-	Layers:
	-	`sha256:fa998948cfd33a55b2120a90b998117bea32698c81f84e340fc1f9fa359825c4`  
		Last Modified: Sat, 22 Feb 2025 04:54:51 GMT  
		Size: 34.8 KB (34765 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:af92e15294f197a3cc4de0e75e012f4e91a996e4fd58ad96e163208aea7f0be3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.4 MB (132399422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89d922b5c31bca4bc340632485ab5243809aaf557e7aaf377fd956c15f4ad0a6`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_VERSION=28.0.0
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-amd64'; 			sha256='7f355525bfaf411302570b705118181b720f18071f4be3f0eaac7b2297d826e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v6'; 			sha256='f841251fd67646e8b6bb4c7e0c2c385f6a1dc7403f5ac6ee7b07c96f0815f7f3'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v7'; 			sha256='81d7040e90e9b69cb0378778f673e1fc2a24ef6dbd47931dc83ab6472fc5809d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm64'; 			sha256='42d5cee287ec7426de5252276a05f3ea565ac2d65d62d052b885a84dd54152d5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-ppc64le'; 			sha256='6a4e6a243f83d80cd46c939f327b2e14cfddd2c6690651cf48d0e208c3345b88'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-riscv64'; 			sha256='eae82aec74a420c3d1734123e6a3bc10b3a2a981aa1d538502373e31c91bf76e'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-s390x'; 			sha256='97b112b3366a471cc375e0f881d65a9a7b07f0962f308834c37f5c3fa75aad08'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 20 Feb 2025 06:04:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD ["sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
VOLUME [/var/lib/docker]
# Thu, 20 Feb 2025 06:04:43 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD []
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:076f26e7389ad2e79a31e03589b2c6943495faa94ce7fc6ecd800dd0c320c71e`  
		Last Modified: Sat, 22 Feb 2025 00:28:38 GMT  
		Size: 8.1 MB (8076430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54483e7ea72052e991e704ef33b6d45d32f2c9886445d70ae79e50a2dd444147`  
		Last Modified: Sat, 22 Feb 2025 00:28:37 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d747fdfb37d0ca59992c4852cab088ffb4549e3f8ef7632b252452c1c12c7989`  
		Last Modified: Sat, 22 Feb 2025 00:28:38 GMT  
		Size: 18.4 MB (18412791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84912acd39dd03fae2cffdb073ec52df5d17e2700910653a8c844d31a916a7eb`  
		Last Modified: Sat, 22 Feb 2025 00:28:39 GMT  
		Size: 20.0 MB (20041446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49191a7f2e90fd89997d49d48799f225e27d4d811c1ab6a1a5ed18c8b5a9f94`  
		Last Modified: Sat, 22 Feb 2025 00:28:40 GMT  
		Size: 19.2 MB (19222674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7debd3993d0af81423e3290841931e4b162ff882877ebb292b10f3dde6dc5694`  
		Last Modified: Sat, 22 Feb 2025 00:28:39 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855282ceddcfc470897f6e2cb33f2ad4742db7c00f24a0386714c91a31a090fa`  
		Last Modified: Sat, 22 Feb 2025 00:28:40 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fbaf9714c72f8c1c56eb53405de18b5c63f82fcfa89814a71a92c9844e1fb8b`  
		Last Modified: Sat, 22 Feb 2025 00:28:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f1efb7aef297fc62aaca013f0102b13d4fb2bd1eb6e39c858c91c440c973f87`  
		Last Modified: Sat, 22 Feb 2025 02:46:00 GMT  
		Size: 7.0 MB (6978850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d301065fd8bf09964f1efc59488efd3c692d574aae6e2460fefc3dac799912b`  
		Last Modified: Sat, 22 Feb 2025 02:46:00 GMT  
		Size: 99.4 KB (99390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d33e0f749652bb606f1e92e433cb70fa6c8e7a30737050979d975e9f06a132f`  
		Last Modified: Sat, 22 Feb 2025 02:45:59 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a409b11008465c3cb7523e669b4d2a064619125185de982089bf11944cf62502`  
		Last Modified: Sat, 22 Feb 2025 02:46:01 GMT  
		Size: 55.6 MB (55566753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff8cdce63f040e68fff768b8a75d7ebdd3f4cd4e69ed0f85ae0ad620baa9c40`  
		Last Modified: Sat, 22 Feb 2025 02:46:00 GMT  
		Size: 1.6 KB (1636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f72a632b800deed0be1fc7ec78852db28106ae059a841b87a966fed6ec7255f`  
		Last Modified: Sat, 22 Feb 2025 02:46:01 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:d6dd49a97960eaef409aa41f89cf8596c02281b55801b3f726b267761031bc90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4105199c766800ff78dca393a5dccdb1435364291ecf731c31deacb4fa6e86a4`

```dockerfile
```

-	Layers:
	-	`sha256:2f7e554767be7baf2d46a3652bbe4405cdcb83972440eb83c19280ab0e991188`  
		Last Modified: Sat, 22 Feb 2025 02:45:59 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:windowsservercore`

```console
$ docker pull docker@sha256:8cbb71e3463881e43b4e46000916a151f195288cba0ad77f0eabef966bc5d438
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

### `docker:windowsservercore` - windows version 10.0.26100.2894; amd64

```console
$ docker pull docker@sha256:13348bcc4ed6fcd578c6aea25afa087bac0759457ff724c916d2fb3624c804ba
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2565217611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:172682bc22fc40249839b093831f2ccdb06d47eda95530dd64db1bf9bba03ee5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Sat, 22 Feb 2025 00:31:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 22 Feb 2025 00:31:31 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 22 Feb 2025 00:31:31 GMT
ENV DOCKER_VERSION=28.0.0
# Sat, 22 Feb 2025 00:31:32 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.0.zip
# Sat, 22 Feb 2025 00:31:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 22 Feb 2025 00:31:42 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Sat, 22 Feb 2025 00:31:42 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.windows-amd64.exe
# Sat, 22 Feb 2025 00:31:43 GMT
ENV DOCKER_BUILDX_SHA256=ab3eba3acbfa6b6612690af075795254f29762efc8abace5f636b8e7628b1851
# Sat, 22 Feb 2025 00:31:51 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 22 Feb 2025 00:31:52 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Sat, 22 Feb 2025 00:31:53 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-windows-x86_64.exe
# Sat, 22 Feb 2025 00:31:53 GMT
ENV DOCKER_COMPOSE_SHA256=01bce3456228d8e1e4b0ba056f4b9730b7fd2c1a7113c8a985144c0fdee797b0
# Sat, 22 Feb 2025 00:32:02 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Tue, 14 Jan 2025 18:53:06 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b538b630814b004320f0f9ee0a9c3594e03b773b5580fed4105a81f74e7c098f`  
		Last Modified: Sat, 22 Feb 2025 00:32:07 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58e25b87bc1505ec562cf342b28ce02166b0c50e250e5b111cae842bd29224a6`  
		Last Modified: Sat, 22 Feb 2025 00:32:08 GMT  
		Size: 382.4 KB (382390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54dec53b66cd21d806f4ecb36e798d52785171b19a3b94a2886816c4b00fc357`  
		Last Modified: Sat, 22 Feb 2025 00:32:07 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:173311079ab932318629c9bfc59957c46ffef6d9500148722bf57885ab4d912e`  
		Last Modified: Sat, 22 Feb 2025 00:32:07 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5ef5273358e9d6949b1c0c7a006b2fe22a9b45af8454771a753c47f67702fc5`  
		Last Modified: Sat, 22 Feb 2025 00:32:09 GMT  
		Size: 19.8 MB (19841357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6550ae8a0cab9e35d0c0177c6afc594dd1f53008f4c0b85bdca771700fa770c`  
		Last Modified: Sat, 22 Feb 2025 00:32:06 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e430e1223ff0212bf349270e614e999171df037e89b09997ff907efa689e97d`  
		Last Modified: Sat, 22 Feb 2025 00:32:06 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adf1c042512ab6127e6371768343f9e2125e122a97350d29044867620964da29`  
		Last Modified: Sat, 22 Feb 2025 00:32:05 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbcc9f9bc1cf9f00d67c29fcbf84300c45479de6c73cf2f49f1ae660cf73bb07`  
		Last Modified: Sat, 22 Feb 2025 00:32:08 GMT  
		Size: 22.8 MB (22778890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b21becac3572331f658c564c93303ec2f6d01292e600e1b7deab5fea30b05ff6`  
		Last Modified: Sat, 22 Feb 2025 00:32:05 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e856f770850ac4d1cb287a7e7807f001c6f669a135f306ccf2fe6e63129def66`  
		Last Modified: Sat, 22 Feb 2025 00:32:05 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e457e71b003d1ce3d61f1df1c12e7500d728f4b5598604334164ddb533cb2ba`  
		Last Modified: Sat, 22 Feb 2025 00:32:05 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f63f581bda80c595a4087c00b71030e7a4d71012bb05cbc2eb9c139f9679e31`  
		Last Modified: Sat, 22 Feb 2025 00:32:08 GMT  
		Size: 21.9 MB (21925519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.20348.3207; amd64

```console
$ docker pull docker@sha256:40cac7c487ab96fd2608d22182da86766f98f6f8726e4a9cc87f61fba1c79f0e
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2328776516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a7dc1af03d6c94095c7be69ba1d7ffcba2c6ddbf201a1901bafc1445c1d7615`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Sat, 22 Feb 2025 00:37:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 22 Feb 2025 00:37:49 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 22 Feb 2025 00:37:49 GMT
ENV DOCKER_VERSION=28.0.0
# Sat, 22 Feb 2025 00:37:50 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.0.zip
# Sat, 22 Feb 2025 00:38:01 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 22 Feb 2025 00:38:01 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Sat, 22 Feb 2025 00:38:02 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.windows-amd64.exe
# Sat, 22 Feb 2025 00:38:02 GMT
ENV DOCKER_BUILDX_SHA256=ab3eba3acbfa6b6612690af075795254f29762efc8abace5f636b8e7628b1851
# Sat, 22 Feb 2025 00:38:11 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 22 Feb 2025 00:38:12 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Sat, 22 Feb 2025 00:38:13 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-windows-x86_64.exe
# Sat, 22 Feb 2025 00:38:13 GMT
ENV DOCKER_COMPOSE_SHA256=01bce3456228d8e1e4b0ba056f4b9730b7fd2c1a7113c8a985144c0fdee797b0
# Sat, 22 Feb 2025 00:38:22 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Tue, 11 Feb 2025 18:38:32 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a513c2ebb5aac6eaccc568c460584aa652a09401a4f865e8b1a9870e4f9826d`  
		Last Modified: Sat, 22 Feb 2025 00:38:28 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f0ea743d1a5ae5f5f7088a7c23ca759ec9b363ca46d674d9e7425aa27739ba`  
		Last Modified: Sat, 22 Feb 2025 00:38:27 GMT  
		Size: 389.0 KB (388984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:401dea1d9556118c14843e687f7eb2f2767205cefe7c534ce370103f7bb4520c`  
		Last Modified: Sat, 22 Feb 2025 00:38:27 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ff218fd9efd93054faba12c9de123bd815f47af0057f0822bebe1980b506039`  
		Last Modified: Sat, 22 Feb 2025 00:38:26 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef9e343cb24c4c76e4c3fbbf11fa22c10da7fea8e22f98be5493a15840e79f6`  
		Last Modified: Sat, 22 Feb 2025 00:38:28 GMT  
		Size: 19.8 MB (19832408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b072185e609fe777fbfd0d1c7e0860cfd307e8d0718c19365cbe22f499636207`  
		Last Modified: Sat, 22 Feb 2025 00:38:26 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a89b4e620aaf525ac2545408e3d49037c7d5b8c99ee26edb1937e8a2a5c181c`  
		Last Modified: Sat, 22 Feb 2025 00:38:25 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7edf322adba1ba7c101c710b53b2f04cb139c273b95e29fcc5d8943f581af167`  
		Last Modified: Sat, 22 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c220811a807867c0315d6291b99472e043388fe4f317d60dcb70cf42963b333`  
		Last Modified: Sat, 22 Feb 2025 00:38:27 GMT  
		Size: 22.8 MB (22770286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a73d03430d6958d170ed89b00d83fa15b1b28a9aa22fbd4ae9018b5671cb08f6`  
		Last Modified: Sat, 22 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:164bc468207a3b25ae55b075dc0b5987de3ca0d425be73ff7f45fe57b49f807f`  
		Last Modified: Sat, 22 Feb 2025 00:38:24 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7307712a7f1b1601e8cf9b306574434f960222e78bb80360573ae2829c165ab9`  
		Last Modified: Sat, 22 Feb 2025 00:38:24 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ff623c1936592d4e22a10ac22c1ba99d55a4c960680df6e5e9da20450cf85d`  
		Last Modified: Sat, 22 Feb 2025 00:38:27 GMT  
		Size: 21.9 MB (21914957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.17763.6893; amd64

```console
$ docker pull docker@sha256:575fd688c3bf866a95546fe93e2564fea753d26e5931ebfc1e32ebd9bc411358
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2201693889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47afabbd0d9bf289e87beda973d92a82859b49c2b2f83325e44032f22df554d7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Sat, 22 Feb 2025 00:36:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 22 Feb 2025 00:37:03 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 22 Feb 2025 00:37:04 GMT
ENV DOCKER_VERSION=28.0.0
# Sat, 22 Feb 2025 00:37:05 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.0.zip
# Sat, 22 Feb 2025 00:37:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 22 Feb 2025 00:37:18 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Sat, 22 Feb 2025 00:37:18 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.windows-amd64.exe
# Sat, 22 Feb 2025 00:37:19 GMT
ENV DOCKER_BUILDX_SHA256=ab3eba3acbfa6b6612690af075795254f29762efc8abace5f636b8e7628b1851
# Sat, 22 Feb 2025 00:37:28 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 22 Feb 2025 00:37:29 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Sat, 22 Feb 2025 00:37:30 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-windows-x86_64.exe
# Sat, 22 Feb 2025 00:37:31 GMT
ENV DOCKER_COMPOSE_SHA256=01bce3456228d8e1e4b0ba056f4b9730b7fd2c1a7113c8a985144c0fdee797b0
# Sat, 22 Feb 2025 00:37:39 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 18:49:50 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d662e474d0eebcc45d26c962c3ea2815d5ad421c4abce3dfca970d20d34206`  
		Last Modified: Sat, 22 Feb 2025 00:37:45 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b80c05d72492cc29e69146de42b5cbab7c6912ef3a85c579caaf8ccb3b7eabb9`  
		Last Modified: Sat, 22 Feb 2025 00:37:44 GMT  
		Size: 343.2 KB (343235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df0623e2321e34b1b589a3f2314cdc767fe978372d17c7d621c1b6e40645f0e2`  
		Last Modified: Sat, 22 Feb 2025 00:37:44 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177b2d1a530b8667811479317d9e8ae2eb9cf1e26892e886e4baa298209fcfa4`  
		Last Modified: Sat, 22 Feb 2025 00:37:44 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3834ee7310198b95517a8b510904c8f38cbdb7c49df0b228572059fee55faa4`  
		Last Modified: Sat, 22 Feb 2025 00:37:46 GMT  
		Size: 19.8 MB (19805126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7d9cad94e2d870741143d557fc15084b8f7f0c3f510618f76861f6c020ec0c`  
		Last Modified: Sat, 22 Feb 2025 00:37:43 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73e623554754f1c6df8e43e93e867af1218d203b9111a1b977befbc4542f33e`  
		Last Modified: Sat, 22 Feb 2025 00:37:43 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39746d0ab1fefcec984bb203b47fb43af6294430288792c106045708180cf90f`  
		Last Modified: Sat, 22 Feb 2025 00:37:43 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb7e0de055ddbb75c2d00fd897c8e623d5d164e9da002c14c5d7b16034ddefb2`  
		Last Modified: Sat, 22 Feb 2025 00:37:45 GMT  
		Size: 22.7 MB (22743044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d103e4264cc2326442d2f2c0d9a6f8a6d63672a9e1888b0eb106211fe4c866a8`  
		Last Modified: Sat, 22 Feb 2025 00:37:42 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e7898abd14f1e9f5aaa3850e26c6e47b5af14ccc7727ace668f06058bb6bbbb`  
		Last Modified: Sat, 22 Feb 2025 00:37:42 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac30b7d53b77634caea695af70ca54fad87eec4119c5d63afcd64b762dadee9f`  
		Last Modified: Sat, 22 Feb 2025 00:37:42 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a13d827d5d10e25d56e691281a38fb310acbe73a53d8ecb6c27a3c737305b83d`  
		Last Modified: Sat, 22 Feb 2025 00:37:44 GMT  
		Size: 21.9 MB (21881997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-1809`

```console
$ docker pull docker@sha256:8b5e611771751fe8360ccf0f5bb3b6c022a079599c9e8dada6351d3682c645b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `docker:windowsservercore-1809` - windows version 10.0.17763.6893; amd64

```console
$ docker pull docker@sha256:575fd688c3bf866a95546fe93e2564fea753d26e5931ebfc1e32ebd9bc411358
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2201693889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47afabbd0d9bf289e87beda973d92a82859b49c2b2f83325e44032f22df554d7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Sat, 22 Feb 2025 00:36:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 22 Feb 2025 00:37:03 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 22 Feb 2025 00:37:04 GMT
ENV DOCKER_VERSION=28.0.0
# Sat, 22 Feb 2025 00:37:05 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.0.zip
# Sat, 22 Feb 2025 00:37:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 22 Feb 2025 00:37:18 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Sat, 22 Feb 2025 00:37:18 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.windows-amd64.exe
# Sat, 22 Feb 2025 00:37:19 GMT
ENV DOCKER_BUILDX_SHA256=ab3eba3acbfa6b6612690af075795254f29762efc8abace5f636b8e7628b1851
# Sat, 22 Feb 2025 00:37:28 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 22 Feb 2025 00:37:29 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Sat, 22 Feb 2025 00:37:30 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-windows-x86_64.exe
# Sat, 22 Feb 2025 00:37:31 GMT
ENV DOCKER_COMPOSE_SHA256=01bce3456228d8e1e4b0ba056f4b9730b7fd2c1a7113c8a985144c0fdee797b0
# Sat, 22 Feb 2025 00:37:39 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 18:49:50 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d662e474d0eebcc45d26c962c3ea2815d5ad421c4abce3dfca970d20d34206`  
		Last Modified: Sat, 22 Feb 2025 00:37:45 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b80c05d72492cc29e69146de42b5cbab7c6912ef3a85c579caaf8ccb3b7eabb9`  
		Last Modified: Sat, 22 Feb 2025 00:37:44 GMT  
		Size: 343.2 KB (343235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df0623e2321e34b1b589a3f2314cdc767fe978372d17c7d621c1b6e40645f0e2`  
		Last Modified: Sat, 22 Feb 2025 00:37:44 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177b2d1a530b8667811479317d9e8ae2eb9cf1e26892e886e4baa298209fcfa4`  
		Last Modified: Sat, 22 Feb 2025 00:37:44 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3834ee7310198b95517a8b510904c8f38cbdb7c49df0b228572059fee55faa4`  
		Last Modified: Sat, 22 Feb 2025 00:37:46 GMT  
		Size: 19.8 MB (19805126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7d9cad94e2d870741143d557fc15084b8f7f0c3f510618f76861f6c020ec0c`  
		Last Modified: Sat, 22 Feb 2025 00:37:43 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73e623554754f1c6df8e43e93e867af1218d203b9111a1b977befbc4542f33e`  
		Last Modified: Sat, 22 Feb 2025 00:37:43 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39746d0ab1fefcec984bb203b47fb43af6294430288792c106045708180cf90f`  
		Last Modified: Sat, 22 Feb 2025 00:37:43 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb7e0de055ddbb75c2d00fd897c8e623d5d164e9da002c14c5d7b16034ddefb2`  
		Last Modified: Sat, 22 Feb 2025 00:37:45 GMT  
		Size: 22.7 MB (22743044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d103e4264cc2326442d2f2c0d9a6f8a6d63672a9e1888b0eb106211fe4c866a8`  
		Last Modified: Sat, 22 Feb 2025 00:37:42 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e7898abd14f1e9f5aaa3850e26c6e47b5af14ccc7727ace668f06058bb6bbbb`  
		Last Modified: Sat, 22 Feb 2025 00:37:42 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac30b7d53b77634caea695af70ca54fad87eec4119c5d63afcd64b762dadee9f`  
		Last Modified: Sat, 22 Feb 2025 00:37:42 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a13d827d5d10e25d56e691281a38fb310acbe73a53d8ecb6c27a3c737305b83d`  
		Last Modified: Sat, 22 Feb 2025 00:37:44 GMT  
		Size: 21.9 MB (21881997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:4a4531319a3d77d264dd66e0056a37a0ce12653a767680d3114dc86e6d50de94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3207; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.3207; amd64

```console
$ docker pull docker@sha256:40cac7c487ab96fd2608d22182da86766f98f6f8726e4a9cc87f61fba1c79f0e
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2328776516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a7dc1af03d6c94095c7be69ba1d7ffcba2c6ddbf201a1901bafc1445c1d7615`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Sat, 22 Feb 2025 00:37:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 22 Feb 2025 00:37:49 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 22 Feb 2025 00:37:49 GMT
ENV DOCKER_VERSION=28.0.0
# Sat, 22 Feb 2025 00:37:50 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.0.zip
# Sat, 22 Feb 2025 00:38:01 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 22 Feb 2025 00:38:01 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Sat, 22 Feb 2025 00:38:02 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.windows-amd64.exe
# Sat, 22 Feb 2025 00:38:02 GMT
ENV DOCKER_BUILDX_SHA256=ab3eba3acbfa6b6612690af075795254f29762efc8abace5f636b8e7628b1851
# Sat, 22 Feb 2025 00:38:11 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 22 Feb 2025 00:38:12 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Sat, 22 Feb 2025 00:38:13 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-windows-x86_64.exe
# Sat, 22 Feb 2025 00:38:13 GMT
ENV DOCKER_COMPOSE_SHA256=01bce3456228d8e1e4b0ba056f4b9730b7fd2c1a7113c8a985144c0fdee797b0
# Sat, 22 Feb 2025 00:38:22 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Tue, 11 Feb 2025 18:38:32 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a513c2ebb5aac6eaccc568c460584aa652a09401a4f865e8b1a9870e4f9826d`  
		Last Modified: Sat, 22 Feb 2025 00:38:28 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f0ea743d1a5ae5f5f7088a7c23ca759ec9b363ca46d674d9e7425aa27739ba`  
		Last Modified: Sat, 22 Feb 2025 00:38:27 GMT  
		Size: 389.0 KB (388984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:401dea1d9556118c14843e687f7eb2f2767205cefe7c534ce370103f7bb4520c`  
		Last Modified: Sat, 22 Feb 2025 00:38:27 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ff218fd9efd93054faba12c9de123bd815f47af0057f0822bebe1980b506039`  
		Last Modified: Sat, 22 Feb 2025 00:38:26 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef9e343cb24c4c76e4c3fbbf11fa22c10da7fea8e22f98be5493a15840e79f6`  
		Last Modified: Sat, 22 Feb 2025 00:38:28 GMT  
		Size: 19.8 MB (19832408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b072185e609fe777fbfd0d1c7e0860cfd307e8d0718c19365cbe22f499636207`  
		Last Modified: Sat, 22 Feb 2025 00:38:26 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a89b4e620aaf525ac2545408e3d49037c7d5b8c99ee26edb1937e8a2a5c181c`  
		Last Modified: Sat, 22 Feb 2025 00:38:25 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7edf322adba1ba7c101c710b53b2f04cb139c273b95e29fcc5d8943f581af167`  
		Last Modified: Sat, 22 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c220811a807867c0315d6291b99472e043388fe4f317d60dcb70cf42963b333`  
		Last Modified: Sat, 22 Feb 2025 00:38:27 GMT  
		Size: 22.8 MB (22770286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a73d03430d6958d170ed89b00d83fa15b1b28a9aa22fbd4ae9018b5671cb08f6`  
		Last Modified: Sat, 22 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:164bc468207a3b25ae55b075dc0b5987de3ca0d425be73ff7f45fe57b49f807f`  
		Last Modified: Sat, 22 Feb 2025 00:38:24 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7307712a7f1b1601e8cf9b306574434f960222e78bb80360573ae2829c165ab9`  
		Last Modified: Sat, 22 Feb 2025 00:38:24 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ff623c1936592d4e22a10ac22c1ba99d55a4c960680df6e5e9da20450cf85d`  
		Last Modified: Sat, 22 Feb 2025 00:38:27 GMT  
		Size: 21.9 MB (21914957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:78307f6a713fd34f43a0d89127421c46b2ff65f06362768394f4e6612dc89989
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.2894; amd64

### `docker:windowsservercore-ltsc2025` - windows version 10.0.26100.2894; amd64

```console
$ docker pull docker@sha256:13348bcc4ed6fcd578c6aea25afa087bac0759457ff724c916d2fb3624c804ba
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2565217611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:172682bc22fc40249839b093831f2ccdb06d47eda95530dd64db1bf9bba03ee5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Sat, 22 Feb 2025 00:31:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 22 Feb 2025 00:31:31 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 22 Feb 2025 00:31:31 GMT
ENV DOCKER_VERSION=28.0.0
# Sat, 22 Feb 2025 00:31:32 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.0.zip
# Sat, 22 Feb 2025 00:31:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 22 Feb 2025 00:31:42 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Sat, 22 Feb 2025 00:31:42 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.windows-amd64.exe
# Sat, 22 Feb 2025 00:31:43 GMT
ENV DOCKER_BUILDX_SHA256=ab3eba3acbfa6b6612690af075795254f29762efc8abace5f636b8e7628b1851
# Sat, 22 Feb 2025 00:31:51 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 22 Feb 2025 00:31:52 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Sat, 22 Feb 2025 00:31:53 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-windows-x86_64.exe
# Sat, 22 Feb 2025 00:31:53 GMT
ENV DOCKER_COMPOSE_SHA256=01bce3456228d8e1e4b0ba056f4b9730b7fd2c1a7113c8a985144c0fdee797b0
# Sat, 22 Feb 2025 00:32:02 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Tue, 14 Jan 2025 18:53:06 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b538b630814b004320f0f9ee0a9c3594e03b773b5580fed4105a81f74e7c098f`  
		Last Modified: Sat, 22 Feb 2025 00:32:07 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58e25b87bc1505ec562cf342b28ce02166b0c50e250e5b111cae842bd29224a6`  
		Last Modified: Sat, 22 Feb 2025 00:32:08 GMT  
		Size: 382.4 KB (382390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54dec53b66cd21d806f4ecb36e798d52785171b19a3b94a2886816c4b00fc357`  
		Last Modified: Sat, 22 Feb 2025 00:32:07 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:173311079ab932318629c9bfc59957c46ffef6d9500148722bf57885ab4d912e`  
		Last Modified: Sat, 22 Feb 2025 00:32:07 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5ef5273358e9d6949b1c0c7a006b2fe22a9b45af8454771a753c47f67702fc5`  
		Last Modified: Sat, 22 Feb 2025 00:32:09 GMT  
		Size: 19.8 MB (19841357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6550ae8a0cab9e35d0c0177c6afc594dd1f53008f4c0b85bdca771700fa770c`  
		Last Modified: Sat, 22 Feb 2025 00:32:06 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e430e1223ff0212bf349270e614e999171df037e89b09997ff907efa689e97d`  
		Last Modified: Sat, 22 Feb 2025 00:32:06 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adf1c042512ab6127e6371768343f9e2125e122a97350d29044867620964da29`  
		Last Modified: Sat, 22 Feb 2025 00:32:05 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbcc9f9bc1cf9f00d67c29fcbf84300c45479de6c73cf2f49f1ae660cf73bb07`  
		Last Modified: Sat, 22 Feb 2025 00:32:08 GMT  
		Size: 22.8 MB (22778890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b21becac3572331f658c564c93303ec2f6d01292e600e1b7deab5fea30b05ff6`  
		Last Modified: Sat, 22 Feb 2025 00:32:05 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e856f770850ac4d1cb287a7e7807f001c6f669a135f306ccf2fe6e63129def66`  
		Last Modified: Sat, 22 Feb 2025 00:32:05 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e457e71b003d1ce3d61f1df1c12e7500d728f4b5598604334164ddb533cb2ba`  
		Last Modified: Sat, 22 Feb 2025 00:32:05 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f63f581bda80c595a4087c00b71030e7a4d71012bb05cbc2eb9c139f9679e31`  
		Last Modified: Sat, 22 Feb 2025 00:32:08 GMT  
		Size: 21.9 MB (21925519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
