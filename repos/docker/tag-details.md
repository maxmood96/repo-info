<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `docker`

-	[`docker:29`](#docker29)
-	[`docker:29-cli`](#docker29-cli)
-	[`docker:29-dind`](#docker29-dind)
-	[`docker:29-dind-rootless`](#docker29-dind-rootless)
-	[`docker:29-windowsservercore`](#docker29-windowsservercore)
-	[`docker:29-windowsservercore-ltsc2022`](#docker29-windowsservercore-ltsc2022)
-	[`docker:29-windowsservercore-ltsc2025`](#docker29-windowsservercore-ltsc2025)
-	[`docker:29.5`](#docker295)
-	[`docker:29.5-cli`](#docker295-cli)
-	[`docker:29.5-dind`](#docker295-dind)
-	[`docker:29.5-dind-rootless`](#docker295-dind-rootless)
-	[`docker:29.5-windowsservercore`](#docker295-windowsservercore)
-	[`docker:29.5-windowsservercore-ltsc2022`](#docker295-windowsservercore-ltsc2022)
-	[`docker:29.5-windowsservercore-ltsc2025`](#docker295-windowsservercore-ltsc2025)
-	[`docker:29.5.2`](#docker2952)
-	[`docker:29.5.2-alpine3.23`](#docker2952-alpine323)
-	[`docker:29.5.2-cli`](#docker2952-cli)
-	[`docker:29.5.2-cli-alpine3.23`](#docker2952-cli-alpine323)
-	[`docker:29.5.2-dind`](#docker2952-dind)
-	[`docker:29.5.2-dind-alpine3.23`](#docker2952-dind-alpine323)
-	[`docker:29.5.2-dind-rootless`](#docker2952-dind-rootless)
-	[`docker:29.5.2-windowsservercore`](#docker2952-windowsservercore)
-	[`docker:29.5.2-windowsservercore-ltsc2022`](#docker2952-windowsservercore-ltsc2022)
-	[`docker:29.5.2-windowsservercore-ltsc2025`](#docker2952-windowsservercore-ltsc2025)
-	[`docker:cli`](#dockercli)
-	[`docker:dind`](#dockerdind)
-	[`docker:dind-rootless`](#dockerdind-rootless)
-	[`docker:latest`](#dockerlatest)
-	[`docker:windowsservercore`](#dockerwindowsservercore)
-	[`docker:windowsservercore-ltsc2022`](#dockerwindowsservercore-ltsc2022)
-	[`docker:windowsservercore-ltsc2025`](#dockerwindowsservercore-ltsc2025)

## `docker:29`

```console
$ docker pull docker@sha256:eed377f3ce14afda560e742c5b3ae446df1ce00a16e1beab2ac6c78c1477fe85
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

### `docker:29` - linux; amd64

```console
$ docker pull docker@sha256:6f156e0882b6f307bcd00e01b7abebdccf6eb96b1bb40e8b160e3e401ba3749b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.7 MB (141660887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a475a10539689996453c7c7aa57795a1c35cb8da621faddaef1fb0f05cdb7723`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Tue, 19 May 2026 18:43:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 19 May 2026 18:43:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 19 May 2026 18:43:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 19 May 2026 18:43:53 GMT
ENV DOCKER_VERSION=29.5.1
# Tue, 19 May 2026 18:43:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 19 May 2026 18:43:53 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Tue, 19 May 2026 18:43:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-amd64'; 			sha256='0144479d5a1cd710be3464ae898628cfa68033e16b225aef52f81930c45ac9b5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v6'; 			sha256='1f34337385921c5da43d63452282726b062aa887fda975f96dd3d6e869648bc6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v7'; 			sha256='3560b5b6fd3485f4d0bd160e7edf56cc1f08f0cb5852c9af28bf3fab9973c7c2'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm64'; 			sha256='565605fe0bb393ed5d11771e5b52fc7ef05c701868861fa85609747c9d74a440'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-ppc64le'; 			sha256='c5ef8012f48a518e1c235ad408d26cd424d7b5fa87eaf78cb2ff4b9048730120'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-riscv64'; 			sha256='80b27d5f3a346591a5045b81217ee5be578ed151ef8cbd883a892c0ec0ac33f1'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-s390x'; 			sha256='04f5bd0d389f682c7e9287a3b3a1777b0848f8e10d58cbf9d4d12c9002bbb378'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 19 May 2026 18:43:54 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Tue, 19 May 2026 18:43:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 19 May 2026 18:43:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 19 May 2026 18:43:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 18:43:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 19 May 2026 18:43:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 19 May 2026 18:43:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 May 2026 18:43:55 GMT
CMD ["sh"]
# Tue, 19 May 2026 18:52:09 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 19 May 2026 18:52:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 19 May 2026 18:52:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 19 May 2026 18:52:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 19 May 2026 18:52:13 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 19 May 2026 18:52:13 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 19 May 2026 18:52:13 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 18:52:13 GMT
VOLUME [/var/lib/docker]
# Tue, 19 May 2026 18:52:13 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 19 May 2026 18:52:13 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 19 May 2026 18:52:13 GMT
CMD []
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959d822c11f4cffde22f6a8ca77070ab678788ee8a60e50bf52240fab7600d55`  
		Last Modified: Tue, 19 May 2026 18:44:02 GMT  
		Size: 8.3 MB (8311621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf748eeffe46320957e43a6d041504e02f6d54efaa90b05ea0a5e76259a3bc9`  
		Last Modified: Tue, 19 May 2026 18:44:01 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29db3e4d2cf2bffd95a0b8c095c0dfc7f4b6ee9717169afb9c613ae0714f22a5`  
		Last Modified: Tue, 19 May 2026 18:44:03 GMT  
		Size: 19.5 MB (19549501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:418895c8a0097a67712f5b2385b094ed4ed5af1359b9b43cb86c07da48ca11c9`  
		Last Modified: Tue, 19 May 2026 18:44:03 GMT  
		Size: 23.0 MB (22988580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4382b5de8ae74e74d495d9d94f0127cf051728dc00cab26dfa163bba8cdbcf13`  
		Last Modified: Tue, 19 May 2026 18:44:03 GMT  
		Size: 11.2 MB (11243752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53914aaed626c98320ff52b5bbe81eb804e9a82d445d07a5908e16e86ac5a5c`  
		Last Modified: Tue, 19 May 2026 18:44:03 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cac0928dd7f6aa6c83aa987350f200df21db15618f2ba47912f35be2b16b3b9`  
		Last Modified: Tue, 19 May 2026 18:44:04 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1c069fc81d4d790f039a7a8160f23dffa6c11a22ee385a0db0fe75ae235dfe1`  
		Last Modified: Tue, 19 May 2026 18:44:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27817872a6ae6fcf22af6f3dbdec0f52f7b055d8b3384cd5b922f74d11358249`  
		Last Modified: Tue, 19 May 2026 18:52:23 GMT  
		Size: 6.9 MB (6941424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a7ba7363a81328286ac28be79b6e6248a1e1c4cb3f1749b808bc8abeb5c686`  
		Last Modified: Tue, 19 May 2026 18:52:23 GMT  
		Size: 92.2 KB (92218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f90442d3c5cd85fdf0fd4683516f39486a803bd57eb9813b3dcb939d9d3fcc`  
		Last Modified: Tue, 19 May 2026 18:52:23 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c588cc6d3552d3ec8363fa8dabb97cfe3ea467efd07c37c45853267ab5c544`  
		Last Modified: Tue, 19 May 2026 18:52:25 GMT  
		Size: 68.7 MB (68661447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa91ecdbc2c72221f7c567a768c787e9b0e27629ad60fecaa37b420555dbec4`  
		Last Modified: Tue, 19 May 2026 18:52:24 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a04f224ef5d78ccf3d32a655e7621773237de1ba0a09780d2011e4e3efc9802`  
		Last Modified: Tue, 19 May 2026 18:52:25 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:8459bca25b1862c9c244d8290b9c289f8f38a28e911360560cef489552fd9996
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca9c00d43298e9a165fe521202b47e762e0e30cdaad754b907fb2241affba41a`

```dockerfile
```

-	Layers:
	-	`sha256:725c95ff8cee96878c88b2d98ed922fc03f42a86c848e44ace4d3602cca233bd`  
		Last Modified: Tue, 19 May 2026 18:52:23 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29` - linux; arm variant v6

```console
$ docker pull docker@sha256:656cd6a2deb516bf1bab86d4eb9e0ea9b2afca3fb8c81a402195068521496791
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.6 MB (133554774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b375b41ebcd63fd76689fd0c53d0cbebdb1c6086df5568f03b1342739485d2f4`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Tue, 19 May 2026 18:46:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 19 May 2026 18:46:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 19 May 2026 18:46:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 19 May 2026 18:46:29 GMT
ENV DOCKER_VERSION=29.5.1
# Tue, 19 May 2026 18:46:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 19 May 2026 18:46:29 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Tue, 19 May 2026 18:46:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-amd64'; 			sha256='0144479d5a1cd710be3464ae898628cfa68033e16b225aef52f81930c45ac9b5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v6'; 			sha256='1f34337385921c5da43d63452282726b062aa887fda975f96dd3d6e869648bc6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v7'; 			sha256='3560b5b6fd3485f4d0bd160e7edf56cc1f08f0cb5852c9af28bf3fab9973c7c2'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm64'; 			sha256='565605fe0bb393ed5d11771e5b52fc7ef05c701868861fa85609747c9d74a440'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-ppc64le'; 			sha256='c5ef8012f48a518e1c235ad408d26cd424d7b5fa87eaf78cb2ff4b9048730120'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-riscv64'; 			sha256='80b27d5f3a346591a5045b81217ee5be578ed151ef8cbd883a892c0ec0ac33f1'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-s390x'; 			sha256='04f5bd0d389f682c7e9287a3b3a1777b0848f8e10d58cbf9d4d12c9002bbb378'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 19 May 2026 18:46:32 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Tue, 19 May 2026 18:46:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 19 May 2026 18:46:33 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 19 May 2026 18:46:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 18:46:33 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 19 May 2026 18:46:34 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 19 May 2026 18:46:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 May 2026 18:46:34 GMT
CMD ["sh"]
# Tue, 19 May 2026 18:48:00 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 19 May 2026 18:48:00 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 19 May 2026 18:48:00 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 19 May 2026 18:48:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 19 May 2026 18:48:04 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 19 May 2026 18:48:04 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 19 May 2026 18:48:04 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 18:48:04 GMT
VOLUME [/var/lib/docker]
# Tue, 19 May 2026 18:48:04 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 19 May 2026 18:48:04 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 19 May 2026 18:48:04 GMT
CMD []
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e510993d358b2182e33432b09c723cb2de90442627624e753d33ff6f58e37cf`  
		Last Modified: Tue, 19 May 2026 18:46:40 GMT  
		Size: 8.2 MB (8211856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac6422e386e61fe4ba4eb1abca9f67aef1bba270f947f3797505168eddc865ef`  
		Last Modified: Tue, 19 May 2026 18:46:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c6104ecd7c2122cba9eadf591b901752e839d28c94e9786023634ab16c4e86`  
		Last Modified: Tue, 19 May 2026 18:46:41 GMT  
		Size: 18.2 MB (18183185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9278a90d0e78f94da7f59f70fe4811830047483868d42c4e25a85b91a3359765`  
		Last Modified: Tue, 19 May 2026 18:46:41 GMT  
		Size: 21.6 MB (21614147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09f94e1195a7d62fc4046fa609e325b2001195cf49352924129c45728445d565`  
		Last Modified: Tue, 19 May 2026 18:46:41 GMT  
		Size: 10.7 MB (10650824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a8126c2985de246f1344d8c4340e5934b14cdf06f269351c0bfeac534be4c3a`  
		Last Modified: Tue, 19 May 2026 18:46:41 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f13c028f2e167a9ccd442fe69b89b5f1ca9e19f4589d7160d5af4d3b451ba862`  
		Last Modified: Tue, 19 May 2026 18:46:42 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa9769c6262cc549e78864817d114f4780b6b611ff08c097bcb018ab9040fd0`  
		Last Modified: Tue, 19 May 2026 18:46:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:125e5e8c972742a3fdece68d1d7efe160fc572758035dc6dd440150a5dff5bf7`  
		Last Modified: Tue, 19 May 2026 18:48:15 GMT  
		Size: 7.3 MB (7278661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:092dd15fda2f6f91745deb58f699d28c2ae054d7fb4d6c4100b53f0f8e3a6d85`  
		Last Modified: Tue, 19 May 2026 18:48:15 GMT  
		Size: 91.5 KB (91516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc718ec10edd9882bc794dfec135ed20f43243a8db5ad70f2ca75ac4b4191815`  
		Last Modified: Tue, 19 May 2026 18:48:15 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf390f2615c4c05543ef083213b7da580fc3a675929438042a5228503644f65`  
		Last Modified: Tue, 19 May 2026 18:48:17 GMT  
		Size: 63.9 MB (63944568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0111492ca1c0d70617ea1ed481e8ae4908695479c10dc5b86fe761dd03edc6b`  
		Last Modified: Tue, 19 May 2026 18:48:16 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b88ff88aa94e286fad9d8f3480fb92ba8ec324a9d55d74cce8cce2e99c36353`  
		Last Modified: Tue, 19 May 2026 18:48:16 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:1fd6b9654a40244c2a32a42dfdbd4b0c2fcd97aaacc719b9c466fed8008b0c05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e4f0d6a13a6e324e492f0fd9ae8856d26b30b034d24e9b3868069907c61ec10`

```dockerfile
```

-	Layers:
	-	`sha256:096e9d4d3b5e87687de3559cc60228911d8179792add0ad0a60e1afd76f2b032`  
		Last Modified: Tue, 19 May 2026 18:48:14 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29` - linux; arm variant v7

```console
$ docker pull docker@sha256:ce68e53519cdc94c6b28b82b2e4af1856aa5dd8e577fb872900952a6ed88f9d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.7 MB (131668449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bc263b60a94589a9d3f238ee64951d8f806cc46c8caed0452715d45111a5b91`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Tue, 19 May 2026 18:50:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 19 May 2026 18:50:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 19 May 2026 18:50:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 19 May 2026 18:50:21 GMT
ENV DOCKER_VERSION=29.5.1
# Tue, 19 May 2026 18:50:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 19 May 2026 18:50:21 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Tue, 19 May 2026 18:50:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-amd64'; 			sha256='0144479d5a1cd710be3464ae898628cfa68033e16b225aef52f81930c45ac9b5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v6'; 			sha256='1f34337385921c5da43d63452282726b062aa887fda975f96dd3d6e869648bc6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v7'; 			sha256='3560b5b6fd3485f4d0bd160e7edf56cc1f08f0cb5852c9af28bf3fab9973c7c2'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm64'; 			sha256='565605fe0bb393ed5d11771e5b52fc7ef05c701868861fa85609747c9d74a440'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-ppc64le'; 			sha256='c5ef8012f48a518e1c235ad408d26cd424d7b5fa87eaf78cb2ff4b9048730120'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-riscv64'; 			sha256='80b27d5f3a346591a5045b81217ee5be578ed151ef8cbd883a892c0ec0ac33f1'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-s390x'; 			sha256='04f5bd0d389f682c7e9287a3b3a1777b0848f8e10d58cbf9d4d12c9002bbb378'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 19 May 2026 18:50:23 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Tue, 19 May 2026 18:50:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 19 May 2026 18:50:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 19 May 2026 18:50:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 18:50:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 19 May 2026 18:50:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 19 May 2026 18:50:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 May 2026 18:50:24 GMT
CMD ["sh"]
# Tue, 19 May 2026 19:11:05 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 19 May 2026 19:11:05 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 19 May 2026 19:11:05 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 19 May 2026 19:11:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 19 May 2026 19:11:10 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 19 May 2026 19:11:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 19 May 2026 19:11:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 19:11:10 GMT
VOLUME [/var/lib/docker]
# Tue, 19 May 2026 19:11:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 19 May 2026 19:11:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 19 May 2026 19:11:10 GMT
CMD []
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e78396f075a6021fa389cbab78d2b7a97c1fa6ccd90c5a3f9aad13a82d9a82d5`  
		Last Modified: Tue, 19 May 2026 18:50:31 GMT  
		Size: 7.5 MB (7520541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55503681071acc50ecd4d54f1a76c32b34fb2e24b116717b8a11a5ed2c4b834b`  
		Last Modified: Tue, 19 May 2026 18:50:30 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:139bfdfb0c5a911c258bd9ca3f33e5d74dc4cdac244e701ffc230dfb2dbcf299`  
		Last Modified: Tue, 19 May 2026 18:50:31 GMT  
		Size: 18.2 MB (18172268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e28d126c0c15c1ddece42e48d16b7989f46d4ba83543ade587e34aae442b162d`  
		Last Modified: Tue, 19 May 2026 18:50:31 GMT  
		Size: 21.6 MB (21600397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb484c140400a96468ac162a856058550dff5319ecf84cb2d15485ffa462cfe5`  
		Last Modified: Tue, 19 May 2026 18:50:31 GMT  
		Size: 10.6 MB (10637143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:458ff3d79525d794f095fe12c99f3a95a84e674163d4ac75823a6bbe91cdca6c`  
		Last Modified: Tue, 19 May 2026 18:50:32 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:252522a027743939f7b115d2d3929238ba7a8fee776336371433d62e17da49f3`  
		Last Modified: Tue, 19 May 2026 18:50:33 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b1fd0762adb2df9e41385aaea4f5aeb069ccb43ec6a5203c0970dbb32f5d39`  
		Last Modified: Tue, 19 May 2026 18:50:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2404388a95cbd53c2924a8956a2b0bd9fed1ed42798ef0d7958645ec50b36503`  
		Last Modified: Tue, 19 May 2026 19:11:21 GMT  
		Size: 6.6 MB (6577150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abebc77c5a81c02e559a6177ab009ea93d155d230027ecb011d71caf8e1319cb`  
		Last Modified: Tue, 19 May 2026 19:11:20 GMT  
		Size: 87.8 KB (87825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:505cb9808a455382b226432bd33efca0786f2b2817e3828966e8ae1880b9a387`  
		Last Modified: Tue, 19 May 2026 19:11:20 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb736cbd14a0b4279f19088aba50827f55f5bd8c64dd5868c81329ee396e19f`  
		Last Modified: Tue, 19 May 2026 19:11:23 GMT  
		Size: 63.8 MB (63781847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b8e0456f81c21846bbc1e4af0c8ce599dde97bbda1d981de3f47999ce045a4`  
		Last Modified: Tue, 19 May 2026 19:11:22 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10bd67dffac6bb7c60a61f90d9e059f51d217061b38efadfa05cfbccc501c4eb`  
		Last Modified: Tue, 19 May 2026 19:11:22 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:38aff3f9f68bc80866a840b6895120e3efd20f227f69ca66663fee2a5c143d5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e771280fb8341ddf485470385301e8a4df555c4889817952e2e3f1bc2d60f3f`

```dockerfile
```

-	Layers:
	-	`sha256:0f43b1170bad091b1f8a038b4c799e044dcbe62f3cf88792df12fd3808abd3db`  
		Last Modified: Tue, 19 May 2026 19:11:20 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:d29f00616a4b5af545c6238d5e5d3f010dabe8cd9373464e7528dcc2ffe932e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.1 MB (131088931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d59db2bca67549c508438fad529bbb4d973798fdf3dac19d4cff714cd0ef24d8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Tue, 19 May 2026 18:52:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 19 May 2026 18:52:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 19 May 2026 18:52:13 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 19 May 2026 18:52:16 GMT
ENV DOCKER_VERSION=29.5.1
# Tue, 19 May 2026 18:52:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 19 May 2026 18:52:16 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Tue, 19 May 2026 18:52:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-amd64'; 			sha256='0144479d5a1cd710be3464ae898628cfa68033e16b225aef52f81930c45ac9b5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v6'; 			sha256='1f34337385921c5da43d63452282726b062aa887fda975f96dd3d6e869648bc6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v7'; 			sha256='3560b5b6fd3485f4d0bd160e7edf56cc1f08f0cb5852c9af28bf3fab9973c7c2'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm64'; 			sha256='565605fe0bb393ed5d11771e5b52fc7ef05c701868861fa85609747c9d74a440'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-ppc64le'; 			sha256='c5ef8012f48a518e1c235ad408d26cd424d7b5fa87eaf78cb2ff4b9048730120'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-riscv64'; 			sha256='80b27d5f3a346591a5045b81217ee5be578ed151ef8cbd883a892c0ec0ac33f1'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-s390x'; 			sha256='04f5bd0d389f682c7e9287a3b3a1777b0848f8e10d58cbf9d4d12c9002bbb378'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 19 May 2026 18:52:17 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Tue, 19 May 2026 18:52:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 19 May 2026 18:52:18 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 19 May 2026 18:52:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 18:52:18 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 19 May 2026 18:52:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 19 May 2026 18:52:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 May 2026 18:52:18 GMT
CMD ["sh"]
# Tue, 19 May 2026 19:11:28 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 19 May 2026 19:11:28 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 19 May 2026 19:11:29 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 19 May 2026 19:11:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 19 May 2026 19:11:31 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 19 May 2026 19:11:31 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 19 May 2026 19:11:31 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 19:11:31 GMT
VOLUME [/var/lib/docker]
# Tue, 19 May 2026 19:11:31 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 19 May 2026 19:11:31 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 19 May 2026 19:11:31 GMT
CMD []
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:439c73b6370f92c891e3dae2ef2ac51ba47633f4382e93fa3a194ab6c9929fcf`  
		Last Modified: Tue, 19 May 2026 18:52:24 GMT  
		Size: 8.4 MB (8368378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:090f26860bbcb42203be1c1ccc78e592537b7d5076712eddc078a4521b65b6ef`  
		Last Modified: Tue, 19 May 2026 18:52:23 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02fa5c43148b510203ce86fd309a24339439966d97d2739e5681dea9fbedd78b`  
		Last Modified: Tue, 19 May 2026 18:52:24 GMT  
		Size: 18.0 MB (18003824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:179aebd9e04e34e062d99c03bced083b59894f9ff9c70a48e5fdde05043d0662`  
		Last Modified: Tue, 19 May 2026 18:52:25 GMT  
		Size: 20.8 MB (20815342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333ebd0d3068df15ad94c847b40ac364dc7140981f38d3a8f08165ef3fe528ac`  
		Last Modified: Tue, 19 May 2026 18:52:25 GMT  
		Size: 10.2 MB (10243275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e7cd72262f0dcb67fc210c582e3d890f8da6bbfea7979a4af0eca2d85493c8`  
		Last Modified: Tue, 19 May 2026 18:52:25 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb8c848507ade63fa035c4247243268bc78609cb843c2c46923fec82cf42e856`  
		Last Modified: Tue, 19 May 2026 18:52:26 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14678f991761f143ab6345db5de4a84ca5f83a1cd44f7d579a88be20ad20871`  
		Last Modified: Tue, 19 May 2026 18:52:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deb061c465c1d4b2683f89277bb8b93644ad86d3b6a034d3848e218ff3a36250`  
		Last Modified: Tue, 19 May 2026 19:11:41 GMT  
		Size: 7.2 MB (7219902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408cc9607ded7836e6377a9012f389a02da93bc2526404ac2125d556fed0607c`  
		Last Modified: Tue, 19 May 2026 19:11:41 GMT  
		Size: 100.9 KB (100930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4813a99698e1ee0cbb52b02f822e9732eb9144586aa3c765fee806857d8cb872`  
		Last Modified: Tue, 19 May 2026 19:11:41 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f364d3985b9e2a29ae89857aa654e13a752db4b807f58b23afc56a7fdddc9ca`  
		Last Modified: Tue, 19 May 2026 19:11:43 GMT  
		Size: 62.1 MB (62129257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34b8039e34935754bb978ab40f852eeb6345408e37deb40c0467f77421c8252`  
		Last Modified: Tue, 19 May 2026 19:11:42 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be12674817c3cc5397950df61ba9f0761de7cbb67e7527d120f671791e1644f9`  
		Last Modified: Tue, 19 May 2026 19:11:42 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:8ac585f5eb9117c0193cbfc718548d3dca67a7e669159a6b08a53ae907925d21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa5bac19b0eae7a6debca0657ab9da39a1528d516c371778235e72d5db216621`

```dockerfile
```

-	Layers:
	-	`sha256:662dc4eaa00e9b2353b08fdbf55f624046c556fe7fa5b07f0332cfd3384d50fb`  
		Last Modified: Tue, 19 May 2026 19:11:40 GMT  
		Size: 34.8 KB (34782 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-cli`

```console
$ docker pull docker@sha256:9ba8e32bfc35a2c7ae2feb1e3241b2778ae21dee80f4dcd31d04e1cfdea86ea2
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

### `docker:29-cli` - linux; amd64

```console
$ docker pull docker@sha256:ec66e6a33f2769030bf8f283b25a7ea135d770ed2c3b91c14195de0ca901e61a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.1 MB (66112304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a190ccdf9e97f139d089920e904db8c97e394f8b5f3ff536cdadeda6c821ded`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Thu, 21 May 2026 22:56:57 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 21 May 2026 22:56:57 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 21 May 2026 22:56:57 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 21 May 2026 22:56:59 GMT
ENV DOCKER_VERSION=29.5.2
# Thu, 21 May 2026 22:56:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 21 May 2026 22:56:59 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 21 May 2026 22:57:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 21 May 2026 22:57:00 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 21 May 2026 22:57:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 21 May 2026 22:57:01 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 21 May 2026 22:57:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 21 May 2026 22:57:01 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 21 May 2026 22:57:01 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 21 May 2026 22:57:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 May 2026 22:57:01 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6cf87df21c231c07f8b8d9c532474fc120946d085773fa15272382636f10b46`  
		Last Modified: Thu, 21 May 2026 22:57:08 GMT  
		Size: 8.3 MB (8311580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54392fc3db24e998571260adc7ac1a1bc098852dfeb30150218d2174da4aa929`  
		Last Modified: Thu, 21 May 2026 22:57:07 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4b052546a5d5d26f7d251d92bd155e2275ee74b4c83a5748550720fa39efe1`  
		Last Modified: Thu, 21 May 2026 22:57:08 GMT  
		Size: 19.5 MB (19549520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b2deac6c9ceba582f6a7f4a7ea2910141ba0dfcf644ee930db818a78947527a`  
		Last Modified: Thu, 21 May 2026 22:57:08 GMT  
		Size: 23.0 MB (22988915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:046b51e466e9d4d0fb090dd060997a0892b36578ab13f0153d1d61f53166d5c6`  
		Last Modified: Thu, 21 May 2026 22:57:09 GMT  
		Size: 11.4 MB (11395947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff5ffb634dd2a67009edb32be895febc923676e8dc0b94f8c857528723140ee`  
		Last Modified: Thu, 21 May 2026 22:57:09 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b162b8dd068432fdb9682bbf9fc7ecbe61c2dbbb72441a22b74a6537f7fe639`  
		Last Modified: Thu, 21 May 2026 22:57:10 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b02815b1d866ccad16190784679c75c04f712dc13f12bd8ec46cf7648796905`  
		Last Modified: Thu, 21 May 2026 22:57:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:d0c058683425ac4a4e35818c3cab8e244bf44bf5629b2606d503eab0302918c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24cd59892835a6bb71bef956c207f451b0ff4ef20ef700549178228a80696991`

```dockerfile
```

-	Layers:
	-	`sha256:e8d0f9a2c1d7978db5312a52983dc91318b6ef2d7b32afeed756151fcba3ed72`  
		Last Modified: Thu, 21 May 2026 22:57:07 GMT  
		Size: 38.1 KB (38056 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:1ea54fcc950d7b127dc87b88d28c747600cca8b48d8c034ecd527709330f2074
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62396270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8d2a98d406c875d3e0db6343c8b5fa56023aa689cb018d156b714f0199d7ab8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Thu, 21 May 2026 22:57:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 21 May 2026 22:57:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 21 May 2026 22:57:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 21 May 2026 22:57:14 GMT
ENV DOCKER_VERSION=29.5.2
# Thu, 21 May 2026 22:57:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 21 May 2026 22:57:14 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 21 May 2026 22:57:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 21 May 2026 22:57:17 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 21 May 2026 22:57:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 21 May 2026 22:57:18 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 21 May 2026 22:57:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 21 May 2026 22:57:19 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 21 May 2026 22:57:19 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 21 May 2026 22:57:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 May 2026 22:57:19 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:686f209ff6de10676a89d77e3e8a6fab30545d5720ccf9054ee0d1b26e38b43a`  
		Last Modified: Thu, 21 May 2026 22:57:25 GMT  
		Size: 8.2 MB (8211872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc482e1b01e42c3c70b99620637bf883c5da46458460af902ddff0ac829fe8be`  
		Last Modified: Thu, 21 May 2026 22:57:24 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6ca55f6f19c616ff991f7a3db821aff9610c17f90b38f47cbd8f4524f46539`  
		Last Modified: Thu, 21 May 2026 22:57:25 GMT  
		Size: 18.2 MB (18183161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83229a063dcdaa05d49b47a377f6266b68058c99c6e0d8dfdc2a7d84012787eb`  
		Last Modified: Thu, 21 May 2026 22:57:25 GMT  
		Size: 21.6 MB (21614627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:940f9c6bb6e92b7182721c14634a231b228afd28fe04caffd78841f7dd24411b`  
		Last Modified: Thu, 21 May 2026 22:57:26 GMT  
		Size: 10.8 MB (10812594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c13701af534883715f5b32ba09cbb6f13feb5042a866f77e574177b03153cb1`  
		Last Modified: Thu, 21 May 2026 22:57:27 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5827618b0a4b3c9209e2ce38a22a9c7e3bf8dc8d55f12ece8a624cec59ca0c0`  
		Last Modified: Thu, 21 May 2026 22:57:27 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:156a2ca1e461bbe26a51cde3454797f4bb525e545ae12a790eb2c832fa3cd344`  
		Last Modified: Thu, 21 May 2026 22:57:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:04ebdfb0eda18157d342b7fb08c62391f19045358bdd9d13363d75b2bf405b48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c878c65dd1bf46ceb912d86983dbbb6747bbc0d9f04388340d7ff40ab6a955b5`

```dockerfile
```

-	Layers:
	-	`sha256:a18fb0bd08433a7ea29e919c067320a3a5064d90b3bf6926746198a604fa7c2e`  
		Last Modified: Thu, 21 May 2026 22:57:24 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:4efa5b423f6548c5521b0093e3276bff164af4e70d51c1368309a76e916622e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61378438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d52d0f5e6c9123362925f36aa888038a8dd446e137138fb8463b681a0bc5dff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Thu, 21 May 2026 22:57:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 21 May 2026 22:57:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 21 May 2026 22:57:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 21 May 2026 22:57:19 GMT
ENV DOCKER_VERSION=29.5.2
# Thu, 21 May 2026 22:57:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 21 May 2026 22:57:19 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 21 May 2026 22:57:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 21 May 2026 22:57:21 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 21 May 2026 22:57:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 21 May 2026 22:57:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 21 May 2026 22:57:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 21 May 2026 22:57:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 21 May 2026 22:57:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 21 May 2026 22:57:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 May 2026 22:57:22 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f52861283d77a40b5946e65011de57aef34bc9327b32604f88a677e6f2cb2a`  
		Last Modified: Thu, 21 May 2026 22:57:29 GMT  
		Size: 7.5 MB (7520603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe77c7d8ef7315ec44519db3cec2d9d47ed19881a859e1f59af47b6ee930987`  
		Last Modified: Thu, 21 May 2026 22:57:29 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb66512e1233e73a0972411ebf4f8c344ca4a394da4d49e6b222234bb111c827`  
		Last Modified: Thu, 21 May 2026 22:57:30 GMT  
		Size: 18.2 MB (18172264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa22bb61dc858338f97353ad033e1a3dfeaedd00a1bc504c85cb83d1d1e1066`  
		Last Modified: Thu, 21 May 2026 22:57:30 GMT  
		Size: 21.6 MB (21600713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36a896b5ff64585ed1221a91d5f2f671787cd3897f86991c0f6fe8525f7d75c0`  
		Last Modified: Thu, 21 May 2026 22:57:30 GMT  
		Size: 10.8 MB (10799582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce88e69f3e7c7ac17129a6b4b87aad6b39a3a2861c81d554e406b2547561f66`  
		Last Modified: Thu, 21 May 2026 22:57:30 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5758ccda3473178260da62e4ab7c4fa36a8dfc1c4ef7d4fed06e0ea0fb533c09`  
		Last Modified: Thu, 21 May 2026 22:57:31 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e4468a079208fc160ee3dd1c7df3de47f866b433f720289671fd2ab2bf8a6d`  
		Last Modified: Thu, 21 May 2026 22:57:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:73a5dfa31ffac43a7e451c867bb1707eb46361077e17b338feea6d1cfe16074c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:213b655767f4e7e1aa870b4cdd07817a9d99c15bc554800b7bf98c33cfb92cc9`

```dockerfile
```

-	Layers:
	-	`sha256:88b55d2936f52c50f0f1b5bdd99b1c08534f7a93ef0c66f562f45ef6679cac29`  
		Last Modified: Thu, 21 May 2026 22:57:28 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:1c27de1f16ee894e6389586d8b58391f4b941f768cb5520cd2970c72d38a8e84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61750058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:156869ccb322d51e7560b80292b10dfaa423516486f6683494060b76d38dabcc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Thu, 21 May 2026 22:56:32 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 21 May 2026 22:56:32 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 21 May 2026 22:56:32 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 21 May 2026 22:56:34 GMT
ENV DOCKER_VERSION=29.5.2
# Thu, 21 May 2026 22:56:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 21 May 2026 22:56:34 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 21 May 2026 22:56:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 21 May 2026 22:56:35 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 21 May 2026 22:56:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 21 May 2026 22:56:36 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 21 May 2026 22:56:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 21 May 2026 22:56:36 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 21 May 2026 22:56:36 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 21 May 2026 22:56:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 May 2026 22:56:36 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae988a6da12e07a4495206223708dfa12193c715305da0959269e07cfe0883c`  
		Last Modified: Thu, 21 May 2026 22:56:42 GMT  
		Size: 8.4 MB (8368391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad63753001c8116da8d4078088f8c226c9d2d5ebb32c543695bad3dfd05cb848`  
		Last Modified: Thu, 21 May 2026 22:56:42 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1523489b9bcf5899f4ec01d3ea4b3b09a7f11127bd6cfac3ad985d4e121a917`  
		Last Modified: Thu, 21 May 2026 22:56:43 GMT  
		Size: 18.0 MB (18003804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4276c1b3c4ca523a976f2b634bcd7b921a29dbff4274ac9aa9cc1e68ed96f93`  
		Last Modified: Thu, 21 May 2026 22:56:43 GMT  
		Size: 20.8 MB (20815981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e3a6fedf4004b1aba4e7b35c15a75f4e30fd0ae9d353199415f18fd99a7cf8`  
		Last Modified: Thu, 21 May 2026 22:56:43 GMT  
		Size: 10.4 MB (10359860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37af9029ae6a6376f88d713b9b54fb69ece2959cf06985f67d3905c6ef36739`  
		Last Modified: Thu, 21 May 2026 22:56:44 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56df60bc257eb03677643450dfa9477ebdad3b524820a408218637a85932c45d`  
		Last Modified: Thu, 21 May 2026 22:56:44 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe07c252ff4b96737716f829e1e8ff46a81625412f850d98480be21cf51f845`  
		Last Modified: Thu, 21 May 2026 22:56:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:a8dedaaa0ddf7100fc1cf4d4aee8dec52a0bd683ada897dc62942f5c0b88d846
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30bdb74e1af7301d0ea10753180b6ea04b819ea07777e30c7cc70392aefbb2db`

```dockerfile
```

-	Layers:
	-	`sha256:ddd2ae6062cdfd1652888a3cbd3bdc652070dde80dc25a31826cfb552cb05649`  
		Last Modified: Thu, 21 May 2026 22:56:42 GMT  
		Size: 38.3 KB (38262 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-dind`

```console
$ docker pull docker@sha256:eed377f3ce14afda560e742c5b3ae446df1ce00a16e1beab2ac6c78c1477fe85
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

### `docker:29-dind` - linux; amd64

```console
$ docker pull docker@sha256:6f156e0882b6f307bcd00e01b7abebdccf6eb96b1bb40e8b160e3e401ba3749b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.7 MB (141660887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a475a10539689996453c7c7aa57795a1c35cb8da621faddaef1fb0f05cdb7723`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Tue, 19 May 2026 18:43:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 19 May 2026 18:43:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 19 May 2026 18:43:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 19 May 2026 18:43:53 GMT
ENV DOCKER_VERSION=29.5.1
# Tue, 19 May 2026 18:43:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 19 May 2026 18:43:53 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Tue, 19 May 2026 18:43:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-amd64'; 			sha256='0144479d5a1cd710be3464ae898628cfa68033e16b225aef52f81930c45ac9b5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v6'; 			sha256='1f34337385921c5da43d63452282726b062aa887fda975f96dd3d6e869648bc6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v7'; 			sha256='3560b5b6fd3485f4d0bd160e7edf56cc1f08f0cb5852c9af28bf3fab9973c7c2'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm64'; 			sha256='565605fe0bb393ed5d11771e5b52fc7ef05c701868861fa85609747c9d74a440'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-ppc64le'; 			sha256='c5ef8012f48a518e1c235ad408d26cd424d7b5fa87eaf78cb2ff4b9048730120'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-riscv64'; 			sha256='80b27d5f3a346591a5045b81217ee5be578ed151ef8cbd883a892c0ec0ac33f1'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-s390x'; 			sha256='04f5bd0d389f682c7e9287a3b3a1777b0848f8e10d58cbf9d4d12c9002bbb378'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 19 May 2026 18:43:54 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Tue, 19 May 2026 18:43:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 19 May 2026 18:43:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 19 May 2026 18:43:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 18:43:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 19 May 2026 18:43:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 19 May 2026 18:43:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 May 2026 18:43:55 GMT
CMD ["sh"]
# Tue, 19 May 2026 18:52:09 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 19 May 2026 18:52:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 19 May 2026 18:52:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 19 May 2026 18:52:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 19 May 2026 18:52:13 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 19 May 2026 18:52:13 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 19 May 2026 18:52:13 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 18:52:13 GMT
VOLUME [/var/lib/docker]
# Tue, 19 May 2026 18:52:13 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 19 May 2026 18:52:13 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 19 May 2026 18:52:13 GMT
CMD []
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959d822c11f4cffde22f6a8ca77070ab678788ee8a60e50bf52240fab7600d55`  
		Last Modified: Tue, 19 May 2026 18:44:02 GMT  
		Size: 8.3 MB (8311621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf748eeffe46320957e43a6d041504e02f6d54efaa90b05ea0a5e76259a3bc9`  
		Last Modified: Tue, 19 May 2026 18:44:01 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29db3e4d2cf2bffd95a0b8c095c0dfc7f4b6ee9717169afb9c613ae0714f22a5`  
		Last Modified: Tue, 19 May 2026 18:44:03 GMT  
		Size: 19.5 MB (19549501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:418895c8a0097a67712f5b2385b094ed4ed5af1359b9b43cb86c07da48ca11c9`  
		Last Modified: Tue, 19 May 2026 18:44:03 GMT  
		Size: 23.0 MB (22988580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4382b5de8ae74e74d495d9d94f0127cf051728dc00cab26dfa163bba8cdbcf13`  
		Last Modified: Tue, 19 May 2026 18:44:03 GMT  
		Size: 11.2 MB (11243752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53914aaed626c98320ff52b5bbe81eb804e9a82d445d07a5908e16e86ac5a5c`  
		Last Modified: Tue, 19 May 2026 18:44:03 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cac0928dd7f6aa6c83aa987350f200df21db15618f2ba47912f35be2b16b3b9`  
		Last Modified: Tue, 19 May 2026 18:44:04 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1c069fc81d4d790f039a7a8160f23dffa6c11a22ee385a0db0fe75ae235dfe1`  
		Last Modified: Tue, 19 May 2026 18:44:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27817872a6ae6fcf22af6f3dbdec0f52f7b055d8b3384cd5b922f74d11358249`  
		Last Modified: Tue, 19 May 2026 18:52:23 GMT  
		Size: 6.9 MB (6941424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a7ba7363a81328286ac28be79b6e6248a1e1c4cb3f1749b808bc8abeb5c686`  
		Last Modified: Tue, 19 May 2026 18:52:23 GMT  
		Size: 92.2 KB (92218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f90442d3c5cd85fdf0fd4683516f39486a803bd57eb9813b3dcb939d9d3fcc`  
		Last Modified: Tue, 19 May 2026 18:52:23 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c588cc6d3552d3ec8363fa8dabb97cfe3ea467efd07c37c45853267ab5c544`  
		Last Modified: Tue, 19 May 2026 18:52:25 GMT  
		Size: 68.7 MB (68661447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa91ecdbc2c72221f7c567a768c787e9b0e27629ad60fecaa37b420555dbec4`  
		Last Modified: Tue, 19 May 2026 18:52:24 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a04f224ef5d78ccf3d32a655e7621773237de1ba0a09780d2011e4e3efc9802`  
		Last Modified: Tue, 19 May 2026 18:52:25 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:8459bca25b1862c9c244d8290b9c289f8f38a28e911360560cef489552fd9996
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca9c00d43298e9a165fe521202b47e762e0e30cdaad754b907fb2241affba41a`

```dockerfile
```

-	Layers:
	-	`sha256:725c95ff8cee96878c88b2d98ed922fc03f42a86c848e44ace4d3602cca233bd`  
		Last Modified: Tue, 19 May 2026 18:52:23 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:656cd6a2deb516bf1bab86d4eb9e0ea9b2afca3fb8c81a402195068521496791
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.6 MB (133554774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b375b41ebcd63fd76689fd0c53d0cbebdb1c6086df5568f03b1342739485d2f4`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Tue, 19 May 2026 18:46:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 19 May 2026 18:46:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 19 May 2026 18:46:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 19 May 2026 18:46:29 GMT
ENV DOCKER_VERSION=29.5.1
# Tue, 19 May 2026 18:46:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 19 May 2026 18:46:29 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Tue, 19 May 2026 18:46:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-amd64'; 			sha256='0144479d5a1cd710be3464ae898628cfa68033e16b225aef52f81930c45ac9b5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v6'; 			sha256='1f34337385921c5da43d63452282726b062aa887fda975f96dd3d6e869648bc6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v7'; 			sha256='3560b5b6fd3485f4d0bd160e7edf56cc1f08f0cb5852c9af28bf3fab9973c7c2'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm64'; 			sha256='565605fe0bb393ed5d11771e5b52fc7ef05c701868861fa85609747c9d74a440'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-ppc64le'; 			sha256='c5ef8012f48a518e1c235ad408d26cd424d7b5fa87eaf78cb2ff4b9048730120'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-riscv64'; 			sha256='80b27d5f3a346591a5045b81217ee5be578ed151ef8cbd883a892c0ec0ac33f1'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-s390x'; 			sha256='04f5bd0d389f682c7e9287a3b3a1777b0848f8e10d58cbf9d4d12c9002bbb378'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 19 May 2026 18:46:32 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Tue, 19 May 2026 18:46:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 19 May 2026 18:46:33 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 19 May 2026 18:46:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 18:46:33 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 19 May 2026 18:46:34 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 19 May 2026 18:46:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 May 2026 18:46:34 GMT
CMD ["sh"]
# Tue, 19 May 2026 18:48:00 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 19 May 2026 18:48:00 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 19 May 2026 18:48:00 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 19 May 2026 18:48:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 19 May 2026 18:48:04 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 19 May 2026 18:48:04 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 19 May 2026 18:48:04 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 18:48:04 GMT
VOLUME [/var/lib/docker]
# Tue, 19 May 2026 18:48:04 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 19 May 2026 18:48:04 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 19 May 2026 18:48:04 GMT
CMD []
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e510993d358b2182e33432b09c723cb2de90442627624e753d33ff6f58e37cf`  
		Last Modified: Tue, 19 May 2026 18:46:40 GMT  
		Size: 8.2 MB (8211856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac6422e386e61fe4ba4eb1abca9f67aef1bba270f947f3797505168eddc865ef`  
		Last Modified: Tue, 19 May 2026 18:46:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c6104ecd7c2122cba9eadf591b901752e839d28c94e9786023634ab16c4e86`  
		Last Modified: Tue, 19 May 2026 18:46:41 GMT  
		Size: 18.2 MB (18183185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9278a90d0e78f94da7f59f70fe4811830047483868d42c4e25a85b91a3359765`  
		Last Modified: Tue, 19 May 2026 18:46:41 GMT  
		Size: 21.6 MB (21614147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09f94e1195a7d62fc4046fa609e325b2001195cf49352924129c45728445d565`  
		Last Modified: Tue, 19 May 2026 18:46:41 GMT  
		Size: 10.7 MB (10650824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a8126c2985de246f1344d8c4340e5934b14cdf06f269351c0bfeac534be4c3a`  
		Last Modified: Tue, 19 May 2026 18:46:41 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f13c028f2e167a9ccd442fe69b89b5f1ca9e19f4589d7160d5af4d3b451ba862`  
		Last Modified: Tue, 19 May 2026 18:46:42 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa9769c6262cc549e78864817d114f4780b6b611ff08c097bcb018ab9040fd0`  
		Last Modified: Tue, 19 May 2026 18:46:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:125e5e8c972742a3fdece68d1d7efe160fc572758035dc6dd440150a5dff5bf7`  
		Last Modified: Tue, 19 May 2026 18:48:15 GMT  
		Size: 7.3 MB (7278661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:092dd15fda2f6f91745deb58f699d28c2ae054d7fb4d6c4100b53f0f8e3a6d85`  
		Last Modified: Tue, 19 May 2026 18:48:15 GMT  
		Size: 91.5 KB (91516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc718ec10edd9882bc794dfec135ed20f43243a8db5ad70f2ca75ac4b4191815`  
		Last Modified: Tue, 19 May 2026 18:48:15 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf390f2615c4c05543ef083213b7da580fc3a675929438042a5228503644f65`  
		Last Modified: Tue, 19 May 2026 18:48:17 GMT  
		Size: 63.9 MB (63944568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0111492ca1c0d70617ea1ed481e8ae4908695479c10dc5b86fe761dd03edc6b`  
		Last Modified: Tue, 19 May 2026 18:48:16 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b88ff88aa94e286fad9d8f3480fb92ba8ec324a9d55d74cce8cce2e99c36353`  
		Last Modified: Tue, 19 May 2026 18:48:16 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:1fd6b9654a40244c2a32a42dfdbd4b0c2fcd97aaacc719b9c466fed8008b0c05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e4f0d6a13a6e324e492f0fd9ae8856d26b30b034d24e9b3868069907c61ec10`

```dockerfile
```

-	Layers:
	-	`sha256:096e9d4d3b5e87687de3559cc60228911d8179792add0ad0a60e1afd76f2b032`  
		Last Modified: Tue, 19 May 2026 18:48:14 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:ce68e53519cdc94c6b28b82b2e4af1856aa5dd8e577fb872900952a6ed88f9d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.7 MB (131668449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bc263b60a94589a9d3f238ee64951d8f806cc46c8caed0452715d45111a5b91`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Tue, 19 May 2026 18:50:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 19 May 2026 18:50:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 19 May 2026 18:50:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 19 May 2026 18:50:21 GMT
ENV DOCKER_VERSION=29.5.1
# Tue, 19 May 2026 18:50:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 19 May 2026 18:50:21 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Tue, 19 May 2026 18:50:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-amd64'; 			sha256='0144479d5a1cd710be3464ae898628cfa68033e16b225aef52f81930c45ac9b5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v6'; 			sha256='1f34337385921c5da43d63452282726b062aa887fda975f96dd3d6e869648bc6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v7'; 			sha256='3560b5b6fd3485f4d0bd160e7edf56cc1f08f0cb5852c9af28bf3fab9973c7c2'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm64'; 			sha256='565605fe0bb393ed5d11771e5b52fc7ef05c701868861fa85609747c9d74a440'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-ppc64le'; 			sha256='c5ef8012f48a518e1c235ad408d26cd424d7b5fa87eaf78cb2ff4b9048730120'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-riscv64'; 			sha256='80b27d5f3a346591a5045b81217ee5be578ed151ef8cbd883a892c0ec0ac33f1'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-s390x'; 			sha256='04f5bd0d389f682c7e9287a3b3a1777b0848f8e10d58cbf9d4d12c9002bbb378'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 19 May 2026 18:50:23 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Tue, 19 May 2026 18:50:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 19 May 2026 18:50:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 19 May 2026 18:50:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 18:50:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 19 May 2026 18:50:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 19 May 2026 18:50:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 May 2026 18:50:24 GMT
CMD ["sh"]
# Tue, 19 May 2026 19:11:05 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 19 May 2026 19:11:05 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 19 May 2026 19:11:05 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 19 May 2026 19:11:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 19 May 2026 19:11:10 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 19 May 2026 19:11:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 19 May 2026 19:11:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 19:11:10 GMT
VOLUME [/var/lib/docker]
# Tue, 19 May 2026 19:11:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 19 May 2026 19:11:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 19 May 2026 19:11:10 GMT
CMD []
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e78396f075a6021fa389cbab78d2b7a97c1fa6ccd90c5a3f9aad13a82d9a82d5`  
		Last Modified: Tue, 19 May 2026 18:50:31 GMT  
		Size: 7.5 MB (7520541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55503681071acc50ecd4d54f1a76c32b34fb2e24b116717b8a11a5ed2c4b834b`  
		Last Modified: Tue, 19 May 2026 18:50:30 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:139bfdfb0c5a911c258bd9ca3f33e5d74dc4cdac244e701ffc230dfb2dbcf299`  
		Last Modified: Tue, 19 May 2026 18:50:31 GMT  
		Size: 18.2 MB (18172268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e28d126c0c15c1ddece42e48d16b7989f46d4ba83543ade587e34aae442b162d`  
		Last Modified: Tue, 19 May 2026 18:50:31 GMT  
		Size: 21.6 MB (21600397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb484c140400a96468ac162a856058550dff5319ecf84cb2d15485ffa462cfe5`  
		Last Modified: Tue, 19 May 2026 18:50:31 GMT  
		Size: 10.6 MB (10637143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:458ff3d79525d794f095fe12c99f3a95a84e674163d4ac75823a6bbe91cdca6c`  
		Last Modified: Tue, 19 May 2026 18:50:32 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:252522a027743939f7b115d2d3929238ba7a8fee776336371433d62e17da49f3`  
		Last Modified: Tue, 19 May 2026 18:50:33 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b1fd0762adb2df9e41385aaea4f5aeb069ccb43ec6a5203c0970dbb32f5d39`  
		Last Modified: Tue, 19 May 2026 18:50:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2404388a95cbd53c2924a8956a2b0bd9fed1ed42798ef0d7958645ec50b36503`  
		Last Modified: Tue, 19 May 2026 19:11:21 GMT  
		Size: 6.6 MB (6577150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abebc77c5a81c02e559a6177ab009ea93d155d230027ecb011d71caf8e1319cb`  
		Last Modified: Tue, 19 May 2026 19:11:20 GMT  
		Size: 87.8 KB (87825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:505cb9808a455382b226432bd33efca0786f2b2817e3828966e8ae1880b9a387`  
		Last Modified: Tue, 19 May 2026 19:11:20 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb736cbd14a0b4279f19088aba50827f55f5bd8c64dd5868c81329ee396e19f`  
		Last Modified: Tue, 19 May 2026 19:11:23 GMT  
		Size: 63.8 MB (63781847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b8e0456f81c21846bbc1e4af0c8ce599dde97bbda1d981de3f47999ce045a4`  
		Last Modified: Tue, 19 May 2026 19:11:22 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10bd67dffac6bb7c60a61f90d9e059f51d217061b38efadfa05cfbccc501c4eb`  
		Last Modified: Tue, 19 May 2026 19:11:22 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:38aff3f9f68bc80866a840b6895120e3efd20f227f69ca66663fee2a5c143d5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e771280fb8341ddf485470385301e8a4df555c4889817952e2e3f1bc2d60f3f`

```dockerfile
```

-	Layers:
	-	`sha256:0f43b1170bad091b1f8a038b4c799e044dcbe62f3cf88792df12fd3808abd3db`  
		Last Modified: Tue, 19 May 2026 19:11:20 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:d29f00616a4b5af545c6238d5e5d3f010dabe8cd9373464e7528dcc2ffe932e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.1 MB (131088931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d59db2bca67549c508438fad529bbb4d973798fdf3dac19d4cff714cd0ef24d8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Tue, 19 May 2026 18:52:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 19 May 2026 18:52:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 19 May 2026 18:52:13 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 19 May 2026 18:52:16 GMT
ENV DOCKER_VERSION=29.5.1
# Tue, 19 May 2026 18:52:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 19 May 2026 18:52:16 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Tue, 19 May 2026 18:52:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-amd64'; 			sha256='0144479d5a1cd710be3464ae898628cfa68033e16b225aef52f81930c45ac9b5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v6'; 			sha256='1f34337385921c5da43d63452282726b062aa887fda975f96dd3d6e869648bc6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v7'; 			sha256='3560b5b6fd3485f4d0bd160e7edf56cc1f08f0cb5852c9af28bf3fab9973c7c2'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm64'; 			sha256='565605fe0bb393ed5d11771e5b52fc7ef05c701868861fa85609747c9d74a440'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-ppc64le'; 			sha256='c5ef8012f48a518e1c235ad408d26cd424d7b5fa87eaf78cb2ff4b9048730120'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-riscv64'; 			sha256='80b27d5f3a346591a5045b81217ee5be578ed151ef8cbd883a892c0ec0ac33f1'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-s390x'; 			sha256='04f5bd0d389f682c7e9287a3b3a1777b0848f8e10d58cbf9d4d12c9002bbb378'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 19 May 2026 18:52:17 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Tue, 19 May 2026 18:52:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 19 May 2026 18:52:18 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 19 May 2026 18:52:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 18:52:18 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 19 May 2026 18:52:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 19 May 2026 18:52:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 May 2026 18:52:18 GMT
CMD ["sh"]
# Tue, 19 May 2026 19:11:28 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 19 May 2026 19:11:28 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 19 May 2026 19:11:29 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 19 May 2026 19:11:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 19 May 2026 19:11:31 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 19 May 2026 19:11:31 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 19 May 2026 19:11:31 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 19:11:31 GMT
VOLUME [/var/lib/docker]
# Tue, 19 May 2026 19:11:31 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 19 May 2026 19:11:31 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 19 May 2026 19:11:31 GMT
CMD []
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:439c73b6370f92c891e3dae2ef2ac51ba47633f4382e93fa3a194ab6c9929fcf`  
		Last Modified: Tue, 19 May 2026 18:52:24 GMT  
		Size: 8.4 MB (8368378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:090f26860bbcb42203be1c1ccc78e592537b7d5076712eddc078a4521b65b6ef`  
		Last Modified: Tue, 19 May 2026 18:52:23 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02fa5c43148b510203ce86fd309a24339439966d97d2739e5681dea9fbedd78b`  
		Last Modified: Tue, 19 May 2026 18:52:24 GMT  
		Size: 18.0 MB (18003824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:179aebd9e04e34e062d99c03bced083b59894f9ff9c70a48e5fdde05043d0662`  
		Last Modified: Tue, 19 May 2026 18:52:25 GMT  
		Size: 20.8 MB (20815342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333ebd0d3068df15ad94c847b40ac364dc7140981f38d3a8f08165ef3fe528ac`  
		Last Modified: Tue, 19 May 2026 18:52:25 GMT  
		Size: 10.2 MB (10243275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e7cd72262f0dcb67fc210c582e3d890f8da6bbfea7979a4af0eca2d85493c8`  
		Last Modified: Tue, 19 May 2026 18:52:25 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb8c848507ade63fa035c4247243268bc78609cb843c2c46923fec82cf42e856`  
		Last Modified: Tue, 19 May 2026 18:52:26 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14678f991761f143ab6345db5de4a84ca5f83a1cd44f7d579a88be20ad20871`  
		Last Modified: Tue, 19 May 2026 18:52:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deb061c465c1d4b2683f89277bb8b93644ad86d3b6a034d3848e218ff3a36250`  
		Last Modified: Tue, 19 May 2026 19:11:41 GMT  
		Size: 7.2 MB (7219902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408cc9607ded7836e6377a9012f389a02da93bc2526404ac2125d556fed0607c`  
		Last Modified: Tue, 19 May 2026 19:11:41 GMT  
		Size: 100.9 KB (100930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4813a99698e1ee0cbb52b02f822e9732eb9144586aa3c765fee806857d8cb872`  
		Last Modified: Tue, 19 May 2026 19:11:41 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f364d3985b9e2a29ae89857aa654e13a752db4b807f58b23afc56a7fdddc9ca`  
		Last Modified: Tue, 19 May 2026 19:11:43 GMT  
		Size: 62.1 MB (62129257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34b8039e34935754bb978ab40f852eeb6345408e37deb40c0467f77421c8252`  
		Last Modified: Tue, 19 May 2026 19:11:42 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be12674817c3cc5397950df61ba9f0761de7cbb67e7527d120f671791e1644f9`  
		Last Modified: Tue, 19 May 2026 19:11:42 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:8ac585f5eb9117c0193cbfc718548d3dca67a7e669159a6b08a53ae907925d21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa5bac19b0eae7a6debca0657ab9da39a1528d516c371778235e72d5db216621`

```dockerfile
```

-	Layers:
	-	`sha256:662dc4eaa00e9b2353b08fdbf55f624046c556fe7fa5b07f0332cfd3384d50fb`  
		Last Modified: Tue, 19 May 2026 19:11:40 GMT  
		Size: 34.8 KB (34782 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-dind-rootless`

```console
$ docker pull docker@sha256:fc34343ecba0eed3f4c4f82dacd33287140cf123e7449f2e7a37fefa6b233a72
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:29-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:54fb8c3eb5b740f6e3660ec25470f773073e6376db6a4edda040eb8ba7105e64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157184836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abc3d62166f739fc25b4f819b724c5c207c6d5e3ccaa7127fc1a33ce1ef2b983`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Tue, 19 May 2026 18:43:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 19 May 2026 18:43:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 19 May 2026 18:43:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 19 May 2026 18:43:53 GMT
ENV DOCKER_VERSION=29.5.1
# Tue, 19 May 2026 18:43:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 19 May 2026 18:43:53 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Tue, 19 May 2026 18:43:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-amd64'; 			sha256='0144479d5a1cd710be3464ae898628cfa68033e16b225aef52f81930c45ac9b5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v6'; 			sha256='1f34337385921c5da43d63452282726b062aa887fda975f96dd3d6e869648bc6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v7'; 			sha256='3560b5b6fd3485f4d0bd160e7edf56cc1f08f0cb5852c9af28bf3fab9973c7c2'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm64'; 			sha256='565605fe0bb393ed5d11771e5b52fc7ef05c701868861fa85609747c9d74a440'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-ppc64le'; 			sha256='c5ef8012f48a518e1c235ad408d26cd424d7b5fa87eaf78cb2ff4b9048730120'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-riscv64'; 			sha256='80b27d5f3a346591a5045b81217ee5be578ed151ef8cbd883a892c0ec0ac33f1'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-s390x'; 			sha256='04f5bd0d389f682c7e9287a3b3a1777b0848f8e10d58cbf9d4d12c9002bbb378'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 19 May 2026 18:43:54 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Tue, 19 May 2026 18:43:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 19 May 2026 18:43:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 19 May 2026 18:43:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 18:43:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 19 May 2026 18:43:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 19 May 2026 18:43:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 May 2026 18:43:55 GMT
CMD ["sh"]
# Tue, 19 May 2026 18:52:09 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 19 May 2026 18:52:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 19 May 2026 18:52:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 19 May 2026 18:52:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 19 May 2026 18:52:13 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 19 May 2026 18:52:13 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 19 May 2026 18:52:13 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 18:52:13 GMT
VOLUME [/var/lib/docker]
# Tue, 19 May 2026 18:52:13 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 19 May 2026 18:52:13 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 19 May 2026 18:52:13 GMT
CMD []
# Tue, 19 May 2026 19:10:23 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Tue, 19 May 2026 19:10:23 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 19 May 2026 19:10:23 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 19 May 2026 19:10:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 	; 	rm rootless.tgz; 		rootlesskit --version # buildkit
# Tue, 19 May 2026 19:10:23 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 19 May 2026 19:10:23 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 19 May 2026 19:10:23 GMT
USER rootless
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959d822c11f4cffde22f6a8ca77070ab678788ee8a60e50bf52240fab7600d55`  
		Last Modified: Tue, 19 May 2026 18:44:02 GMT  
		Size: 8.3 MB (8311621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf748eeffe46320957e43a6d041504e02f6d54efaa90b05ea0a5e76259a3bc9`  
		Last Modified: Tue, 19 May 2026 18:44:01 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29db3e4d2cf2bffd95a0b8c095c0dfc7f4b6ee9717169afb9c613ae0714f22a5`  
		Last Modified: Tue, 19 May 2026 18:44:03 GMT  
		Size: 19.5 MB (19549501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:418895c8a0097a67712f5b2385b094ed4ed5af1359b9b43cb86c07da48ca11c9`  
		Last Modified: Tue, 19 May 2026 18:44:03 GMT  
		Size: 23.0 MB (22988580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4382b5de8ae74e74d495d9d94f0127cf051728dc00cab26dfa163bba8cdbcf13`  
		Last Modified: Tue, 19 May 2026 18:44:03 GMT  
		Size: 11.2 MB (11243752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53914aaed626c98320ff52b5bbe81eb804e9a82d445d07a5908e16e86ac5a5c`  
		Last Modified: Tue, 19 May 2026 18:44:03 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cac0928dd7f6aa6c83aa987350f200df21db15618f2ba47912f35be2b16b3b9`  
		Last Modified: Tue, 19 May 2026 18:44:04 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1c069fc81d4d790f039a7a8160f23dffa6c11a22ee385a0db0fe75ae235dfe1`  
		Last Modified: Tue, 19 May 2026 18:44:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27817872a6ae6fcf22af6f3dbdec0f52f7b055d8b3384cd5b922f74d11358249`  
		Last Modified: Tue, 19 May 2026 18:52:23 GMT  
		Size: 6.9 MB (6941424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a7ba7363a81328286ac28be79b6e6248a1e1c4cb3f1749b808bc8abeb5c686`  
		Last Modified: Tue, 19 May 2026 18:52:23 GMT  
		Size: 92.2 KB (92218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f90442d3c5cd85fdf0fd4683516f39486a803bd57eb9813b3dcb939d9d3fcc`  
		Last Modified: Tue, 19 May 2026 18:52:23 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c588cc6d3552d3ec8363fa8dabb97cfe3ea467efd07c37c45853267ab5c544`  
		Last Modified: Tue, 19 May 2026 18:52:25 GMT  
		Size: 68.7 MB (68661447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa91ecdbc2c72221f7c567a768c787e9b0e27629ad60fecaa37b420555dbec4`  
		Last Modified: Tue, 19 May 2026 18:52:24 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a04f224ef5d78ccf3d32a655e7621773237de1ba0a09780d2011e4e3efc9802`  
		Last Modified: Tue, 19 May 2026 18:52:25 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cecc87fe83d1eed7164980cba609d8af5ce21512b7a270c9fff3a717b56885d`  
		Last Modified: Tue, 19 May 2026 19:10:29 GMT  
		Size: 3.4 MB (3420112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f1de764b59139da153ed5c910b6f1016ba4c34bfe850397d4515465af03b14`  
		Last Modified: Tue, 19 May 2026 19:10:28 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810353487b2c22447155b48ee25ce68046853c053cd2683969fef6360cc51933`  
		Last Modified: Tue, 19 May 2026 19:10:29 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51c09f12615ecc2d61dce57d65b327703b94b167fc1f44f161403ac443d684f2`  
		Last Modified: Tue, 19 May 2026 19:10:29 GMT  
		Size: 12.1 MB (12102496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9688d32ac36d4f90efdf6379ecbdf84feb518c202f038c402b312b45fe270a28`  
		Last Modified: Tue, 19 May 2026 19:10:30 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:110a0812130d4441ce1773cd1230225e01f2e770f5ecf5f5641a4baf88df3911
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a854ed3332b83327cbd69c19dfffceb9982c23ed85413639f28ad3c4e8a4cbd`

```dockerfile
```

-	Layers:
	-	`sha256:8786627e00c646555d675e83986675375d51e2130c10d9a3645ebd3a70b82cd2`  
		Last Modified: Tue, 19 May 2026 19:10:28 GMT  
		Size: 30.5 KB (30493 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:f69d2ff1f367dac480263f11eb4bb9237f140d4ebe4349325c75b4fd0d06bd28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.7 MB (145721341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a4e4d8a17819a06713e6ac6acfa7f117cf9cd4e8567cf58372f73eca47616c4`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Tue, 19 May 2026 18:52:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 19 May 2026 18:52:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 19 May 2026 18:52:13 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 19 May 2026 18:52:16 GMT
ENV DOCKER_VERSION=29.5.1
# Tue, 19 May 2026 18:52:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 19 May 2026 18:52:16 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Tue, 19 May 2026 18:52:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-amd64'; 			sha256='0144479d5a1cd710be3464ae898628cfa68033e16b225aef52f81930c45ac9b5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v6'; 			sha256='1f34337385921c5da43d63452282726b062aa887fda975f96dd3d6e869648bc6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v7'; 			sha256='3560b5b6fd3485f4d0bd160e7edf56cc1f08f0cb5852c9af28bf3fab9973c7c2'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm64'; 			sha256='565605fe0bb393ed5d11771e5b52fc7ef05c701868861fa85609747c9d74a440'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-ppc64le'; 			sha256='c5ef8012f48a518e1c235ad408d26cd424d7b5fa87eaf78cb2ff4b9048730120'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-riscv64'; 			sha256='80b27d5f3a346591a5045b81217ee5be578ed151ef8cbd883a892c0ec0ac33f1'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-s390x'; 			sha256='04f5bd0d389f682c7e9287a3b3a1777b0848f8e10d58cbf9d4d12c9002bbb378'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 19 May 2026 18:52:17 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Tue, 19 May 2026 18:52:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 19 May 2026 18:52:18 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 19 May 2026 18:52:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 18:52:18 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 19 May 2026 18:52:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 19 May 2026 18:52:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 May 2026 18:52:18 GMT
CMD ["sh"]
# Tue, 19 May 2026 19:11:28 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 19 May 2026 19:11:28 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 19 May 2026 19:11:29 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 19 May 2026 19:11:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 19 May 2026 19:11:31 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 19 May 2026 19:11:31 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 19 May 2026 19:11:31 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 19:11:31 GMT
VOLUME [/var/lib/docker]
# Tue, 19 May 2026 19:11:31 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 19 May 2026 19:11:31 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 19 May 2026 19:11:31 GMT
CMD []
# Tue, 19 May 2026 20:10:18 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Tue, 19 May 2026 20:10:18 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 19 May 2026 20:10:18 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 19 May 2026 20:10:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 	; 	rm rootless.tgz; 		rootlesskit --version # buildkit
# Tue, 19 May 2026 20:10:18 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 19 May 2026 20:10:18 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 19 May 2026 20:10:18 GMT
USER rootless
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:439c73b6370f92c891e3dae2ef2ac51ba47633f4382e93fa3a194ab6c9929fcf`  
		Last Modified: Tue, 19 May 2026 18:52:24 GMT  
		Size: 8.4 MB (8368378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:090f26860bbcb42203be1c1ccc78e592537b7d5076712eddc078a4521b65b6ef`  
		Last Modified: Tue, 19 May 2026 18:52:23 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02fa5c43148b510203ce86fd309a24339439966d97d2739e5681dea9fbedd78b`  
		Last Modified: Tue, 19 May 2026 18:52:24 GMT  
		Size: 18.0 MB (18003824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:179aebd9e04e34e062d99c03bced083b59894f9ff9c70a48e5fdde05043d0662`  
		Last Modified: Tue, 19 May 2026 18:52:25 GMT  
		Size: 20.8 MB (20815342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333ebd0d3068df15ad94c847b40ac364dc7140981f38d3a8f08165ef3fe528ac`  
		Last Modified: Tue, 19 May 2026 18:52:25 GMT  
		Size: 10.2 MB (10243275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e7cd72262f0dcb67fc210c582e3d890f8da6bbfea7979a4af0eca2d85493c8`  
		Last Modified: Tue, 19 May 2026 18:52:25 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb8c848507ade63fa035c4247243268bc78609cb843c2c46923fec82cf42e856`  
		Last Modified: Tue, 19 May 2026 18:52:26 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14678f991761f143ab6345db5de4a84ca5f83a1cd44f7d579a88be20ad20871`  
		Last Modified: Tue, 19 May 2026 18:52:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deb061c465c1d4b2683f89277bb8b93644ad86d3b6a034d3848e218ff3a36250`  
		Last Modified: Tue, 19 May 2026 19:11:41 GMT  
		Size: 7.2 MB (7219902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408cc9607ded7836e6377a9012f389a02da93bc2526404ac2125d556fed0607c`  
		Last Modified: Tue, 19 May 2026 19:11:41 GMT  
		Size: 100.9 KB (100930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4813a99698e1ee0cbb52b02f822e9732eb9144586aa3c765fee806857d8cb872`  
		Last Modified: Tue, 19 May 2026 19:11:41 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f364d3985b9e2a29ae89857aa654e13a752db4b807f58b23afc56a7fdddc9ca`  
		Last Modified: Tue, 19 May 2026 19:11:43 GMT  
		Size: 62.1 MB (62129257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34b8039e34935754bb978ab40f852eeb6345408e37deb40c0467f77421c8252`  
		Last Modified: Tue, 19 May 2026 19:11:42 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be12674817c3cc5397950df61ba9f0761de7cbb67e7527d120f671791e1644f9`  
		Last Modified: Tue, 19 May 2026 19:11:42 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e2794603590245d075eed606ac34301c58fda88a8a80f4eaa3ffce3d78a905`  
		Last Modified: Tue, 19 May 2026 20:10:24 GMT  
		Size: 3.4 MB (3394549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afc77214cc9ebf151912fa095a575ef37f668cb6338ba1a94904c1edaf262ceb`  
		Last Modified: Tue, 19 May 2026 20:10:24 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ead735ef17a546ca40080e700f3c11ff2c11b5cdc13bafd2c98e028f26c5940`  
		Last Modified: Tue, 19 May 2026 20:10:24 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51aaf502457f6ce01bba562fab571d3a6ae959cb483cd95636a71243072df558`  
		Last Modified: Tue, 19 May 2026 20:10:24 GMT  
		Size: 11.2 MB (11236521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b0ca64e0e966609139e6199a7a8b766c498d0350d644cd8d18ab622a42d3fc9`  
		Last Modified: Tue, 19 May 2026 20:10:25 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:4fe949a9f9e01f26d41d7540737c598ccada6b62562db26845b13a0cf57f124a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 KB (30663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d49dc7a383ab1fdb7ccd92405afa131cc367a1c519e6a245d1ff68df7e85a66`

```dockerfile
```

-	Layers:
	-	`sha256:e83fa8083ea898497b6c983d8641259136e040f0b533861df142a73520bda5fe`  
		Last Modified: Tue, 19 May 2026 20:10:23 GMT  
		Size: 30.7 KB (30663 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-windowsservercore`

```console
$ docker pull docker@sha256:76a2595299d5d831461bbff176d00c8005cc1b58a48fe70127d90155b250253f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32860; amd64
	-	windows version 10.0.20348.5139; amd64

### `docker:29-windowsservercore` - windows version 10.0.26100.32860; amd64

```console
$ docker pull docker@sha256:189f1d53b9d0831a7663f55ac4dfcfe317baa879af86a90a44e1c83e9f9fbf6a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2262683896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c993dcdab4e74415b546e3486a219f555369a5b9db18c96ed98e36915f6572`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 10 May 2026 10:08:54 GMT
RUN Install update 10.0.26100.32860
# Thu, 21 May 2026 23:13:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 21 May 2026 23:15:10 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 21 May 2026 23:15:11 GMT
ENV DOCKER_VERSION=29.5.2
# Thu, 21 May 2026 23:15:13 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.5.2.zip
# Thu, 21 May 2026 23:15:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 21 May 2026 23:15:38 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 21 May 2026 23:15:39 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.windows-amd64.exe
# Thu, 21 May 2026 23:15:39 GMT
ENV DOCKER_BUILDX_SHA256=41e1b3fff6541d5f5febb18ff4c9108bec30afd7bf9133b82783735c2078eac1
# Thu, 21 May 2026 23:15:58 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 21 May 2026 23:15:58 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 21 May 2026 23:15:59 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-windows-x86_64.exe
# Thu, 21 May 2026 23:16:00 GMT
ENV DOCKER_COMPOSE_SHA256=e1a8faff28c7433635201a2222171b727f33ecdb0ed367e54d162d00432f39aa
# Thu, 21 May 2026 23:16:10 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f787ad06f38db673c3d304f21c09a82ff9a1ced32062515ea52fdb0383457b24`  
		Last Modified: Tue, 12 May 2026 18:03:01 GMT  
		Size: 682.9 MB (682882530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c26092efbc05ba0447d81394df46314e3b86ab224685126b2d6dfd994d4dc11`  
		Last Modified: Thu, 21 May 2026 23:16:20 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83ade171b063bb36658cc0d1e2c9c6cb333ea25a3ad1e4129615adf825b64a46`  
		Last Modified: Thu, 21 May 2026 23:16:20 GMT  
		Size: 406.4 KB (406376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78577312456309bc4fe740995c1663317c15ecc17bcedded51adf9a9982366ca`  
		Last Modified: Thu, 21 May 2026 23:16:18 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee76c01ce753f169a4b6e55abafceb2769603948efcc72907de3e6aeb33cce42`  
		Last Modified: Thu, 21 May 2026 23:16:18 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc27681d28a3246dcf30c481b3852d6dbdc170d9cf5b284e019a90ade4d9cee8`  
		Last Modified: Thu, 21 May 2026 23:16:21 GMT  
		Size: 20.3 MB (20271957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c75db7b4635a1d76c37b80319e3dd1bdff20dd7ef77265097ecdb2861b340b99`  
		Last Modified: Thu, 21 May 2026 23:16:17 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48d982239ff1380cf0818ab9cc60083eac7f15cd44054f9f67433be9035d8a31`  
		Last Modified: Thu, 21 May 2026 23:16:17 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c096a591d4ea5f003d7be2a803cf5e81d42655e886b4df3ea31db5ab4f1289f`  
		Last Modified: Thu, 21 May 2026 23:16:17 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f795f325466c0a11f5a6c88330d8ab8b3fcad025e8fc95a56b3cc2d15f7884bb`  
		Last Modified: Thu, 21 May 2026 23:16:32 GMT  
		Size: 23.9 MB (23933638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b824c613a9ba32b1fcec65a639d38947346d62eddad555e9a7e295010f6937d`  
		Last Modified: Thu, 21 May 2026 23:16:15 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62db1e13ba58abbe1229ca941f68bceaa49a84ce729b12c843e3c1914052407d`  
		Last Modified: Thu, 21 May 2026 23:16:15 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7286144ed984b89e44b176cd42f189f5d30dc6bdd1357032bbb549bb0c96975`  
		Last Modified: Thu, 21 May 2026 23:16:15 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8922b65b3736da43bcb9ea86b5abf5ea19ee56a9c642200696decef2214beb0`  
		Last Modified: Thu, 21 May 2026 23:16:17 GMT  
		Size: 12.1 MB (12118551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:29-windowsservercore` - windows version 10.0.20348.5139; amd64

```console
$ docker pull docker@sha256:fecc0a5137c67dad8b14e94db06043867e6b74bb784840642f699cfd8d9abe16
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2179150500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52496b21f2e24bac1a6601b61b2de6417374b43f89a6f9cfd8eefedf65fdd4a7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Thu, 21 May 2026 23:37:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 21 May 2026 23:38:14 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 21 May 2026 23:38:15 GMT
ENV DOCKER_VERSION=29.5.2
# Thu, 21 May 2026 23:38:17 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.5.2.zip
# Thu, 21 May 2026 23:38:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 21 May 2026 23:38:44 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 21 May 2026 23:38:45 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.windows-amd64.exe
# Thu, 21 May 2026 23:38:46 GMT
ENV DOCKER_BUILDX_SHA256=41e1b3fff6541d5f5febb18ff4c9108bec30afd7bf9133b82783735c2078eac1
# Thu, 21 May 2026 23:39:10 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 21 May 2026 23:39:11 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 21 May 2026 23:39:12 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-windows-x86_64.exe
# Thu, 21 May 2026 23:39:13 GMT
ENV DOCKER_COMPOSE_SHA256=e1a8faff28c7433635201a2222171b727f33ecdb0ed367e54d162d00432f39aa
# Thu, 21 May 2026 23:39:31 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857865ad3eca4da109d969134a9cab7225d9de49597914ae325d43661900f513`  
		Last Modified: Tue, 12 May 2026 17:34:16 GMT  
		Size: 633.4 MB (633401492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17fd8e1d39e88259a0e6383034d2a7ad6d90356547cec5bbbf94f3a3e0afc763`  
		Last Modified: Thu, 21 May 2026 23:39:40 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1756702264897e3d6bb006dbce5e5260ae7bc8fa54384b6a031c460ac01476e`  
		Last Modified: Thu, 21 May 2026 23:39:39 GMT  
		Size: 505.7 KB (505666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da4ab93ed88956a88f0eb095aaf8977d5b9bbba18d08b7757eb1ccff28e80d2a`  
		Last Modified: Thu, 21 May 2026 23:39:39 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c2528cc62d1c88f5003aa2f0b62055544c66be0ec0d65cf6a8550455e0747`  
		Last Modified: Thu, 21 May 2026 23:39:38 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e531632899bf060a3ff8e9b29f0c3c81b857c0b311b97f241e35d94ffe66d3cb`  
		Last Modified: Thu, 21 May 2026 23:39:41 GMT  
		Size: 20.2 MB (20231436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34d5b3db47edaa5e44e34cad2ba31b4be5c5b6c483cef5a09b33460c4747302`  
		Last Modified: Thu, 21 May 2026 23:39:37 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:751d900578d8658aa1097acdfcd5f97aff829261a5e29a8f16b2f40effa4f532`  
		Last Modified: Thu, 21 May 2026 23:39:37 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eeb843d181536cfa4d4d838d626f63e191094c2468d26f3d0330a50f2b526c4`  
		Last Modified: Thu, 21 May 2026 23:39:37 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b58742ef314900bc96dda8fc677f8a1b98faf7970eb6fa39992b3a0150a7d36`  
		Last Modified: Thu, 21 May 2026 23:39:51 GMT  
		Size: 23.9 MB (23901391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:435a34db22345529d906d3448943e90cfc37ae51e15ea8ec70cd87e01c5b16d8`  
		Last Modified: Thu, 21 May 2026 23:39:35 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1f19e0160f0c9a3c97ced5e763b905a949f0f5af2882f68638e276a43a62af`  
		Last Modified: Thu, 21 May 2026 23:39:35 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60db139392fbadfa06ac3c12862fab33f209dc6d2a7f076d7d0b52eec402dc3b`  
		Last Modified: Thu, 21 May 2026 23:39:35 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ddde0e1dba54298e42dcefa7d09742c8714bba4bc7d5a59eb1950f87975208`  
		Last Modified: Thu, 21 May 2026 23:39:37 GMT  
		Size: 12.1 MB (12079670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:45ff7aebeb53a14d066b607ae70acc6e3ca4f3cc6835a76438078df370c9857f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `docker:29-windowsservercore-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull docker@sha256:fecc0a5137c67dad8b14e94db06043867e6b74bb784840642f699cfd8d9abe16
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2179150500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52496b21f2e24bac1a6601b61b2de6417374b43f89a6f9cfd8eefedf65fdd4a7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Thu, 21 May 2026 23:37:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 21 May 2026 23:38:14 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 21 May 2026 23:38:15 GMT
ENV DOCKER_VERSION=29.5.2
# Thu, 21 May 2026 23:38:17 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.5.2.zip
# Thu, 21 May 2026 23:38:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 21 May 2026 23:38:44 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 21 May 2026 23:38:45 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.windows-amd64.exe
# Thu, 21 May 2026 23:38:46 GMT
ENV DOCKER_BUILDX_SHA256=41e1b3fff6541d5f5febb18ff4c9108bec30afd7bf9133b82783735c2078eac1
# Thu, 21 May 2026 23:39:10 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 21 May 2026 23:39:11 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 21 May 2026 23:39:12 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-windows-x86_64.exe
# Thu, 21 May 2026 23:39:13 GMT
ENV DOCKER_COMPOSE_SHA256=e1a8faff28c7433635201a2222171b727f33ecdb0ed367e54d162d00432f39aa
# Thu, 21 May 2026 23:39:31 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857865ad3eca4da109d969134a9cab7225d9de49597914ae325d43661900f513`  
		Last Modified: Tue, 12 May 2026 17:34:16 GMT  
		Size: 633.4 MB (633401492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17fd8e1d39e88259a0e6383034d2a7ad6d90356547cec5bbbf94f3a3e0afc763`  
		Last Modified: Thu, 21 May 2026 23:39:40 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1756702264897e3d6bb006dbce5e5260ae7bc8fa54384b6a031c460ac01476e`  
		Last Modified: Thu, 21 May 2026 23:39:39 GMT  
		Size: 505.7 KB (505666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da4ab93ed88956a88f0eb095aaf8977d5b9bbba18d08b7757eb1ccff28e80d2a`  
		Last Modified: Thu, 21 May 2026 23:39:39 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c2528cc62d1c88f5003aa2f0b62055544c66be0ec0d65cf6a8550455e0747`  
		Last Modified: Thu, 21 May 2026 23:39:38 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e531632899bf060a3ff8e9b29f0c3c81b857c0b311b97f241e35d94ffe66d3cb`  
		Last Modified: Thu, 21 May 2026 23:39:41 GMT  
		Size: 20.2 MB (20231436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34d5b3db47edaa5e44e34cad2ba31b4be5c5b6c483cef5a09b33460c4747302`  
		Last Modified: Thu, 21 May 2026 23:39:37 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:751d900578d8658aa1097acdfcd5f97aff829261a5e29a8f16b2f40effa4f532`  
		Last Modified: Thu, 21 May 2026 23:39:37 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eeb843d181536cfa4d4d838d626f63e191094c2468d26f3d0330a50f2b526c4`  
		Last Modified: Thu, 21 May 2026 23:39:37 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b58742ef314900bc96dda8fc677f8a1b98faf7970eb6fa39992b3a0150a7d36`  
		Last Modified: Thu, 21 May 2026 23:39:51 GMT  
		Size: 23.9 MB (23901391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:435a34db22345529d906d3448943e90cfc37ae51e15ea8ec70cd87e01c5b16d8`  
		Last Modified: Thu, 21 May 2026 23:39:35 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1f19e0160f0c9a3c97ced5e763b905a949f0f5af2882f68638e276a43a62af`  
		Last Modified: Thu, 21 May 2026 23:39:35 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60db139392fbadfa06ac3c12862fab33f209dc6d2a7f076d7d0b52eec402dc3b`  
		Last Modified: Thu, 21 May 2026 23:39:35 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ddde0e1dba54298e42dcefa7d09742c8714bba4bc7d5a59eb1950f87975208`  
		Last Modified: Thu, 21 May 2026 23:39:37 GMT  
		Size: 12.1 MB (12079670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:38a6d8d2632ca78eb3229980b6b255413aa7fafcf1d3ad906265d8c05df98652
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32860; amd64

### `docker:29-windowsservercore-ltsc2025` - windows version 10.0.26100.32860; amd64

```console
$ docker pull docker@sha256:189f1d53b9d0831a7663f55ac4dfcfe317baa879af86a90a44e1c83e9f9fbf6a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2262683896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c993dcdab4e74415b546e3486a219f555369a5b9db18c96ed98e36915f6572`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 10 May 2026 10:08:54 GMT
RUN Install update 10.0.26100.32860
# Thu, 21 May 2026 23:13:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 21 May 2026 23:15:10 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 21 May 2026 23:15:11 GMT
ENV DOCKER_VERSION=29.5.2
# Thu, 21 May 2026 23:15:13 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.5.2.zip
# Thu, 21 May 2026 23:15:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 21 May 2026 23:15:38 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 21 May 2026 23:15:39 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.windows-amd64.exe
# Thu, 21 May 2026 23:15:39 GMT
ENV DOCKER_BUILDX_SHA256=41e1b3fff6541d5f5febb18ff4c9108bec30afd7bf9133b82783735c2078eac1
# Thu, 21 May 2026 23:15:58 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 21 May 2026 23:15:58 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 21 May 2026 23:15:59 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-windows-x86_64.exe
# Thu, 21 May 2026 23:16:00 GMT
ENV DOCKER_COMPOSE_SHA256=e1a8faff28c7433635201a2222171b727f33ecdb0ed367e54d162d00432f39aa
# Thu, 21 May 2026 23:16:10 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f787ad06f38db673c3d304f21c09a82ff9a1ced32062515ea52fdb0383457b24`  
		Last Modified: Tue, 12 May 2026 18:03:01 GMT  
		Size: 682.9 MB (682882530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c26092efbc05ba0447d81394df46314e3b86ab224685126b2d6dfd994d4dc11`  
		Last Modified: Thu, 21 May 2026 23:16:20 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83ade171b063bb36658cc0d1e2c9c6cb333ea25a3ad1e4129615adf825b64a46`  
		Last Modified: Thu, 21 May 2026 23:16:20 GMT  
		Size: 406.4 KB (406376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78577312456309bc4fe740995c1663317c15ecc17bcedded51adf9a9982366ca`  
		Last Modified: Thu, 21 May 2026 23:16:18 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee76c01ce753f169a4b6e55abafceb2769603948efcc72907de3e6aeb33cce42`  
		Last Modified: Thu, 21 May 2026 23:16:18 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc27681d28a3246dcf30c481b3852d6dbdc170d9cf5b284e019a90ade4d9cee8`  
		Last Modified: Thu, 21 May 2026 23:16:21 GMT  
		Size: 20.3 MB (20271957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c75db7b4635a1d76c37b80319e3dd1bdff20dd7ef77265097ecdb2861b340b99`  
		Last Modified: Thu, 21 May 2026 23:16:17 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48d982239ff1380cf0818ab9cc60083eac7f15cd44054f9f67433be9035d8a31`  
		Last Modified: Thu, 21 May 2026 23:16:17 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c096a591d4ea5f003d7be2a803cf5e81d42655e886b4df3ea31db5ab4f1289f`  
		Last Modified: Thu, 21 May 2026 23:16:17 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f795f325466c0a11f5a6c88330d8ab8b3fcad025e8fc95a56b3cc2d15f7884bb`  
		Last Modified: Thu, 21 May 2026 23:16:32 GMT  
		Size: 23.9 MB (23933638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b824c613a9ba32b1fcec65a639d38947346d62eddad555e9a7e295010f6937d`  
		Last Modified: Thu, 21 May 2026 23:16:15 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62db1e13ba58abbe1229ca941f68bceaa49a84ce729b12c843e3c1914052407d`  
		Last Modified: Thu, 21 May 2026 23:16:15 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7286144ed984b89e44b176cd42f189f5d30dc6bdd1357032bbb549bb0c96975`  
		Last Modified: Thu, 21 May 2026 23:16:15 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8922b65b3736da43bcb9ea86b5abf5ea19ee56a9c642200696decef2214beb0`  
		Last Modified: Thu, 21 May 2026 23:16:17 GMT  
		Size: 12.1 MB (12118551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.5`

```console
$ docker pull docker@sha256:eed377f3ce14afda560e742c5b3ae446df1ce00a16e1beab2ac6c78c1477fe85
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

### `docker:29.5` - linux; amd64

```console
$ docker pull docker@sha256:6f156e0882b6f307bcd00e01b7abebdccf6eb96b1bb40e8b160e3e401ba3749b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.7 MB (141660887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a475a10539689996453c7c7aa57795a1c35cb8da621faddaef1fb0f05cdb7723`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Tue, 19 May 2026 18:43:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 19 May 2026 18:43:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 19 May 2026 18:43:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 19 May 2026 18:43:53 GMT
ENV DOCKER_VERSION=29.5.1
# Tue, 19 May 2026 18:43:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 19 May 2026 18:43:53 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Tue, 19 May 2026 18:43:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-amd64'; 			sha256='0144479d5a1cd710be3464ae898628cfa68033e16b225aef52f81930c45ac9b5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v6'; 			sha256='1f34337385921c5da43d63452282726b062aa887fda975f96dd3d6e869648bc6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v7'; 			sha256='3560b5b6fd3485f4d0bd160e7edf56cc1f08f0cb5852c9af28bf3fab9973c7c2'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm64'; 			sha256='565605fe0bb393ed5d11771e5b52fc7ef05c701868861fa85609747c9d74a440'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-ppc64le'; 			sha256='c5ef8012f48a518e1c235ad408d26cd424d7b5fa87eaf78cb2ff4b9048730120'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-riscv64'; 			sha256='80b27d5f3a346591a5045b81217ee5be578ed151ef8cbd883a892c0ec0ac33f1'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-s390x'; 			sha256='04f5bd0d389f682c7e9287a3b3a1777b0848f8e10d58cbf9d4d12c9002bbb378'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 19 May 2026 18:43:54 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Tue, 19 May 2026 18:43:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 19 May 2026 18:43:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 19 May 2026 18:43:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 18:43:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 19 May 2026 18:43:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 19 May 2026 18:43:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 May 2026 18:43:55 GMT
CMD ["sh"]
# Tue, 19 May 2026 18:52:09 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 19 May 2026 18:52:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 19 May 2026 18:52:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 19 May 2026 18:52:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 19 May 2026 18:52:13 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 19 May 2026 18:52:13 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 19 May 2026 18:52:13 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 18:52:13 GMT
VOLUME [/var/lib/docker]
# Tue, 19 May 2026 18:52:13 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 19 May 2026 18:52:13 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 19 May 2026 18:52:13 GMT
CMD []
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959d822c11f4cffde22f6a8ca77070ab678788ee8a60e50bf52240fab7600d55`  
		Last Modified: Tue, 19 May 2026 18:44:02 GMT  
		Size: 8.3 MB (8311621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf748eeffe46320957e43a6d041504e02f6d54efaa90b05ea0a5e76259a3bc9`  
		Last Modified: Tue, 19 May 2026 18:44:01 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29db3e4d2cf2bffd95a0b8c095c0dfc7f4b6ee9717169afb9c613ae0714f22a5`  
		Last Modified: Tue, 19 May 2026 18:44:03 GMT  
		Size: 19.5 MB (19549501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:418895c8a0097a67712f5b2385b094ed4ed5af1359b9b43cb86c07da48ca11c9`  
		Last Modified: Tue, 19 May 2026 18:44:03 GMT  
		Size: 23.0 MB (22988580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4382b5de8ae74e74d495d9d94f0127cf051728dc00cab26dfa163bba8cdbcf13`  
		Last Modified: Tue, 19 May 2026 18:44:03 GMT  
		Size: 11.2 MB (11243752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53914aaed626c98320ff52b5bbe81eb804e9a82d445d07a5908e16e86ac5a5c`  
		Last Modified: Tue, 19 May 2026 18:44:03 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cac0928dd7f6aa6c83aa987350f200df21db15618f2ba47912f35be2b16b3b9`  
		Last Modified: Tue, 19 May 2026 18:44:04 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1c069fc81d4d790f039a7a8160f23dffa6c11a22ee385a0db0fe75ae235dfe1`  
		Last Modified: Tue, 19 May 2026 18:44:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27817872a6ae6fcf22af6f3dbdec0f52f7b055d8b3384cd5b922f74d11358249`  
		Last Modified: Tue, 19 May 2026 18:52:23 GMT  
		Size: 6.9 MB (6941424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a7ba7363a81328286ac28be79b6e6248a1e1c4cb3f1749b808bc8abeb5c686`  
		Last Modified: Tue, 19 May 2026 18:52:23 GMT  
		Size: 92.2 KB (92218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f90442d3c5cd85fdf0fd4683516f39486a803bd57eb9813b3dcb939d9d3fcc`  
		Last Modified: Tue, 19 May 2026 18:52:23 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c588cc6d3552d3ec8363fa8dabb97cfe3ea467efd07c37c45853267ab5c544`  
		Last Modified: Tue, 19 May 2026 18:52:25 GMT  
		Size: 68.7 MB (68661447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa91ecdbc2c72221f7c567a768c787e9b0e27629ad60fecaa37b420555dbec4`  
		Last Modified: Tue, 19 May 2026 18:52:24 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a04f224ef5d78ccf3d32a655e7621773237de1ba0a09780d2011e4e3efc9802`  
		Last Modified: Tue, 19 May 2026 18:52:25 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.5` - unknown; unknown

```console
$ docker pull docker@sha256:8459bca25b1862c9c244d8290b9c289f8f38a28e911360560cef489552fd9996
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca9c00d43298e9a165fe521202b47e762e0e30cdaad754b907fb2241affba41a`

```dockerfile
```

-	Layers:
	-	`sha256:725c95ff8cee96878c88b2d98ed922fc03f42a86c848e44ace4d3602cca233bd`  
		Last Modified: Tue, 19 May 2026 18:52:23 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.5` - linux; arm variant v6

```console
$ docker pull docker@sha256:656cd6a2deb516bf1bab86d4eb9e0ea9b2afca3fb8c81a402195068521496791
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.6 MB (133554774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b375b41ebcd63fd76689fd0c53d0cbebdb1c6086df5568f03b1342739485d2f4`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Tue, 19 May 2026 18:46:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 19 May 2026 18:46:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 19 May 2026 18:46:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 19 May 2026 18:46:29 GMT
ENV DOCKER_VERSION=29.5.1
# Tue, 19 May 2026 18:46:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 19 May 2026 18:46:29 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Tue, 19 May 2026 18:46:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-amd64'; 			sha256='0144479d5a1cd710be3464ae898628cfa68033e16b225aef52f81930c45ac9b5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v6'; 			sha256='1f34337385921c5da43d63452282726b062aa887fda975f96dd3d6e869648bc6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v7'; 			sha256='3560b5b6fd3485f4d0bd160e7edf56cc1f08f0cb5852c9af28bf3fab9973c7c2'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm64'; 			sha256='565605fe0bb393ed5d11771e5b52fc7ef05c701868861fa85609747c9d74a440'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-ppc64le'; 			sha256='c5ef8012f48a518e1c235ad408d26cd424d7b5fa87eaf78cb2ff4b9048730120'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-riscv64'; 			sha256='80b27d5f3a346591a5045b81217ee5be578ed151ef8cbd883a892c0ec0ac33f1'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-s390x'; 			sha256='04f5bd0d389f682c7e9287a3b3a1777b0848f8e10d58cbf9d4d12c9002bbb378'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 19 May 2026 18:46:32 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Tue, 19 May 2026 18:46:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 19 May 2026 18:46:33 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 19 May 2026 18:46:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 18:46:33 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 19 May 2026 18:46:34 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 19 May 2026 18:46:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 May 2026 18:46:34 GMT
CMD ["sh"]
# Tue, 19 May 2026 18:48:00 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 19 May 2026 18:48:00 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 19 May 2026 18:48:00 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 19 May 2026 18:48:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 19 May 2026 18:48:04 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 19 May 2026 18:48:04 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 19 May 2026 18:48:04 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 18:48:04 GMT
VOLUME [/var/lib/docker]
# Tue, 19 May 2026 18:48:04 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 19 May 2026 18:48:04 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 19 May 2026 18:48:04 GMT
CMD []
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e510993d358b2182e33432b09c723cb2de90442627624e753d33ff6f58e37cf`  
		Last Modified: Tue, 19 May 2026 18:46:40 GMT  
		Size: 8.2 MB (8211856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac6422e386e61fe4ba4eb1abca9f67aef1bba270f947f3797505168eddc865ef`  
		Last Modified: Tue, 19 May 2026 18:46:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c6104ecd7c2122cba9eadf591b901752e839d28c94e9786023634ab16c4e86`  
		Last Modified: Tue, 19 May 2026 18:46:41 GMT  
		Size: 18.2 MB (18183185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9278a90d0e78f94da7f59f70fe4811830047483868d42c4e25a85b91a3359765`  
		Last Modified: Tue, 19 May 2026 18:46:41 GMT  
		Size: 21.6 MB (21614147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09f94e1195a7d62fc4046fa609e325b2001195cf49352924129c45728445d565`  
		Last Modified: Tue, 19 May 2026 18:46:41 GMT  
		Size: 10.7 MB (10650824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a8126c2985de246f1344d8c4340e5934b14cdf06f269351c0bfeac534be4c3a`  
		Last Modified: Tue, 19 May 2026 18:46:41 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f13c028f2e167a9ccd442fe69b89b5f1ca9e19f4589d7160d5af4d3b451ba862`  
		Last Modified: Tue, 19 May 2026 18:46:42 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa9769c6262cc549e78864817d114f4780b6b611ff08c097bcb018ab9040fd0`  
		Last Modified: Tue, 19 May 2026 18:46:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:125e5e8c972742a3fdece68d1d7efe160fc572758035dc6dd440150a5dff5bf7`  
		Last Modified: Tue, 19 May 2026 18:48:15 GMT  
		Size: 7.3 MB (7278661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:092dd15fda2f6f91745deb58f699d28c2ae054d7fb4d6c4100b53f0f8e3a6d85`  
		Last Modified: Tue, 19 May 2026 18:48:15 GMT  
		Size: 91.5 KB (91516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc718ec10edd9882bc794dfec135ed20f43243a8db5ad70f2ca75ac4b4191815`  
		Last Modified: Tue, 19 May 2026 18:48:15 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf390f2615c4c05543ef083213b7da580fc3a675929438042a5228503644f65`  
		Last Modified: Tue, 19 May 2026 18:48:17 GMT  
		Size: 63.9 MB (63944568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0111492ca1c0d70617ea1ed481e8ae4908695479c10dc5b86fe761dd03edc6b`  
		Last Modified: Tue, 19 May 2026 18:48:16 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b88ff88aa94e286fad9d8f3480fb92ba8ec324a9d55d74cce8cce2e99c36353`  
		Last Modified: Tue, 19 May 2026 18:48:16 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.5` - unknown; unknown

```console
$ docker pull docker@sha256:1fd6b9654a40244c2a32a42dfdbd4b0c2fcd97aaacc719b9c466fed8008b0c05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e4f0d6a13a6e324e492f0fd9ae8856d26b30b034d24e9b3868069907c61ec10`

```dockerfile
```

-	Layers:
	-	`sha256:096e9d4d3b5e87687de3559cc60228911d8179792add0ad0a60e1afd76f2b032`  
		Last Modified: Tue, 19 May 2026 18:48:14 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.5` - linux; arm variant v7

```console
$ docker pull docker@sha256:ce68e53519cdc94c6b28b82b2e4af1856aa5dd8e577fb872900952a6ed88f9d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.7 MB (131668449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bc263b60a94589a9d3f238ee64951d8f806cc46c8caed0452715d45111a5b91`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Tue, 19 May 2026 18:50:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 19 May 2026 18:50:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 19 May 2026 18:50:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 19 May 2026 18:50:21 GMT
ENV DOCKER_VERSION=29.5.1
# Tue, 19 May 2026 18:50:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 19 May 2026 18:50:21 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Tue, 19 May 2026 18:50:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-amd64'; 			sha256='0144479d5a1cd710be3464ae898628cfa68033e16b225aef52f81930c45ac9b5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v6'; 			sha256='1f34337385921c5da43d63452282726b062aa887fda975f96dd3d6e869648bc6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v7'; 			sha256='3560b5b6fd3485f4d0bd160e7edf56cc1f08f0cb5852c9af28bf3fab9973c7c2'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm64'; 			sha256='565605fe0bb393ed5d11771e5b52fc7ef05c701868861fa85609747c9d74a440'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-ppc64le'; 			sha256='c5ef8012f48a518e1c235ad408d26cd424d7b5fa87eaf78cb2ff4b9048730120'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-riscv64'; 			sha256='80b27d5f3a346591a5045b81217ee5be578ed151ef8cbd883a892c0ec0ac33f1'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-s390x'; 			sha256='04f5bd0d389f682c7e9287a3b3a1777b0848f8e10d58cbf9d4d12c9002bbb378'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 19 May 2026 18:50:23 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Tue, 19 May 2026 18:50:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 19 May 2026 18:50:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 19 May 2026 18:50:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 18:50:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 19 May 2026 18:50:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 19 May 2026 18:50:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 May 2026 18:50:24 GMT
CMD ["sh"]
# Tue, 19 May 2026 19:11:05 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 19 May 2026 19:11:05 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 19 May 2026 19:11:05 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 19 May 2026 19:11:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 19 May 2026 19:11:10 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 19 May 2026 19:11:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 19 May 2026 19:11:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 19:11:10 GMT
VOLUME [/var/lib/docker]
# Tue, 19 May 2026 19:11:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 19 May 2026 19:11:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 19 May 2026 19:11:10 GMT
CMD []
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e78396f075a6021fa389cbab78d2b7a97c1fa6ccd90c5a3f9aad13a82d9a82d5`  
		Last Modified: Tue, 19 May 2026 18:50:31 GMT  
		Size: 7.5 MB (7520541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55503681071acc50ecd4d54f1a76c32b34fb2e24b116717b8a11a5ed2c4b834b`  
		Last Modified: Tue, 19 May 2026 18:50:30 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:139bfdfb0c5a911c258bd9ca3f33e5d74dc4cdac244e701ffc230dfb2dbcf299`  
		Last Modified: Tue, 19 May 2026 18:50:31 GMT  
		Size: 18.2 MB (18172268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e28d126c0c15c1ddece42e48d16b7989f46d4ba83543ade587e34aae442b162d`  
		Last Modified: Tue, 19 May 2026 18:50:31 GMT  
		Size: 21.6 MB (21600397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb484c140400a96468ac162a856058550dff5319ecf84cb2d15485ffa462cfe5`  
		Last Modified: Tue, 19 May 2026 18:50:31 GMT  
		Size: 10.6 MB (10637143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:458ff3d79525d794f095fe12c99f3a95a84e674163d4ac75823a6bbe91cdca6c`  
		Last Modified: Tue, 19 May 2026 18:50:32 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:252522a027743939f7b115d2d3929238ba7a8fee776336371433d62e17da49f3`  
		Last Modified: Tue, 19 May 2026 18:50:33 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b1fd0762adb2df9e41385aaea4f5aeb069ccb43ec6a5203c0970dbb32f5d39`  
		Last Modified: Tue, 19 May 2026 18:50:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2404388a95cbd53c2924a8956a2b0bd9fed1ed42798ef0d7958645ec50b36503`  
		Last Modified: Tue, 19 May 2026 19:11:21 GMT  
		Size: 6.6 MB (6577150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abebc77c5a81c02e559a6177ab009ea93d155d230027ecb011d71caf8e1319cb`  
		Last Modified: Tue, 19 May 2026 19:11:20 GMT  
		Size: 87.8 KB (87825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:505cb9808a455382b226432bd33efca0786f2b2817e3828966e8ae1880b9a387`  
		Last Modified: Tue, 19 May 2026 19:11:20 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb736cbd14a0b4279f19088aba50827f55f5bd8c64dd5868c81329ee396e19f`  
		Last Modified: Tue, 19 May 2026 19:11:23 GMT  
		Size: 63.8 MB (63781847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b8e0456f81c21846bbc1e4af0c8ce599dde97bbda1d981de3f47999ce045a4`  
		Last Modified: Tue, 19 May 2026 19:11:22 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10bd67dffac6bb7c60a61f90d9e059f51d217061b38efadfa05cfbccc501c4eb`  
		Last Modified: Tue, 19 May 2026 19:11:22 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.5` - unknown; unknown

```console
$ docker pull docker@sha256:38aff3f9f68bc80866a840b6895120e3efd20f227f69ca66663fee2a5c143d5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e771280fb8341ddf485470385301e8a4df555c4889817952e2e3f1bc2d60f3f`

```dockerfile
```

-	Layers:
	-	`sha256:0f43b1170bad091b1f8a038b4c799e044dcbe62f3cf88792df12fd3808abd3db`  
		Last Modified: Tue, 19 May 2026 19:11:20 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.5` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:d29f00616a4b5af545c6238d5e5d3f010dabe8cd9373464e7528dcc2ffe932e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.1 MB (131088931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d59db2bca67549c508438fad529bbb4d973798fdf3dac19d4cff714cd0ef24d8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Tue, 19 May 2026 18:52:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 19 May 2026 18:52:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 19 May 2026 18:52:13 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 19 May 2026 18:52:16 GMT
ENV DOCKER_VERSION=29.5.1
# Tue, 19 May 2026 18:52:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 19 May 2026 18:52:16 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Tue, 19 May 2026 18:52:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-amd64'; 			sha256='0144479d5a1cd710be3464ae898628cfa68033e16b225aef52f81930c45ac9b5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v6'; 			sha256='1f34337385921c5da43d63452282726b062aa887fda975f96dd3d6e869648bc6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v7'; 			sha256='3560b5b6fd3485f4d0bd160e7edf56cc1f08f0cb5852c9af28bf3fab9973c7c2'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm64'; 			sha256='565605fe0bb393ed5d11771e5b52fc7ef05c701868861fa85609747c9d74a440'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-ppc64le'; 			sha256='c5ef8012f48a518e1c235ad408d26cd424d7b5fa87eaf78cb2ff4b9048730120'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-riscv64'; 			sha256='80b27d5f3a346591a5045b81217ee5be578ed151ef8cbd883a892c0ec0ac33f1'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-s390x'; 			sha256='04f5bd0d389f682c7e9287a3b3a1777b0848f8e10d58cbf9d4d12c9002bbb378'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 19 May 2026 18:52:17 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Tue, 19 May 2026 18:52:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 19 May 2026 18:52:18 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 19 May 2026 18:52:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 18:52:18 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 19 May 2026 18:52:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 19 May 2026 18:52:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 May 2026 18:52:18 GMT
CMD ["sh"]
# Tue, 19 May 2026 19:11:28 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 19 May 2026 19:11:28 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 19 May 2026 19:11:29 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 19 May 2026 19:11:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 19 May 2026 19:11:31 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 19 May 2026 19:11:31 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 19 May 2026 19:11:31 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 19:11:31 GMT
VOLUME [/var/lib/docker]
# Tue, 19 May 2026 19:11:31 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 19 May 2026 19:11:31 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 19 May 2026 19:11:31 GMT
CMD []
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:439c73b6370f92c891e3dae2ef2ac51ba47633f4382e93fa3a194ab6c9929fcf`  
		Last Modified: Tue, 19 May 2026 18:52:24 GMT  
		Size: 8.4 MB (8368378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:090f26860bbcb42203be1c1ccc78e592537b7d5076712eddc078a4521b65b6ef`  
		Last Modified: Tue, 19 May 2026 18:52:23 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02fa5c43148b510203ce86fd309a24339439966d97d2739e5681dea9fbedd78b`  
		Last Modified: Tue, 19 May 2026 18:52:24 GMT  
		Size: 18.0 MB (18003824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:179aebd9e04e34e062d99c03bced083b59894f9ff9c70a48e5fdde05043d0662`  
		Last Modified: Tue, 19 May 2026 18:52:25 GMT  
		Size: 20.8 MB (20815342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333ebd0d3068df15ad94c847b40ac364dc7140981f38d3a8f08165ef3fe528ac`  
		Last Modified: Tue, 19 May 2026 18:52:25 GMT  
		Size: 10.2 MB (10243275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e7cd72262f0dcb67fc210c582e3d890f8da6bbfea7979a4af0eca2d85493c8`  
		Last Modified: Tue, 19 May 2026 18:52:25 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb8c848507ade63fa035c4247243268bc78609cb843c2c46923fec82cf42e856`  
		Last Modified: Tue, 19 May 2026 18:52:26 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14678f991761f143ab6345db5de4a84ca5f83a1cd44f7d579a88be20ad20871`  
		Last Modified: Tue, 19 May 2026 18:52:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deb061c465c1d4b2683f89277bb8b93644ad86d3b6a034d3848e218ff3a36250`  
		Last Modified: Tue, 19 May 2026 19:11:41 GMT  
		Size: 7.2 MB (7219902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408cc9607ded7836e6377a9012f389a02da93bc2526404ac2125d556fed0607c`  
		Last Modified: Tue, 19 May 2026 19:11:41 GMT  
		Size: 100.9 KB (100930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4813a99698e1ee0cbb52b02f822e9732eb9144586aa3c765fee806857d8cb872`  
		Last Modified: Tue, 19 May 2026 19:11:41 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f364d3985b9e2a29ae89857aa654e13a752db4b807f58b23afc56a7fdddc9ca`  
		Last Modified: Tue, 19 May 2026 19:11:43 GMT  
		Size: 62.1 MB (62129257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34b8039e34935754bb978ab40f852eeb6345408e37deb40c0467f77421c8252`  
		Last Modified: Tue, 19 May 2026 19:11:42 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be12674817c3cc5397950df61ba9f0761de7cbb67e7527d120f671791e1644f9`  
		Last Modified: Tue, 19 May 2026 19:11:42 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.5` - unknown; unknown

```console
$ docker pull docker@sha256:8ac585f5eb9117c0193cbfc718548d3dca67a7e669159a6b08a53ae907925d21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa5bac19b0eae7a6debca0657ab9da39a1528d516c371778235e72d5db216621`

```dockerfile
```

-	Layers:
	-	`sha256:662dc4eaa00e9b2353b08fdbf55f624046c556fe7fa5b07f0332cfd3384d50fb`  
		Last Modified: Tue, 19 May 2026 19:11:40 GMT  
		Size: 34.8 KB (34782 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.5-cli`

```console
$ docker pull docker@sha256:9ba8e32bfc35a2c7ae2feb1e3241b2778ae21dee80f4dcd31d04e1cfdea86ea2
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

### `docker:29.5-cli` - linux; amd64

```console
$ docker pull docker@sha256:ec66e6a33f2769030bf8f283b25a7ea135d770ed2c3b91c14195de0ca901e61a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.1 MB (66112304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a190ccdf9e97f139d089920e904db8c97e394f8b5f3ff536cdadeda6c821ded`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Thu, 21 May 2026 22:56:57 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 21 May 2026 22:56:57 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 21 May 2026 22:56:57 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 21 May 2026 22:56:59 GMT
ENV DOCKER_VERSION=29.5.2
# Thu, 21 May 2026 22:56:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 21 May 2026 22:56:59 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 21 May 2026 22:57:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 21 May 2026 22:57:00 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 21 May 2026 22:57:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 21 May 2026 22:57:01 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 21 May 2026 22:57:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 21 May 2026 22:57:01 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 21 May 2026 22:57:01 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 21 May 2026 22:57:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 May 2026 22:57:01 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6cf87df21c231c07f8b8d9c532474fc120946d085773fa15272382636f10b46`  
		Last Modified: Thu, 21 May 2026 22:57:08 GMT  
		Size: 8.3 MB (8311580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54392fc3db24e998571260adc7ac1a1bc098852dfeb30150218d2174da4aa929`  
		Last Modified: Thu, 21 May 2026 22:57:07 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4b052546a5d5d26f7d251d92bd155e2275ee74b4c83a5748550720fa39efe1`  
		Last Modified: Thu, 21 May 2026 22:57:08 GMT  
		Size: 19.5 MB (19549520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b2deac6c9ceba582f6a7f4a7ea2910141ba0dfcf644ee930db818a78947527a`  
		Last Modified: Thu, 21 May 2026 22:57:08 GMT  
		Size: 23.0 MB (22988915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:046b51e466e9d4d0fb090dd060997a0892b36578ab13f0153d1d61f53166d5c6`  
		Last Modified: Thu, 21 May 2026 22:57:09 GMT  
		Size: 11.4 MB (11395947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff5ffb634dd2a67009edb32be895febc923676e8dc0b94f8c857528723140ee`  
		Last Modified: Thu, 21 May 2026 22:57:09 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b162b8dd068432fdb9682bbf9fc7ecbe61c2dbbb72441a22b74a6537f7fe639`  
		Last Modified: Thu, 21 May 2026 22:57:10 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b02815b1d866ccad16190784679c75c04f712dc13f12bd8ec46cf7648796905`  
		Last Modified: Thu, 21 May 2026 22:57:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.5-cli` - unknown; unknown

```console
$ docker pull docker@sha256:d0c058683425ac4a4e35818c3cab8e244bf44bf5629b2606d503eab0302918c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24cd59892835a6bb71bef956c207f451b0ff4ef20ef700549178228a80696991`

```dockerfile
```

-	Layers:
	-	`sha256:e8d0f9a2c1d7978db5312a52983dc91318b6ef2d7b32afeed756151fcba3ed72`  
		Last Modified: Thu, 21 May 2026 22:57:07 GMT  
		Size: 38.1 KB (38056 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.5-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:1ea54fcc950d7b127dc87b88d28c747600cca8b48d8c034ecd527709330f2074
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62396270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8d2a98d406c875d3e0db6343c8b5fa56023aa689cb018d156b714f0199d7ab8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Thu, 21 May 2026 22:57:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 21 May 2026 22:57:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 21 May 2026 22:57:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 21 May 2026 22:57:14 GMT
ENV DOCKER_VERSION=29.5.2
# Thu, 21 May 2026 22:57:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 21 May 2026 22:57:14 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 21 May 2026 22:57:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 21 May 2026 22:57:17 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 21 May 2026 22:57:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 21 May 2026 22:57:18 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 21 May 2026 22:57:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 21 May 2026 22:57:19 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 21 May 2026 22:57:19 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 21 May 2026 22:57:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 May 2026 22:57:19 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:686f209ff6de10676a89d77e3e8a6fab30545d5720ccf9054ee0d1b26e38b43a`  
		Last Modified: Thu, 21 May 2026 22:57:25 GMT  
		Size: 8.2 MB (8211872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc482e1b01e42c3c70b99620637bf883c5da46458460af902ddff0ac829fe8be`  
		Last Modified: Thu, 21 May 2026 22:57:24 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6ca55f6f19c616ff991f7a3db821aff9610c17f90b38f47cbd8f4524f46539`  
		Last Modified: Thu, 21 May 2026 22:57:25 GMT  
		Size: 18.2 MB (18183161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83229a063dcdaa05d49b47a377f6266b68058c99c6e0d8dfdc2a7d84012787eb`  
		Last Modified: Thu, 21 May 2026 22:57:25 GMT  
		Size: 21.6 MB (21614627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:940f9c6bb6e92b7182721c14634a231b228afd28fe04caffd78841f7dd24411b`  
		Last Modified: Thu, 21 May 2026 22:57:26 GMT  
		Size: 10.8 MB (10812594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c13701af534883715f5b32ba09cbb6f13feb5042a866f77e574177b03153cb1`  
		Last Modified: Thu, 21 May 2026 22:57:27 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5827618b0a4b3c9209e2ce38a22a9c7e3bf8dc8d55f12ece8a624cec59ca0c0`  
		Last Modified: Thu, 21 May 2026 22:57:27 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:156a2ca1e461bbe26a51cde3454797f4bb525e545ae12a790eb2c832fa3cd344`  
		Last Modified: Thu, 21 May 2026 22:57:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.5-cli` - unknown; unknown

```console
$ docker pull docker@sha256:04ebdfb0eda18157d342b7fb08c62391f19045358bdd9d13363d75b2bf405b48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c878c65dd1bf46ceb912d86983dbbb6747bbc0d9f04388340d7ff40ab6a955b5`

```dockerfile
```

-	Layers:
	-	`sha256:a18fb0bd08433a7ea29e919c067320a3a5064d90b3bf6926746198a604fa7c2e`  
		Last Modified: Thu, 21 May 2026 22:57:24 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.5-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:4efa5b423f6548c5521b0093e3276bff164af4e70d51c1368309a76e916622e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61378438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d52d0f5e6c9123362925f36aa888038a8dd446e137138fb8463b681a0bc5dff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Thu, 21 May 2026 22:57:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 21 May 2026 22:57:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 21 May 2026 22:57:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 21 May 2026 22:57:19 GMT
ENV DOCKER_VERSION=29.5.2
# Thu, 21 May 2026 22:57:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 21 May 2026 22:57:19 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 21 May 2026 22:57:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 21 May 2026 22:57:21 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 21 May 2026 22:57:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 21 May 2026 22:57:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 21 May 2026 22:57:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 21 May 2026 22:57:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 21 May 2026 22:57:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 21 May 2026 22:57:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 May 2026 22:57:22 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f52861283d77a40b5946e65011de57aef34bc9327b32604f88a677e6f2cb2a`  
		Last Modified: Thu, 21 May 2026 22:57:29 GMT  
		Size: 7.5 MB (7520603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe77c7d8ef7315ec44519db3cec2d9d47ed19881a859e1f59af47b6ee930987`  
		Last Modified: Thu, 21 May 2026 22:57:29 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb66512e1233e73a0972411ebf4f8c344ca4a394da4d49e6b222234bb111c827`  
		Last Modified: Thu, 21 May 2026 22:57:30 GMT  
		Size: 18.2 MB (18172264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa22bb61dc858338f97353ad033e1a3dfeaedd00a1bc504c85cb83d1d1e1066`  
		Last Modified: Thu, 21 May 2026 22:57:30 GMT  
		Size: 21.6 MB (21600713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36a896b5ff64585ed1221a91d5f2f671787cd3897f86991c0f6fe8525f7d75c0`  
		Last Modified: Thu, 21 May 2026 22:57:30 GMT  
		Size: 10.8 MB (10799582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce88e69f3e7c7ac17129a6b4b87aad6b39a3a2861c81d554e406b2547561f66`  
		Last Modified: Thu, 21 May 2026 22:57:30 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5758ccda3473178260da62e4ab7c4fa36a8dfc1c4ef7d4fed06e0ea0fb533c09`  
		Last Modified: Thu, 21 May 2026 22:57:31 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e4468a079208fc160ee3dd1c7df3de47f866b433f720289671fd2ab2bf8a6d`  
		Last Modified: Thu, 21 May 2026 22:57:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.5-cli` - unknown; unknown

```console
$ docker pull docker@sha256:73a5dfa31ffac43a7e451c867bb1707eb46361077e17b338feea6d1cfe16074c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:213b655767f4e7e1aa870b4cdd07817a9d99c15bc554800b7bf98c33cfb92cc9`

```dockerfile
```

-	Layers:
	-	`sha256:88b55d2936f52c50f0f1b5bdd99b1c08534f7a93ef0c66f562f45ef6679cac29`  
		Last Modified: Thu, 21 May 2026 22:57:28 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.5-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:1c27de1f16ee894e6389586d8b58391f4b941f768cb5520cd2970c72d38a8e84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61750058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:156869ccb322d51e7560b80292b10dfaa423516486f6683494060b76d38dabcc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Thu, 21 May 2026 22:56:32 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 21 May 2026 22:56:32 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 21 May 2026 22:56:32 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 21 May 2026 22:56:34 GMT
ENV DOCKER_VERSION=29.5.2
# Thu, 21 May 2026 22:56:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 21 May 2026 22:56:34 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 21 May 2026 22:56:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 21 May 2026 22:56:35 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 21 May 2026 22:56:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 21 May 2026 22:56:36 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 21 May 2026 22:56:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 21 May 2026 22:56:36 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 21 May 2026 22:56:36 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 21 May 2026 22:56:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 May 2026 22:56:36 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae988a6da12e07a4495206223708dfa12193c715305da0959269e07cfe0883c`  
		Last Modified: Thu, 21 May 2026 22:56:42 GMT  
		Size: 8.4 MB (8368391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad63753001c8116da8d4078088f8c226c9d2d5ebb32c543695bad3dfd05cb848`  
		Last Modified: Thu, 21 May 2026 22:56:42 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1523489b9bcf5899f4ec01d3ea4b3b09a7f11127bd6cfac3ad985d4e121a917`  
		Last Modified: Thu, 21 May 2026 22:56:43 GMT  
		Size: 18.0 MB (18003804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4276c1b3c4ca523a976f2b634bcd7b921a29dbff4274ac9aa9cc1e68ed96f93`  
		Last Modified: Thu, 21 May 2026 22:56:43 GMT  
		Size: 20.8 MB (20815981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e3a6fedf4004b1aba4e7b35c15a75f4e30fd0ae9d353199415f18fd99a7cf8`  
		Last Modified: Thu, 21 May 2026 22:56:43 GMT  
		Size: 10.4 MB (10359860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37af9029ae6a6376f88d713b9b54fb69ece2959cf06985f67d3905c6ef36739`  
		Last Modified: Thu, 21 May 2026 22:56:44 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56df60bc257eb03677643450dfa9477ebdad3b524820a408218637a85932c45d`  
		Last Modified: Thu, 21 May 2026 22:56:44 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe07c252ff4b96737716f829e1e8ff46a81625412f850d98480be21cf51f845`  
		Last Modified: Thu, 21 May 2026 22:56:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.5-cli` - unknown; unknown

```console
$ docker pull docker@sha256:a8dedaaa0ddf7100fc1cf4d4aee8dec52a0bd683ada897dc62942f5c0b88d846
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30bdb74e1af7301d0ea10753180b6ea04b819ea07777e30c7cc70392aefbb2db`

```dockerfile
```

-	Layers:
	-	`sha256:ddd2ae6062cdfd1652888a3cbd3bdc652070dde80dc25a31826cfb552cb05649`  
		Last Modified: Thu, 21 May 2026 22:56:42 GMT  
		Size: 38.3 KB (38262 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.5-dind`

```console
$ docker pull docker@sha256:eed377f3ce14afda560e742c5b3ae446df1ce00a16e1beab2ac6c78c1477fe85
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

### `docker:29.5-dind` - linux; amd64

```console
$ docker pull docker@sha256:6f156e0882b6f307bcd00e01b7abebdccf6eb96b1bb40e8b160e3e401ba3749b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.7 MB (141660887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a475a10539689996453c7c7aa57795a1c35cb8da621faddaef1fb0f05cdb7723`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Tue, 19 May 2026 18:43:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 19 May 2026 18:43:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 19 May 2026 18:43:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 19 May 2026 18:43:53 GMT
ENV DOCKER_VERSION=29.5.1
# Tue, 19 May 2026 18:43:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 19 May 2026 18:43:53 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Tue, 19 May 2026 18:43:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-amd64'; 			sha256='0144479d5a1cd710be3464ae898628cfa68033e16b225aef52f81930c45ac9b5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v6'; 			sha256='1f34337385921c5da43d63452282726b062aa887fda975f96dd3d6e869648bc6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v7'; 			sha256='3560b5b6fd3485f4d0bd160e7edf56cc1f08f0cb5852c9af28bf3fab9973c7c2'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm64'; 			sha256='565605fe0bb393ed5d11771e5b52fc7ef05c701868861fa85609747c9d74a440'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-ppc64le'; 			sha256='c5ef8012f48a518e1c235ad408d26cd424d7b5fa87eaf78cb2ff4b9048730120'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-riscv64'; 			sha256='80b27d5f3a346591a5045b81217ee5be578ed151ef8cbd883a892c0ec0ac33f1'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-s390x'; 			sha256='04f5bd0d389f682c7e9287a3b3a1777b0848f8e10d58cbf9d4d12c9002bbb378'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 19 May 2026 18:43:54 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Tue, 19 May 2026 18:43:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 19 May 2026 18:43:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 19 May 2026 18:43:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 18:43:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 19 May 2026 18:43:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 19 May 2026 18:43:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 May 2026 18:43:55 GMT
CMD ["sh"]
# Tue, 19 May 2026 18:52:09 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 19 May 2026 18:52:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 19 May 2026 18:52:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 19 May 2026 18:52:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 19 May 2026 18:52:13 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 19 May 2026 18:52:13 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 19 May 2026 18:52:13 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 18:52:13 GMT
VOLUME [/var/lib/docker]
# Tue, 19 May 2026 18:52:13 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 19 May 2026 18:52:13 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 19 May 2026 18:52:13 GMT
CMD []
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959d822c11f4cffde22f6a8ca77070ab678788ee8a60e50bf52240fab7600d55`  
		Last Modified: Tue, 19 May 2026 18:44:02 GMT  
		Size: 8.3 MB (8311621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf748eeffe46320957e43a6d041504e02f6d54efaa90b05ea0a5e76259a3bc9`  
		Last Modified: Tue, 19 May 2026 18:44:01 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29db3e4d2cf2bffd95a0b8c095c0dfc7f4b6ee9717169afb9c613ae0714f22a5`  
		Last Modified: Tue, 19 May 2026 18:44:03 GMT  
		Size: 19.5 MB (19549501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:418895c8a0097a67712f5b2385b094ed4ed5af1359b9b43cb86c07da48ca11c9`  
		Last Modified: Tue, 19 May 2026 18:44:03 GMT  
		Size: 23.0 MB (22988580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4382b5de8ae74e74d495d9d94f0127cf051728dc00cab26dfa163bba8cdbcf13`  
		Last Modified: Tue, 19 May 2026 18:44:03 GMT  
		Size: 11.2 MB (11243752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53914aaed626c98320ff52b5bbe81eb804e9a82d445d07a5908e16e86ac5a5c`  
		Last Modified: Tue, 19 May 2026 18:44:03 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cac0928dd7f6aa6c83aa987350f200df21db15618f2ba47912f35be2b16b3b9`  
		Last Modified: Tue, 19 May 2026 18:44:04 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1c069fc81d4d790f039a7a8160f23dffa6c11a22ee385a0db0fe75ae235dfe1`  
		Last Modified: Tue, 19 May 2026 18:44:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27817872a6ae6fcf22af6f3dbdec0f52f7b055d8b3384cd5b922f74d11358249`  
		Last Modified: Tue, 19 May 2026 18:52:23 GMT  
		Size: 6.9 MB (6941424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a7ba7363a81328286ac28be79b6e6248a1e1c4cb3f1749b808bc8abeb5c686`  
		Last Modified: Tue, 19 May 2026 18:52:23 GMT  
		Size: 92.2 KB (92218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f90442d3c5cd85fdf0fd4683516f39486a803bd57eb9813b3dcb939d9d3fcc`  
		Last Modified: Tue, 19 May 2026 18:52:23 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c588cc6d3552d3ec8363fa8dabb97cfe3ea467efd07c37c45853267ab5c544`  
		Last Modified: Tue, 19 May 2026 18:52:25 GMT  
		Size: 68.7 MB (68661447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa91ecdbc2c72221f7c567a768c787e9b0e27629ad60fecaa37b420555dbec4`  
		Last Modified: Tue, 19 May 2026 18:52:24 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a04f224ef5d78ccf3d32a655e7621773237de1ba0a09780d2011e4e3efc9802`  
		Last Modified: Tue, 19 May 2026 18:52:25 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.5-dind` - unknown; unknown

```console
$ docker pull docker@sha256:8459bca25b1862c9c244d8290b9c289f8f38a28e911360560cef489552fd9996
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca9c00d43298e9a165fe521202b47e762e0e30cdaad754b907fb2241affba41a`

```dockerfile
```

-	Layers:
	-	`sha256:725c95ff8cee96878c88b2d98ed922fc03f42a86c848e44ace4d3602cca233bd`  
		Last Modified: Tue, 19 May 2026 18:52:23 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.5-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:656cd6a2deb516bf1bab86d4eb9e0ea9b2afca3fb8c81a402195068521496791
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.6 MB (133554774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b375b41ebcd63fd76689fd0c53d0cbebdb1c6086df5568f03b1342739485d2f4`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Tue, 19 May 2026 18:46:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 19 May 2026 18:46:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 19 May 2026 18:46:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 19 May 2026 18:46:29 GMT
ENV DOCKER_VERSION=29.5.1
# Tue, 19 May 2026 18:46:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 19 May 2026 18:46:29 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Tue, 19 May 2026 18:46:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-amd64'; 			sha256='0144479d5a1cd710be3464ae898628cfa68033e16b225aef52f81930c45ac9b5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v6'; 			sha256='1f34337385921c5da43d63452282726b062aa887fda975f96dd3d6e869648bc6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v7'; 			sha256='3560b5b6fd3485f4d0bd160e7edf56cc1f08f0cb5852c9af28bf3fab9973c7c2'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm64'; 			sha256='565605fe0bb393ed5d11771e5b52fc7ef05c701868861fa85609747c9d74a440'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-ppc64le'; 			sha256='c5ef8012f48a518e1c235ad408d26cd424d7b5fa87eaf78cb2ff4b9048730120'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-riscv64'; 			sha256='80b27d5f3a346591a5045b81217ee5be578ed151ef8cbd883a892c0ec0ac33f1'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-s390x'; 			sha256='04f5bd0d389f682c7e9287a3b3a1777b0848f8e10d58cbf9d4d12c9002bbb378'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 19 May 2026 18:46:32 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Tue, 19 May 2026 18:46:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 19 May 2026 18:46:33 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 19 May 2026 18:46:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 18:46:33 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 19 May 2026 18:46:34 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 19 May 2026 18:46:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 May 2026 18:46:34 GMT
CMD ["sh"]
# Tue, 19 May 2026 18:48:00 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 19 May 2026 18:48:00 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 19 May 2026 18:48:00 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 19 May 2026 18:48:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 19 May 2026 18:48:04 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 19 May 2026 18:48:04 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 19 May 2026 18:48:04 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 18:48:04 GMT
VOLUME [/var/lib/docker]
# Tue, 19 May 2026 18:48:04 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 19 May 2026 18:48:04 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 19 May 2026 18:48:04 GMT
CMD []
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e510993d358b2182e33432b09c723cb2de90442627624e753d33ff6f58e37cf`  
		Last Modified: Tue, 19 May 2026 18:46:40 GMT  
		Size: 8.2 MB (8211856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac6422e386e61fe4ba4eb1abca9f67aef1bba270f947f3797505168eddc865ef`  
		Last Modified: Tue, 19 May 2026 18:46:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c6104ecd7c2122cba9eadf591b901752e839d28c94e9786023634ab16c4e86`  
		Last Modified: Tue, 19 May 2026 18:46:41 GMT  
		Size: 18.2 MB (18183185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9278a90d0e78f94da7f59f70fe4811830047483868d42c4e25a85b91a3359765`  
		Last Modified: Tue, 19 May 2026 18:46:41 GMT  
		Size: 21.6 MB (21614147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09f94e1195a7d62fc4046fa609e325b2001195cf49352924129c45728445d565`  
		Last Modified: Tue, 19 May 2026 18:46:41 GMT  
		Size: 10.7 MB (10650824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a8126c2985de246f1344d8c4340e5934b14cdf06f269351c0bfeac534be4c3a`  
		Last Modified: Tue, 19 May 2026 18:46:41 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f13c028f2e167a9ccd442fe69b89b5f1ca9e19f4589d7160d5af4d3b451ba862`  
		Last Modified: Tue, 19 May 2026 18:46:42 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa9769c6262cc549e78864817d114f4780b6b611ff08c097bcb018ab9040fd0`  
		Last Modified: Tue, 19 May 2026 18:46:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:125e5e8c972742a3fdece68d1d7efe160fc572758035dc6dd440150a5dff5bf7`  
		Last Modified: Tue, 19 May 2026 18:48:15 GMT  
		Size: 7.3 MB (7278661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:092dd15fda2f6f91745deb58f699d28c2ae054d7fb4d6c4100b53f0f8e3a6d85`  
		Last Modified: Tue, 19 May 2026 18:48:15 GMT  
		Size: 91.5 KB (91516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc718ec10edd9882bc794dfec135ed20f43243a8db5ad70f2ca75ac4b4191815`  
		Last Modified: Tue, 19 May 2026 18:48:15 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf390f2615c4c05543ef083213b7da580fc3a675929438042a5228503644f65`  
		Last Modified: Tue, 19 May 2026 18:48:17 GMT  
		Size: 63.9 MB (63944568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0111492ca1c0d70617ea1ed481e8ae4908695479c10dc5b86fe761dd03edc6b`  
		Last Modified: Tue, 19 May 2026 18:48:16 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b88ff88aa94e286fad9d8f3480fb92ba8ec324a9d55d74cce8cce2e99c36353`  
		Last Modified: Tue, 19 May 2026 18:48:16 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.5-dind` - unknown; unknown

```console
$ docker pull docker@sha256:1fd6b9654a40244c2a32a42dfdbd4b0c2fcd97aaacc719b9c466fed8008b0c05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e4f0d6a13a6e324e492f0fd9ae8856d26b30b034d24e9b3868069907c61ec10`

```dockerfile
```

-	Layers:
	-	`sha256:096e9d4d3b5e87687de3559cc60228911d8179792add0ad0a60e1afd76f2b032`  
		Last Modified: Tue, 19 May 2026 18:48:14 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.5-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:ce68e53519cdc94c6b28b82b2e4af1856aa5dd8e577fb872900952a6ed88f9d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.7 MB (131668449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bc263b60a94589a9d3f238ee64951d8f806cc46c8caed0452715d45111a5b91`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Tue, 19 May 2026 18:50:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 19 May 2026 18:50:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 19 May 2026 18:50:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 19 May 2026 18:50:21 GMT
ENV DOCKER_VERSION=29.5.1
# Tue, 19 May 2026 18:50:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 19 May 2026 18:50:21 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Tue, 19 May 2026 18:50:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-amd64'; 			sha256='0144479d5a1cd710be3464ae898628cfa68033e16b225aef52f81930c45ac9b5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v6'; 			sha256='1f34337385921c5da43d63452282726b062aa887fda975f96dd3d6e869648bc6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v7'; 			sha256='3560b5b6fd3485f4d0bd160e7edf56cc1f08f0cb5852c9af28bf3fab9973c7c2'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm64'; 			sha256='565605fe0bb393ed5d11771e5b52fc7ef05c701868861fa85609747c9d74a440'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-ppc64le'; 			sha256='c5ef8012f48a518e1c235ad408d26cd424d7b5fa87eaf78cb2ff4b9048730120'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-riscv64'; 			sha256='80b27d5f3a346591a5045b81217ee5be578ed151ef8cbd883a892c0ec0ac33f1'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-s390x'; 			sha256='04f5bd0d389f682c7e9287a3b3a1777b0848f8e10d58cbf9d4d12c9002bbb378'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 19 May 2026 18:50:23 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Tue, 19 May 2026 18:50:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 19 May 2026 18:50:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 19 May 2026 18:50:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 18:50:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 19 May 2026 18:50:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 19 May 2026 18:50:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 May 2026 18:50:24 GMT
CMD ["sh"]
# Tue, 19 May 2026 19:11:05 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 19 May 2026 19:11:05 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 19 May 2026 19:11:05 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 19 May 2026 19:11:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 19 May 2026 19:11:10 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 19 May 2026 19:11:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 19 May 2026 19:11:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 19:11:10 GMT
VOLUME [/var/lib/docker]
# Tue, 19 May 2026 19:11:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 19 May 2026 19:11:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 19 May 2026 19:11:10 GMT
CMD []
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e78396f075a6021fa389cbab78d2b7a97c1fa6ccd90c5a3f9aad13a82d9a82d5`  
		Last Modified: Tue, 19 May 2026 18:50:31 GMT  
		Size: 7.5 MB (7520541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55503681071acc50ecd4d54f1a76c32b34fb2e24b116717b8a11a5ed2c4b834b`  
		Last Modified: Tue, 19 May 2026 18:50:30 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:139bfdfb0c5a911c258bd9ca3f33e5d74dc4cdac244e701ffc230dfb2dbcf299`  
		Last Modified: Tue, 19 May 2026 18:50:31 GMT  
		Size: 18.2 MB (18172268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e28d126c0c15c1ddece42e48d16b7989f46d4ba83543ade587e34aae442b162d`  
		Last Modified: Tue, 19 May 2026 18:50:31 GMT  
		Size: 21.6 MB (21600397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb484c140400a96468ac162a856058550dff5319ecf84cb2d15485ffa462cfe5`  
		Last Modified: Tue, 19 May 2026 18:50:31 GMT  
		Size: 10.6 MB (10637143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:458ff3d79525d794f095fe12c99f3a95a84e674163d4ac75823a6bbe91cdca6c`  
		Last Modified: Tue, 19 May 2026 18:50:32 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:252522a027743939f7b115d2d3929238ba7a8fee776336371433d62e17da49f3`  
		Last Modified: Tue, 19 May 2026 18:50:33 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b1fd0762adb2df9e41385aaea4f5aeb069ccb43ec6a5203c0970dbb32f5d39`  
		Last Modified: Tue, 19 May 2026 18:50:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2404388a95cbd53c2924a8956a2b0bd9fed1ed42798ef0d7958645ec50b36503`  
		Last Modified: Tue, 19 May 2026 19:11:21 GMT  
		Size: 6.6 MB (6577150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abebc77c5a81c02e559a6177ab009ea93d155d230027ecb011d71caf8e1319cb`  
		Last Modified: Tue, 19 May 2026 19:11:20 GMT  
		Size: 87.8 KB (87825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:505cb9808a455382b226432bd33efca0786f2b2817e3828966e8ae1880b9a387`  
		Last Modified: Tue, 19 May 2026 19:11:20 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb736cbd14a0b4279f19088aba50827f55f5bd8c64dd5868c81329ee396e19f`  
		Last Modified: Tue, 19 May 2026 19:11:23 GMT  
		Size: 63.8 MB (63781847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b8e0456f81c21846bbc1e4af0c8ce599dde97bbda1d981de3f47999ce045a4`  
		Last Modified: Tue, 19 May 2026 19:11:22 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10bd67dffac6bb7c60a61f90d9e059f51d217061b38efadfa05cfbccc501c4eb`  
		Last Modified: Tue, 19 May 2026 19:11:22 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.5-dind` - unknown; unknown

```console
$ docker pull docker@sha256:38aff3f9f68bc80866a840b6895120e3efd20f227f69ca66663fee2a5c143d5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e771280fb8341ddf485470385301e8a4df555c4889817952e2e3f1bc2d60f3f`

```dockerfile
```

-	Layers:
	-	`sha256:0f43b1170bad091b1f8a038b4c799e044dcbe62f3cf88792df12fd3808abd3db`  
		Last Modified: Tue, 19 May 2026 19:11:20 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.5-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:d29f00616a4b5af545c6238d5e5d3f010dabe8cd9373464e7528dcc2ffe932e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.1 MB (131088931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d59db2bca67549c508438fad529bbb4d973798fdf3dac19d4cff714cd0ef24d8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Tue, 19 May 2026 18:52:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 19 May 2026 18:52:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 19 May 2026 18:52:13 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 19 May 2026 18:52:16 GMT
ENV DOCKER_VERSION=29.5.1
# Tue, 19 May 2026 18:52:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 19 May 2026 18:52:16 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Tue, 19 May 2026 18:52:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-amd64'; 			sha256='0144479d5a1cd710be3464ae898628cfa68033e16b225aef52f81930c45ac9b5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v6'; 			sha256='1f34337385921c5da43d63452282726b062aa887fda975f96dd3d6e869648bc6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v7'; 			sha256='3560b5b6fd3485f4d0bd160e7edf56cc1f08f0cb5852c9af28bf3fab9973c7c2'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm64'; 			sha256='565605fe0bb393ed5d11771e5b52fc7ef05c701868861fa85609747c9d74a440'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-ppc64le'; 			sha256='c5ef8012f48a518e1c235ad408d26cd424d7b5fa87eaf78cb2ff4b9048730120'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-riscv64'; 			sha256='80b27d5f3a346591a5045b81217ee5be578ed151ef8cbd883a892c0ec0ac33f1'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-s390x'; 			sha256='04f5bd0d389f682c7e9287a3b3a1777b0848f8e10d58cbf9d4d12c9002bbb378'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 19 May 2026 18:52:17 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Tue, 19 May 2026 18:52:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 19 May 2026 18:52:18 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 19 May 2026 18:52:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 18:52:18 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 19 May 2026 18:52:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 19 May 2026 18:52:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 May 2026 18:52:18 GMT
CMD ["sh"]
# Tue, 19 May 2026 19:11:28 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 19 May 2026 19:11:28 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 19 May 2026 19:11:29 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 19 May 2026 19:11:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 19 May 2026 19:11:31 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 19 May 2026 19:11:31 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 19 May 2026 19:11:31 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 19:11:31 GMT
VOLUME [/var/lib/docker]
# Tue, 19 May 2026 19:11:31 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 19 May 2026 19:11:31 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 19 May 2026 19:11:31 GMT
CMD []
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:439c73b6370f92c891e3dae2ef2ac51ba47633f4382e93fa3a194ab6c9929fcf`  
		Last Modified: Tue, 19 May 2026 18:52:24 GMT  
		Size: 8.4 MB (8368378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:090f26860bbcb42203be1c1ccc78e592537b7d5076712eddc078a4521b65b6ef`  
		Last Modified: Tue, 19 May 2026 18:52:23 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02fa5c43148b510203ce86fd309a24339439966d97d2739e5681dea9fbedd78b`  
		Last Modified: Tue, 19 May 2026 18:52:24 GMT  
		Size: 18.0 MB (18003824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:179aebd9e04e34e062d99c03bced083b59894f9ff9c70a48e5fdde05043d0662`  
		Last Modified: Tue, 19 May 2026 18:52:25 GMT  
		Size: 20.8 MB (20815342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333ebd0d3068df15ad94c847b40ac364dc7140981f38d3a8f08165ef3fe528ac`  
		Last Modified: Tue, 19 May 2026 18:52:25 GMT  
		Size: 10.2 MB (10243275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e7cd72262f0dcb67fc210c582e3d890f8da6bbfea7979a4af0eca2d85493c8`  
		Last Modified: Tue, 19 May 2026 18:52:25 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb8c848507ade63fa035c4247243268bc78609cb843c2c46923fec82cf42e856`  
		Last Modified: Tue, 19 May 2026 18:52:26 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14678f991761f143ab6345db5de4a84ca5f83a1cd44f7d579a88be20ad20871`  
		Last Modified: Tue, 19 May 2026 18:52:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deb061c465c1d4b2683f89277bb8b93644ad86d3b6a034d3848e218ff3a36250`  
		Last Modified: Tue, 19 May 2026 19:11:41 GMT  
		Size: 7.2 MB (7219902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408cc9607ded7836e6377a9012f389a02da93bc2526404ac2125d556fed0607c`  
		Last Modified: Tue, 19 May 2026 19:11:41 GMT  
		Size: 100.9 KB (100930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4813a99698e1ee0cbb52b02f822e9732eb9144586aa3c765fee806857d8cb872`  
		Last Modified: Tue, 19 May 2026 19:11:41 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f364d3985b9e2a29ae89857aa654e13a752db4b807f58b23afc56a7fdddc9ca`  
		Last Modified: Tue, 19 May 2026 19:11:43 GMT  
		Size: 62.1 MB (62129257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34b8039e34935754bb978ab40f852eeb6345408e37deb40c0467f77421c8252`  
		Last Modified: Tue, 19 May 2026 19:11:42 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be12674817c3cc5397950df61ba9f0761de7cbb67e7527d120f671791e1644f9`  
		Last Modified: Tue, 19 May 2026 19:11:42 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.5-dind` - unknown; unknown

```console
$ docker pull docker@sha256:8ac585f5eb9117c0193cbfc718548d3dca67a7e669159a6b08a53ae907925d21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa5bac19b0eae7a6debca0657ab9da39a1528d516c371778235e72d5db216621`

```dockerfile
```

-	Layers:
	-	`sha256:662dc4eaa00e9b2353b08fdbf55f624046c556fe7fa5b07f0332cfd3384d50fb`  
		Last Modified: Tue, 19 May 2026 19:11:40 GMT  
		Size: 34.8 KB (34782 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.5-dind-rootless`

```console
$ docker pull docker@sha256:fc34343ecba0eed3f4c4f82dacd33287140cf123e7449f2e7a37fefa6b233a72
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:29.5-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:54fb8c3eb5b740f6e3660ec25470f773073e6376db6a4edda040eb8ba7105e64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157184836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abc3d62166f739fc25b4f819b724c5c207c6d5e3ccaa7127fc1a33ce1ef2b983`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Tue, 19 May 2026 18:43:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 19 May 2026 18:43:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 19 May 2026 18:43:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 19 May 2026 18:43:53 GMT
ENV DOCKER_VERSION=29.5.1
# Tue, 19 May 2026 18:43:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 19 May 2026 18:43:53 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Tue, 19 May 2026 18:43:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-amd64'; 			sha256='0144479d5a1cd710be3464ae898628cfa68033e16b225aef52f81930c45ac9b5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v6'; 			sha256='1f34337385921c5da43d63452282726b062aa887fda975f96dd3d6e869648bc6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v7'; 			sha256='3560b5b6fd3485f4d0bd160e7edf56cc1f08f0cb5852c9af28bf3fab9973c7c2'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm64'; 			sha256='565605fe0bb393ed5d11771e5b52fc7ef05c701868861fa85609747c9d74a440'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-ppc64le'; 			sha256='c5ef8012f48a518e1c235ad408d26cd424d7b5fa87eaf78cb2ff4b9048730120'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-riscv64'; 			sha256='80b27d5f3a346591a5045b81217ee5be578ed151ef8cbd883a892c0ec0ac33f1'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-s390x'; 			sha256='04f5bd0d389f682c7e9287a3b3a1777b0848f8e10d58cbf9d4d12c9002bbb378'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 19 May 2026 18:43:54 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Tue, 19 May 2026 18:43:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 19 May 2026 18:43:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 19 May 2026 18:43:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 18:43:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 19 May 2026 18:43:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 19 May 2026 18:43:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 May 2026 18:43:55 GMT
CMD ["sh"]
# Tue, 19 May 2026 18:52:09 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 19 May 2026 18:52:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 19 May 2026 18:52:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 19 May 2026 18:52:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 19 May 2026 18:52:13 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 19 May 2026 18:52:13 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 19 May 2026 18:52:13 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 18:52:13 GMT
VOLUME [/var/lib/docker]
# Tue, 19 May 2026 18:52:13 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 19 May 2026 18:52:13 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 19 May 2026 18:52:13 GMT
CMD []
# Tue, 19 May 2026 19:10:23 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Tue, 19 May 2026 19:10:23 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 19 May 2026 19:10:23 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 19 May 2026 19:10:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 	; 	rm rootless.tgz; 		rootlesskit --version # buildkit
# Tue, 19 May 2026 19:10:23 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 19 May 2026 19:10:23 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 19 May 2026 19:10:23 GMT
USER rootless
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959d822c11f4cffde22f6a8ca77070ab678788ee8a60e50bf52240fab7600d55`  
		Last Modified: Tue, 19 May 2026 18:44:02 GMT  
		Size: 8.3 MB (8311621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf748eeffe46320957e43a6d041504e02f6d54efaa90b05ea0a5e76259a3bc9`  
		Last Modified: Tue, 19 May 2026 18:44:01 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29db3e4d2cf2bffd95a0b8c095c0dfc7f4b6ee9717169afb9c613ae0714f22a5`  
		Last Modified: Tue, 19 May 2026 18:44:03 GMT  
		Size: 19.5 MB (19549501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:418895c8a0097a67712f5b2385b094ed4ed5af1359b9b43cb86c07da48ca11c9`  
		Last Modified: Tue, 19 May 2026 18:44:03 GMT  
		Size: 23.0 MB (22988580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4382b5de8ae74e74d495d9d94f0127cf051728dc00cab26dfa163bba8cdbcf13`  
		Last Modified: Tue, 19 May 2026 18:44:03 GMT  
		Size: 11.2 MB (11243752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53914aaed626c98320ff52b5bbe81eb804e9a82d445d07a5908e16e86ac5a5c`  
		Last Modified: Tue, 19 May 2026 18:44:03 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cac0928dd7f6aa6c83aa987350f200df21db15618f2ba47912f35be2b16b3b9`  
		Last Modified: Tue, 19 May 2026 18:44:04 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1c069fc81d4d790f039a7a8160f23dffa6c11a22ee385a0db0fe75ae235dfe1`  
		Last Modified: Tue, 19 May 2026 18:44:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27817872a6ae6fcf22af6f3dbdec0f52f7b055d8b3384cd5b922f74d11358249`  
		Last Modified: Tue, 19 May 2026 18:52:23 GMT  
		Size: 6.9 MB (6941424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a7ba7363a81328286ac28be79b6e6248a1e1c4cb3f1749b808bc8abeb5c686`  
		Last Modified: Tue, 19 May 2026 18:52:23 GMT  
		Size: 92.2 KB (92218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f90442d3c5cd85fdf0fd4683516f39486a803bd57eb9813b3dcb939d9d3fcc`  
		Last Modified: Tue, 19 May 2026 18:52:23 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c588cc6d3552d3ec8363fa8dabb97cfe3ea467efd07c37c45853267ab5c544`  
		Last Modified: Tue, 19 May 2026 18:52:25 GMT  
		Size: 68.7 MB (68661447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa91ecdbc2c72221f7c567a768c787e9b0e27629ad60fecaa37b420555dbec4`  
		Last Modified: Tue, 19 May 2026 18:52:24 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a04f224ef5d78ccf3d32a655e7621773237de1ba0a09780d2011e4e3efc9802`  
		Last Modified: Tue, 19 May 2026 18:52:25 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cecc87fe83d1eed7164980cba609d8af5ce21512b7a270c9fff3a717b56885d`  
		Last Modified: Tue, 19 May 2026 19:10:29 GMT  
		Size: 3.4 MB (3420112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f1de764b59139da153ed5c910b6f1016ba4c34bfe850397d4515465af03b14`  
		Last Modified: Tue, 19 May 2026 19:10:28 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810353487b2c22447155b48ee25ce68046853c053cd2683969fef6360cc51933`  
		Last Modified: Tue, 19 May 2026 19:10:29 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51c09f12615ecc2d61dce57d65b327703b94b167fc1f44f161403ac443d684f2`  
		Last Modified: Tue, 19 May 2026 19:10:29 GMT  
		Size: 12.1 MB (12102496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9688d32ac36d4f90efdf6379ecbdf84feb518c202f038c402b312b45fe270a28`  
		Last Modified: Tue, 19 May 2026 19:10:30 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.5-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:110a0812130d4441ce1773cd1230225e01f2e770f5ecf5f5641a4baf88df3911
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a854ed3332b83327cbd69c19dfffceb9982c23ed85413639f28ad3c4e8a4cbd`

```dockerfile
```

-	Layers:
	-	`sha256:8786627e00c646555d675e83986675375d51e2130c10d9a3645ebd3a70b82cd2`  
		Last Modified: Tue, 19 May 2026 19:10:28 GMT  
		Size: 30.5 KB (30493 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.5-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:f69d2ff1f367dac480263f11eb4bb9237f140d4ebe4349325c75b4fd0d06bd28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.7 MB (145721341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a4e4d8a17819a06713e6ac6acfa7f117cf9cd4e8567cf58372f73eca47616c4`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Tue, 19 May 2026 18:52:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 19 May 2026 18:52:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 19 May 2026 18:52:13 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 19 May 2026 18:52:16 GMT
ENV DOCKER_VERSION=29.5.1
# Tue, 19 May 2026 18:52:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 19 May 2026 18:52:16 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Tue, 19 May 2026 18:52:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-amd64'; 			sha256='0144479d5a1cd710be3464ae898628cfa68033e16b225aef52f81930c45ac9b5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v6'; 			sha256='1f34337385921c5da43d63452282726b062aa887fda975f96dd3d6e869648bc6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v7'; 			sha256='3560b5b6fd3485f4d0bd160e7edf56cc1f08f0cb5852c9af28bf3fab9973c7c2'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm64'; 			sha256='565605fe0bb393ed5d11771e5b52fc7ef05c701868861fa85609747c9d74a440'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-ppc64le'; 			sha256='c5ef8012f48a518e1c235ad408d26cd424d7b5fa87eaf78cb2ff4b9048730120'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-riscv64'; 			sha256='80b27d5f3a346591a5045b81217ee5be578ed151ef8cbd883a892c0ec0ac33f1'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-s390x'; 			sha256='04f5bd0d389f682c7e9287a3b3a1777b0848f8e10d58cbf9d4d12c9002bbb378'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 19 May 2026 18:52:17 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Tue, 19 May 2026 18:52:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 19 May 2026 18:52:18 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 19 May 2026 18:52:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 18:52:18 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 19 May 2026 18:52:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 19 May 2026 18:52:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 May 2026 18:52:18 GMT
CMD ["sh"]
# Tue, 19 May 2026 19:11:28 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 19 May 2026 19:11:28 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 19 May 2026 19:11:29 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 19 May 2026 19:11:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 19 May 2026 19:11:31 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 19 May 2026 19:11:31 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 19 May 2026 19:11:31 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 19:11:31 GMT
VOLUME [/var/lib/docker]
# Tue, 19 May 2026 19:11:31 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 19 May 2026 19:11:31 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 19 May 2026 19:11:31 GMT
CMD []
# Tue, 19 May 2026 20:10:18 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Tue, 19 May 2026 20:10:18 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 19 May 2026 20:10:18 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 19 May 2026 20:10:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 	; 	rm rootless.tgz; 		rootlesskit --version # buildkit
# Tue, 19 May 2026 20:10:18 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 19 May 2026 20:10:18 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 19 May 2026 20:10:18 GMT
USER rootless
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:439c73b6370f92c891e3dae2ef2ac51ba47633f4382e93fa3a194ab6c9929fcf`  
		Last Modified: Tue, 19 May 2026 18:52:24 GMT  
		Size: 8.4 MB (8368378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:090f26860bbcb42203be1c1ccc78e592537b7d5076712eddc078a4521b65b6ef`  
		Last Modified: Tue, 19 May 2026 18:52:23 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02fa5c43148b510203ce86fd309a24339439966d97d2739e5681dea9fbedd78b`  
		Last Modified: Tue, 19 May 2026 18:52:24 GMT  
		Size: 18.0 MB (18003824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:179aebd9e04e34e062d99c03bced083b59894f9ff9c70a48e5fdde05043d0662`  
		Last Modified: Tue, 19 May 2026 18:52:25 GMT  
		Size: 20.8 MB (20815342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333ebd0d3068df15ad94c847b40ac364dc7140981f38d3a8f08165ef3fe528ac`  
		Last Modified: Tue, 19 May 2026 18:52:25 GMT  
		Size: 10.2 MB (10243275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e7cd72262f0dcb67fc210c582e3d890f8da6bbfea7979a4af0eca2d85493c8`  
		Last Modified: Tue, 19 May 2026 18:52:25 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb8c848507ade63fa035c4247243268bc78609cb843c2c46923fec82cf42e856`  
		Last Modified: Tue, 19 May 2026 18:52:26 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14678f991761f143ab6345db5de4a84ca5f83a1cd44f7d579a88be20ad20871`  
		Last Modified: Tue, 19 May 2026 18:52:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deb061c465c1d4b2683f89277bb8b93644ad86d3b6a034d3848e218ff3a36250`  
		Last Modified: Tue, 19 May 2026 19:11:41 GMT  
		Size: 7.2 MB (7219902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408cc9607ded7836e6377a9012f389a02da93bc2526404ac2125d556fed0607c`  
		Last Modified: Tue, 19 May 2026 19:11:41 GMT  
		Size: 100.9 KB (100930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4813a99698e1ee0cbb52b02f822e9732eb9144586aa3c765fee806857d8cb872`  
		Last Modified: Tue, 19 May 2026 19:11:41 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f364d3985b9e2a29ae89857aa654e13a752db4b807f58b23afc56a7fdddc9ca`  
		Last Modified: Tue, 19 May 2026 19:11:43 GMT  
		Size: 62.1 MB (62129257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34b8039e34935754bb978ab40f852eeb6345408e37deb40c0467f77421c8252`  
		Last Modified: Tue, 19 May 2026 19:11:42 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be12674817c3cc5397950df61ba9f0761de7cbb67e7527d120f671791e1644f9`  
		Last Modified: Tue, 19 May 2026 19:11:42 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e2794603590245d075eed606ac34301c58fda88a8a80f4eaa3ffce3d78a905`  
		Last Modified: Tue, 19 May 2026 20:10:24 GMT  
		Size: 3.4 MB (3394549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afc77214cc9ebf151912fa095a575ef37f668cb6338ba1a94904c1edaf262ceb`  
		Last Modified: Tue, 19 May 2026 20:10:24 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ead735ef17a546ca40080e700f3c11ff2c11b5cdc13bafd2c98e028f26c5940`  
		Last Modified: Tue, 19 May 2026 20:10:24 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51aaf502457f6ce01bba562fab571d3a6ae959cb483cd95636a71243072df558`  
		Last Modified: Tue, 19 May 2026 20:10:24 GMT  
		Size: 11.2 MB (11236521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b0ca64e0e966609139e6199a7a8b766c498d0350d644cd8d18ab622a42d3fc9`  
		Last Modified: Tue, 19 May 2026 20:10:25 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.5-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:4fe949a9f9e01f26d41d7540737c598ccada6b62562db26845b13a0cf57f124a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 KB (30663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d49dc7a383ab1fdb7ccd92405afa131cc367a1c519e6a245d1ff68df7e85a66`

```dockerfile
```

-	Layers:
	-	`sha256:e83fa8083ea898497b6c983d8641259136e040f0b533861df142a73520bda5fe`  
		Last Modified: Tue, 19 May 2026 20:10:23 GMT  
		Size: 30.7 KB (30663 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.5-windowsservercore`

```console
$ docker pull docker@sha256:76a2595299d5d831461bbff176d00c8005cc1b58a48fe70127d90155b250253f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32860; amd64
	-	windows version 10.0.20348.5139; amd64

### `docker:29.5-windowsservercore` - windows version 10.0.26100.32860; amd64

```console
$ docker pull docker@sha256:189f1d53b9d0831a7663f55ac4dfcfe317baa879af86a90a44e1c83e9f9fbf6a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2262683896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c993dcdab4e74415b546e3486a219f555369a5b9db18c96ed98e36915f6572`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 10 May 2026 10:08:54 GMT
RUN Install update 10.0.26100.32860
# Thu, 21 May 2026 23:13:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 21 May 2026 23:15:10 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 21 May 2026 23:15:11 GMT
ENV DOCKER_VERSION=29.5.2
# Thu, 21 May 2026 23:15:13 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.5.2.zip
# Thu, 21 May 2026 23:15:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 21 May 2026 23:15:38 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 21 May 2026 23:15:39 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.windows-amd64.exe
# Thu, 21 May 2026 23:15:39 GMT
ENV DOCKER_BUILDX_SHA256=41e1b3fff6541d5f5febb18ff4c9108bec30afd7bf9133b82783735c2078eac1
# Thu, 21 May 2026 23:15:58 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 21 May 2026 23:15:58 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 21 May 2026 23:15:59 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-windows-x86_64.exe
# Thu, 21 May 2026 23:16:00 GMT
ENV DOCKER_COMPOSE_SHA256=e1a8faff28c7433635201a2222171b727f33ecdb0ed367e54d162d00432f39aa
# Thu, 21 May 2026 23:16:10 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f787ad06f38db673c3d304f21c09a82ff9a1ced32062515ea52fdb0383457b24`  
		Last Modified: Tue, 12 May 2026 18:03:01 GMT  
		Size: 682.9 MB (682882530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c26092efbc05ba0447d81394df46314e3b86ab224685126b2d6dfd994d4dc11`  
		Last Modified: Thu, 21 May 2026 23:16:20 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83ade171b063bb36658cc0d1e2c9c6cb333ea25a3ad1e4129615adf825b64a46`  
		Last Modified: Thu, 21 May 2026 23:16:20 GMT  
		Size: 406.4 KB (406376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78577312456309bc4fe740995c1663317c15ecc17bcedded51adf9a9982366ca`  
		Last Modified: Thu, 21 May 2026 23:16:18 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee76c01ce753f169a4b6e55abafceb2769603948efcc72907de3e6aeb33cce42`  
		Last Modified: Thu, 21 May 2026 23:16:18 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc27681d28a3246dcf30c481b3852d6dbdc170d9cf5b284e019a90ade4d9cee8`  
		Last Modified: Thu, 21 May 2026 23:16:21 GMT  
		Size: 20.3 MB (20271957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c75db7b4635a1d76c37b80319e3dd1bdff20dd7ef77265097ecdb2861b340b99`  
		Last Modified: Thu, 21 May 2026 23:16:17 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48d982239ff1380cf0818ab9cc60083eac7f15cd44054f9f67433be9035d8a31`  
		Last Modified: Thu, 21 May 2026 23:16:17 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c096a591d4ea5f003d7be2a803cf5e81d42655e886b4df3ea31db5ab4f1289f`  
		Last Modified: Thu, 21 May 2026 23:16:17 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f795f325466c0a11f5a6c88330d8ab8b3fcad025e8fc95a56b3cc2d15f7884bb`  
		Last Modified: Thu, 21 May 2026 23:16:32 GMT  
		Size: 23.9 MB (23933638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b824c613a9ba32b1fcec65a639d38947346d62eddad555e9a7e295010f6937d`  
		Last Modified: Thu, 21 May 2026 23:16:15 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62db1e13ba58abbe1229ca941f68bceaa49a84ce729b12c843e3c1914052407d`  
		Last Modified: Thu, 21 May 2026 23:16:15 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7286144ed984b89e44b176cd42f189f5d30dc6bdd1357032bbb549bb0c96975`  
		Last Modified: Thu, 21 May 2026 23:16:15 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8922b65b3736da43bcb9ea86b5abf5ea19ee56a9c642200696decef2214beb0`  
		Last Modified: Thu, 21 May 2026 23:16:17 GMT  
		Size: 12.1 MB (12118551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:29.5-windowsservercore` - windows version 10.0.20348.5139; amd64

```console
$ docker pull docker@sha256:fecc0a5137c67dad8b14e94db06043867e6b74bb784840642f699cfd8d9abe16
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2179150500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52496b21f2e24bac1a6601b61b2de6417374b43f89a6f9cfd8eefedf65fdd4a7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Thu, 21 May 2026 23:37:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 21 May 2026 23:38:14 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 21 May 2026 23:38:15 GMT
ENV DOCKER_VERSION=29.5.2
# Thu, 21 May 2026 23:38:17 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.5.2.zip
# Thu, 21 May 2026 23:38:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 21 May 2026 23:38:44 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 21 May 2026 23:38:45 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.windows-amd64.exe
# Thu, 21 May 2026 23:38:46 GMT
ENV DOCKER_BUILDX_SHA256=41e1b3fff6541d5f5febb18ff4c9108bec30afd7bf9133b82783735c2078eac1
# Thu, 21 May 2026 23:39:10 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 21 May 2026 23:39:11 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 21 May 2026 23:39:12 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-windows-x86_64.exe
# Thu, 21 May 2026 23:39:13 GMT
ENV DOCKER_COMPOSE_SHA256=e1a8faff28c7433635201a2222171b727f33ecdb0ed367e54d162d00432f39aa
# Thu, 21 May 2026 23:39:31 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857865ad3eca4da109d969134a9cab7225d9de49597914ae325d43661900f513`  
		Last Modified: Tue, 12 May 2026 17:34:16 GMT  
		Size: 633.4 MB (633401492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17fd8e1d39e88259a0e6383034d2a7ad6d90356547cec5bbbf94f3a3e0afc763`  
		Last Modified: Thu, 21 May 2026 23:39:40 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1756702264897e3d6bb006dbce5e5260ae7bc8fa54384b6a031c460ac01476e`  
		Last Modified: Thu, 21 May 2026 23:39:39 GMT  
		Size: 505.7 KB (505666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da4ab93ed88956a88f0eb095aaf8977d5b9bbba18d08b7757eb1ccff28e80d2a`  
		Last Modified: Thu, 21 May 2026 23:39:39 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c2528cc62d1c88f5003aa2f0b62055544c66be0ec0d65cf6a8550455e0747`  
		Last Modified: Thu, 21 May 2026 23:39:38 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e531632899bf060a3ff8e9b29f0c3c81b857c0b311b97f241e35d94ffe66d3cb`  
		Last Modified: Thu, 21 May 2026 23:39:41 GMT  
		Size: 20.2 MB (20231436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34d5b3db47edaa5e44e34cad2ba31b4be5c5b6c483cef5a09b33460c4747302`  
		Last Modified: Thu, 21 May 2026 23:39:37 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:751d900578d8658aa1097acdfcd5f97aff829261a5e29a8f16b2f40effa4f532`  
		Last Modified: Thu, 21 May 2026 23:39:37 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eeb843d181536cfa4d4d838d626f63e191094c2468d26f3d0330a50f2b526c4`  
		Last Modified: Thu, 21 May 2026 23:39:37 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b58742ef314900bc96dda8fc677f8a1b98faf7970eb6fa39992b3a0150a7d36`  
		Last Modified: Thu, 21 May 2026 23:39:51 GMT  
		Size: 23.9 MB (23901391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:435a34db22345529d906d3448943e90cfc37ae51e15ea8ec70cd87e01c5b16d8`  
		Last Modified: Thu, 21 May 2026 23:39:35 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1f19e0160f0c9a3c97ced5e763b905a949f0f5af2882f68638e276a43a62af`  
		Last Modified: Thu, 21 May 2026 23:39:35 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60db139392fbadfa06ac3c12862fab33f209dc6d2a7f076d7d0b52eec402dc3b`  
		Last Modified: Thu, 21 May 2026 23:39:35 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ddde0e1dba54298e42dcefa7d09742c8714bba4bc7d5a59eb1950f87975208`  
		Last Modified: Thu, 21 May 2026 23:39:37 GMT  
		Size: 12.1 MB (12079670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.5-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:45ff7aebeb53a14d066b607ae70acc6e3ca4f3cc6835a76438078df370c9857f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `docker:29.5-windowsservercore-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull docker@sha256:fecc0a5137c67dad8b14e94db06043867e6b74bb784840642f699cfd8d9abe16
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2179150500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52496b21f2e24bac1a6601b61b2de6417374b43f89a6f9cfd8eefedf65fdd4a7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Thu, 21 May 2026 23:37:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 21 May 2026 23:38:14 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 21 May 2026 23:38:15 GMT
ENV DOCKER_VERSION=29.5.2
# Thu, 21 May 2026 23:38:17 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.5.2.zip
# Thu, 21 May 2026 23:38:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 21 May 2026 23:38:44 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 21 May 2026 23:38:45 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.windows-amd64.exe
# Thu, 21 May 2026 23:38:46 GMT
ENV DOCKER_BUILDX_SHA256=41e1b3fff6541d5f5febb18ff4c9108bec30afd7bf9133b82783735c2078eac1
# Thu, 21 May 2026 23:39:10 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 21 May 2026 23:39:11 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 21 May 2026 23:39:12 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-windows-x86_64.exe
# Thu, 21 May 2026 23:39:13 GMT
ENV DOCKER_COMPOSE_SHA256=e1a8faff28c7433635201a2222171b727f33ecdb0ed367e54d162d00432f39aa
# Thu, 21 May 2026 23:39:31 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857865ad3eca4da109d969134a9cab7225d9de49597914ae325d43661900f513`  
		Last Modified: Tue, 12 May 2026 17:34:16 GMT  
		Size: 633.4 MB (633401492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17fd8e1d39e88259a0e6383034d2a7ad6d90356547cec5bbbf94f3a3e0afc763`  
		Last Modified: Thu, 21 May 2026 23:39:40 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1756702264897e3d6bb006dbce5e5260ae7bc8fa54384b6a031c460ac01476e`  
		Last Modified: Thu, 21 May 2026 23:39:39 GMT  
		Size: 505.7 KB (505666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da4ab93ed88956a88f0eb095aaf8977d5b9bbba18d08b7757eb1ccff28e80d2a`  
		Last Modified: Thu, 21 May 2026 23:39:39 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c2528cc62d1c88f5003aa2f0b62055544c66be0ec0d65cf6a8550455e0747`  
		Last Modified: Thu, 21 May 2026 23:39:38 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e531632899bf060a3ff8e9b29f0c3c81b857c0b311b97f241e35d94ffe66d3cb`  
		Last Modified: Thu, 21 May 2026 23:39:41 GMT  
		Size: 20.2 MB (20231436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34d5b3db47edaa5e44e34cad2ba31b4be5c5b6c483cef5a09b33460c4747302`  
		Last Modified: Thu, 21 May 2026 23:39:37 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:751d900578d8658aa1097acdfcd5f97aff829261a5e29a8f16b2f40effa4f532`  
		Last Modified: Thu, 21 May 2026 23:39:37 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eeb843d181536cfa4d4d838d626f63e191094c2468d26f3d0330a50f2b526c4`  
		Last Modified: Thu, 21 May 2026 23:39:37 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b58742ef314900bc96dda8fc677f8a1b98faf7970eb6fa39992b3a0150a7d36`  
		Last Modified: Thu, 21 May 2026 23:39:51 GMT  
		Size: 23.9 MB (23901391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:435a34db22345529d906d3448943e90cfc37ae51e15ea8ec70cd87e01c5b16d8`  
		Last Modified: Thu, 21 May 2026 23:39:35 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1f19e0160f0c9a3c97ced5e763b905a949f0f5af2882f68638e276a43a62af`  
		Last Modified: Thu, 21 May 2026 23:39:35 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60db139392fbadfa06ac3c12862fab33f209dc6d2a7f076d7d0b52eec402dc3b`  
		Last Modified: Thu, 21 May 2026 23:39:35 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ddde0e1dba54298e42dcefa7d09742c8714bba4bc7d5a59eb1950f87975208`  
		Last Modified: Thu, 21 May 2026 23:39:37 GMT  
		Size: 12.1 MB (12079670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.5-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:38a6d8d2632ca78eb3229980b6b255413aa7fafcf1d3ad906265d8c05df98652
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32860; amd64

### `docker:29.5-windowsservercore-ltsc2025` - windows version 10.0.26100.32860; amd64

```console
$ docker pull docker@sha256:189f1d53b9d0831a7663f55ac4dfcfe317baa879af86a90a44e1c83e9f9fbf6a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2262683896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c993dcdab4e74415b546e3486a219f555369a5b9db18c96ed98e36915f6572`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 10 May 2026 10:08:54 GMT
RUN Install update 10.0.26100.32860
# Thu, 21 May 2026 23:13:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 21 May 2026 23:15:10 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 21 May 2026 23:15:11 GMT
ENV DOCKER_VERSION=29.5.2
# Thu, 21 May 2026 23:15:13 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.5.2.zip
# Thu, 21 May 2026 23:15:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 21 May 2026 23:15:38 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 21 May 2026 23:15:39 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.windows-amd64.exe
# Thu, 21 May 2026 23:15:39 GMT
ENV DOCKER_BUILDX_SHA256=41e1b3fff6541d5f5febb18ff4c9108bec30afd7bf9133b82783735c2078eac1
# Thu, 21 May 2026 23:15:58 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 21 May 2026 23:15:58 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 21 May 2026 23:15:59 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-windows-x86_64.exe
# Thu, 21 May 2026 23:16:00 GMT
ENV DOCKER_COMPOSE_SHA256=e1a8faff28c7433635201a2222171b727f33ecdb0ed367e54d162d00432f39aa
# Thu, 21 May 2026 23:16:10 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f787ad06f38db673c3d304f21c09a82ff9a1ced32062515ea52fdb0383457b24`  
		Last Modified: Tue, 12 May 2026 18:03:01 GMT  
		Size: 682.9 MB (682882530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c26092efbc05ba0447d81394df46314e3b86ab224685126b2d6dfd994d4dc11`  
		Last Modified: Thu, 21 May 2026 23:16:20 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83ade171b063bb36658cc0d1e2c9c6cb333ea25a3ad1e4129615adf825b64a46`  
		Last Modified: Thu, 21 May 2026 23:16:20 GMT  
		Size: 406.4 KB (406376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78577312456309bc4fe740995c1663317c15ecc17bcedded51adf9a9982366ca`  
		Last Modified: Thu, 21 May 2026 23:16:18 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee76c01ce753f169a4b6e55abafceb2769603948efcc72907de3e6aeb33cce42`  
		Last Modified: Thu, 21 May 2026 23:16:18 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc27681d28a3246dcf30c481b3852d6dbdc170d9cf5b284e019a90ade4d9cee8`  
		Last Modified: Thu, 21 May 2026 23:16:21 GMT  
		Size: 20.3 MB (20271957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c75db7b4635a1d76c37b80319e3dd1bdff20dd7ef77265097ecdb2861b340b99`  
		Last Modified: Thu, 21 May 2026 23:16:17 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48d982239ff1380cf0818ab9cc60083eac7f15cd44054f9f67433be9035d8a31`  
		Last Modified: Thu, 21 May 2026 23:16:17 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c096a591d4ea5f003d7be2a803cf5e81d42655e886b4df3ea31db5ab4f1289f`  
		Last Modified: Thu, 21 May 2026 23:16:17 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f795f325466c0a11f5a6c88330d8ab8b3fcad025e8fc95a56b3cc2d15f7884bb`  
		Last Modified: Thu, 21 May 2026 23:16:32 GMT  
		Size: 23.9 MB (23933638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b824c613a9ba32b1fcec65a639d38947346d62eddad555e9a7e295010f6937d`  
		Last Modified: Thu, 21 May 2026 23:16:15 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62db1e13ba58abbe1229ca941f68bceaa49a84ce729b12c843e3c1914052407d`  
		Last Modified: Thu, 21 May 2026 23:16:15 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7286144ed984b89e44b176cd42f189f5d30dc6bdd1357032bbb549bb0c96975`  
		Last Modified: Thu, 21 May 2026 23:16:15 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8922b65b3736da43bcb9ea86b5abf5ea19ee56a9c642200696decef2214beb0`  
		Last Modified: Thu, 21 May 2026 23:16:17 GMT  
		Size: 12.1 MB (12118551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.5.2`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:29.5.2-alpine3.23`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:29.5.2-cli`

```console
$ docker pull docker@sha256:9ba8e32bfc35a2c7ae2feb1e3241b2778ae21dee80f4dcd31d04e1cfdea86ea2
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

### `docker:29.5.2-cli` - linux; amd64

```console
$ docker pull docker@sha256:ec66e6a33f2769030bf8f283b25a7ea135d770ed2c3b91c14195de0ca901e61a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.1 MB (66112304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a190ccdf9e97f139d089920e904db8c97e394f8b5f3ff536cdadeda6c821ded`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Thu, 21 May 2026 22:56:57 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 21 May 2026 22:56:57 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 21 May 2026 22:56:57 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 21 May 2026 22:56:59 GMT
ENV DOCKER_VERSION=29.5.2
# Thu, 21 May 2026 22:56:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 21 May 2026 22:56:59 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 21 May 2026 22:57:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 21 May 2026 22:57:00 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 21 May 2026 22:57:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 21 May 2026 22:57:01 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 21 May 2026 22:57:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 21 May 2026 22:57:01 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 21 May 2026 22:57:01 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 21 May 2026 22:57:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 May 2026 22:57:01 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6cf87df21c231c07f8b8d9c532474fc120946d085773fa15272382636f10b46`  
		Last Modified: Thu, 21 May 2026 22:57:08 GMT  
		Size: 8.3 MB (8311580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54392fc3db24e998571260adc7ac1a1bc098852dfeb30150218d2174da4aa929`  
		Last Modified: Thu, 21 May 2026 22:57:07 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4b052546a5d5d26f7d251d92bd155e2275ee74b4c83a5748550720fa39efe1`  
		Last Modified: Thu, 21 May 2026 22:57:08 GMT  
		Size: 19.5 MB (19549520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b2deac6c9ceba582f6a7f4a7ea2910141ba0dfcf644ee930db818a78947527a`  
		Last Modified: Thu, 21 May 2026 22:57:08 GMT  
		Size: 23.0 MB (22988915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:046b51e466e9d4d0fb090dd060997a0892b36578ab13f0153d1d61f53166d5c6`  
		Last Modified: Thu, 21 May 2026 22:57:09 GMT  
		Size: 11.4 MB (11395947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff5ffb634dd2a67009edb32be895febc923676e8dc0b94f8c857528723140ee`  
		Last Modified: Thu, 21 May 2026 22:57:09 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b162b8dd068432fdb9682bbf9fc7ecbe61c2dbbb72441a22b74a6537f7fe639`  
		Last Modified: Thu, 21 May 2026 22:57:10 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b02815b1d866ccad16190784679c75c04f712dc13f12bd8ec46cf7648796905`  
		Last Modified: Thu, 21 May 2026 22:57:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.5.2-cli` - unknown; unknown

```console
$ docker pull docker@sha256:d0c058683425ac4a4e35818c3cab8e244bf44bf5629b2606d503eab0302918c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24cd59892835a6bb71bef956c207f451b0ff4ef20ef700549178228a80696991`

```dockerfile
```

-	Layers:
	-	`sha256:e8d0f9a2c1d7978db5312a52983dc91318b6ef2d7b32afeed756151fcba3ed72`  
		Last Modified: Thu, 21 May 2026 22:57:07 GMT  
		Size: 38.1 KB (38056 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.5.2-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:1ea54fcc950d7b127dc87b88d28c747600cca8b48d8c034ecd527709330f2074
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62396270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8d2a98d406c875d3e0db6343c8b5fa56023aa689cb018d156b714f0199d7ab8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Thu, 21 May 2026 22:57:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 21 May 2026 22:57:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 21 May 2026 22:57:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 21 May 2026 22:57:14 GMT
ENV DOCKER_VERSION=29.5.2
# Thu, 21 May 2026 22:57:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 21 May 2026 22:57:14 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 21 May 2026 22:57:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 21 May 2026 22:57:17 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 21 May 2026 22:57:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 21 May 2026 22:57:18 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 21 May 2026 22:57:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 21 May 2026 22:57:19 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 21 May 2026 22:57:19 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 21 May 2026 22:57:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 May 2026 22:57:19 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:686f209ff6de10676a89d77e3e8a6fab30545d5720ccf9054ee0d1b26e38b43a`  
		Last Modified: Thu, 21 May 2026 22:57:25 GMT  
		Size: 8.2 MB (8211872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc482e1b01e42c3c70b99620637bf883c5da46458460af902ddff0ac829fe8be`  
		Last Modified: Thu, 21 May 2026 22:57:24 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6ca55f6f19c616ff991f7a3db821aff9610c17f90b38f47cbd8f4524f46539`  
		Last Modified: Thu, 21 May 2026 22:57:25 GMT  
		Size: 18.2 MB (18183161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83229a063dcdaa05d49b47a377f6266b68058c99c6e0d8dfdc2a7d84012787eb`  
		Last Modified: Thu, 21 May 2026 22:57:25 GMT  
		Size: 21.6 MB (21614627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:940f9c6bb6e92b7182721c14634a231b228afd28fe04caffd78841f7dd24411b`  
		Last Modified: Thu, 21 May 2026 22:57:26 GMT  
		Size: 10.8 MB (10812594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c13701af534883715f5b32ba09cbb6f13feb5042a866f77e574177b03153cb1`  
		Last Modified: Thu, 21 May 2026 22:57:27 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5827618b0a4b3c9209e2ce38a22a9c7e3bf8dc8d55f12ece8a624cec59ca0c0`  
		Last Modified: Thu, 21 May 2026 22:57:27 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:156a2ca1e461bbe26a51cde3454797f4bb525e545ae12a790eb2c832fa3cd344`  
		Last Modified: Thu, 21 May 2026 22:57:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.5.2-cli` - unknown; unknown

```console
$ docker pull docker@sha256:04ebdfb0eda18157d342b7fb08c62391f19045358bdd9d13363d75b2bf405b48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c878c65dd1bf46ceb912d86983dbbb6747bbc0d9f04388340d7ff40ab6a955b5`

```dockerfile
```

-	Layers:
	-	`sha256:a18fb0bd08433a7ea29e919c067320a3a5064d90b3bf6926746198a604fa7c2e`  
		Last Modified: Thu, 21 May 2026 22:57:24 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.5.2-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:4efa5b423f6548c5521b0093e3276bff164af4e70d51c1368309a76e916622e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61378438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d52d0f5e6c9123362925f36aa888038a8dd446e137138fb8463b681a0bc5dff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Thu, 21 May 2026 22:57:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 21 May 2026 22:57:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 21 May 2026 22:57:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 21 May 2026 22:57:19 GMT
ENV DOCKER_VERSION=29.5.2
# Thu, 21 May 2026 22:57:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 21 May 2026 22:57:19 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 21 May 2026 22:57:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 21 May 2026 22:57:21 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 21 May 2026 22:57:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 21 May 2026 22:57:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 21 May 2026 22:57:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 21 May 2026 22:57:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 21 May 2026 22:57:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 21 May 2026 22:57:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 May 2026 22:57:22 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f52861283d77a40b5946e65011de57aef34bc9327b32604f88a677e6f2cb2a`  
		Last Modified: Thu, 21 May 2026 22:57:29 GMT  
		Size: 7.5 MB (7520603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe77c7d8ef7315ec44519db3cec2d9d47ed19881a859e1f59af47b6ee930987`  
		Last Modified: Thu, 21 May 2026 22:57:29 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb66512e1233e73a0972411ebf4f8c344ca4a394da4d49e6b222234bb111c827`  
		Last Modified: Thu, 21 May 2026 22:57:30 GMT  
		Size: 18.2 MB (18172264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa22bb61dc858338f97353ad033e1a3dfeaedd00a1bc504c85cb83d1d1e1066`  
		Last Modified: Thu, 21 May 2026 22:57:30 GMT  
		Size: 21.6 MB (21600713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36a896b5ff64585ed1221a91d5f2f671787cd3897f86991c0f6fe8525f7d75c0`  
		Last Modified: Thu, 21 May 2026 22:57:30 GMT  
		Size: 10.8 MB (10799582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce88e69f3e7c7ac17129a6b4b87aad6b39a3a2861c81d554e406b2547561f66`  
		Last Modified: Thu, 21 May 2026 22:57:30 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5758ccda3473178260da62e4ab7c4fa36a8dfc1c4ef7d4fed06e0ea0fb533c09`  
		Last Modified: Thu, 21 May 2026 22:57:31 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e4468a079208fc160ee3dd1c7df3de47f866b433f720289671fd2ab2bf8a6d`  
		Last Modified: Thu, 21 May 2026 22:57:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.5.2-cli` - unknown; unknown

```console
$ docker pull docker@sha256:73a5dfa31ffac43a7e451c867bb1707eb46361077e17b338feea6d1cfe16074c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:213b655767f4e7e1aa870b4cdd07817a9d99c15bc554800b7bf98c33cfb92cc9`

```dockerfile
```

-	Layers:
	-	`sha256:88b55d2936f52c50f0f1b5bdd99b1c08534f7a93ef0c66f562f45ef6679cac29`  
		Last Modified: Thu, 21 May 2026 22:57:28 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.5.2-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:1c27de1f16ee894e6389586d8b58391f4b941f768cb5520cd2970c72d38a8e84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61750058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:156869ccb322d51e7560b80292b10dfaa423516486f6683494060b76d38dabcc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Thu, 21 May 2026 22:56:32 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 21 May 2026 22:56:32 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 21 May 2026 22:56:32 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 21 May 2026 22:56:34 GMT
ENV DOCKER_VERSION=29.5.2
# Thu, 21 May 2026 22:56:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 21 May 2026 22:56:34 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 21 May 2026 22:56:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 21 May 2026 22:56:35 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 21 May 2026 22:56:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 21 May 2026 22:56:36 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 21 May 2026 22:56:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 21 May 2026 22:56:36 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 21 May 2026 22:56:36 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 21 May 2026 22:56:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 May 2026 22:56:36 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae988a6da12e07a4495206223708dfa12193c715305da0959269e07cfe0883c`  
		Last Modified: Thu, 21 May 2026 22:56:42 GMT  
		Size: 8.4 MB (8368391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad63753001c8116da8d4078088f8c226c9d2d5ebb32c543695bad3dfd05cb848`  
		Last Modified: Thu, 21 May 2026 22:56:42 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1523489b9bcf5899f4ec01d3ea4b3b09a7f11127bd6cfac3ad985d4e121a917`  
		Last Modified: Thu, 21 May 2026 22:56:43 GMT  
		Size: 18.0 MB (18003804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4276c1b3c4ca523a976f2b634bcd7b921a29dbff4274ac9aa9cc1e68ed96f93`  
		Last Modified: Thu, 21 May 2026 22:56:43 GMT  
		Size: 20.8 MB (20815981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e3a6fedf4004b1aba4e7b35c15a75f4e30fd0ae9d353199415f18fd99a7cf8`  
		Last Modified: Thu, 21 May 2026 22:56:43 GMT  
		Size: 10.4 MB (10359860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37af9029ae6a6376f88d713b9b54fb69ece2959cf06985f67d3905c6ef36739`  
		Last Modified: Thu, 21 May 2026 22:56:44 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56df60bc257eb03677643450dfa9477ebdad3b524820a408218637a85932c45d`  
		Last Modified: Thu, 21 May 2026 22:56:44 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe07c252ff4b96737716f829e1e8ff46a81625412f850d98480be21cf51f845`  
		Last Modified: Thu, 21 May 2026 22:56:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.5.2-cli` - unknown; unknown

```console
$ docker pull docker@sha256:a8dedaaa0ddf7100fc1cf4d4aee8dec52a0bd683ada897dc62942f5c0b88d846
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30bdb74e1af7301d0ea10753180b6ea04b819ea07777e30c7cc70392aefbb2db`

```dockerfile
```

-	Layers:
	-	`sha256:ddd2ae6062cdfd1652888a3cbd3bdc652070dde80dc25a31826cfb552cb05649`  
		Last Modified: Thu, 21 May 2026 22:56:42 GMT  
		Size: 38.3 KB (38262 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.5.2-cli-alpine3.23`

```console
$ docker pull docker@sha256:9ba8e32bfc35a2c7ae2feb1e3241b2778ae21dee80f4dcd31d04e1cfdea86ea2
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

### `docker:29.5.2-cli-alpine3.23` - linux; amd64

```console
$ docker pull docker@sha256:ec66e6a33f2769030bf8f283b25a7ea135d770ed2c3b91c14195de0ca901e61a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.1 MB (66112304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a190ccdf9e97f139d089920e904db8c97e394f8b5f3ff536cdadeda6c821ded`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Thu, 21 May 2026 22:56:57 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 21 May 2026 22:56:57 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 21 May 2026 22:56:57 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 21 May 2026 22:56:59 GMT
ENV DOCKER_VERSION=29.5.2
# Thu, 21 May 2026 22:56:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 21 May 2026 22:56:59 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 21 May 2026 22:57:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 21 May 2026 22:57:00 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 21 May 2026 22:57:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 21 May 2026 22:57:01 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 21 May 2026 22:57:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 21 May 2026 22:57:01 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 21 May 2026 22:57:01 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 21 May 2026 22:57:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 May 2026 22:57:01 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6cf87df21c231c07f8b8d9c532474fc120946d085773fa15272382636f10b46`  
		Last Modified: Thu, 21 May 2026 22:57:08 GMT  
		Size: 8.3 MB (8311580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54392fc3db24e998571260adc7ac1a1bc098852dfeb30150218d2174da4aa929`  
		Last Modified: Thu, 21 May 2026 22:57:07 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4b052546a5d5d26f7d251d92bd155e2275ee74b4c83a5748550720fa39efe1`  
		Last Modified: Thu, 21 May 2026 22:57:08 GMT  
		Size: 19.5 MB (19549520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b2deac6c9ceba582f6a7f4a7ea2910141ba0dfcf644ee930db818a78947527a`  
		Last Modified: Thu, 21 May 2026 22:57:08 GMT  
		Size: 23.0 MB (22988915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:046b51e466e9d4d0fb090dd060997a0892b36578ab13f0153d1d61f53166d5c6`  
		Last Modified: Thu, 21 May 2026 22:57:09 GMT  
		Size: 11.4 MB (11395947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff5ffb634dd2a67009edb32be895febc923676e8dc0b94f8c857528723140ee`  
		Last Modified: Thu, 21 May 2026 22:57:09 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b162b8dd068432fdb9682bbf9fc7ecbe61c2dbbb72441a22b74a6537f7fe639`  
		Last Modified: Thu, 21 May 2026 22:57:10 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b02815b1d866ccad16190784679c75c04f712dc13f12bd8ec46cf7648796905`  
		Last Modified: Thu, 21 May 2026 22:57:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.5.2-cli-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:d0c058683425ac4a4e35818c3cab8e244bf44bf5629b2606d503eab0302918c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24cd59892835a6bb71bef956c207f451b0ff4ef20ef700549178228a80696991`

```dockerfile
```

-	Layers:
	-	`sha256:e8d0f9a2c1d7978db5312a52983dc91318b6ef2d7b32afeed756151fcba3ed72`  
		Last Modified: Thu, 21 May 2026 22:57:07 GMT  
		Size: 38.1 KB (38056 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.5.2-cli-alpine3.23` - linux; arm variant v6

```console
$ docker pull docker@sha256:1ea54fcc950d7b127dc87b88d28c747600cca8b48d8c034ecd527709330f2074
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62396270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8d2a98d406c875d3e0db6343c8b5fa56023aa689cb018d156b714f0199d7ab8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Thu, 21 May 2026 22:57:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 21 May 2026 22:57:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 21 May 2026 22:57:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 21 May 2026 22:57:14 GMT
ENV DOCKER_VERSION=29.5.2
# Thu, 21 May 2026 22:57:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 21 May 2026 22:57:14 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 21 May 2026 22:57:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 21 May 2026 22:57:17 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 21 May 2026 22:57:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 21 May 2026 22:57:18 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 21 May 2026 22:57:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 21 May 2026 22:57:19 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 21 May 2026 22:57:19 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 21 May 2026 22:57:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 May 2026 22:57:19 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:686f209ff6de10676a89d77e3e8a6fab30545d5720ccf9054ee0d1b26e38b43a`  
		Last Modified: Thu, 21 May 2026 22:57:25 GMT  
		Size: 8.2 MB (8211872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc482e1b01e42c3c70b99620637bf883c5da46458460af902ddff0ac829fe8be`  
		Last Modified: Thu, 21 May 2026 22:57:24 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6ca55f6f19c616ff991f7a3db821aff9610c17f90b38f47cbd8f4524f46539`  
		Last Modified: Thu, 21 May 2026 22:57:25 GMT  
		Size: 18.2 MB (18183161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83229a063dcdaa05d49b47a377f6266b68058c99c6e0d8dfdc2a7d84012787eb`  
		Last Modified: Thu, 21 May 2026 22:57:25 GMT  
		Size: 21.6 MB (21614627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:940f9c6bb6e92b7182721c14634a231b228afd28fe04caffd78841f7dd24411b`  
		Last Modified: Thu, 21 May 2026 22:57:26 GMT  
		Size: 10.8 MB (10812594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c13701af534883715f5b32ba09cbb6f13feb5042a866f77e574177b03153cb1`  
		Last Modified: Thu, 21 May 2026 22:57:27 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5827618b0a4b3c9209e2ce38a22a9c7e3bf8dc8d55f12ece8a624cec59ca0c0`  
		Last Modified: Thu, 21 May 2026 22:57:27 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:156a2ca1e461bbe26a51cde3454797f4bb525e545ae12a790eb2c832fa3cd344`  
		Last Modified: Thu, 21 May 2026 22:57:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.5.2-cli-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:04ebdfb0eda18157d342b7fb08c62391f19045358bdd9d13363d75b2bf405b48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c878c65dd1bf46ceb912d86983dbbb6747bbc0d9f04388340d7ff40ab6a955b5`

```dockerfile
```

-	Layers:
	-	`sha256:a18fb0bd08433a7ea29e919c067320a3a5064d90b3bf6926746198a604fa7c2e`  
		Last Modified: Thu, 21 May 2026 22:57:24 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.5.2-cli-alpine3.23` - linux; arm variant v7

```console
$ docker pull docker@sha256:4efa5b423f6548c5521b0093e3276bff164af4e70d51c1368309a76e916622e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61378438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d52d0f5e6c9123362925f36aa888038a8dd446e137138fb8463b681a0bc5dff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Thu, 21 May 2026 22:57:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 21 May 2026 22:57:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 21 May 2026 22:57:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 21 May 2026 22:57:19 GMT
ENV DOCKER_VERSION=29.5.2
# Thu, 21 May 2026 22:57:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 21 May 2026 22:57:19 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 21 May 2026 22:57:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 21 May 2026 22:57:21 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 21 May 2026 22:57:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 21 May 2026 22:57:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 21 May 2026 22:57:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 21 May 2026 22:57:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 21 May 2026 22:57:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 21 May 2026 22:57:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 May 2026 22:57:22 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f52861283d77a40b5946e65011de57aef34bc9327b32604f88a677e6f2cb2a`  
		Last Modified: Thu, 21 May 2026 22:57:29 GMT  
		Size: 7.5 MB (7520603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe77c7d8ef7315ec44519db3cec2d9d47ed19881a859e1f59af47b6ee930987`  
		Last Modified: Thu, 21 May 2026 22:57:29 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb66512e1233e73a0972411ebf4f8c344ca4a394da4d49e6b222234bb111c827`  
		Last Modified: Thu, 21 May 2026 22:57:30 GMT  
		Size: 18.2 MB (18172264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa22bb61dc858338f97353ad033e1a3dfeaedd00a1bc504c85cb83d1d1e1066`  
		Last Modified: Thu, 21 May 2026 22:57:30 GMT  
		Size: 21.6 MB (21600713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36a896b5ff64585ed1221a91d5f2f671787cd3897f86991c0f6fe8525f7d75c0`  
		Last Modified: Thu, 21 May 2026 22:57:30 GMT  
		Size: 10.8 MB (10799582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce88e69f3e7c7ac17129a6b4b87aad6b39a3a2861c81d554e406b2547561f66`  
		Last Modified: Thu, 21 May 2026 22:57:30 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5758ccda3473178260da62e4ab7c4fa36a8dfc1c4ef7d4fed06e0ea0fb533c09`  
		Last Modified: Thu, 21 May 2026 22:57:31 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e4468a079208fc160ee3dd1c7df3de47f866b433f720289671fd2ab2bf8a6d`  
		Last Modified: Thu, 21 May 2026 22:57:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.5.2-cli-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:73a5dfa31ffac43a7e451c867bb1707eb46361077e17b338feea6d1cfe16074c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:213b655767f4e7e1aa870b4cdd07817a9d99c15bc554800b7bf98c33cfb92cc9`

```dockerfile
```

-	Layers:
	-	`sha256:88b55d2936f52c50f0f1b5bdd99b1c08534f7a93ef0c66f562f45ef6679cac29`  
		Last Modified: Thu, 21 May 2026 22:57:28 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.5.2-cli-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:1c27de1f16ee894e6389586d8b58391f4b941f768cb5520cd2970c72d38a8e84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61750058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:156869ccb322d51e7560b80292b10dfaa423516486f6683494060b76d38dabcc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Thu, 21 May 2026 22:56:32 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 21 May 2026 22:56:32 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 21 May 2026 22:56:32 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 21 May 2026 22:56:34 GMT
ENV DOCKER_VERSION=29.5.2
# Thu, 21 May 2026 22:56:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 21 May 2026 22:56:34 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 21 May 2026 22:56:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 21 May 2026 22:56:35 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 21 May 2026 22:56:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 21 May 2026 22:56:36 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 21 May 2026 22:56:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 21 May 2026 22:56:36 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 21 May 2026 22:56:36 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 21 May 2026 22:56:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 May 2026 22:56:36 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae988a6da12e07a4495206223708dfa12193c715305da0959269e07cfe0883c`  
		Last Modified: Thu, 21 May 2026 22:56:42 GMT  
		Size: 8.4 MB (8368391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad63753001c8116da8d4078088f8c226c9d2d5ebb32c543695bad3dfd05cb848`  
		Last Modified: Thu, 21 May 2026 22:56:42 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1523489b9bcf5899f4ec01d3ea4b3b09a7f11127bd6cfac3ad985d4e121a917`  
		Last Modified: Thu, 21 May 2026 22:56:43 GMT  
		Size: 18.0 MB (18003804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4276c1b3c4ca523a976f2b634bcd7b921a29dbff4274ac9aa9cc1e68ed96f93`  
		Last Modified: Thu, 21 May 2026 22:56:43 GMT  
		Size: 20.8 MB (20815981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e3a6fedf4004b1aba4e7b35c15a75f4e30fd0ae9d353199415f18fd99a7cf8`  
		Last Modified: Thu, 21 May 2026 22:56:43 GMT  
		Size: 10.4 MB (10359860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37af9029ae6a6376f88d713b9b54fb69ece2959cf06985f67d3905c6ef36739`  
		Last Modified: Thu, 21 May 2026 22:56:44 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56df60bc257eb03677643450dfa9477ebdad3b524820a408218637a85932c45d`  
		Last Modified: Thu, 21 May 2026 22:56:44 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe07c252ff4b96737716f829e1e8ff46a81625412f850d98480be21cf51f845`  
		Last Modified: Thu, 21 May 2026 22:56:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.5.2-cli-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:a8dedaaa0ddf7100fc1cf4d4aee8dec52a0bd683ada897dc62942f5c0b88d846
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30bdb74e1af7301d0ea10753180b6ea04b819ea07777e30c7cc70392aefbb2db`

```dockerfile
```

-	Layers:
	-	`sha256:ddd2ae6062cdfd1652888a3cbd3bdc652070dde80dc25a31826cfb552cb05649`  
		Last Modified: Thu, 21 May 2026 22:56:42 GMT  
		Size: 38.3 KB (38262 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.5.2-dind`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:29.5.2-dind-alpine3.23`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:29.5.2-dind-rootless`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:29.5.2-windowsservercore`

```console
$ docker pull docker@sha256:76a2595299d5d831461bbff176d00c8005cc1b58a48fe70127d90155b250253f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32860; amd64
	-	windows version 10.0.20348.5139; amd64

### `docker:29.5.2-windowsservercore` - windows version 10.0.26100.32860; amd64

```console
$ docker pull docker@sha256:189f1d53b9d0831a7663f55ac4dfcfe317baa879af86a90a44e1c83e9f9fbf6a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2262683896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c993dcdab4e74415b546e3486a219f555369a5b9db18c96ed98e36915f6572`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 10 May 2026 10:08:54 GMT
RUN Install update 10.0.26100.32860
# Thu, 21 May 2026 23:13:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 21 May 2026 23:15:10 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 21 May 2026 23:15:11 GMT
ENV DOCKER_VERSION=29.5.2
# Thu, 21 May 2026 23:15:13 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.5.2.zip
# Thu, 21 May 2026 23:15:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 21 May 2026 23:15:38 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 21 May 2026 23:15:39 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.windows-amd64.exe
# Thu, 21 May 2026 23:15:39 GMT
ENV DOCKER_BUILDX_SHA256=41e1b3fff6541d5f5febb18ff4c9108bec30afd7bf9133b82783735c2078eac1
# Thu, 21 May 2026 23:15:58 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 21 May 2026 23:15:58 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 21 May 2026 23:15:59 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-windows-x86_64.exe
# Thu, 21 May 2026 23:16:00 GMT
ENV DOCKER_COMPOSE_SHA256=e1a8faff28c7433635201a2222171b727f33ecdb0ed367e54d162d00432f39aa
# Thu, 21 May 2026 23:16:10 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f787ad06f38db673c3d304f21c09a82ff9a1ced32062515ea52fdb0383457b24`  
		Last Modified: Tue, 12 May 2026 18:03:01 GMT  
		Size: 682.9 MB (682882530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c26092efbc05ba0447d81394df46314e3b86ab224685126b2d6dfd994d4dc11`  
		Last Modified: Thu, 21 May 2026 23:16:20 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83ade171b063bb36658cc0d1e2c9c6cb333ea25a3ad1e4129615adf825b64a46`  
		Last Modified: Thu, 21 May 2026 23:16:20 GMT  
		Size: 406.4 KB (406376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78577312456309bc4fe740995c1663317c15ecc17bcedded51adf9a9982366ca`  
		Last Modified: Thu, 21 May 2026 23:16:18 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee76c01ce753f169a4b6e55abafceb2769603948efcc72907de3e6aeb33cce42`  
		Last Modified: Thu, 21 May 2026 23:16:18 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc27681d28a3246dcf30c481b3852d6dbdc170d9cf5b284e019a90ade4d9cee8`  
		Last Modified: Thu, 21 May 2026 23:16:21 GMT  
		Size: 20.3 MB (20271957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c75db7b4635a1d76c37b80319e3dd1bdff20dd7ef77265097ecdb2861b340b99`  
		Last Modified: Thu, 21 May 2026 23:16:17 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48d982239ff1380cf0818ab9cc60083eac7f15cd44054f9f67433be9035d8a31`  
		Last Modified: Thu, 21 May 2026 23:16:17 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c096a591d4ea5f003d7be2a803cf5e81d42655e886b4df3ea31db5ab4f1289f`  
		Last Modified: Thu, 21 May 2026 23:16:17 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f795f325466c0a11f5a6c88330d8ab8b3fcad025e8fc95a56b3cc2d15f7884bb`  
		Last Modified: Thu, 21 May 2026 23:16:32 GMT  
		Size: 23.9 MB (23933638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b824c613a9ba32b1fcec65a639d38947346d62eddad555e9a7e295010f6937d`  
		Last Modified: Thu, 21 May 2026 23:16:15 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62db1e13ba58abbe1229ca941f68bceaa49a84ce729b12c843e3c1914052407d`  
		Last Modified: Thu, 21 May 2026 23:16:15 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7286144ed984b89e44b176cd42f189f5d30dc6bdd1357032bbb549bb0c96975`  
		Last Modified: Thu, 21 May 2026 23:16:15 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8922b65b3736da43bcb9ea86b5abf5ea19ee56a9c642200696decef2214beb0`  
		Last Modified: Thu, 21 May 2026 23:16:17 GMT  
		Size: 12.1 MB (12118551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:29.5.2-windowsservercore` - windows version 10.0.20348.5139; amd64

```console
$ docker pull docker@sha256:fecc0a5137c67dad8b14e94db06043867e6b74bb784840642f699cfd8d9abe16
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2179150500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52496b21f2e24bac1a6601b61b2de6417374b43f89a6f9cfd8eefedf65fdd4a7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Thu, 21 May 2026 23:37:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 21 May 2026 23:38:14 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 21 May 2026 23:38:15 GMT
ENV DOCKER_VERSION=29.5.2
# Thu, 21 May 2026 23:38:17 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.5.2.zip
# Thu, 21 May 2026 23:38:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 21 May 2026 23:38:44 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 21 May 2026 23:38:45 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.windows-amd64.exe
# Thu, 21 May 2026 23:38:46 GMT
ENV DOCKER_BUILDX_SHA256=41e1b3fff6541d5f5febb18ff4c9108bec30afd7bf9133b82783735c2078eac1
# Thu, 21 May 2026 23:39:10 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 21 May 2026 23:39:11 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 21 May 2026 23:39:12 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-windows-x86_64.exe
# Thu, 21 May 2026 23:39:13 GMT
ENV DOCKER_COMPOSE_SHA256=e1a8faff28c7433635201a2222171b727f33ecdb0ed367e54d162d00432f39aa
# Thu, 21 May 2026 23:39:31 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857865ad3eca4da109d969134a9cab7225d9de49597914ae325d43661900f513`  
		Last Modified: Tue, 12 May 2026 17:34:16 GMT  
		Size: 633.4 MB (633401492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17fd8e1d39e88259a0e6383034d2a7ad6d90356547cec5bbbf94f3a3e0afc763`  
		Last Modified: Thu, 21 May 2026 23:39:40 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1756702264897e3d6bb006dbce5e5260ae7bc8fa54384b6a031c460ac01476e`  
		Last Modified: Thu, 21 May 2026 23:39:39 GMT  
		Size: 505.7 KB (505666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da4ab93ed88956a88f0eb095aaf8977d5b9bbba18d08b7757eb1ccff28e80d2a`  
		Last Modified: Thu, 21 May 2026 23:39:39 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c2528cc62d1c88f5003aa2f0b62055544c66be0ec0d65cf6a8550455e0747`  
		Last Modified: Thu, 21 May 2026 23:39:38 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e531632899bf060a3ff8e9b29f0c3c81b857c0b311b97f241e35d94ffe66d3cb`  
		Last Modified: Thu, 21 May 2026 23:39:41 GMT  
		Size: 20.2 MB (20231436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34d5b3db47edaa5e44e34cad2ba31b4be5c5b6c483cef5a09b33460c4747302`  
		Last Modified: Thu, 21 May 2026 23:39:37 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:751d900578d8658aa1097acdfcd5f97aff829261a5e29a8f16b2f40effa4f532`  
		Last Modified: Thu, 21 May 2026 23:39:37 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eeb843d181536cfa4d4d838d626f63e191094c2468d26f3d0330a50f2b526c4`  
		Last Modified: Thu, 21 May 2026 23:39:37 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b58742ef314900bc96dda8fc677f8a1b98faf7970eb6fa39992b3a0150a7d36`  
		Last Modified: Thu, 21 May 2026 23:39:51 GMT  
		Size: 23.9 MB (23901391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:435a34db22345529d906d3448943e90cfc37ae51e15ea8ec70cd87e01c5b16d8`  
		Last Modified: Thu, 21 May 2026 23:39:35 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1f19e0160f0c9a3c97ced5e763b905a949f0f5af2882f68638e276a43a62af`  
		Last Modified: Thu, 21 May 2026 23:39:35 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60db139392fbadfa06ac3c12862fab33f209dc6d2a7f076d7d0b52eec402dc3b`  
		Last Modified: Thu, 21 May 2026 23:39:35 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ddde0e1dba54298e42dcefa7d09742c8714bba4bc7d5a59eb1950f87975208`  
		Last Modified: Thu, 21 May 2026 23:39:37 GMT  
		Size: 12.1 MB (12079670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.5.2-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:45ff7aebeb53a14d066b607ae70acc6e3ca4f3cc6835a76438078df370c9857f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `docker:29.5.2-windowsservercore-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull docker@sha256:fecc0a5137c67dad8b14e94db06043867e6b74bb784840642f699cfd8d9abe16
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2179150500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52496b21f2e24bac1a6601b61b2de6417374b43f89a6f9cfd8eefedf65fdd4a7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Thu, 21 May 2026 23:37:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 21 May 2026 23:38:14 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 21 May 2026 23:38:15 GMT
ENV DOCKER_VERSION=29.5.2
# Thu, 21 May 2026 23:38:17 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.5.2.zip
# Thu, 21 May 2026 23:38:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 21 May 2026 23:38:44 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 21 May 2026 23:38:45 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.windows-amd64.exe
# Thu, 21 May 2026 23:38:46 GMT
ENV DOCKER_BUILDX_SHA256=41e1b3fff6541d5f5febb18ff4c9108bec30afd7bf9133b82783735c2078eac1
# Thu, 21 May 2026 23:39:10 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 21 May 2026 23:39:11 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 21 May 2026 23:39:12 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-windows-x86_64.exe
# Thu, 21 May 2026 23:39:13 GMT
ENV DOCKER_COMPOSE_SHA256=e1a8faff28c7433635201a2222171b727f33ecdb0ed367e54d162d00432f39aa
# Thu, 21 May 2026 23:39:31 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857865ad3eca4da109d969134a9cab7225d9de49597914ae325d43661900f513`  
		Last Modified: Tue, 12 May 2026 17:34:16 GMT  
		Size: 633.4 MB (633401492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17fd8e1d39e88259a0e6383034d2a7ad6d90356547cec5bbbf94f3a3e0afc763`  
		Last Modified: Thu, 21 May 2026 23:39:40 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1756702264897e3d6bb006dbce5e5260ae7bc8fa54384b6a031c460ac01476e`  
		Last Modified: Thu, 21 May 2026 23:39:39 GMT  
		Size: 505.7 KB (505666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da4ab93ed88956a88f0eb095aaf8977d5b9bbba18d08b7757eb1ccff28e80d2a`  
		Last Modified: Thu, 21 May 2026 23:39:39 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c2528cc62d1c88f5003aa2f0b62055544c66be0ec0d65cf6a8550455e0747`  
		Last Modified: Thu, 21 May 2026 23:39:38 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e531632899bf060a3ff8e9b29f0c3c81b857c0b311b97f241e35d94ffe66d3cb`  
		Last Modified: Thu, 21 May 2026 23:39:41 GMT  
		Size: 20.2 MB (20231436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34d5b3db47edaa5e44e34cad2ba31b4be5c5b6c483cef5a09b33460c4747302`  
		Last Modified: Thu, 21 May 2026 23:39:37 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:751d900578d8658aa1097acdfcd5f97aff829261a5e29a8f16b2f40effa4f532`  
		Last Modified: Thu, 21 May 2026 23:39:37 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eeb843d181536cfa4d4d838d626f63e191094c2468d26f3d0330a50f2b526c4`  
		Last Modified: Thu, 21 May 2026 23:39:37 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b58742ef314900bc96dda8fc677f8a1b98faf7970eb6fa39992b3a0150a7d36`  
		Last Modified: Thu, 21 May 2026 23:39:51 GMT  
		Size: 23.9 MB (23901391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:435a34db22345529d906d3448943e90cfc37ae51e15ea8ec70cd87e01c5b16d8`  
		Last Modified: Thu, 21 May 2026 23:39:35 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1f19e0160f0c9a3c97ced5e763b905a949f0f5af2882f68638e276a43a62af`  
		Last Modified: Thu, 21 May 2026 23:39:35 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60db139392fbadfa06ac3c12862fab33f209dc6d2a7f076d7d0b52eec402dc3b`  
		Last Modified: Thu, 21 May 2026 23:39:35 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ddde0e1dba54298e42dcefa7d09742c8714bba4bc7d5a59eb1950f87975208`  
		Last Modified: Thu, 21 May 2026 23:39:37 GMT  
		Size: 12.1 MB (12079670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.5.2-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:38a6d8d2632ca78eb3229980b6b255413aa7fafcf1d3ad906265d8c05df98652
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32860; amd64

### `docker:29.5.2-windowsservercore-ltsc2025` - windows version 10.0.26100.32860; amd64

```console
$ docker pull docker@sha256:189f1d53b9d0831a7663f55ac4dfcfe317baa879af86a90a44e1c83e9f9fbf6a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2262683896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c993dcdab4e74415b546e3486a219f555369a5b9db18c96ed98e36915f6572`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 10 May 2026 10:08:54 GMT
RUN Install update 10.0.26100.32860
# Thu, 21 May 2026 23:13:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 21 May 2026 23:15:10 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 21 May 2026 23:15:11 GMT
ENV DOCKER_VERSION=29.5.2
# Thu, 21 May 2026 23:15:13 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.5.2.zip
# Thu, 21 May 2026 23:15:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 21 May 2026 23:15:38 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 21 May 2026 23:15:39 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.windows-amd64.exe
# Thu, 21 May 2026 23:15:39 GMT
ENV DOCKER_BUILDX_SHA256=41e1b3fff6541d5f5febb18ff4c9108bec30afd7bf9133b82783735c2078eac1
# Thu, 21 May 2026 23:15:58 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 21 May 2026 23:15:58 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 21 May 2026 23:15:59 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-windows-x86_64.exe
# Thu, 21 May 2026 23:16:00 GMT
ENV DOCKER_COMPOSE_SHA256=e1a8faff28c7433635201a2222171b727f33ecdb0ed367e54d162d00432f39aa
# Thu, 21 May 2026 23:16:10 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f787ad06f38db673c3d304f21c09a82ff9a1ced32062515ea52fdb0383457b24`  
		Last Modified: Tue, 12 May 2026 18:03:01 GMT  
		Size: 682.9 MB (682882530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c26092efbc05ba0447d81394df46314e3b86ab224685126b2d6dfd994d4dc11`  
		Last Modified: Thu, 21 May 2026 23:16:20 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83ade171b063bb36658cc0d1e2c9c6cb333ea25a3ad1e4129615adf825b64a46`  
		Last Modified: Thu, 21 May 2026 23:16:20 GMT  
		Size: 406.4 KB (406376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78577312456309bc4fe740995c1663317c15ecc17bcedded51adf9a9982366ca`  
		Last Modified: Thu, 21 May 2026 23:16:18 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee76c01ce753f169a4b6e55abafceb2769603948efcc72907de3e6aeb33cce42`  
		Last Modified: Thu, 21 May 2026 23:16:18 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc27681d28a3246dcf30c481b3852d6dbdc170d9cf5b284e019a90ade4d9cee8`  
		Last Modified: Thu, 21 May 2026 23:16:21 GMT  
		Size: 20.3 MB (20271957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c75db7b4635a1d76c37b80319e3dd1bdff20dd7ef77265097ecdb2861b340b99`  
		Last Modified: Thu, 21 May 2026 23:16:17 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48d982239ff1380cf0818ab9cc60083eac7f15cd44054f9f67433be9035d8a31`  
		Last Modified: Thu, 21 May 2026 23:16:17 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c096a591d4ea5f003d7be2a803cf5e81d42655e886b4df3ea31db5ab4f1289f`  
		Last Modified: Thu, 21 May 2026 23:16:17 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f795f325466c0a11f5a6c88330d8ab8b3fcad025e8fc95a56b3cc2d15f7884bb`  
		Last Modified: Thu, 21 May 2026 23:16:32 GMT  
		Size: 23.9 MB (23933638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b824c613a9ba32b1fcec65a639d38947346d62eddad555e9a7e295010f6937d`  
		Last Modified: Thu, 21 May 2026 23:16:15 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62db1e13ba58abbe1229ca941f68bceaa49a84ce729b12c843e3c1914052407d`  
		Last Modified: Thu, 21 May 2026 23:16:15 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7286144ed984b89e44b176cd42f189f5d30dc6bdd1357032bbb549bb0c96975`  
		Last Modified: Thu, 21 May 2026 23:16:15 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8922b65b3736da43bcb9ea86b5abf5ea19ee56a9c642200696decef2214beb0`  
		Last Modified: Thu, 21 May 2026 23:16:17 GMT  
		Size: 12.1 MB (12118551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:cli`

```console
$ docker pull docker@sha256:9ba8e32bfc35a2c7ae2feb1e3241b2778ae21dee80f4dcd31d04e1cfdea86ea2
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
$ docker pull docker@sha256:ec66e6a33f2769030bf8f283b25a7ea135d770ed2c3b91c14195de0ca901e61a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.1 MB (66112304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a190ccdf9e97f139d089920e904db8c97e394f8b5f3ff536cdadeda6c821ded`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Thu, 21 May 2026 22:56:57 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 21 May 2026 22:56:57 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 21 May 2026 22:56:57 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 21 May 2026 22:56:59 GMT
ENV DOCKER_VERSION=29.5.2
# Thu, 21 May 2026 22:56:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 21 May 2026 22:56:59 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 21 May 2026 22:57:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 21 May 2026 22:57:00 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 21 May 2026 22:57:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 21 May 2026 22:57:01 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 21 May 2026 22:57:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 21 May 2026 22:57:01 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 21 May 2026 22:57:01 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 21 May 2026 22:57:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 May 2026 22:57:01 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6cf87df21c231c07f8b8d9c532474fc120946d085773fa15272382636f10b46`  
		Last Modified: Thu, 21 May 2026 22:57:08 GMT  
		Size: 8.3 MB (8311580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54392fc3db24e998571260adc7ac1a1bc098852dfeb30150218d2174da4aa929`  
		Last Modified: Thu, 21 May 2026 22:57:07 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4b052546a5d5d26f7d251d92bd155e2275ee74b4c83a5748550720fa39efe1`  
		Last Modified: Thu, 21 May 2026 22:57:08 GMT  
		Size: 19.5 MB (19549520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b2deac6c9ceba582f6a7f4a7ea2910141ba0dfcf644ee930db818a78947527a`  
		Last Modified: Thu, 21 May 2026 22:57:08 GMT  
		Size: 23.0 MB (22988915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:046b51e466e9d4d0fb090dd060997a0892b36578ab13f0153d1d61f53166d5c6`  
		Last Modified: Thu, 21 May 2026 22:57:09 GMT  
		Size: 11.4 MB (11395947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff5ffb634dd2a67009edb32be895febc923676e8dc0b94f8c857528723140ee`  
		Last Modified: Thu, 21 May 2026 22:57:09 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b162b8dd068432fdb9682bbf9fc7ecbe61c2dbbb72441a22b74a6537f7fe639`  
		Last Modified: Thu, 21 May 2026 22:57:10 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b02815b1d866ccad16190784679c75c04f712dc13f12bd8ec46cf7648796905`  
		Last Modified: Thu, 21 May 2026 22:57:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:d0c058683425ac4a4e35818c3cab8e244bf44bf5629b2606d503eab0302918c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24cd59892835a6bb71bef956c207f451b0ff4ef20ef700549178228a80696991`

```dockerfile
```

-	Layers:
	-	`sha256:e8d0f9a2c1d7978db5312a52983dc91318b6ef2d7b32afeed756151fcba3ed72`  
		Last Modified: Thu, 21 May 2026 22:57:07 GMT  
		Size: 38.1 KB (38056 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:1ea54fcc950d7b127dc87b88d28c747600cca8b48d8c034ecd527709330f2074
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62396270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8d2a98d406c875d3e0db6343c8b5fa56023aa689cb018d156b714f0199d7ab8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Thu, 21 May 2026 22:57:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 21 May 2026 22:57:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 21 May 2026 22:57:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 21 May 2026 22:57:14 GMT
ENV DOCKER_VERSION=29.5.2
# Thu, 21 May 2026 22:57:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 21 May 2026 22:57:14 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 21 May 2026 22:57:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 21 May 2026 22:57:17 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 21 May 2026 22:57:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 21 May 2026 22:57:18 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 21 May 2026 22:57:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 21 May 2026 22:57:19 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 21 May 2026 22:57:19 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 21 May 2026 22:57:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 May 2026 22:57:19 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:686f209ff6de10676a89d77e3e8a6fab30545d5720ccf9054ee0d1b26e38b43a`  
		Last Modified: Thu, 21 May 2026 22:57:25 GMT  
		Size: 8.2 MB (8211872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc482e1b01e42c3c70b99620637bf883c5da46458460af902ddff0ac829fe8be`  
		Last Modified: Thu, 21 May 2026 22:57:24 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6ca55f6f19c616ff991f7a3db821aff9610c17f90b38f47cbd8f4524f46539`  
		Last Modified: Thu, 21 May 2026 22:57:25 GMT  
		Size: 18.2 MB (18183161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83229a063dcdaa05d49b47a377f6266b68058c99c6e0d8dfdc2a7d84012787eb`  
		Last Modified: Thu, 21 May 2026 22:57:25 GMT  
		Size: 21.6 MB (21614627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:940f9c6bb6e92b7182721c14634a231b228afd28fe04caffd78841f7dd24411b`  
		Last Modified: Thu, 21 May 2026 22:57:26 GMT  
		Size: 10.8 MB (10812594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c13701af534883715f5b32ba09cbb6f13feb5042a866f77e574177b03153cb1`  
		Last Modified: Thu, 21 May 2026 22:57:27 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5827618b0a4b3c9209e2ce38a22a9c7e3bf8dc8d55f12ece8a624cec59ca0c0`  
		Last Modified: Thu, 21 May 2026 22:57:27 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:156a2ca1e461bbe26a51cde3454797f4bb525e545ae12a790eb2c832fa3cd344`  
		Last Modified: Thu, 21 May 2026 22:57:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:04ebdfb0eda18157d342b7fb08c62391f19045358bdd9d13363d75b2bf405b48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c878c65dd1bf46ceb912d86983dbbb6747bbc0d9f04388340d7ff40ab6a955b5`

```dockerfile
```

-	Layers:
	-	`sha256:a18fb0bd08433a7ea29e919c067320a3a5064d90b3bf6926746198a604fa7c2e`  
		Last Modified: Thu, 21 May 2026 22:57:24 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:4efa5b423f6548c5521b0093e3276bff164af4e70d51c1368309a76e916622e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61378438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d52d0f5e6c9123362925f36aa888038a8dd446e137138fb8463b681a0bc5dff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Thu, 21 May 2026 22:57:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 21 May 2026 22:57:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 21 May 2026 22:57:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 21 May 2026 22:57:19 GMT
ENV DOCKER_VERSION=29.5.2
# Thu, 21 May 2026 22:57:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 21 May 2026 22:57:19 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 21 May 2026 22:57:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 21 May 2026 22:57:21 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 21 May 2026 22:57:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 21 May 2026 22:57:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 21 May 2026 22:57:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 21 May 2026 22:57:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 21 May 2026 22:57:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 21 May 2026 22:57:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 May 2026 22:57:22 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f52861283d77a40b5946e65011de57aef34bc9327b32604f88a677e6f2cb2a`  
		Last Modified: Thu, 21 May 2026 22:57:29 GMT  
		Size: 7.5 MB (7520603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe77c7d8ef7315ec44519db3cec2d9d47ed19881a859e1f59af47b6ee930987`  
		Last Modified: Thu, 21 May 2026 22:57:29 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb66512e1233e73a0972411ebf4f8c344ca4a394da4d49e6b222234bb111c827`  
		Last Modified: Thu, 21 May 2026 22:57:30 GMT  
		Size: 18.2 MB (18172264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa22bb61dc858338f97353ad033e1a3dfeaedd00a1bc504c85cb83d1d1e1066`  
		Last Modified: Thu, 21 May 2026 22:57:30 GMT  
		Size: 21.6 MB (21600713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36a896b5ff64585ed1221a91d5f2f671787cd3897f86991c0f6fe8525f7d75c0`  
		Last Modified: Thu, 21 May 2026 22:57:30 GMT  
		Size: 10.8 MB (10799582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce88e69f3e7c7ac17129a6b4b87aad6b39a3a2861c81d554e406b2547561f66`  
		Last Modified: Thu, 21 May 2026 22:57:30 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5758ccda3473178260da62e4ab7c4fa36a8dfc1c4ef7d4fed06e0ea0fb533c09`  
		Last Modified: Thu, 21 May 2026 22:57:31 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e4468a079208fc160ee3dd1c7df3de47f866b433f720289671fd2ab2bf8a6d`  
		Last Modified: Thu, 21 May 2026 22:57:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:73a5dfa31ffac43a7e451c867bb1707eb46361077e17b338feea6d1cfe16074c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:213b655767f4e7e1aa870b4cdd07817a9d99c15bc554800b7bf98c33cfb92cc9`

```dockerfile
```

-	Layers:
	-	`sha256:88b55d2936f52c50f0f1b5bdd99b1c08534f7a93ef0c66f562f45ef6679cac29`  
		Last Modified: Thu, 21 May 2026 22:57:28 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:1c27de1f16ee894e6389586d8b58391f4b941f768cb5520cd2970c72d38a8e84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61750058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:156869ccb322d51e7560b80292b10dfaa423516486f6683494060b76d38dabcc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Thu, 21 May 2026 22:56:32 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 21 May 2026 22:56:32 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 21 May 2026 22:56:32 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 21 May 2026 22:56:34 GMT
ENV DOCKER_VERSION=29.5.2
# Thu, 21 May 2026 22:56:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 21 May 2026 22:56:34 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 21 May 2026 22:56:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 21 May 2026 22:56:35 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 21 May 2026 22:56:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 21 May 2026 22:56:36 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 21 May 2026 22:56:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 21 May 2026 22:56:36 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 21 May 2026 22:56:36 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 21 May 2026 22:56:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 May 2026 22:56:36 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae988a6da12e07a4495206223708dfa12193c715305da0959269e07cfe0883c`  
		Last Modified: Thu, 21 May 2026 22:56:42 GMT  
		Size: 8.4 MB (8368391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad63753001c8116da8d4078088f8c226c9d2d5ebb32c543695bad3dfd05cb848`  
		Last Modified: Thu, 21 May 2026 22:56:42 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1523489b9bcf5899f4ec01d3ea4b3b09a7f11127bd6cfac3ad985d4e121a917`  
		Last Modified: Thu, 21 May 2026 22:56:43 GMT  
		Size: 18.0 MB (18003804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4276c1b3c4ca523a976f2b634bcd7b921a29dbff4274ac9aa9cc1e68ed96f93`  
		Last Modified: Thu, 21 May 2026 22:56:43 GMT  
		Size: 20.8 MB (20815981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e3a6fedf4004b1aba4e7b35c15a75f4e30fd0ae9d353199415f18fd99a7cf8`  
		Last Modified: Thu, 21 May 2026 22:56:43 GMT  
		Size: 10.4 MB (10359860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37af9029ae6a6376f88d713b9b54fb69ece2959cf06985f67d3905c6ef36739`  
		Last Modified: Thu, 21 May 2026 22:56:44 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56df60bc257eb03677643450dfa9477ebdad3b524820a408218637a85932c45d`  
		Last Modified: Thu, 21 May 2026 22:56:44 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe07c252ff4b96737716f829e1e8ff46a81625412f850d98480be21cf51f845`  
		Last Modified: Thu, 21 May 2026 22:56:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:a8dedaaa0ddf7100fc1cf4d4aee8dec52a0bd683ada897dc62942f5c0b88d846
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30bdb74e1af7301d0ea10753180b6ea04b819ea07777e30c7cc70392aefbb2db`

```dockerfile
```

-	Layers:
	-	`sha256:ddd2ae6062cdfd1652888a3cbd3bdc652070dde80dc25a31826cfb552cb05649`  
		Last Modified: Thu, 21 May 2026 22:56:42 GMT  
		Size: 38.3 KB (38262 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind`

```console
$ docker pull docker@sha256:eed377f3ce14afda560e742c5b3ae446df1ce00a16e1beab2ac6c78c1477fe85
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
$ docker pull docker@sha256:6f156e0882b6f307bcd00e01b7abebdccf6eb96b1bb40e8b160e3e401ba3749b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.7 MB (141660887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a475a10539689996453c7c7aa57795a1c35cb8da621faddaef1fb0f05cdb7723`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Tue, 19 May 2026 18:43:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 19 May 2026 18:43:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 19 May 2026 18:43:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 19 May 2026 18:43:53 GMT
ENV DOCKER_VERSION=29.5.1
# Tue, 19 May 2026 18:43:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 19 May 2026 18:43:53 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Tue, 19 May 2026 18:43:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-amd64'; 			sha256='0144479d5a1cd710be3464ae898628cfa68033e16b225aef52f81930c45ac9b5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v6'; 			sha256='1f34337385921c5da43d63452282726b062aa887fda975f96dd3d6e869648bc6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v7'; 			sha256='3560b5b6fd3485f4d0bd160e7edf56cc1f08f0cb5852c9af28bf3fab9973c7c2'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm64'; 			sha256='565605fe0bb393ed5d11771e5b52fc7ef05c701868861fa85609747c9d74a440'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-ppc64le'; 			sha256='c5ef8012f48a518e1c235ad408d26cd424d7b5fa87eaf78cb2ff4b9048730120'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-riscv64'; 			sha256='80b27d5f3a346591a5045b81217ee5be578ed151ef8cbd883a892c0ec0ac33f1'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-s390x'; 			sha256='04f5bd0d389f682c7e9287a3b3a1777b0848f8e10d58cbf9d4d12c9002bbb378'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 19 May 2026 18:43:54 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Tue, 19 May 2026 18:43:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 19 May 2026 18:43:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 19 May 2026 18:43:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 18:43:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 19 May 2026 18:43:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 19 May 2026 18:43:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 May 2026 18:43:55 GMT
CMD ["sh"]
# Tue, 19 May 2026 18:52:09 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 19 May 2026 18:52:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 19 May 2026 18:52:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 19 May 2026 18:52:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 19 May 2026 18:52:13 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 19 May 2026 18:52:13 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 19 May 2026 18:52:13 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 18:52:13 GMT
VOLUME [/var/lib/docker]
# Tue, 19 May 2026 18:52:13 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 19 May 2026 18:52:13 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 19 May 2026 18:52:13 GMT
CMD []
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959d822c11f4cffde22f6a8ca77070ab678788ee8a60e50bf52240fab7600d55`  
		Last Modified: Tue, 19 May 2026 18:44:02 GMT  
		Size: 8.3 MB (8311621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf748eeffe46320957e43a6d041504e02f6d54efaa90b05ea0a5e76259a3bc9`  
		Last Modified: Tue, 19 May 2026 18:44:01 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29db3e4d2cf2bffd95a0b8c095c0dfc7f4b6ee9717169afb9c613ae0714f22a5`  
		Last Modified: Tue, 19 May 2026 18:44:03 GMT  
		Size: 19.5 MB (19549501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:418895c8a0097a67712f5b2385b094ed4ed5af1359b9b43cb86c07da48ca11c9`  
		Last Modified: Tue, 19 May 2026 18:44:03 GMT  
		Size: 23.0 MB (22988580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4382b5de8ae74e74d495d9d94f0127cf051728dc00cab26dfa163bba8cdbcf13`  
		Last Modified: Tue, 19 May 2026 18:44:03 GMT  
		Size: 11.2 MB (11243752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53914aaed626c98320ff52b5bbe81eb804e9a82d445d07a5908e16e86ac5a5c`  
		Last Modified: Tue, 19 May 2026 18:44:03 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cac0928dd7f6aa6c83aa987350f200df21db15618f2ba47912f35be2b16b3b9`  
		Last Modified: Tue, 19 May 2026 18:44:04 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1c069fc81d4d790f039a7a8160f23dffa6c11a22ee385a0db0fe75ae235dfe1`  
		Last Modified: Tue, 19 May 2026 18:44:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27817872a6ae6fcf22af6f3dbdec0f52f7b055d8b3384cd5b922f74d11358249`  
		Last Modified: Tue, 19 May 2026 18:52:23 GMT  
		Size: 6.9 MB (6941424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a7ba7363a81328286ac28be79b6e6248a1e1c4cb3f1749b808bc8abeb5c686`  
		Last Modified: Tue, 19 May 2026 18:52:23 GMT  
		Size: 92.2 KB (92218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f90442d3c5cd85fdf0fd4683516f39486a803bd57eb9813b3dcb939d9d3fcc`  
		Last Modified: Tue, 19 May 2026 18:52:23 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c588cc6d3552d3ec8363fa8dabb97cfe3ea467efd07c37c45853267ab5c544`  
		Last Modified: Tue, 19 May 2026 18:52:25 GMT  
		Size: 68.7 MB (68661447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa91ecdbc2c72221f7c567a768c787e9b0e27629ad60fecaa37b420555dbec4`  
		Last Modified: Tue, 19 May 2026 18:52:24 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a04f224ef5d78ccf3d32a655e7621773237de1ba0a09780d2011e4e3efc9802`  
		Last Modified: Tue, 19 May 2026 18:52:25 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:8459bca25b1862c9c244d8290b9c289f8f38a28e911360560cef489552fd9996
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca9c00d43298e9a165fe521202b47e762e0e30cdaad754b907fb2241affba41a`

```dockerfile
```

-	Layers:
	-	`sha256:725c95ff8cee96878c88b2d98ed922fc03f42a86c848e44ace4d3602cca233bd`  
		Last Modified: Tue, 19 May 2026 18:52:23 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:656cd6a2deb516bf1bab86d4eb9e0ea9b2afca3fb8c81a402195068521496791
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.6 MB (133554774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b375b41ebcd63fd76689fd0c53d0cbebdb1c6086df5568f03b1342739485d2f4`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Tue, 19 May 2026 18:46:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 19 May 2026 18:46:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 19 May 2026 18:46:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 19 May 2026 18:46:29 GMT
ENV DOCKER_VERSION=29.5.1
# Tue, 19 May 2026 18:46:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 19 May 2026 18:46:29 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Tue, 19 May 2026 18:46:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-amd64'; 			sha256='0144479d5a1cd710be3464ae898628cfa68033e16b225aef52f81930c45ac9b5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v6'; 			sha256='1f34337385921c5da43d63452282726b062aa887fda975f96dd3d6e869648bc6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v7'; 			sha256='3560b5b6fd3485f4d0bd160e7edf56cc1f08f0cb5852c9af28bf3fab9973c7c2'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm64'; 			sha256='565605fe0bb393ed5d11771e5b52fc7ef05c701868861fa85609747c9d74a440'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-ppc64le'; 			sha256='c5ef8012f48a518e1c235ad408d26cd424d7b5fa87eaf78cb2ff4b9048730120'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-riscv64'; 			sha256='80b27d5f3a346591a5045b81217ee5be578ed151ef8cbd883a892c0ec0ac33f1'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-s390x'; 			sha256='04f5bd0d389f682c7e9287a3b3a1777b0848f8e10d58cbf9d4d12c9002bbb378'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 19 May 2026 18:46:32 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Tue, 19 May 2026 18:46:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 19 May 2026 18:46:33 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 19 May 2026 18:46:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 18:46:33 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 19 May 2026 18:46:34 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 19 May 2026 18:46:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 May 2026 18:46:34 GMT
CMD ["sh"]
# Tue, 19 May 2026 18:48:00 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 19 May 2026 18:48:00 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 19 May 2026 18:48:00 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 19 May 2026 18:48:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 19 May 2026 18:48:04 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 19 May 2026 18:48:04 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 19 May 2026 18:48:04 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 18:48:04 GMT
VOLUME [/var/lib/docker]
# Tue, 19 May 2026 18:48:04 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 19 May 2026 18:48:04 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 19 May 2026 18:48:04 GMT
CMD []
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e510993d358b2182e33432b09c723cb2de90442627624e753d33ff6f58e37cf`  
		Last Modified: Tue, 19 May 2026 18:46:40 GMT  
		Size: 8.2 MB (8211856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac6422e386e61fe4ba4eb1abca9f67aef1bba270f947f3797505168eddc865ef`  
		Last Modified: Tue, 19 May 2026 18:46:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c6104ecd7c2122cba9eadf591b901752e839d28c94e9786023634ab16c4e86`  
		Last Modified: Tue, 19 May 2026 18:46:41 GMT  
		Size: 18.2 MB (18183185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9278a90d0e78f94da7f59f70fe4811830047483868d42c4e25a85b91a3359765`  
		Last Modified: Tue, 19 May 2026 18:46:41 GMT  
		Size: 21.6 MB (21614147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09f94e1195a7d62fc4046fa609e325b2001195cf49352924129c45728445d565`  
		Last Modified: Tue, 19 May 2026 18:46:41 GMT  
		Size: 10.7 MB (10650824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a8126c2985de246f1344d8c4340e5934b14cdf06f269351c0bfeac534be4c3a`  
		Last Modified: Tue, 19 May 2026 18:46:41 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f13c028f2e167a9ccd442fe69b89b5f1ca9e19f4589d7160d5af4d3b451ba862`  
		Last Modified: Tue, 19 May 2026 18:46:42 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa9769c6262cc549e78864817d114f4780b6b611ff08c097bcb018ab9040fd0`  
		Last Modified: Tue, 19 May 2026 18:46:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:125e5e8c972742a3fdece68d1d7efe160fc572758035dc6dd440150a5dff5bf7`  
		Last Modified: Tue, 19 May 2026 18:48:15 GMT  
		Size: 7.3 MB (7278661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:092dd15fda2f6f91745deb58f699d28c2ae054d7fb4d6c4100b53f0f8e3a6d85`  
		Last Modified: Tue, 19 May 2026 18:48:15 GMT  
		Size: 91.5 KB (91516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc718ec10edd9882bc794dfec135ed20f43243a8db5ad70f2ca75ac4b4191815`  
		Last Modified: Tue, 19 May 2026 18:48:15 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf390f2615c4c05543ef083213b7da580fc3a675929438042a5228503644f65`  
		Last Modified: Tue, 19 May 2026 18:48:17 GMT  
		Size: 63.9 MB (63944568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0111492ca1c0d70617ea1ed481e8ae4908695479c10dc5b86fe761dd03edc6b`  
		Last Modified: Tue, 19 May 2026 18:48:16 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b88ff88aa94e286fad9d8f3480fb92ba8ec324a9d55d74cce8cce2e99c36353`  
		Last Modified: Tue, 19 May 2026 18:48:16 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:1fd6b9654a40244c2a32a42dfdbd4b0c2fcd97aaacc719b9c466fed8008b0c05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e4f0d6a13a6e324e492f0fd9ae8856d26b30b034d24e9b3868069907c61ec10`

```dockerfile
```

-	Layers:
	-	`sha256:096e9d4d3b5e87687de3559cc60228911d8179792add0ad0a60e1afd76f2b032`  
		Last Modified: Tue, 19 May 2026 18:48:14 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:ce68e53519cdc94c6b28b82b2e4af1856aa5dd8e577fb872900952a6ed88f9d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.7 MB (131668449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bc263b60a94589a9d3f238ee64951d8f806cc46c8caed0452715d45111a5b91`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Tue, 19 May 2026 18:50:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 19 May 2026 18:50:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 19 May 2026 18:50:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 19 May 2026 18:50:21 GMT
ENV DOCKER_VERSION=29.5.1
# Tue, 19 May 2026 18:50:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 19 May 2026 18:50:21 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Tue, 19 May 2026 18:50:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-amd64'; 			sha256='0144479d5a1cd710be3464ae898628cfa68033e16b225aef52f81930c45ac9b5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v6'; 			sha256='1f34337385921c5da43d63452282726b062aa887fda975f96dd3d6e869648bc6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v7'; 			sha256='3560b5b6fd3485f4d0bd160e7edf56cc1f08f0cb5852c9af28bf3fab9973c7c2'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm64'; 			sha256='565605fe0bb393ed5d11771e5b52fc7ef05c701868861fa85609747c9d74a440'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-ppc64le'; 			sha256='c5ef8012f48a518e1c235ad408d26cd424d7b5fa87eaf78cb2ff4b9048730120'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-riscv64'; 			sha256='80b27d5f3a346591a5045b81217ee5be578ed151ef8cbd883a892c0ec0ac33f1'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-s390x'; 			sha256='04f5bd0d389f682c7e9287a3b3a1777b0848f8e10d58cbf9d4d12c9002bbb378'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 19 May 2026 18:50:23 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Tue, 19 May 2026 18:50:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 19 May 2026 18:50:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 19 May 2026 18:50:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 18:50:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 19 May 2026 18:50:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 19 May 2026 18:50:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 May 2026 18:50:24 GMT
CMD ["sh"]
# Tue, 19 May 2026 19:11:05 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 19 May 2026 19:11:05 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 19 May 2026 19:11:05 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 19 May 2026 19:11:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 19 May 2026 19:11:10 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 19 May 2026 19:11:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 19 May 2026 19:11:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 19:11:10 GMT
VOLUME [/var/lib/docker]
# Tue, 19 May 2026 19:11:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 19 May 2026 19:11:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 19 May 2026 19:11:10 GMT
CMD []
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e78396f075a6021fa389cbab78d2b7a97c1fa6ccd90c5a3f9aad13a82d9a82d5`  
		Last Modified: Tue, 19 May 2026 18:50:31 GMT  
		Size: 7.5 MB (7520541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55503681071acc50ecd4d54f1a76c32b34fb2e24b116717b8a11a5ed2c4b834b`  
		Last Modified: Tue, 19 May 2026 18:50:30 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:139bfdfb0c5a911c258bd9ca3f33e5d74dc4cdac244e701ffc230dfb2dbcf299`  
		Last Modified: Tue, 19 May 2026 18:50:31 GMT  
		Size: 18.2 MB (18172268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e28d126c0c15c1ddece42e48d16b7989f46d4ba83543ade587e34aae442b162d`  
		Last Modified: Tue, 19 May 2026 18:50:31 GMT  
		Size: 21.6 MB (21600397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb484c140400a96468ac162a856058550dff5319ecf84cb2d15485ffa462cfe5`  
		Last Modified: Tue, 19 May 2026 18:50:31 GMT  
		Size: 10.6 MB (10637143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:458ff3d79525d794f095fe12c99f3a95a84e674163d4ac75823a6bbe91cdca6c`  
		Last Modified: Tue, 19 May 2026 18:50:32 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:252522a027743939f7b115d2d3929238ba7a8fee776336371433d62e17da49f3`  
		Last Modified: Tue, 19 May 2026 18:50:33 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b1fd0762adb2df9e41385aaea4f5aeb069ccb43ec6a5203c0970dbb32f5d39`  
		Last Modified: Tue, 19 May 2026 18:50:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2404388a95cbd53c2924a8956a2b0bd9fed1ed42798ef0d7958645ec50b36503`  
		Last Modified: Tue, 19 May 2026 19:11:21 GMT  
		Size: 6.6 MB (6577150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abebc77c5a81c02e559a6177ab009ea93d155d230027ecb011d71caf8e1319cb`  
		Last Modified: Tue, 19 May 2026 19:11:20 GMT  
		Size: 87.8 KB (87825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:505cb9808a455382b226432bd33efca0786f2b2817e3828966e8ae1880b9a387`  
		Last Modified: Tue, 19 May 2026 19:11:20 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb736cbd14a0b4279f19088aba50827f55f5bd8c64dd5868c81329ee396e19f`  
		Last Modified: Tue, 19 May 2026 19:11:23 GMT  
		Size: 63.8 MB (63781847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b8e0456f81c21846bbc1e4af0c8ce599dde97bbda1d981de3f47999ce045a4`  
		Last Modified: Tue, 19 May 2026 19:11:22 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10bd67dffac6bb7c60a61f90d9e059f51d217061b38efadfa05cfbccc501c4eb`  
		Last Modified: Tue, 19 May 2026 19:11:22 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:38aff3f9f68bc80866a840b6895120e3efd20f227f69ca66663fee2a5c143d5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e771280fb8341ddf485470385301e8a4df555c4889817952e2e3f1bc2d60f3f`

```dockerfile
```

-	Layers:
	-	`sha256:0f43b1170bad091b1f8a038b4c799e044dcbe62f3cf88792df12fd3808abd3db`  
		Last Modified: Tue, 19 May 2026 19:11:20 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:d29f00616a4b5af545c6238d5e5d3f010dabe8cd9373464e7528dcc2ffe932e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.1 MB (131088931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d59db2bca67549c508438fad529bbb4d973798fdf3dac19d4cff714cd0ef24d8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Tue, 19 May 2026 18:52:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 19 May 2026 18:52:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 19 May 2026 18:52:13 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 19 May 2026 18:52:16 GMT
ENV DOCKER_VERSION=29.5.1
# Tue, 19 May 2026 18:52:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 19 May 2026 18:52:16 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Tue, 19 May 2026 18:52:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-amd64'; 			sha256='0144479d5a1cd710be3464ae898628cfa68033e16b225aef52f81930c45ac9b5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v6'; 			sha256='1f34337385921c5da43d63452282726b062aa887fda975f96dd3d6e869648bc6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v7'; 			sha256='3560b5b6fd3485f4d0bd160e7edf56cc1f08f0cb5852c9af28bf3fab9973c7c2'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm64'; 			sha256='565605fe0bb393ed5d11771e5b52fc7ef05c701868861fa85609747c9d74a440'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-ppc64le'; 			sha256='c5ef8012f48a518e1c235ad408d26cd424d7b5fa87eaf78cb2ff4b9048730120'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-riscv64'; 			sha256='80b27d5f3a346591a5045b81217ee5be578ed151ef8cbd883a892c0ec0ac33f1'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-s390x'; 			sha256='04f5bd0d389f682c7e9287a3b3a1777b0848f8e10d58cbf9d4d12c9002bbb378'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 19 May 2026 18:52:17 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Tue, 19 May 2026 18:52:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 19 May 2026 18:52:18 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 19 May 2026 18:52:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 18:52:18 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 19 May 2026 18:52:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 19 May 2026 18:52:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 May 2026 18:52:18 GMT
CMD ["sh"]
# Tue, 19 May 2026 19:11:28 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 19 May 2026 19:11:28 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 19 May 2026 19:11:29 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 19 May 2026 19:11:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 19 May 2026 19:11:31 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 19 May 2026 19:11:31 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 19 May 2026 19:11:31 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 19:11:31 GMT
VOLUME [/var/lib/docker]
# Tue, 19 May 2026 19:11:31 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 19 May 2026 19:11:31 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 19 May 2026 19:11:31 GMT
CMD []
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:439c73b6370f92c891e3dae2ef2ac51ba47633f4382e93fa3a194ab6c9929fcf`  
		Last Modified: Tue, 19 May 2026 18:52:24 GMT  
		Size: 8.4 MB (8368378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:090f26860bbcb42203be1c1ccc78e592537b7d5076712eddc078a4521b65b6ef`  
		Last Modified: Tue, 19 May 2026 18:52:23 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02fa5c43148b510203ce86fd309a24339439966d97d2739e5681dea9fbedd78b`  
		Last Modified: Tue, 19 May 2026 18:52:24 GMT  
		Size: 18.0 MB (18003824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:179aebd9e04e34e062d99c03bced083b59894f9ff9c70a48e5fdde05043d0662`  
		Last Modified: Tue, 19 May 2026 18:52:25 GMT  
		Size: 20.8 MB (20815342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333ebd0d3068df15ad94c847b40ac364dc7140981f38d3a8f08165ef3fe528ac`  
		Last Modified: Tue, 19 May 2026 18:52:25 GMT  
		Size: 10.2 MB (10243275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e7cd72262f0dcb67fc210c582e3d890f8da6bbfea7979a4af0eca2d85493c8`  
		Last Modified: Tue, 19 May 2026 18:52:25 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb8c848507ade63fa035c4247243268bc78609cb843c2c46923fec82cf42e856`  
		Last Modified: Tue, 19 May 2026 18:52:26 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14678f991761f143ab6345db5de4a84ca5f83a1cd44f7d579a88be20ad20871`  
		Last Modified: Tue, 19 May 2026 18:52:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deb061c465c1d4b2683f89277bb8b93644ad86d3b6a034d3848e218ff3a36250`  
		Last Modified: Tue, 19 May 2026 19:11:41 GMT  
		Size: 7.2 MB (7219902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408cc9607ded7836e6377a9012f389a02da93bc2526404ac2125d556fed0607c`  
		Last Modified: Tue, 19 May 2026 19:11:41 GMT  
		Size: 100.9 KB (100930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4813a99698e1ee0cbb52b02f822e9732eb9144586aa3c765fee806857d8cb872`  
		Last Modified: Tue, 19 May 2026 19:11:41 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f364d3985b9e2a29ae89857aa654e13a752db4b807f58b23afc56a7fdddc9ca`  
		Last Modified: Tue, 19 May 2026 19:11:43 GMT  
		Size: 62.1 MB (62129257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34b8039e34935754bb978ab40f852eeb6345408e37deb40c0467f77421c8252`  
		Last Modified: Tue, 19 May 2026 19:11:42 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be12674817c3cc5397950df61ba9f0761de7cbb67e7527d120f671791e1644f9`  
		Last Modified: Tue, 19 May 2026 19:11:42 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:8ac585f5eb9117c0193cbfc718548d3dca67a7e669159a6b08a53ae907925d21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa5bac19b0eae7a6debca0657ab9da39a1528d516c371778235e72d5db216621`

```dockerfile
```

-	Layers:
	-	`sha256:662dc4eaa00e9b2353b08fdbf55f624046c556fe7fa5b07f0332cfd3384d50fb`  
		Last Modified: Tue, 19 May 2026 19:11:40 GMT  
		Size: 34.8 KB (34782 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind-rootless`

```console
$ docker pull docker@sha256:fc34343ecba0eed3f4c4f82dacd33287140cf123e7449f2e7a37fefa6b233a72
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:54fb8c3eb5b740f6e3660ec25470f773073e6376db6a4edda040eb8ba7105e64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157184836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abc3d62166f739fc25b4f819b724c5c207c6d5e3ccaa7127fc1a33ce1ef2b983`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Tue, 19 May 2026 18:43:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 19 May 2026 18:43:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 19 May 2026 18:43:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 19 May 2026 18:43:53 GMT
ENV DOCKER_VERSION=29.5.1
# Tue, 19 May 2026 18:43:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 19 May 2026 18:43:53 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Tue, 19 May 2026 18:43:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-amd64'; 			sha256='0144479d5a1cd710be3464ae898628cfa68033e16b225aef52f81930c45ac9b5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v6'; 			sha256='1f34337385921c5da43d63452282726b062aa887fda975f96dd3d6e869648bc6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v7'; 			sha256='3560b5b6fd3485f4d0bd160e7edf56cc1f08f0cb5852c9af28bf3fab9973c7c2'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm64'; 			sha256='565605fe0bb393ed5d11771e5b52fc7ef05c701868861fa85609747c9d74a440'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-ppc64le'; 			sha256='c5ef8012f48a518e1c235ad408d26cd424d7b5fa87eaf78cb2ff4b9048730120'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-riscv64'; 			sha256='80b27d5f3a346591a5045b81217ee5be578ed151ef8cbd883a892c0ec0ac33f1'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-s390x'; 			sha256='04f5bd0d389f682c7e9287a3b3a1777b0848f8e10d58cbf9d4d12c9002bbb378'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 19 May 2026 18:43:54 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Tue, 19 May 2026 18:43:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 19 May 2026 18:43:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 19 May 2026 18:43:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 18:43:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 19 May 2026 18:43:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 19 May 2026 18:43:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 May 2026 18:43:55 GMT
CMD ["sh"]
# Tue, 19 May 2026 18:52:09 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 19 May 2026 18:52:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 19 May 2026 18:52:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 19 May 2026 18:52:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 19 May 2026 18:52:13 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 19 May 2026 18:52:13 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 19 May 2026 18:52:13 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 18:52:13 GMT
VOLUME [/var/lib/docker]
# Tue, 19 May 2026 18:52:13 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 19 May 2026 18:52:13 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 19 May 2026 18:52:13 GMT
CMD []
# Tue, 19 May 2026 19:10:23 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Tue, 19 May 2026 19:10:23 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 19 May 2026 19:10:23 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 19 May 2026 19:10:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 	; 	rm rootless.tgz; 		rootlesskit --version # buildkit
# Tue, 19 May 2026 19:10:23 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 19 May 2026 19:10:23 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 19 May 2026 19:10:23 GMT
USER rootless
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959d822c11f4cffde22f6a8ca77070ab678788ee8a60e50bf52240fab7600d55`  
		Last Modified: Tue, 19 May 2026 18:44:02 GMT  
		Size: 8.3 MB (8311621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf748eeffe46320957e43a6d041504e02f6d54efaa90b05ea0a5e76259a3bc9`  
		Last Modified: Tue, 19 May 2026 18:44:01 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29db3e4d2cf2bffd95a0b8c095c0dfc7f4b6ee9717169afb9c613ae0714f22a5`  
		Last Modified: Tue, 19 May 2026 18:44:03 GMT  
		Size: 19.5 MB (19549501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:418895c8a0097a67712f5b2385b094ed4ed5af1359b9b43cb86c07da48ca11c9`  
		Last Modified: Tue, 19 May 2026 18:44:03 GMT  
		Size: 23.0 MB (22988580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4382b5de8ae74e74d495d9d94f0127cf051728dc00cab26dfa163bba8cdbcf13`  
		Last Modified: Tue, 19 May 2026 18:44:03 GMT  
		Size: 11.2 MB (11243752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53914aaed626c98320ff52b5bbe81eb804e9a82d445d07a5908e16e86ac5a5c`  
		Last Modified: Tue, 19 May 2026 18:44:03 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cac0928dd7f6aa6c83aa987350f200df21db15618f2ba47912f35be2b16b3b9`  
		Last Modified: Tue, 19 May 2026 18:44:04 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1c069fc81d4d790f039a7a8160f23dffa6c11a22ee385a0db0fe75ae235dfe1`  
		Last Modified: Tue, 19 May 2026 18:44:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27817872a6ae6fcf22af6f3dbdec0f52f7b055d8b3384cd5b922f74d11358249`  
		Last Modified: Tue, 19 May 2026 18:52:23 GMT  
		Size: 6.9 MB (6941424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a7ba7363a81328286ac28be79b6e6248a1e1c4cb3f1749b808bc8abeb5c686`  
		Last Modified: Tue, 19 May 2026 18:52:23 GMT  
		Size: 92.2 KB (92218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f90442d3c5cd85fdf0fd4683516f39486a803bd57eb9813b3dcb939d9d3fcc`  
		Last Modified: Tue, 19 May 2026 18:52:23 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c588cc6d3552d3ec8363fa8dabb97cfe3ea467efd07c37c45853267ab5c544`  
		Last Modified: Tue, 19 May 2026 18:52:25 GMT  
		Size: 68.7 MB (68661447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa91ecdbc2c72221f7c567a768c787e9b0e27629ad60fecaa37b420555dbec4`  
		Last Modified: Tue, 19 May 2026 18:52:24 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a04f224ef5d78ccf3d32a655e7621773237de1ba0a09780d2011e4e3efc9802`  
		Last Modified: Tue, 19 May 2026 18:52:25 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cecc87fe83d1eed7164980cba609d8af5ce21512b7a270c9fff3a717b56885d`  
		Last Modified: Tue, 19 May 2026 19:10:29 GMT  
		Size: 3.4 MB (3420112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f1de764b59139da153ed5c910b6f1016ba4c34bfe850397d4515465af03b14`  
		Last Modified: Tue, 19 May 2026 19:10:28 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810353487b2c22447155b48ee25ce68046853c053cd2683969fef6360cc51933`  
		Last Modified: Tue, 19 May 2026 19:10:29 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51c09f12615ecc2d61dce57d65b327703b94b167fc1f44f161403ac443d684f2`  
		Last Modified: Tue, 19 May 2026 19:10:29 GMT  
		Size: 12.1 MB (12102496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9688d32ac36d4f90efdf6379ecbdf84feb518c202f038c402b312b45fe270a28`  
		Last Modified: Tue, 19 May 2026 19:10:30 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:110a0812130d4441ce1773cd1230225e01f2e770f5ecf5f5641a4baf88df3911
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a854ed3332b83327cbd69c19dfffceb9982c23ed85413639f28ad3c4e8a4cbd`

```dockerfile
```

-	Layers:
	-	`sha256:8786627e00c646555d675e83986675375d51e2130c10d9a3645ebd3a70b82cd2`  
		Last Modified: Tue, 19 May 2026 19:10:28 GMT  
		Size: 30.5 KB (30493 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:f69d2ff1f367dac480263f11eb4bb9237f140d4ebe4349325c75b4fd0d06bd28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.7 MB (145721341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a4e4d8a17819a06713e6ac6acfa7f117cf9cd4e8567cf58372f73eca47616c4`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Tue, 19 May 2026 18:52:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 19 May 2026 18:52:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 19 May 2026 18:52:13 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 19 May 2026 18:52:16 GMT
ENV DOCKER_VERSION=29.5.1
# Tue, 19 May 2026 18:52:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 19 May 2026 18:52:16 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Tue, 19 May 2026 18:52:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-amd64'; 			sha256='0144479d5a1cd710be3464ae898628cfa68033e16b225aef52f81930c45ac9b5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v6'; 			sha256='1f34337385921c5da43d63452282726b062aa887fda975f96dd3d6e869648bc6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v7'; 			sha256='3560b5b6fd3485f4d0bd160e7edf56cc1f08f0cb5852c9af28bf3fab9973c7c2'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm64'; 			sha256='565605fe0bb393ed5d11771e5b52fc7ef05c701868861fa85609747c9d74a440'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-ppc64le'; 			sha256='c5ef8012f48a518e1c235ad408d26cd424d7b5fa87eaf78cb2ff4b9048730120'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-riscv64'; 			sha256='80b27d5f3a346591a5045b81217ee5be578ed151ef8cbd883a892c0ec0ac33f1'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-s390x'; 			sha256='04f5bd0d389f682c7e9287a3b3a1777b0848f8e10d58cbf9d4d12c9002bbb378'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 19 May 2026 18:52:17 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Tue, 19 May 2026 18:52:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 19 May 2026 18:52:18 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 19 May 2026 18:52:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 18:52:18 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 19 May 2026 18:52:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 19 May 2026 18:52:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 May 2026 18:52:18 GMT
CMD ["sh"]
# Tue, 19 May 2026 19:11:28 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 19 May 2026 19:11:28 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 19 May 2026 19:11:29 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 19 May 2026 19:11:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 19 May 2026 19:11:31 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 19 May 2026 19:11:31 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 19 May 2026 19:11:31 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 19:11:31 GMT
VOLUME [/var/lib/docker]
# Tue, 19 May 2026 19:11:31 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 19 May 2026 19:11:31 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 19 May 2026 19:11:31 GMT
CMD []
# Tue, 19 May 2026 20:10:18 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Tue, 19 May 2026 20:10:18 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 19 May 2026 20:10:18 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 19 May 2026 20:10:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 	; 	rm rootless.tgz; 		rootlesskit --version # buildkit
# Tue, 19 May 2026 20:10:18 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 19 May 2026 20:10:18 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 19 May 2026 20:10:18 GMT
USER rootless
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:439c73b6370f92c891e3dae2ef2ac51ba47633f4382e93fa3a194ab6c9929fcf`  
		Last Modified: Tue, 19 May 2026 18:52:24 GMT  
		Size: 8.4 MB (8368378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:090f26860bbcb42203be1c1ccc78e592537b7d5076712eddc078a4521b65b6ef`  
		Last Modified: Tue, 19 May 2026 18:52:23 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02fa5c43148b510203ce86fd309a24339439966d97d2739e5681dea9fbedd78b`  
		Last Modified: Tue, 19 May 2026 18:52:24 GMT  
		Size: 18.0 MB (18003824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:179aebd9e04e34e062d99c03bced083b59894f9ff9c70a48e5fdde05043d0662`  
		Last Modified: Tue, 19 May 2026 18:52:25 GMT  
		Size: 20.8 MB (20815342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333ebd0d3068df15ad94c847b40ac364dc7140981f38d3a8f08165ef3fe528ac`  
		Last Modified: Tue, 19 May 2026 18:52:25 GMT  
		Size: 10.2 MB (10243275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e7cd72262f0dcb67fc210c582e3d890f8da6bbfea7979a4af0eca2d85493c8`  
		Last Modified: Tue, 19 May 2026 18:52:25 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb8c848507ade63fa035c4247243268bc78609cb843c2c46923fec82cf42e856`  
		Last Modified: Tue, 19 May 2026 18:52:26 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14678f991761f143ab6345db5de4a84ca5f83a1cd44f7d579a88be20ad20871`  
		Last Modified: Tue, 19 May 2026 18:52:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deb061c465c1d4b2683f89277bb8b93644ad86d3b6a034d3848e218ff3a36250`  
		Last Modified: Tue, 19 May 2026 19:11:41 GMT  
		Size: 7.2 MB (7219902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408cc9607ded7836e6377a9012f389a02da93bc2526404ac2125d556fed0607c`  
		Last Modified: Tue, 19 May 2026 19:11:41 GMT  
		Size: 100.9 KB (100930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4813a99698e1ee0cbb52b02f822e9732eb9144586aa3c765fee806857d8cb872`  
		Last Modified: Tue, 19 May 2026 19:11:41 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f364d3985b9e2a29ae89857aa654e13a752db4b807f58b23afc56a7fdddc9ca`  
		Last Modified: Tue, 19 May 2026 19:11:43 GMT  
		Size: 62.1 MB (62129257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34b8039e34935754bb978ab40f852eeb6345408e37deb40c0467f77421c8252`  
		Last Modified: Tue, 19 May 2026 19:11:42 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be12674817c3cc5397950df61ba9f0761de7cbb67e7527d120f671791e1644f9`  
		Last Modified: Tue, 19 May 2026 19:11:42 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e2794603590245d075eed606ac34301c58fda88a8a80f4eaa3ffce3d78a905`  
		Last Modified: Tue, 19 May 2026 20:10:24 GMT  
		Size: 3.4 MB (3394549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afc77214cc9ebf151912fa095a575ef37f668cb6338ba1a94904c1edaf262ceb`  
		Last Modified: Tue, 19 May 2026 20:10:24 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ead735ef17a546ca40080e700f3c11ff2c11b5cdc13bafd2c98e028f26c5940`  
		Last Modified: Tue, 19 May 2026 20:10:24 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51aaf502457f6ce01bba562fab571d3a6ae959cb483cd95636a71243072df558`  
		Last Modified: Tue, 19 May 2026 20:10:24 GMT  
		Size: 11.2 MB (11236521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b0ca64e0e966609139e6199a7a8b766c498d0350d644cd8d18ab622a42d3fc9`  
		Last Modified: Tue, 19 May 2026 20:10:25 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:4fe949a9f9e01f26d41d7540737c598ccada6b62562db26845b13a0cf57f124a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 KB (30663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d49dc7a383ab1fdb7ccd92405afa131cc367a1c519e6a245d1ff68df7e85a66`

```dockerfile
```

-	Layers:
	-	`sha256:e83fa8083ea898497b6c983d8641259136e040f0b533861df142a73520bda5fe`  
		Last Modified: Tue, 19 May 2026 20:10:23 GMT  
		Size: 30.7 KB (30663 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:latest`

```console
$ docker pull docker@sha256:eed377f3ce14afda560e742c5b3ae446df1ce00a16e1beab2ac6c78c1477fe85
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
$ docker pull docker@sha256:6f156e0882b6f307bcd00e01b7abebdccf6eb96b1bb40e8b160e3e401ba3749b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.7 MB (141660887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a475a10539689996453c7c7aa57795a1c35cb8da621faddaef1fb0f05cdb7723`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Tue, 19 May 2026 18:43:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 19 May 2026 18:43:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 19 May 2026 18:43:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 19 May 2026 18:43:53 GMT
ENV DOCKER_VERSION=29.5.1
# Tue, 19 May 2026 18:43:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 19 May 2026 18:43:53 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Tue, 19 May 2026 18:43:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-amd64'; 			sha256='0144479d5a1cd710be3464ae898628cfa68033e16b225aef52f81930c45ac9b5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v6'; 			sha256='1f34337385921c5da43d63452282726b062aa887fda975f96dd3d6e869648bc6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v7'; 			sha256='3560b5b6fd3485f4d0bd160e7edf56cc1f08f0cb5852c9af28bf3fab9973c7c2'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm64'; 			sha256='565605fe0bb393ed5d11771e5b52fc7ef05c701868861fa85609747c9d74a440'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-ppc64le'; 			sha256='c5ef8012f48a518e1c235ad408d26cd424d7b5fa87eaf78cb2ff4b9048730120'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-riscv64'; 			sha256='80b27d5f3a346591a5045b81217ee5be578ed151ef8cbd883a892c0ec0ac33f1'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-s390x'; 			sha256='04f5bd0d389f682c7e9287a3b3a1777b0848f8e10d58cbf9d4d12c9002bbb378'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 19 May 2026 18:43:54 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Tue, 19 May 2026 18:43:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 19 May 2026 18:43:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 19 May 2026 18:43:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 18:43:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 19 May 2026 18:43:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 19 May 2026 18:43:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 May 2026 18:43:55 GMT
CMD ["sh"]
# Tue, 19 May 2026 18:52:09 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 19 May 2026 18:52:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 19 May 2026 18:52:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 19 May 2026 18:52:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 19 May 2026 18:52:13 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 19 May 2026 18:52:13 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 19 May 2026 18:52:13 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 18:52:13 GMT
VOLUME [/var/lib/docker]
# Tue, 19 May 2026 18:52:13 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 19 May 2026 18:52:13 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 19 May 2026 18:52:13 GMT
CMD []
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959d822c11f4cffde22f6a8ca77070ab678788ee8a60e50bf52240fab7600d55`  
		Last Modified: Tue, 19 May 2026 18:44:02 GMT  
		Size: 8.3 MB (8311621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf748eeffe46320957e43a6d041504e02f6d54efaa90b05ea0a5e76259a3bc9`  
		Last Modified: Tue, 19 May 2026 18:44:01 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29db3e4d2cf2bffd95a0b8c095c0dfc7f4b6ee9717169afb9c613ae0714f22a5`  
		Last Modified: Tue, 19 May 2026 18:44:03 GMT  
		Size: 19.5 MB (19549501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:418895c8a0097a67712f5b2385b094ed4ed5af1359b9b43cb86c07da48ca11c9`  
		Last Modified: Tue, 19 May 2026 18:44:03 GMT  
		Size: 23.0 MB (22988580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4382b5de8ae74e74d495d9d94f0127cf051728dc00cab26dfa163bba8cdbcf13`  
		Last Modified: Tue, 19 May 2026 18:44:03 GMT  
		Size: 11.2 MB (11243752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53914aaed626c98320ff52b5bbe81eb804e9a82d445d07a5908e16e86ac5a5c`  
		Last Modified: Tue, 19 May 2026 18:44:03 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cac0928dd7f6aa6c83aa987350f200df21db15618f2ba47912f35be2b16b3b9`  
		Last Modified: Tue, 19 May 2026 18:44:04 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1c069fc81d4d790f039a7a8160f23dffa6c11a22ee385a0db0fe75ae235dfe1`  
		Last Modified: Tue, 19 May 2026 18:44:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27817872a6ae6fcf22af6f3dbdec0f52f7b055d8b3384cd5b922f74d11358249`  
		Last Modified: Tue, 19 May 2026 18:52:23 GMT  
		Size: 6.9 MB (6941424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a7ba7363a81328286ac28be79b6e6248a1e1c4cb3f1749b808bc8abeb5c686`  
		Last Modified: Tue, 19 May 2026 18:52:23 GMT  
		Size: 92.2 KB (92218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f90442d3c5cd85fdf0fd4683516f39486a803bd57eb9813b3dcb939d9d3fcc`  
		Last Modified: Tue, 19 May 2026 18:52:23 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c588cc6d3552d3ec8363fa8dabb97cfe3ea467efd07c37c45853267ab5c544`  
		Last Modified: Tue, 19 May 2026 18:52:25 GMT  
		Size: 68.7 MB (68661447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa91ecdbc2c72221f7c567a768c787e9b0e27629ad60fecaa37b420555dbec4`  
		Last Modified: Tue, 19 May 2026 18:52:24 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a04f224ef5d78ccf3d32a655e7621773237de1ba0a09780d2011e4e3efc9802`  
		Last Modified: Tue, 19 May 2026 18:52:25 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:8459bca25b1862c9c244d8290b9c289f8f38a28e911360560cef489552fd9996
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca9c00d43298e9a165fe521202b47e762e0e30cdaad754b907fb2241affba41a`

```dockerfile
```

-	Layers:
	-	`sha256:725c95ff8cee96878c88b2d98ed922fc03f42a86c848e44ace4d3602cca233bd`  
		Last Modified: Tue, 19 May 2026 18:52:23 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v6

```console
$ docker pull docker@sha256:656cd6a2deb516bf1bab86d4eb9e0ea9b2afca3fb8c81a402195068521496791
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.6 MB (133554774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b375b41ebcd63fd76689fd0c53d0cbebdb1c6086df5568f03b1342739485d2f4`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Tue, 19 May 2026 18:46:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 19 May 2026 18:46:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 19 May 2026 18:46:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 19 May 2026 18:46:29 GMT
ENV DOCKER_VERSION=29.5.1
# Tue, 19 May 2026 18:46:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 19 May 2026 18:46:29 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Tue, 19 May 2026 18:46:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-amd64'; 			sha256='0144479d5a1cd710be3464ae898628cfa68033e16b225aef52f81930c45ac9b5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v6'; 			sha256='1f34337385921c5da43d63452282726b062aa887fda975f96dd3d6e869648bc6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v7'; 			sha256='3560b5b6fd3485f4d0bd160e7edf56cc1f08f0cb5852c9af28bf3fab9973c7c2'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm64'; 			sha256='565605fe0bb393ed5d11771e5b52fc7ef05c701868861fa85609747c9d74a440'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-ppc64le'; 			sha256='c5ef8012f48a518e1c235ad408d26cd424d7b5fa87eaf78cb2ff4b9048730120'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-riscv64'; 			sha256='80b27d5f3a346591a5045b81217ee5be578ed151ef8cbd883a892c0ec0ac33f1'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-s390x'; 			sha256='04f5bd0d389f682c7e9287a3b3a1777b0848f8e10d58cbf9d4d12c9002bbb378'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 19 May 2026 18:46:32 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Tue, 19 May 2026 18:46:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 19 May 2026 18:46:33 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 19 May 2026 18:46:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 18:46:33 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 19 May 2026 18:46:34 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 19 May 2026 18:46:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 May 2026 18:46:34 GMT
CMD ["sh"]
# Tue, 19 May 2026 18:48:00 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 19 May 2026 18:48:00 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 19 May 2026 18:48:00 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 19 May 2026 18:48:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 19 May 2026 18:48:04 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 19 May 2026 18:48:04 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 19 May 2026 18:48:04 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 18:48:04 GMT
VOLUME [/var/lib/docker]
# Tue, 19 May 2026 18:48:04 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 19 May 2026 18:48:04 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 19 May 2026 18:48:04 GMT
CMD []
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e510993d358b2182e33432b09c723cb2de90442627624e753d33ff6f58e37cf`  
		Last Modified: Tue, 19 May 2026 18:46:40 GMT  
		Size: 8.2 MB (8211856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac6422e386e61fe4ba4eb1abca9f67aef1bba270f947f3797505168eddc865ef`  
		Last Modified: Tue, 19 May 2026 18:46:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c6104ecd7c2122cba9eadf591b901752e839d28c94e9786023634ab16c4e86`  
		Last Modified: Tue, 19 May 2026 18:46:41 GMT  
		Size: 18.2 MB (18183185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9278a90d0e78f94da7f59f70fe4811830047483868d42c4e25a85b91a3359765`  
		Last Modified: Tue, 19 May 2026 18:46:41 GMT  
		Size: 21.6 MB (21614147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09f94e1195a7d62fc4046fa609e325b2001195cf49352924129c45728445d565`  
		Last Modified: Tue, 19 May 2026 18:46:41 GMT  
		Size: 10.7 MB (10650824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a8126c2985de246f1344d8c4340e5934b14cdf06f269351c0bfeac534be4c3a`  
		Last Modified: Tue, 19 May 2026 18:46:41 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f13c028f2e167a9ccd442fe69b89b5f1ca9e19f4589d7160d5af4d3b451ba862`  
		Last Modified: Tue, 19 May 2026 18:46:42 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa9769c6262cc549e78864817d114f4780b6b611ff08c097bcb018ab9040fd0`  
		Last Modified: Tue, 19 May 2026 18:46:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:125e5e8c972742a3fdece68d1d7efe160fc572758035dc6dd440150a5dff5bf7`  
		Last Modified: Tue, 19 May 2026 18:48:15 GMT  
		Size: 7.3 MB (7278661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:092dd15fda2f6f91745deb58f699d28c2ae054d7fb4d6c4100b53f0f8e3a6d85`  
		Last Modified: Tue, 19 May 2026 18:48:15 GMT  
		Size: 91.5 KB (91516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc718ec10edd9882bc794dfec135ed20f43243a8db5ad70f2ca75ac4b4191815`  
		Last Modified: Tue, 19 May 2026 18:48:15 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf390f2615c4c05543ef083213b7da580fc3a675929438042a5228503644f65`  
		Last Modified: Tue, 19 May 2026 18:48:17 GMT  
		Size: 63.9 MB (63944568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0111492ca1c0d70617ea1ed481e8ae4908695479c10dc5b86fe761dd03edc6b`  
		Last Modified: Tue, 19 May 2026 18:48:16 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b88ff88aa94e286fad9d8f3480fb92ba8ec324a9d55d74cce8cce2e99c36353`  
		Last Modified: Tue, 19 May 2026 18:48:16 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:1fd6b9654a40244c2a32a42dfdbd4b0c2fcd97aaacc719b9c466fed8008b0c05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e4f0d6a13a6e324e492f0fd9ae8856d26b30b034d24e9b3868069907c61ec10`

```dockerfile
```

-	Layers:
	-	`sha256:096e9d4d3b5e87687de3559cc60228911d8179792add0ad0a60e1afd76f2b032`  
		Last Modified: Tue, 19 May 2026 18:48:14 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v7

```console
$ docker pull docker@sha256:ce68e53519cdc94c6b28b82b2e4af1856aa5dd8e577fb872900952a6ed88f9d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.7 MB (131668449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bc263b60a94589a9d3f238ee64951d8f806cc46c8caed0452715d45111a5b91`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Tue, 19 May 2026 18:50:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 19 May 2026 18:50:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 19 May 2026 18:50:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 19 May 2026 18:50:21 GMT
ENV DOCKER_VERSION=29.5.1
# Tue, 19 May 2026 18:50:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 19 May 2026 18:50:21 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Tue, 19 May 2026 18:50:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-amd64'; 			sha256='0144479d5a1cd710be3464ae898628cfa68033e16b225aef52f81930c45ac9b5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v6'; 			sha256='1f34337385921c5da43d63452282726b062aa887fda975f96dd3d6e869648bc6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v7'; 			sha256='3560b5b6fd3485f4d0bd160e7edf56cc1f08f0cb5852c9af28bf3fab9973c7c2'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm64'; 			sha256='565605fe0bb393ed5d11771e5b52fc7ef05c701868861fa85609747c9d74a440'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-ppc64le'; 			sha256='c5ef8012f48a518e1c235ad408d26cd424d7b5fa87eaf78cb2ff4b9048730120'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-riscv64'; 			sha256='80b27d5f3a346591a5045b81217ee5be578ed151ef8cbd883a892c0ec0ac33f1'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-s390x'; 			sha256='04f5bd0d389f682c7e9287a3b3a1777b0848f8e10d58cbf9d4d12c9002bbb378'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 19 May 2026 18:50:23 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Tue, 19 May 2026 18:50:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 19 May 2026 18:50:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 19 May 2026 18:50:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 18:50:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 19 May 2026 18:50:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 19 May 2026 18:50:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 May 2026 18:50:24 GMT
CMD ["sh"]
# Tue, 19 May 2026 19:11:05 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 19 May 2026 19:11:05 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 19 May 2026 19:11:05 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 19 May 2026 19:11:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 19 May 2026 19:11:10 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 19 May 2026 19:11:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 19 May 2026 19:11:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 19:11:10 GMT
VOLUME [/var/lib/docker]
# Tue, 19 May 2026 19:11:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 19 May 2026 19:11:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 19 May 2026 19:11:10 GMT
CMD []
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e78396f075a6021fa389cbab78d2b7a97c1fa6ccd90c5a3f9aad13a82d9a82d5`  
		Last Modified: Tue, 19 May 2026 18:50:31 GMT  
		Size: 7.5 MB (7520541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55503681071acc50ecd4d54f1a76c32b34fb2e24b116717b8a11a5ed2c4b834b`  
		Last Modified: Tue, 19 May 2026 18:50:30 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:139bfdfb0c5a911c258bd9ca3f33e5d74dc4cdac244e701ffc230dfb2dbcf299`  
		Last Modified: Tue, 19 May 2026 18:50:31 GMT  
		Size: 18.2 MB (18172268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e28d126c0c15c1ddece42e48d16b7989f46d4ba83543ade587e34aae442b162d`  
		Last Modified: Tue, 19 May 2026 18:50:31 GMT  
		Size: 21.6 MB (21600397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb484c140400a96468ac162a856058550dff5319ecf84cb2d15485ffa462cfe5`  
		Last Modified: Tue, 19 May 2026 18:50:31 GMT  
		Size: 10.6 MB (10637143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:458ff3d79525d794f095fe12c99f3a95a84e674163d4ac75823a6bbe91cdca6c`  
		Last Modified: Tue, 19 May 2026 18:50:32 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:252522a027743939f7b115d2d3929238ba7a8fee776336371433d62e17da49f3`  
		Last Modified: Tue, 19 May 2026 18:50:33 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b1fd0762adb2df9e41385aaea4f5aeb069ccb43ec6a5203c0970dbb32f5d39`  
		Last Modified: Tue, 19 May 2026 18:50:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2404388a95cbd53c2924a8956a2b0bd9fed1ed42798ef0d7958645ec50b36503`  
		Last Modified: Tue, 19 May 2026 19:11:21 GMT  
		Size: 6.6 MB (6577150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abebc77c5a81c02e559a6177ab009ea93d155d230027ecb011d71caf8e1319cb`  
		Last Modified: Tue, 19 May 2026 19:11:20 GMT  
		Size: 87.8 KB (87825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:505cb9808a455382b226432bd33efca0786f2b2817e3828966e8ae1880b9a387`  
		Last Modified: Tue, 19 May 2026 19:11:20 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb736cbd14a0b4279f19088aba50827f55f5bd8c64dd5868c81329ee396e19f`  
		Last Modified: Tue, 19 May 2026 19:11:23 GMT  
		Size: 63.8 MB (63781847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b8e0456f81c21846bbc1e4af0c8ce599dde97bbda1d981de3f47999ce045a4`  
		Last Modified: Tue, 19 May 2026 19:11:22 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10bd67dffac6bb7c60a61f90d9e059f51d217061b38efadfa05cfbccc501c4eb`  
		Last Modified: Tue, 19 May 2026 19:11:22 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:38aff3f9f68bc80866a840b6895120e3efd20f227f69ca66663fee2a5c143d5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e771280fb8341ddf485470385301e8a4df555c4889817952e2e3f1bc2d60f3f`

```dockerfile
```

-	Layers:
	-	`sha256:0f43b1170bad091b1f8a038b4c799e044dcbe62f3cf88792df12fd3808abd3db`  
		Last Modified: Tue, 19 May 2026 19:11:20 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:d29f00616a4b5af545c6238d5e5d3f010dabe8cd9373464e7528dcc2ffe932e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.1 MB (131088931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d59db2bca67549c508438fad529bbb4d973798fdf3dac19d4cff714cd0ef24d8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Tue, 19 May 2026 18:52:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 19 May 2026 18:52:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 19 May 2026 18:52:13 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 19 May 2026 18:52:16 GMT
ENV DOCKER_VERSION=29.5.1
# Tue, 19 May 2026 18:52:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 19 May 2026 18:52:16 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Tue, 19 May 2026 18:52:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-amd64'; 			sha256='0144479d5a1cd710be3464ae898628cfa68033e16b225aef52f81930c45ac9b5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v6'; 			sha256='1f34337385921c5da43d63452282726b062aa887fda975f96dd3d6e869648bc6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v7'; 			sha256='3560b5b6fd3485f4d0bd160e7edf56cc1f08f0cb5852c9af28bf3fab9973c7c2'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm64'; 			sha256='565605fe0bb393ed5d11771e5b52fc7ef05c701868861fa85609747c9d74a440'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-ppc64le'; 			sha256='c5ef8012f48a518e1c235ad408d26cd424d7b5fa87eaf78cb2ff4b9048730120'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-riscv64'; 			sha256='80b27d5f3a346591a5045b81217ee5be578ed151ef8cbd883a892c0ec0ac33f1'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-s390x'; 			sha256='04f5bd0d389f682c7e9287a3b3a1777b0848f8e10d58cbf9d4d12c9002bbb378'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 19 May 2026 18:52:17 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Tue, 19 May 2026 18:52:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 19 May 2026 18:52:18 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 19 May 2026 18:52:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 18:52:18 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 19 May 2026 18:52:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 19 May 2026 18:52:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 May 2026 18:52:18 GMT
CMD ["sh"]
# Tue, 19 May 2026 19:11:28 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 19 May 2026 19:11:28 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 19 May 2026 19:11:29 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 19 May 2026 19:11:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 19 May 2026 19:11:31 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 19 May 2026 19:11:31 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 19 May 2026 19:11:31 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 19:11:31 GMT
VOLUME [/var/lib/docker]
# Tue, 19 May 2026 19:11:31 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 19 May 2026 19:11:31 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 19 May 2026 19:11:31 GMT
CMD []
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:439c73b6370f92c891e3dae2ef2ac51ba47633f4382e93fa3a194ab6c9929fcf`  
		Last Modified: Tue, 19 May 2026 18:52:24 GMT  
		Size: 8.4 MB (8368378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:090f26860bbcb42203be1c1ccc78e592537b7d5076712eddc078a4521b65b6ef`  
		Last Modified: Tue, 19 May 2026 18:52:23 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02fa5c43148b510203ce86fd309a24339439966d97d2739e5681dea9fbedd78b`  
		Last Modified: Tue, 19 May 2026 18:52:24 GMT  
		Size: 18.0 MB (18003824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:179aebd9e04e34e062d99c03bced083b59894f9ff9c70a48e5fdde05043d0662`  
		Last Modified: Tue, 19 May 2026 18:52:25 GMT  
		Size: 20.8 MB (20815342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333ebd0d3068df15ad94c847b40ac364dc7140981f38d3a8f08165ef3fe528ac`  
		Last Modified: Tue, 19 May 2026 18:52:25 GMT  
		Size: 10.2 MB (10243275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e7cd72262f0dcb67fc210c582e3d890f8da6bbfea7979a4af0eca2d85493c8`  
		Last Modified: Tue, 19 May 2026 18:52:25 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb8c848507ade63fa035c4247243268bc78609cb843c2c46923fec82cf42e856`  
		Last Modified: Tue, 19 May 2026 18:52:26 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14678f991761f143ab6345db5de4a84ca5f83a1cd44f7d579a88be20ad20871`  
		Last Modified: Tue, 19 May 2026 18:52:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deb061c465c1d4b2683f89277bb8b93644ad86d3b6a034d3848e218ff3a36250`  
		Last Modified: Tue, 19 May 2026 19:11:41 GMT  
		Size: 7.2 MB (7219902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408cc9607ded7836e6377a9012f389a02da93bc2526404ac2125d556fed0607c`  
		Last Modified: Tue, 19 May 2026 19:11:41 GMT  
		Size: 100.9 KB (100930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4813a99698e1ee0cbb52b02f822e9732eb9144586aa3c765fee806857d8cb872`  
		Last Modified: Tue, 19 May 2026 19:11:41 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f364d3985b9e2a29ae89857aa654e13a752db4b807f58b23afc56a7fdddc9ca`  
		Last Modified: Tue, 19 May 2026 19:11:43 GMT  
		Size: 62.1 MB (62129257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34b8039e34935754bb978ab40f852eeb6345408e37deb40c0467f77421c8252`  
		Last Modified: Tue, 19 May 2026 19:11:42 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be12674817c3cc5397950df61ba9f0761de7cbb67e7527d120f671791e1644f9`  
		Last Modified: Tue, 19 May 2026 19:11:42 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:8ac585f5eb9117c0193cbfc718548d3dca67a7e669159a6b08a53ae907925d21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa5bac19b0eae7a6debca0657ab9da39a1528d516c371778235e72d5db216621`

```dockerfile
```

-	Layers:
	-	`sha256:662dc4eaa00e9b2353b08fdbf55f624046c556fe7fa5b07f0332cfd3384d50fb`  
		Last Modified: Tue, 19 May 2026 19:11:40 GMT  
		Size: 34.8 KB (34782 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:windowsservercore`

```console
$ docker pull docker@sha256:76a2595299d5d831461bbff176d00c8005cc1b58a48fe70127d90155b250253f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32860; amd64
	-	windows version 10.0.20348.5139; amd64

### `docker:windowsservercore` - windows version 10.0.26100.32860; amd64

```console
$ docker pull docker@sha256:189f1d53b9d0831a7663f55ac4dfcfe317baa879af86a90a44e1c83e9f9fbf6a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2262683896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c993dcdab4e74415b546e3486a219f555369a5b9db18c96ed98e36915f6572`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 10 May 2026 10:08:54 GMT
RUN Install update 10.0.26100.32860
# Thu, 21 May 2026 23:13:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 21 May 2026 23:15:10 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 21 May 2026 23:15:11 GMT
ENV DOCKER_VERSION=29.5.2
# Thu, 21 May 2026 23:15:13 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.5.2.zip
# Thu, 21 May 2026 23:15:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 21 May 2026 23:15:38 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 21 May 2026 23:15:39 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.windows-amd64.exe
# Thu, 21 May 2026 23:15:39 GMT
ENV DOCKER_BUILDX_SHA256=41e1b3fff6541d5f5febb18ff4c9108bec30afd7bf9133b82783735c2078eac1
# Thu, 21 May 2026 23:15:58 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 21 May 2026 23:15:58 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 21 May 2026 23:15:59 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-windows-x86_64.exe
# Thu, 21 May 2026 23:16:00 GMT
ENV DOCKER_COMPOSE_SHA256=e1a8faff28c7433635201a2222171b727f33ecdb0ed367e54d162d00432f39aa
# Thu, 21 May 2026 23:16:10 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f787ad06f38db673c3d304f21c09a82ff9a1ced32062515ea52fdb0383457b24`  
		Last Modified: Tue, 12 May 2026 18:03:01 GMT  
		Size: 682.9 MB (682882530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c26092efbc05ba0447d81394df46314e3b86ab224685126b2d6dfd994d4dc11`  
		Last Modified: Thu, 21 May 2026 23:16:20 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83ade171b063bb36658cc0d1e2c9c6cb333ea25a3ad1e4129615adf825b64a46`  
		Last Modified: Thu, 21 May 2026 23:16:20 GMT  
		Size: 406.4 KB (406376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78577312456309bc4fe740995c1663317c15ecc17bcedded51adf9a9982366ca`  
		Last Modified: Thu, 21 May 2026 23:16:18 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee76c01ce753f169a4b6e55abafceb2769603948efcc72907de3e6aeb33cce42`  
		Last Modified: Thu, 21 May 2026 23:16:18 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc27681d28a3246dcf30c481b3852d6dbdc170d9cf5b284e019a90ade4d9cee8`  
		Last Modified: Thu, 21 May 2026 23:16:21 GMT  
		Size: 20.3 MB (20271957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c75db7b4635a1d76c37b80319e3dd1bdff20dd7ef77265097ecdb2861b340b99`  
		Last Modified: Thu, 21 May 2026 23:16:17 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48d982239ff1380cf0818ab9cc60083eac7f15cd44054f9f67433be9035d8a31`  
		Last Modified: Thu, 21 May 2026 23:16:17 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c096a591d4ea5f003d7be2a803cf5e81d42655e886b4df3ea31db5ab4f1289f`  
		Last Modified: Thu, 21 May 2026 23:16:17 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f795f325466c0a11f5a6c88330d8ab8b3fcad025e8fc95a56b3cc2d15f7884bb`  
		Last Modified: Thu, 21 May 2026 23:16:32 GMT  
		Size: 23.9 MB (23933638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b824c613a9ba32b1fcec65a639d38947346d62eddad555e9a7e295010f6937d`  
		Last Modified: Thu, 21 May 2026 23:16:15 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62db1e13ba58abbe1229ca941f68bceaa49a84ce729b12c843e3c1914052407d`  
		Last Modified: Thu, 21 May 2026 23:16:15 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7286144ed984b89e44b176cd42f189f5d30dc6bdd1357032bbb549bb0c96975`  
		Last Modified: Thu, 21 May 2026 23:16:15 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8922b65b3736da43bcb9ea86b5abf5ea19ee56a9c642200696decef2214beb0`  
		Last Modified: Thu, 21 May 2026 23:16:17 GMT  
		Size: 12.1 MB (12118551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.20348.5139; amd64

```console
$ docker pull docker@sha256:fecc0a5137c67dad8b14e94db06043867e6b74bb784840642f699cfd8d9abe16
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2179150500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52496b21f2e24bac1a6601b61b2de6417374b43f89a6f9cfd8eefedf65fdd4a7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Thu, 21 May 2026 23:37:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 21 May 2026 23:38:14 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 21 May 2026 23:38:15 GMT
ENV DOCKER_VERSION=29.5.2
# Thu, 21 May 2026 23:38:17 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.5.2.zip
# Thu, 21 May 2026 23:38:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 21 May 2026 23:38:44 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 21 May 2026 23:38:45 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.windows-amd64.exe
# Thu, 21 May 2026 23:38:46 GMT
ENV DOCKER_BUILDX_SHA256=41e1b3fff6541d5f5febb18ff4c9108bec30afd7bf9133b82783735c2078eac1
# Thu, 21 May 2026 23:39:10 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 21 May 2026 23:39:11 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 21 May 2026 23:39:12 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-windows-x86_64.exe
# Thu, 21 May 2026 23:39:13 GMT
ENV DOCKER_COMPOSE_SHA256=e1a8faff28c7433635201a2222171b727f33ecdb0ed367e54d162d00432f39aa
# Thu, 21 May 2026 23:39:31 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857865ad3eca4da109d969134a9cab7225d9de49597914ae325d43661900f513`  
		Last Modified: Tue, 12 May 2026 17:34:16 GMT  
		Size: 633.4 MB (633401492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17fd8e1d39e88259a0e6383034d2a7ad6d90356547cec5bbbf94f3a3e0afc763`  
		Last Modified: Thu, 21 May 2026 23:39:40 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1756702264897e3d6bb006dbce5e5260ae7bc8fa54384b6a031c460ac01476e`  
		Last Modified: Thu, 21 May 2026 23:39:39 GMT  
		Size: 505.7 KB (505666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da4ab93ed88956a88f0eb095aaf8977d5b9bbba18d08b7757eb1ccff28e80d2a`  
		Last Modified: Thu, 21 May 2026 23:39:39 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c2528cc62d1c88f5003aa2f0b62055544c66be0ec0d65cf6a8550455e0747`  
		Last Modified: Thu, 21 May 2026 23:39:38 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e531632899bf060a3ff8e9b29f0c3c81b857c0b311b97f241e35d94ffe66d3cb`  
		Last Modified: Thu, 21 May 2026 23:39:41 GMT  
		Size: 20.2 MB (20231436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34d5b3db47edaa5e44e34cad2ba31b4be5c5b6c483cef5a09b33460c4747302`  
		Last Modified: Thu, 21 May 2026 23:39:37 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:751d900578d8658aa1097acdfcd5f97aff829261a5e29a8f16b2f40effa4f532`  
		Last Modified: Thu, 21 May 2026 23:39:37 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eeb843d181536cfa4d4d838d626f63e191094c2468d26f3d0330a50f2b526c4`  
		Last Modified: Thu, 21 May 2026 23:39:37 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b58742ef314900bc96dda8fc677f8a1b98faf7970eb6fa39992b3a0150a7d36`  
		Last Modified: Thu, 21 May 2026 23:39:51 GMT  
		Size: 23.9 MB (23901391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:435a34db22345529d906d3448943e90cfc37ae51e15ea8ec70cd87e01c5b16d8`  
		Last Modified: Thu, 21 May 2026 23:39:35 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1f19e0160f0c9a3c97ced5e763b905a949f0f5af2882f68638e276a43a62af`  
		Last Modified: Thu, 21 May 2026 23:39:35 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60db139392fbadfa06ac3c12862fab33f209dc6d2a7f076d7d0b52eec402dc3b`  
		Last Modified: Thu, 21 May 2026 23:39:35 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ddde0e1dba54298e42dcefa7d09742c8714bba4bc7d5a59eb1950f87975208`  
		Last Modified: Thu, 21 May 2026 23:39:37 GMT  
		Size: 12.1 MB (12079670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:45ff7aebeb53a14d066b607ae70acc6e3ca4f3cc6835a76438078df370c9857f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull docker@sha256:fecc0a5137c67dad8b14e94db06043867e6b74bb784840642f699cfd8d9abe16
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2179150500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52496b21f2e24bac1a6601b61b2de6417374b43f89a6f9cfd8eefedf65fdd4a7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Thu, 21 May 2026 23:37:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 21 May 2026 23:38:14 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 21 May 2026 23:38:15 GMT
ENV DOCKER_VERSION=29.5.2
# Thu, 21 May 2026 23:38:17 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.5.2.zip
# Thu, 21 May 2026 23:38:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 21 May 2026 23:38:44 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 21 May 2026 23:38:45 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.windows-amd64.exe
# Thu, 21 May 2026 23:38:46 GMT
ENV DOCKER_BUILDX_SHA256=41e1b3fff6541d5f5febb18ff4c9108bec30afd7bf9133b82783735c2078eac1
# Thu, 21 May 2026 23:39:10 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 21 May 2026 23:39:11 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 21 May 2026 23:39:12 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-windows-x86_64.exe
# Thu, 21 May 2026 23:39:13 GMT
ENV DOCKER_COMPOSE_SHA256=e1a8faff28c7433635201a2222171b727f33ecdb0ed367e54d162d00432f39aa
# Thu, 21 May 2026 23:39:31 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857865ad3eca4da109d969134a9cab7225d9de49597914ae325d43661900f513`  
		Last Modified: Tue, 12 May 2026 17:34:16 GMT  
		Size: 633.4 MB (633401492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17fd8e1d39e88259a0e6383034d2a7ad6d90356547cec5bbbf94f3a3e0afc763`  
		Last Modified: Thu, 21 May 2026 23:39:40 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1756702264897e3d6bb006dbce5e5260ae7bc8fa54384b6a031c460ac01476e`  
		Last Modified: Thu, 21 May 2026 23:39:39 GMT  
		Size: 505.7 KB (505666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da4ab93ed88956a88f0eb095aaf8977d5b9bbba18d08b7757eb1ccff28e80d2a`  
		Last Modified: Thu, 21 May 2026 23:39:39 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c2528cc62d1c88f5003aa2f0b62055544c66be0ec0d65cf6a8550455e0747`  
		Last Modified: Thu, 21 May 2026 23:39:38 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e531632899bf060a3ff8e9b29f0c3c81b857c0b311b97f241e35d94ffe66d3cb`  
		Last Modified: Thu, 21 May 2026 23:39:41 GMT  
		Size: 20.2 MB (20231436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34d5b3db47edaa5e44e34cad2ba31b4be5c5b6c483cef5a09b33460c4747302`  
		Last Modified: Thu, 21 May 2026 23:39:37 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:751d900578d8658aa1097acdfcd5f97aff829261a5e29a8f16b2f40effa4f532`  
		Last Modified: Thu, 21 May 2026 23:39:37 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eeb843d181536cfa4d4d838d626f63e191094c2468d26f3d0330a50f2b526c4`  
		Last Modified: Thu, 21 May 2026 23:39:37 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b58742ef314900bc96dda8fc677f8a1b98faf7970eb6fa39992b3a0150a7d36`  
		Last Modified: Thu, 21 May 2026 23:39:51 GMT  
		Size: 23.9 MB (23901391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:435a34db22345529d906d3448943e90cfc37ae51e15ea8ec70cd87e01c5b16d8`  
		Last Modified: Thu, 21 May 2026 23:39:35 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1f19e0160f0c9a3c97ced5e763b905a949f0f5af2882f68638e276a43a62af`  
		Last Modified: Thu, 21 May 2026 23:39:35 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60db139392fbadfa06ac3c12862fab33f209dc6d2a7f076d7d0b52eec402dc3b`  
		Last Modified: Thu, 21 May 2026 23:39:35 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ddde0e1dba54298e42dcefa7d09742c8714bba4bc7d5a59eb1950f87975208`  
		Last Modified: Thu, 21 May 2026 23:39:37 GMT  
		Size: 12.1 MB (12079670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:38a6d8d2632ca78eb3229980b6b255413aa7fafcf1d3ad906265d8c05df98652
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32860; amd64

### `docker:windowsservercore-ltsc2025` - windows version 10.0.26100.32860; amd64

```console
$ docker pull docker@sha256:189f1d53b9d0831a7663f55ac4dfcfe317baa879af86a90a44e1c83e9f9fbf6a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2262683896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c993dcdab4e74415b546e3486a219f555369a5b9db18c96ed98e36915f6572`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 10 May 2026 10:08:54 GMT
RUN Install update 10.0.26100.32860
# Thu, 21 May 2026 23:13:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 21 May 2026 23:15:10 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 21 May 2026 23:15:11 GMT
ENV DOCKER_VERSION=29.5.2
# Thu, 21 May 2026 23:15:13 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.5.2.zip
# Thu, 21 May 2026 23:15:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 21 May 2026 23:15:38 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 21 May 2026 23:15:39 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.windows-amd64.exe
# Thu, 21 May 2026 23:15:39 GMT
ENV DOCKER_BUILDX_SHA256=41e1b3fff6541d5f5febb18ff4c9108bec30afd7bf9133b82783735c2078eac1
# Thu, 21 May 2026 23:15:58 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 21 May 2026 23:15:58 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 21 May 2026 23:15:59 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-windows-x86_64.exe
# Thu, 21 May 2026 23:16:00 GMT
ENV DOCKER_COMPOSE_SHA256=e1a8faff28c7433635201a2222171b727f33ecdb0ed367e54d162d00432f39aa
# Thu, 21 May 2026 23:16:10 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f787ad06f38db673c3d304f21c09a82ff9a1ced32062515ea52fdb0383457b24`  
		Last Modified: Tue, 12 May 2026 18:03:01 GMT  
		Size: 682.9 MB (682882530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c26092efbc05ba0447d81394df46314e3b86ab224685126b2d6dfd994d4dc11`  
		Last Modified: Thu, 21 May 2026 23:16:20 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83ade171b063bb36658cc0d1e2c9c6cb333ea25a3ad1e4129615adf825b64a46`  
		Last Modified: Thu, 21 May 2026 23:16:20 GMT  
		Size: 406.4 KB (406376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78577312456309bc4fe740995c1663317c15ecc17bcedded51adf9a9982366ca`  
		Last Modified: Thu, 21 May 2026 23:16:18 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee76c01ce753f169a4b6e55abafceb2769603948efcc72907de3e6aeb33cce42`  
		Last Modified: Thu, 21 May 2026 23:16:18 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc27681d28a3246dcf30c481b3852d6dbdc170d9cf5b284e019a90ade4d9cee8`  
		Last Modified: Thu, 21 May 2026 23:16:21 GMT  
		Size: 20.3 MB (20271957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c75db7b4635a1d76c37b80319e3dd1bdff20dd7ef77265097ecdb2861b340b99`  
		Last Modified: Thu, 21 May 2026 23:16:17 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48d982239ff1380cf0818ab9cc60083eac7f15cd44054f9f67433be9035d8a31`  
		Last Modified: Thu, 21 May 2026 23:16:17 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c096a591d4ea5f003d7be2a803cf5e81d42655e886b4df3ea31db5ab4f1289f`  
		Last Modified: Thu, 21 May 2026 23:16:17 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f795f325466c0a11f5a6c88330d8ab8b3fcad025e8fc95a56b3cc2d15f7884bb`  
		Last Modified: Thu, 21 May 2026 23:16:32 GMT  
		Size: 23.9 MB (23933638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b824c613a9ba32b1fcec65a639d38947346d62eddad555e9a7e295010f6937d`  
		Last Modified: Thu, 21 May 2026 23:16:15 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62db1e13ba58abbe1229ca941f68bceaa49a84ce729b12c843e3c1914052407d`  
		Last Modified: Thu, 21 May 2026 23:16:15 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7286144ed984b89e44b176cd42f189f5d30dc6bdd1357032bbb549bb0c96975`  
		Last Modified: Thu, 21 May 2026 23:16:15 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8922b65b3736da43bcb9ea86b5abf5ea19ee56a9c642200696decef2214beb0`  
		Last Modified: Thu, 21 May 2026 23:16:17 GMT  
		Size: 12.1 MB (12118551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
