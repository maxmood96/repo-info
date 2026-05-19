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
-	[`docker:29.5.1`](#docker2951)
-	[`docker:29.5.1-alpine3.23`](#docker2951-alpine323)
-	[`docker:29.5.1-cli`](#docker2951-cli)
-	[`docker:29.5.1-cli-alpine3.23`](#docker2951-cli-alpine323)
-	[`docker:29.5.1-dind`](#docker2951-dind)
-	[`docker:29.5.1-dind-alpine3.23`](#docker2951-dind-alpine323)
-	[`docker:29.5.1-dind-rootless`](#docker2951-dind-rootless)
-	[`docker:29.5.1-windowsservercore`](#docker2951-windowsservercore)
-	[`docker:29.5.1-windowsservercore-ltsc2022`](#docker2951-windowsservercore-ltsc2022)
-	[`docker:29.5.1-windowsservercore-ltsc2025`](#docker2951-windowsservercore-ltsc2025)
-	[`docker:cli`](#dockercli)
-	[`docker:dind`](#dockerdind)
-	[`docker:dind-rootless`](#dockerdind-rootless)
-	[`docker:latest`](#dockerlatest)
-	[`docker:windowsservercore`](#dockerwindowsservercore)
-	[`docker:windowsservercore-ltsc2022`](#dockerwindowsservercore-ltsc2022)
-	[`docker:windowsservercore-ltsc2025`](#dockerwindowsservercore-ltsc2025)

## `docker:29`

```console
$ docker pull docker@sha256:d0c942e5e2c14a74da706cff670ea2449fb57f9bc6abae7164461d0c6322b8b4
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
$ docker pull docker@sha256:74328f9b3824edb27d1c5b57abfa5765aa1742806ad77e3e90b2ee328aba8301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.7 MB (141655694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71837a59b95c3653383ca90ce81fbcee4f34adb0fbbf8b357e75da9affc77579`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Fri, 15 May 2026 22:12:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 15 May 2026 22:12:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 15 May 2026 22:12:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 15 May 2026 22:12:17 GMT
ENV DOCKER_VERSION=29.5.0
# Fri, 15 May 2026 22:12:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 15 May 2026 22:12:17 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Fri, 15 May 2026 22:12:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-amd64'; 			sha256='0144479d5a1cd710be3464ae898628cfa68033e16b225aef52f81930c45ac9b5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v6'; 			sha256='1f34337385921c5da43d63452282726b062aa887fda975f96dd3d6e869648bc6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v7'; 			sha256='3560b5b6fd3485f4d0bd160e7edf56cc1f08f0cb5852c9af28bf3fab9973c7c2'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm64'; 			sha256='565605fe0bb393ed5d11771e5b52fc7ef05c701868861fa85609747c9d74a440'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-ppc64le'; 			sha256='c5ef8012f48a518e1c235ad408d26cd424d7b5fa87eaf78cb2ff4b9048730120'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-riscv64'; 			sha256='80b27d5f3a346591a5045b81217ee5be578ed151ef8cbd883a892c0ec0ac33f1'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-s390x'; 			sha256='04f5bd0d389f682c7e9287a3b3a1777b0848f8e10d58cbf9d4d12c9002bbb378'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 15 May 2026 22:12:18 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Fri, 15 May 2026 22:12:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 15 May 2026 22:12:19 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 15 May 2026 22:12:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 22:12:19 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 15 May 2026 22:12:19 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 15 May 2026 22:12:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2026 22:12:19 GMT
CMD ["sh"]
# Fri, 15 May 2026 22:45:52 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 15 May 2026 22:45:52 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 15 May 2026 22:45:52 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 15 May 2026 22:45:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 15 May 2026 22:45:55 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 15 May 2026 22:45:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 15 May 2026 22:45:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 22:45:55 GMT
VOLUME [/var/lib/docker]
# Fri, 15 May 2026 22:45:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 15 May 2026 22:45:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 15 May 2026 22:45:55 GMT
CMD []
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2240a8f6be9241c8313b7887a9f6b272758fa6f323a29ae88da91f004c59d0d6`  
		Last Modified: Fri, 15 May 2026 22:12:26 GMT  
		Size: 8.3 MB (8311611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee8f29570b73bc6fb95364db2374f726e9b921827f4d1383a6d310769c050e2`  
		Last Modified: Fri, 15 May 2026 22:12:26 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb157a4a9b724e516e2a50f94be797a8145642f3c45f0f8d7bc236aa4848960`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 19.5 MB (19549502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f6e87dc813cb0ce7fd8d1277ed2d283a03d11b6492284e50fc16c959ccf8cb1`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 23.0 MB (22988578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4642ba5a86eb9921fd340045e353c9b3723a87f535731ae12659016c86bd3a48`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 11.2 MB (11243758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53d662cd1653019365b80d59af307d893de60a95d5d03aa7faddf0654b0162a7`  
		Last Modified: Fri, 15 May 2026 22:12:28 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45636b869c7065c939fb09da20708b05eb4bffe960ae3cb0102e1101147bf702`  
		Last Modified: Fri, 15 May 2026 22:12:28 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9074eaed06bf00c4914e361b510e55cd12bb8b0305b732d777ef95e01914b4f4`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f0de530d70a206bbf99372d4e80b56da6aa52a05b01bd6390d3bb3f4317466`  
		Last Modified: Fri, 15 May 2026 22:46:06 GMT  
		Size: 6.9 MB (6941385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc4ad90df2e9375f24da713fdbd03d16ffd44bcab544ed61a9d388fcc342e85`  
		Last Modified: Fri, 15 May 2026 22:46:06 GMT  
		Size: 92.2 KB (92210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f7d81cca6c2e02237a63044b96fc4e4432bffd61e595b15c8c2d952370deeed`  
		Last Modified: Fri, 15 May 2026 22:46:06 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb7196e21df03c1f04999bead8f104980dd964263cd7b78f05f013ad70dc5e2`  
		Last Modified: Fri, 15 May 2026 22:46:08 GMT  
		Size: 68.7 MB (68656308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403fc89c99ec573758e84c2e171afabefeec367c0c3ac712710c2c280fac6f51`  
		Last Modified: Fri, 15 May 2026 22:46:07 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6ba97049938b6a09c6a9ac2e32cd77fd36080fff06433e8e5f31af12220583`  
		Last Modified: Fri, 15 May 2026 22:46:07 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:bd3f7470c6236fcdb2cf1e2c99310e54bbd3ad7060762321c8003d30700a4adf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c743ab7cd39dee28326b6ff67c26d9c04b6169c89078262749d30845200dbb5b`

```dockerfile
```

-	Layers:
	-	`sha256:d84803d0d069e3f761b94992b6e3e50d1af7858113038a4930bde2b44ff43a64`  
		Last Modified: Fri, 15 May 2026 22:46:06 GMT  
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
$ docker pull docker@sha256:ef239f5a75ebd13a6e3a3ab62b4968537548555442e51b74688fefeee15455d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.7 MB (131665508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e6993f94a7073e22d9d8fa213b4f91cc953dac434c0511af155e03ba2bbbd8c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Fri, 15 May 2026 22:11:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 15 May 2026 22:11:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 15 May 2026 22:12:00 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 15 May 2026 22:12:04 GMT
ENV DOCKER_VERSION=29.5.0
# Fri, 15 May 2026 22:12:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 15 May 2026 22:12:04 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Fri, 15 May 2026 22:12:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-amd64'; 			sha256='0144479d5a1cd710be3464ae898628cfa68033e16b225aef52f81930c45ac9b5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v6'; 			sha256='1f34337385921c5da43d63452282726b062aa887fda975f96dd3d6e869648bc6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v7'; 			sha256='3560b5b6fd3485f4d0bd160e7edf56cc1f08f0cb5852c9af28bf3fab9973c7c2'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm64'; 			sha256='565605fe0bb393ed5d11771e5b52fc7ef05c701868861fa85609747c9d74a440'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-ppc64le'; 			sha256='c5ef8012f48a518e1c235ad408d26cd424d7b5fa87eaf78cb2ff4b9048730120'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-riscv64'; 			sha256='80b27d5f3a346591a5045b81217ee5be578ed151ef8cbd883a892c0ec0ac33f1'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-s390x'; 			sha256='04f5bd0d389f682c7e9287a3b3a1777b0848f8e10d58cbf9d4d12c9002bbb378'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 15 May 2026 22:12:07 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Fri, 15 May 2026 22:12:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 15 May 2026 22:12:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 15 May 2026 22:12:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 22:12:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 15 May 2026 22:12:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 15 May 2026 22:12:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2026 22:12:10 GMT
CMD ["sh"]
# Fri, 15 May 2026 22:14:39 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 15 May 2026 22:14:40 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 15 May 2026 22:14:40 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 15 May 2026 22:14:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 15 May 2026 22:14:43 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 15 May 2026 22:14:43 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 15 May 2026 22:14:43 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 22:14:43 GMT
VOLUME [/var/lib/docker]
# Fri, 15 May 2026 22:14:43 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 15 May 2026 22:14:43 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 15 May 2026 22:14:43 GMT
CMD []
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb53acd779ed72fcbca92822c9c8dca72fc19b59b4367fc8edbe5c8edd184829`  
		Last Modified: Fri, 15 May 2026 22:12:16 GMT  
		Size: 7.5 MB (7520515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3717dbbea465f22997cb871db7b421cb78bfc5d2353e0fbb9c24a4d7f4eead8b`  
		Last Modified: Fri, 15 May 2026 22:12:16 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2765ebda46cc899cbdd1066e7e900d81e9e6227536c38218d156a6c6ffc93324`  
		Last Modified: Fri, 15 May 2026 22:12:17 GMT  
		Size: 18.2 MB (18172266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8e62c2751306352d388df5f6ed3f91e4f160f2da7a249168dc387777896b44`  
		Last Modified: Fri, 15 May 2026 22:12:17 GMT  
		Size: 21.6 MB (21600397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e74677ed12033b201cddf684740d6f5f9540e22ab253c874ab4d21644f5b592`  
		Last Modified: Fri, 15 May 2026 22:12:17 GMT  
		Size: 10.6 MB (10637133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d76fc015f6b878f4335aa2e01b8ef18fcc9e9b2cb962b48d46350deb994e02d`  
		Last Modified: Fri, 15 May 2026 22:12:17 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad7ca5f5e6e176e7d1835e181fe35affc2155c45a6a1148aa7f18ea76d9d05e`  
		Last Modified: Fri, 15 May 2026 22:12:18 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdab469dc84864d9800ae053f9d87586d2515da2b650cf6f13f5ee84e15b2276`  
		Last Modified: Fri, 15 May 2026 22:12:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e61fa784a50d39d698bb4131e0cdda87523cb190f1d964d336a0eb9670b6fd`  
		Last Modified: Fri, 15 May 2026 22:14:53 GMT  
		Size: 6.6 MB (6577169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6091cd81f80a383632ea922a26439e61a5003e64d76dfc3d4bfec40420f0f921`  
		Last Modified: Fri, 15 May 2026 22:14:53 GMT  
		Size: 87.8 KB (87833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:858404ad7c646164306853c3153ee071dd35b14abaf989078b504a287c341dec`  
		Last Modified: Fri, 15 May 2026 22:14:53 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4328aaffaeedc3768196c5928da4c98cee1bfc491c8e951d2dc43da2d38acd04`  
		Last Modified: Fri, 15 May 2026 22:14:55 GMT  
		Size: 63.8 MB (63778918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f84fcf533486742f994566043a25c7a7c23e263cd00704b53a1653242d0b0b8`  
		Last Modified: Fri, 15 May 2026 22:14:55 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95db86311c1bf70966aa5d474d44b82d7521ce7b749c0450d9a393fc88161168`  
		Last Modified: Fri, 15 May 2026 22:14:55 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:6b79b3ac684b96301be66c5f36fd56c5a6c5756cf5a41c478f6d1945686b8349
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:709fc5e54befeab0806a68f4887f40378c59005ec285f228919d0e515f79e46b`

```dockerfile
```

-	Layers:
	-	`sha256:0107810b79e283361584a1b052454ef6bbd5468de93976e803fe7b0ac4ee3336`  
		Last Modified: Fri, 15 May 2026 22:14:53 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:6271c82062c42bdbc409cb458dce06d11f74ce961c30a90c6eb58a998c28afee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.1 MB (131088703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e575b474f12e2e286b308aeaf79fda6e9fec3855a23edec1474dc5b5b8dd4427`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Fri, 15 May 2026 22:12:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 15 May 2026 22:12:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 15 May 2026 22:12:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 15 May 2026 22:12:17 GMT
ENV DOCKER_VERSION=29.5.0
# Fri, 15 May 2026 22:12:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 15 May 2026 22:12:17 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Fri, 15 May 2026 22:12:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-amd64'; 			sha256='0144479d5a1cd710be3464ae898628cfa68033e16b225aef52f81930c45ac9b5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v6'; 			sha256='1f34337385921c5da43d63452282726b062aa887fda975f96dd3d6e869648bc6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v7'; 			sha256='3560b5b6fd3485f4d0bd160e7edf56cc1f08f0cb5852c9af28bf3fab9973c7c2'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm64'; 			sha256='565605fe0bb393ed5d11771e5b52fc7ef05c701868861fa85609747c9d74a440'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-ppc64le'; 			sha256='c5ef8012f48a518e1c235ad408d26cd424d7b5fa87eaf78cb2ff4b9048730120'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-riscv64'; 			sha256='80b27d5f3a346591a5045b81217ee5be578ed151ef8cbd883a892c0ec0ac33f1'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-s390x'; 			sha256='04f5bd0d389f682c7e9287a3b3a1777b0848f8e10d58cbf9d4d12c9002bbb378'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 15 May 2026 22:12:18 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Fri, 15 May 2026 22:12:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 15 May 2026 22:12:19 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 15 May 2026 22:12:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 22:12:19 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 15 May 2026 22:12:19 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 15 May 2026 22:12:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2026 22:12:19 GMT
CMD ["sh"]
# Fri, 15 May 2026 22:46:13 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 15 May 2026 22:46:14 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 15 May 2026 22:46:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 15 May 2026 22:46:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 15 May 2026 22:46:17 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 15 May 2026 22:46:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 15 May 2026 22:46:17 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 22:46:17 GMT
VOLUME [/var/lib/docker]
# Fri, 15 May 2026 22:46:17 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 15 May 2026 22:46:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 15 May 2026 22:46:17 GMT
CMD []
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd51147f6d8210f56d90e095c69db7468c6a7f4c96b15954bec62a38d029c230`  
		Last Modified: Fri, 15 May 2026 22:12:26 GMT  
		Size: 8.4 MB (8368382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca485120792b1bdb82820fd08df20937c87c36c02b044d113785a278f04c9c5e`  
		Last Modified: Fri, 15 May 2026 22:12:25 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76be2953b1820f6b03454f4cc64611d855fbccf3feb3c9d49c80e129eddcad5`  
		Last Modified: Fri, 15 May 2026 22:12:26 GMT  
		Size: 18.0 MB (18003835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc8387c97690c1e6db50aa3de5c90f1742500af7c360287ddfe4acd0578e0eb`  
		Last Modified: Fri, 15 May 2026 22:12:26 GMT  
		Size: 20.8 MB (20815340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3087ee8252be9dcbda43072f57a958f8f37983b3932bdca55c49fc7420da93f`  
		Last Modified: Fri, 15 May 2026 22:12:26 GMT  
		Size: 10.2 MB (10243274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027710042ccab2488d5291cd625bb62305844954e320f530f618c56b53ef928c`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0557313fec61d76b6a60306c806eb278032cfc80335daa86db37ad9979e81756`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9074eaed06bf00c4914e361b510e55cd12bb8b0305b732d777ef95e01914b4f4`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43b2d205b3daf8cb2c6ef3c0e0999b4106fc7a6595ba5568e8605a7e7b0722d8`  
		Last Modified: Fri, 15 May 2026 22:46:26 GMT  
		Size: 7.2 MB (7219897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0304531f0ed7ae27db4e86f747d65dfef2567fd5f396a4b3922c5ff5780d1f2`  
		Last Modified: Fri, 15 May 2026 22:46:26 GMT  
		Size: 100.9 KB (100934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95e602dc9bf9e82e229534494ecc27788dfc15984a25ad6683a47603dfb112ff`  
		Last Modified: Fri, 15 May 2026 22:46:26 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb752877659a29a329ac376438ffc77fd5832ef8ec7713badc224dc70797bd6`  
		Last Modified: Fri, 15 May 2026 22:46:29 GMT  
		Size: 62.1 MB (62129016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1ca5de4993dc83a36fb35a72b4fedf78533c646f254850669127c3e34a022a`  
		Last Modified: Fri, 15 May 2026 22:46:27 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27981b508a5db9a4e2a2c0b87eb0017d532fc5cc5bd11529ba120cd1e843ae91`  
		Last Modified: Fri, 15 May 2026 22:46:28 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:75f2ca4085188952af0189876ba5792cdd9148db56893b95a052e1a878bd4763
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9a506d026912de6f5e76fbcaf2f074cae0ccb50f7496d643ebb7bb3454ee5b0`

```dockerfile
```

-	Layers:
	-	`sha256:8cf936b97b7e42d4fcbb8824339486e8226b6af0c069484bcb894b3a1d54a301`  
		Last Modified: Fri, 15 May 2026 22:46:26 GMT  
		Size: 34.8 KB (34782 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-cli`

```console
$ docker pull docker@sha256:22eb9db6081c0bc3c05137a5e8f26720e1b09aaafd3f18b923b494bcd6283a3a
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
$ docker pull docker@sha256:93afea9ac780f8706540408cba1e801ba285071476b0c2bff424a0ca0037869c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.0 MB (65959799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54560465c89852384428d8b003c70278f2a11fdee74fde28173fea1077416da9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:e6e636232d7064d32da9c46ef93c11a565c43d61068daa1785a2d63bb664c190
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:973ee0a24a2536030656c4b9be0b463122f73df6150f6b0949b3d3601798afd1`

```dockerfile
```

-	Layers:
	-	`sha256:dbed7195f208034adcef893e2efc57ce071c5d914a8a9624d5a8a7fbb1a9f99e`  
		Last Modified: Tue, 19 May 2026 18:44:01 GMT  
		Size: 38.1 KB (38056 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:663439730373cf7597a3f83ae50ab11f8a171b59b1e9ce95a730be4c0b42eb22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62234030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f0de2aee792b8ce4ffb303432b131ae0026fdd58af954221ecf5bcb4f293705`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:866404ab9edde4226ee79d91959d86956cc3fe71a933e10c9c282f3bb9fe1e24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1f84764e1609e718085281484003ba89b5bd9d8cbb6984808cae3079115e48a`

```dockerfile
```

-	Layers:
	-	`sha256:60a6451bb1e2eecccb01163a32454bf66adbc39c153e56f1b682485c3f73fbc4`  
		Last Modified: Tue, 19 May 2026 18:46:40 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:9ec11722eadaf4ecb19592ea19d512fc17ef941738677435dc52f1f70e3b4da2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61215589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:376a20891ab4edb0bcada5d8b3ba3f89f105c6351ce5368f2cafee22c9c2e764`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Fri, 15 May 2026 22:11:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 15 May 2026 22:11:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 15 May 2026 22:12:00 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 15 May 2026 22:12:04 GMT
ENV DOCKER_VERSION=29.5.0
# Fri, 15 May 2026 22:12:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 15 May 2026 22:12:04 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Fri, 15 May 2026 22:12:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-amd64'; 			sha256='0144479d5a1cd710be3464ae898628cfa68033e16b225aef52f81930c45ac9b5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v6'; 			sha256='1f34337385921c5da43d63452282726b062aa887fda975f96dd3d6e869648bc6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v7'; 			sha256='3560b5b6fd3485f4d0bd160e7edf56cc1f08f0cb5852c9af28bf3fab9973c7c2'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm64'; 			sha256='565605fe0bb393ed5d11771e5b52fc7ef05c701868861fa85609747c9d74a440'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-ppc64le'; 			sha256='c5ef8012f48a518e1c235ad408d26cd424d7b5fa87eaf78cb2ff4b9048730120'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-riscv64'; 			sha256='80b27d5f3a346591a5045b81217ee5be578ed151ef8cbd883a892c0ec0ac33f1'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-s390x'; 			sha256='04f5bd0d389f682c7e9287a3b3a1777b0848f8e10d58cbf9d4d12c9002bbb378'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 15 May 2026 22:12:07 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Fri, 15 May 2026 22:12:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 15 May 2026 22:12:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 15 May 2026 22:12:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 22:12:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 15 May 2026 22:12:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 15 May 2026 22:12:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2026 22:12:10 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb53acd779ed72fcbca92822c9c8dca72fc19b59b4367fc8edbe5c8edd184829`  
		Last Modified: Fri, 15 May 2026 22:12:16 GMT  
		Size: 7.5 MB (7520515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3717dbbea465f22997cb871db7b421cb78bfc5d2353e0fbb9c24a4d7f4eead8b`  
		Last Modified: Fri, 15 May 2026 22:12:16 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2765ebda46cc899cbdd1066e7e900d81e9e6227536c38218d156a6c6ffc93324`  
		Last Modified: Fri, 15 May 2026 22:12:17 GMT  
		Size: 18.2 MB (18172266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8e62c2751306352d388df5f6ed3f91e4f160f2da7a249168dc387777896b44`  
		Last Modified: Fri, 15 May 2026 22:12:17 GMT  
		Size: 21.6 MB (21600397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e74677ed12033b201cddf684740d6f5f9540e22ab253c874ab4d21644f5b592`  
		Last Modified: Fri, 15 May 2026 22:12:17 GMT  
		Size: 10.6 MB (10637133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d76fc015f6b878f4335aa2e01b8ef18fcc9e9b2cb962b48d46350deb994e02d`  
		Last Modified: Fri, 15 May 2026 22:12:17 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad7ca5f5e6e176e7d1835e181fe35affc2155c45a6a1148aa7f18ea76d9d05e`  
		Last Modified: Fri, 15 May 2026 22:12:18 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdab469dc84864d9800ae053f9d87586d2515da2b650cf6f13f5ee84e15b2276`  
		Last Modified: Fri, 15 May 2026 22:12:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:3733f58f759836ce9f96949b34cf083d5873acad577a5181e080afb4bf3249f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14f8c9cf97e3e4d9ec70c8edcea1d71eca3c988ea012b28acc4d35eea629ae37`

```dockerfile
```

-	Layers:
	-	`sha256:7ce1554139b841ff42f6ca82b422a07755ca34b9f40a43a8f69db42b7b360f47`  
		Last Modified: Fri, 15 May 2026 22:12:16 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e211ecf9a3c37d57418eef652252ba0ca62fc942cdfa0d8dec160bc3086bd9c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61632856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee4f6ad10554b836d3f6dad4bf015212f96fc505f746c44c549df3e29d3fd2a2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Fri, 15 May 2026 22:12:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 15 May 2026 22:12:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 15 May 2026 22:12:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 15 May 2026 22:12:17 GMT
ENV DOCKER_VERSION=29.5.0
# Fri, 15 May 2026 22:12:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 15 May 2026 22:12:17 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Fri, 15 May 2026 22:12:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-amd64'; 			sha256='0144479d5a1cd710be3464ae898628cfa68033e16b225aef52f81930c45ac9b5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v6'; 			sha256='1f34337385921c5da43d63452282726b062aa887fda975f96dd3d6e869648bc6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v7'; 			sha256='3560b5b6fd3485f4d0bd160e7edf56cc1f08f0cb5852c9af28bf3fab9973c7c2'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm64'; 			sha256='565605fe0bb393ed5d11771e5b52fc7ef05c701868861fa85609747c9d74a440'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-ppc64le'; 			sha256='c5ef8012f48a518e1c235ad408d26cd424d7b5fa87eaf78cb2ff4b9048730120'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-riscv64'; 			sha256='80b27d5f3a346591a5045b81217ee5be578ed151ef8cbd883a892c0ec0ac33f1'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-s390x'; 			sha256='04f5bd0d389f682c7e9287a3b3a1777b0848f8e10d58cbf9d4d12c9002bbb378'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 15 May 2026 22:12:18 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Fri, 15 May 2026 22:12:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 15 May 2026 22:12:19 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 15 May 2026 22:12:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 22:12:19 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 15 May 2026 22:12:19 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 15 May 2026 22:12:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2026 22:12:19 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd51147f6d8210f56d90e095c69db7468c6a7f4c96b15954bec62a38d029c230`  
		Last Modified: Fri, 15 May 2026 22:12:26 GMT  
		Size: 8.4 MB (8368382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca485120792b1bdb82820fd08df20937c87c36c02b044d113785a278f04c9c5e`  
		Last Modified: Fri, 15 May 2026 22:12:25 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76be2953b1820f6b03454f4cc64611d855fbccf3feb3c9d49c80e129eddcad5`  
		Last Modified: Fri, 15 May 2026 22:12:26 GMT  
		Size: 18.0 MB (18003835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc8387c97690c1e6db50aa3de5c90f1742500af7c360287ddfe4acd0578e0eb`  
		Last Modified: Fri, 15 May 2026 22:12:26 GMT  
		Size: 20.8 MB (20815340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3087ee8252be9dcbda43072f57a958f8f37983b3932bdca55c49fc7420da93f`  
		Last Modified: Fri, 15 May 2026 22:12:26 GMT  
		Size: 10.2 MB (10243274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027710042ccab2488d5291cd625bb62305844954e320f530f618c56b53ef928c`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0557313fec61d76b6a60306c806eb278032cfc80335daa86db37ad9979e81756`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9074eaed06bf00c4914e361b510e55cd12bb8b0305b732d777ef95e01914b4f4`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:06da91c70ff029cd54c906f93a84997c38caa126b495b2f94c29d83561aa534a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c299b9b46a49c14a1255ad31a3c17438482a28e9408b1dcd36db58d87d66247`

```dockerfile
```

-	Layers:
	-	`sha256:912e2047614870aa935e1c45fd05fb52050a876007557a6795c50c8237ff6549`  
		Last Modified: Fri, 15 May 2026 22:12:24 GMT  
		Size: 38.3 KB (38262 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-dind`

```console
$ docker pull docker@sha256:d0c942e5e2c14a74da706cff670ea2449fb57f9bc6abae7164461d0c6322b8b4
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
$ docker pull docker@sha256:74328f9b3824edb27d1c5b57abfa5765aa1742806ad77e3e90b2ee328aba8301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.7 MB (141655694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71837a59b95c3653383ca90ce81fbcee4f34adb0fbbf8b357e75da9affc77579`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Fri, 15 May 2026 22:12:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 15 May 2026 22:12:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 15 May 2026 22:12:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 15 May 2026 22:12:17 GMT
ENV DOCKER_VERSION=29.5.0
# Fri, 15 May 2026 22:12:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 15 May 2026 22:12:17 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Fri, 15 May 2026 22:12:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-amd64'; 			sha256='0144479d5a1cd710be3464ae898628cfa68033e16b225aef52f81930c45ac9b5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v6'; 			sha256='1f34337385921c5da43d63452282726b062aa887fda975f96dd3d6e869648bc6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v7'; 			sha256='3560b5b6fd3485f4d0bd160e7edf56cc1f08f0cb5852c9af28bf3fab9973c7c2'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm64'; 			sha256='565605fe0bb393ed5d11771e5b52fc7ef05c701868861fa85609747c9d74a440'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-ppc64le'; 			sha256='c5ef8012f48a518e1c235ad408d26cd424d7b5fa87eaf78cb2ff4b9048730120'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-riscv64'; 			sha256='80b27d5f3a346591a5045b81217ee5be578ed151ef8cbd883a892c0ec0ac33f1'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-s390x'; 			sha256='04f5bd0d389f682c7e9287a3b3a1777b0848f8e10d58cbf9d4d12c9002bbb378'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 15 May 2026 22:12:18 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Fri, 15 May 2026 22:12:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 15 May 2026 22:12:19 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 15 May 2026 22:12:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 22:12:19 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 15 May 2026 22:12:19 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 15 May 2026 22:12:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2026 22:12:19 GMT
CMD ["sh"]
# Fri, 15 May 2026 22:45:52 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 15 May 2026 22:45:52 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 15 May 2026 22:45:52 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 15 May 2026 22:45:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 15 May 2026 22:45:55 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 15 May 2026 22:45:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 15 May 2026 22:45:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 22:45:55 GMT
VOLUME [/var/lib/docker]
# Fri, 15 May 2026 22:45:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 15 May 2026 22:45:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 15 May 2026 22:45:55 GMT
CMD []
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2240a8f6be9241c8313b7887a9f6b272758fa6f323a29ae88da91f004c59d0d6`  
		Last Modified: Fri, 15 May 2026 22:12:26 GMT  
		Size: 8.3 MB (8311611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee8f29570b73bc6fb95364db2374f726e9b921827f4d1383a6d310769c050e2`  
		Last Modified: Fri, 15 May 2026 22:12:26 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb157a4a9b724e516e2a50f94be797a8145642f3c45f0f8d7bc236aa4848960`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 19.5 MB (19549502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f6e87dc813cb0ce7fd8d1277ed2d283a03d11b6492284e50fc16c959ccf8cb1`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 23.0 MB (22988578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4642ba5a86eb9921fd340045e353c9b3723a87f535731ae12659016c86bd3a48`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 11.2 MB (11243758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53d662cd1653019365b80d59af307d893de60a95d5d03aa7faddf0654b0162a7`  
		Last Modified: Fri, 15 May 2026 22:12:28 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45636b869c7065c939fb09da20708b05eb4bffe960ae3cb0102e1101147bf702`  
		Last Modified: Fri, 15 May 2026 22:12:28 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9074eaed06bf00c4914e361b510e55cd12bb8b0305b732d777ef95e01914b4f4`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f0de530d70a206bbf99372d4e80b56da6aa52a05b01bd6390d3bb3f4317466`  
		Last Modified: Fri, 15 May 2026 22:46:06 GMT  
		Size: 6.9 MB (6941385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc4ad90df2e9375f24da713fdbd03d16ffd44bcab544ed61a9d388fcc342e85`  
		Last Modified: Fri, 15 May 2026 22:46:06 GMT  
		Size: 92.2 KB (92210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f7d81cca6c2e02237a63044b96fc4e4432bffd61e595b15c8c2d952370deeed`  
		Last Modified: Fri, 15 May 2026 22:46:06 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb7196e21df03c1f04999bead8f104980dd964263cd7b78f05f013ad70dc5e2`  
		Last Modified: Fri, 15 May 2026 22:46:08 GMT  
		Size: 68.7 MB (68656308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403fc89c99ec573758e84c2e171afabefeec367c0c3ac712710c2c280fac6f51`  
		Last Modified: Fri, 15 May 2026 22:46:07 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6ba97049938b6a09c6a9ac2e32cd77fd36080fff06433e8e5f31af12220583`  
		Last Modified: Fri, 15 May 2026 22:46:07 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:bd3f7470c6236fcdb2cf1e2c99310e54bbd3ad7060762321c8003d30700a4adf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c743ab7cd39dee28326b6ff67c26d9c04b6169c89078262749d30845200dbb5b`

```dockerfile
```

-	Layers:
	-	`sha256:d84803d0d069e3f761b94992b6e3e50d1af7858113038a4930bde2b44ff43a64`  
		Last Modified: Fri, 15 May 2026 22:46:06 GMT  
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
$ docker pull docker@sha256:ef239f5a75ebd13a6e3a3ab62b4968537548555442e51b74688fefeee15455d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.7 MB (131665508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e6993f94a7073e22d9d8fa213b4f91cc953dac434c0511af155e03ba2bbbd8c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Fri, 15 May 2026 22:11:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 15 May 2026 22:11:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 15 May 2026 22:12:00 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 15 May 2026 22:12:04 GMT
ENV DOCKER_VERSION=29.5.0
# Fri, 15 May 2026 22:12:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 15 May 2026 22:12:04 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Fri, 15 May 2026 22:12:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-amd64'; 			sha256='0144479d5a1cd710be3464ae898628cfa68033e16b225aef52f81930c45ac9b5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v6'; 			sha256='1f34337385921c5da43d63452282726b062aa887fda975f96dd3d6e869648bc6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v7'; 			sha256='3560b5b6fd3485f4d0bd160e7edf56cc1f08f0cb5852c9af28bf3fab9973c7c2'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm64'; 			sha256='565605fe0bb393ed5d11771e5b52fc7ef05c701868861fa85609747c9d74a440'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-ppc64le'; 			sha256='c5ef8012f48a518e1c235ad408d26cd424d7b5fa87eaf78cb2ff4b9048730120'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-riscv64'; 			sha256='80b27d5f3a346591a5045b81217ee5be578ed151ef8cbd883a892c0ec0ac33f1'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-s390x'; 			sha256='04f5bd0d389f682c7e9287a3b3a1777b0848f8e10d58cbf9d4d12c9002bbb378'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 15 May 2026 22:12:07 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Fri, 15 May 2026 22:12:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 15 May 2026 22:12:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 15 May 2026 22:12:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 22:12:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 15 May 2026 22:12:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 15 May 2026 22:12:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2026 22:12:10 GMT
CMD ["sh"]
# Fri, 15 May 2026 22:14:39 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 15 May 2026 22:14:40 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 15 May 2026 22:14:40 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 15 May 2026 22:14:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 15 May 2026 22:14:43 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 15 May 2026 22:14:43 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 15 May 2026 22:14:43 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 22:14:43 GMT
VOLUME [/var/lib/docker]
# Fri, 15 May 2026 22:14:43 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 15 May 2026 22:14:43 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 15 May 2026 22:14:43 GMT
CMD []
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb53acd779ed72fcbca92822c9c8dca72fc19b59b4367fc8edbe5c8edd184829`  
		Last Modified: Fri, 15 May 2026 22:12:16 GMT  
		Size: 7.5 MB (7520515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3717dbbea465f22997cb871db7b421cb78bfc5d2353e0fbb9c24a4d7f4eead8b`  
		Last Modified: Fri, 15 May 2026 22:12:16 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2765ebda46cc899cbdd1066e7e900d81e9e6227536c38218d156a6c6ffc93324`  
		Last Modified: Fri, 15 May 2026 22:12:17 GMT  
		Size: 18.2 MB (18172266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8e62c2751306352d388df5f6ed3f91e4f160f2da7a249168dc387777896b44`  
		Last Modified: Fri, 15 May 2026 22:12:17 GMT  
		Size: 21.6 MB (21600397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e74677ed12033b201cddf684740d6f5f9540e22ab253c874ab4d21644f5b592`  
		Last Modified: Fri, 15 May 2026 22:12:17 GMT  
		Size: 10.6 MB (10637133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d76fc015f6b878f4335aa2e01b8ef18fcc9e9b2cb962b48d46350deb994e02d`  
		Last Modified: Fri, 15 May 2026 22:12:17 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad7ca5f5e6e176e7d1835e181fe35affc2155c45a6a1148aa7f18ea76d9d05e`  
		Last Modified: Fri, 15 May 2026 22:12:18 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdab469dc84864d9800ae053f9d87586d2515da2b650cf6f13f5ee84e15b2276`  
		Last Modified: Fri, 15 May 2026 22:12:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e61fa784a50d39d698bb4131e0cdda87523cb190f1d964d336a0eb9670b6fd`  
		Last Modified: Fri, 15 May 2026 22:14:53 GMT  
		Size: 6.6 MB (6577169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6091cd81f80a383632ea922a26439e61a5003e64d76dfc3d4bfec40420f0f921`  
		Last Modified: Fri, 15 May 2026 22:14:53 GMT  
		Size: 87.8 KB (87833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:858404ad7c646164306853c3153ee071dd35b14abaf989078b504a287c341dec`  
		Last Modified: Fri, 15 May 2026 22:14:53 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4328aaffaeedc3768196c5928da4c98cee1bfc491c8e951d2dc43da2d38acd04`  
		Last Modified: Fri, 15 May 2026 22:14:55 GMT  
		Size: 63.8 MB (63778918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f84fcf533486742f994566043a25c7a7c23e263cd00704b53a1653242d0b0b8`  
		Last Modified: Fri, 15 May 2026 22:14:55 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95db86311c1bf70966aa5d474d44b82d7521ce7b749c0450d9a393fc88161168`  
		Last Modified: Fri, 15 May 2026 22:14:55 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:6b79b3ac684b96301be66c5f36fd56c5a6c5756cf5a41c478f6d1945686b8349
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:709fc5e54befeab0806a68f4887f40378c59005ec285f228919d0e515f79e46b`

```dockerfile
```

-	Layers:
	-	`sha256:0107810b79e283361584a1b052454ef6bbd5468de93976e803fe7b0ac4ee3336`  
		Last Modified: Fri, 15 May 2026 22:14:53 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:6271c82062c42bdbc409cb458dce06d11f74ce961c30a90c6eb58a998c28afee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.1 MB (131088703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e575b474f12e2e286b308aeaf79fda6e9fec3855a23edec1474dc5b5b8dd4427`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Fri, 15 May 2026 22:12:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 15 May 2026 22:12:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 15 May 2026 22:12:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 15 May 2026 22:12:17 GMT
ENV DOCKER_VERSION=29.5.0
# Fri, 15 May 2026 22:12:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 15 May 2026 22:12:17 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Fri, 15 May 2026 22:12:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-amd64'; 			sha256='0144479d5a1cd710be3464ae898628cfa68033e16b225aef52f81930c45ac9b5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v6'; 			sha256='1f34337385921c5da43d63452282726b062aa887fda975f96dd3d6e869648bc6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v7'; 			sha256='3560b5b6fd3485f4d0bd160e7edf56cc1f08f0cb5852c9af28bf3fab9973c7c2'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm64'; 			sha256='565605fe0bb393ed5d11771e5b52fc7ef05c701868861fa85609747c9d74a440'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-ppc64le'; 			sha256='c5ef8012f48a518e1c235ad408d26cd424d7b5fa87eaf78cb2ff4b9048730120'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-riscv64'; 			sha256='80b27d5f3a346591a5045b81217ee5be578ed151ef8cbd883a892c0ec0ac33f1'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-s390x'; 			sha256='04f5bd0d389f682c7e9287a3b3a1777b0848f8e10d58cbf9d4d12c9002bbb378'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 15 May 2026 22:12:18 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Fri, 15 May 2026 22:12:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 15 May 2026 22:12:19 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 15 May 2026 22:12:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 22:12:19 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 15 May 2026 22:12:19 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 15 May 2026 22:12:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2026 22:12:19 GMT
CMD ["sh"]
# Fri, 15 May 2026 22:46:13 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 15 May 2026 22:46:14 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 15 May 2026 22:46:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 15 May 2026 22:46:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 15 May 2026 22:46:17 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 15 May 2026 22:46:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 15 May 2026 22:46:17 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 22:46:17 GMT
VOLUME [/var/lib/docker]
# Fri, 15 May 2026 22:46:17 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 15 May 2026 22:46:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 15 May 2026 22:46:17 GMT
CMD []
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd51147f6d8210f56d90e095c69db7468c6a7f4c96b15954bec62a38d029c230`  
		Last Modified: Fri, 15 May 2026 22:12:26 GMT  
		Size: 8.4 MB (8368382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca485120792b1bdb82820fd08df20937c87c36c02b044d113785a278f04c9c5e`  
		Last Modified: Fri, 15 May 2026 22:12:25 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76be2953b1820f6b03454f4cc64611d855fbccf3feb3c9d49c80e129eddcad5`  
		Last Modified: Fri, 15 May 2026 22:12:26 GMT  
		Size: 18.0 MB (18003835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc8387c97690c1e6db50aa3de5c90f1742500af7c360287ddfe4acd0578e0eb`  
		Last Modified: Fri, 15 May 2026 22:12:26 GMT  
		Size: 20.8 MB (20815340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3087ee8252be9dcbda43072f57a958f8f37983b3932bdca55c49fc7420da93f`  
		Last Modified: Fri, 15 May 2026 22:12:26 GMT  
		Size: 10.2 MB (10243274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027710042ccab2488d5291cd625bb62305844954e320f530f618c56b53ef928c`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0557313fec61d76b6a60306c806eb278032cfc80335daa86db37ad9979e81756`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9074eaed06bf00c4914e361b510e55cd12bb8b0305b732d777ef95e01914b4f4`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43b2d205b3daf8cb2c6ef3c0e0999b4106fc7a6595ba5568e8605a7e7b0722d8`  
		Last Modified: Fri, 15 May 2026 22:46:26 GMT  
		Size: 7.2 MB (7219897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0304531f0ed7ae27db4e86f747d65dfef2567fd5f396a4b3922c5ff5780d1f2`  
		Last Modified: Fri, 15 May 2026 22:46:26 GMT  
		Size: 100.9 KB (100934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95e602dc9bf9e82e229534494ecc27788dfc15984a25ad6683a47603dfb112ff`  
		Last Modified: Fri, 15 May 2026 22:46:26 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb752877659a29a329ac376438ffc77fd5832ef8ec7713badc224dc70797bd6`  
		Last Modified: Fri, 15 May 2026 22:46:29 GMT  
		Size: 62.1 MB (62129016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1ca5de4993dc83a36fb35a72b4fedf78533c646f254850669127c3e34a022a`  
		Last Modified: Fri, 15 May 2026 22:46:27 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27981b508a5db9a4e2a2c0b87eb0017d532fc5cc5bd11529ba120cd1e843ae91`  
		Last Modified: Fri, 15 May 2026 22:46:28 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:75f2ca4085188952af0189876ba5792cdd9148db56893b95a052e1a878bd4763
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9a506d026912de6f5e76fbcaf2f074cae0ccb50f7496d643ebb7bb3454ee5b0`

```dockerfile
```

-	Layers:
	-	`sha256:8cf936b97b7e42d4fcbb8824339486e8226b6af0c069484bcb894b3a1d54a301`  
		Last Modified: Fri, 15 May 2026 22:46:26 GMT  
		Size: 34.8 KB (34782 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-dind-rootless`

```console
$ docker pull docker@sha256:2379588ca8e9ed0d452464f4aed5361da6361791ec1a2111d44515c3985b2659
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:29-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:86dd1e4303fe60a2cd5f155db3c77e30011cfd8aaa9950188cece42d5e9f8ac3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157179647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f66937a706e25d69d45209cbd13b73c920e1d5ae4415214c93da738b95c779a0`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Fri, 15 May 2026 22:12:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 15 May 2026 22:12:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 15 May 2026 22:12:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 15 May 2026 22:12:17 GMT
ENV DOCKER_VERSION=29.5.0
# Fri, 15 May 2026 22:12:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 15 May 2026 22:12:17 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Fri, 15 May 2026 22:12:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-amd64'; 			sha256='0144479d5a1cd710be3464ae898628cfa68033e16b225aef52f81930c45ac9b5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v6'; 			sha256='1f34337385921c5da43d63452282726b062aa887fda975f96dd3d6e869648bc6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v7'; 			sha256='3560b5b6fd3485f4d0bd160e7edf56cc1f08f0cb5852c9af28bf3fab9973c7c2'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm64'; 			sha256='565605fe0bb393ed5d11771e5b52fc7ef05c701868861fa85609747c9d74a440'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-ppc64le'; 			sha256='c5ef8012f48a518e1c235ad408d26cd424d7b5fa87eaf78cb2ff4b9048730120'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-riscv64'; 			sha256='80b27d5f3a346591a5045b81217ee5be578ed151ef8cbd883a892c0ec0ac33f1'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-s390x'; 			sha256='04f5bd0d389f682c7e9287a3b3a1777b0848f8e10d58cbf9d4d12c9002bbb378'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 15 May 2026 22:12:18 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Fri, 15 May 2026 22:12:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 15 May 2026 22:12:19 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 15 May 2026 22:12:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 22:12:19 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 15 May 2026 22:12:19 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 15 May 2026 22:12:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2026 22:12:19 GMT
CMD ["sh"]
# Fri, 15 May 2026 22:45:52 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 15 May 2026 22:45:52 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 15 May 2026 22:45:52 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 15 May 2026 22:45:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 15 May 2026 22:45:55 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 15 May 2026 22:45:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 15 May 2026 22:45:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 22:45:55 GMT
VOLUME [/var/lib/docker]
# Fri, 15 May 2026 22:45:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 15 May 2026 22:45:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 15 May 2026 22:45:55 GMT
CMD []
# Sat, 16 May 2026 00:10:18 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Sat, 16 May 2026 00:10:18 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Sat, 16 May 2026 00:10:18 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Sat, 16 May 2026 00:10:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 	; 	rm rootless.tgz; 		rootlesskit --version # buildkit
# Sat, 16 May 2026 00:10:18 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Sat, 16 May 2026 00:10:18 GMT
VOLUME [/home/rootless/.local/share/docker]
# Sat, 16 May 2026 00:10:18 GMT
USER rootless
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2240a8f6be9241c8313b7887a9f6b272758fa6f323a29ae88da91f004c59d0d6`  
		Last Modified: Fri, 15 May 2026 22:12:26 GMT  
		Size: 8.3 MB (8311611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee8f29570b73bc6fb95364db2374f726e9b921827f4d1383a6d310769c050e2`  
		Last Modified: Fri, 15 May 2026 22:12:26 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb157a4a9b724e516e2a50f94be797a8145642f3c45f0f8d7bc236aa4848960`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 19.5 MB (19549502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f6e87dc813cb0ce7fd8d1277ed2d283a03d11b6492284e50fc16c959ccf8cb1`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 23.0 MB (22988578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4642ba5a86eb9921fd340045e353c9b3723a87f535731ae12659016c86bd3a48`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 11.2 MB (11243758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53d662cd1653019365b80d59af307d893de60a95d5d03aa7faddf0654b0162a7`  
		Last Modified: Fri, 15 May 2026 22:12:28 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45636b869c7065c939fb09da20708b05eb4bffe960ae3cb0102e1101147bf702`  
		Last Modified: Fri, 15 May 2026 22:12:28 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9074eaed06bf00c4914e361b510e55cd12bb8b0305b732d777ef95e01914b4f4`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f0de530d70a206bbf99372d4e80b56da6aa52a05b01bd6390d3bb3f4317466`  
		Last Modified: Fri, 15 May 2026 22:46:06 GMT  
		Size: 6.9 MB (6941385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc4ad90df2e9375f24da713fdbd03d16ffd44bcab544ed61a9d388fcc342e85`  
		Last Modified: Fri, 15 May 2026 22:46:06 GMT  
		Size: 92.2 KB (92210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f7d81cca6c2e02237a63044b96fc4e4432bffd61e595b15c8c2d952370deeed`  
		Last Modified: Fri, 15 May 2026 22:46:06 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb7196e21df03c1f04999bead8f104980dd964263cd7b78f05f013ad70dc5e2`  
		Last Modified: Fri, 15 May 2026 22:46:08 GMT  
		Size: 68.7 MB (68656308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403fc89c99ec573758e84c2e171afabefeec367c0c3ac712710c2c280fac6f51`  
		Last Modified: Fri, 15 May 2026 22:46:07 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6ba97049938b6a09c6a9ac2e32cd77fd36080fff06433e8e5f31af12220583`  
		Last Modified: Fri, 15 May 2026 22:46:07 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3aecd32c9a7b429826161d546e29c1dff0ac6eea914337b0b9d0a168b785fe5`  
		Last Modified: Sat, 16 May 2026 00:10:24 GMT  
		Size: 3.4 MB (3420116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75a1fd367a70907870ec61c5541633c1016315039aa85446173764ece77df84`  
		Last Modified: Sat, 16 May 2026 00:10:23 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896453e7017b28888cd072db72945d8e744a934faf06c8d0afe071918a3ab492`  
		Last Modified: Sat, 16 May 2026 00:10:23 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8de78d541dc09dba7c55cf30b416cc37bf4cadc540afd919f470b8c6ea68c5`  
		Last Modified: Sat, 16 May 2026 00:10:24 GMT  
		Size: 12.1 MB (12102497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307ee9ce5b3abe899d1554ebbfe999955a855268f925239ee277ff0542c7424f`  
		Last Modified: Sat, 16 May 2026 00:10:25 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:a928bb65ab1afe6b79776cfe5fec97b7de2ce78299935d0f2a6d93a022bbf33d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10081df2ff0f054ec55a6ba8b0e73f3f8660a710ebcd84146466c7e415b001f2`

```dockerfile
```

-	Layers:
	-	`sha256:ef654a1e85deabbd5d572b1aa6d9feaba8a368d7af558b844574a48c0af89e2c`  
		Last Modified: Sat, 16 May 2026 00:10:23 GMT  
		Size: 30.5 KB (30492 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:beddbc20555efb8bc7641a98e7a58a5104329118a81b075bd2373de0e1dca5c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.7 MB (145721108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7cb4b74b39f9eb3c077215fb0f4c6f7d8395bd86b29015b4743c1a5b13d2f24`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Fri, 15 May 2026 22:12:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 15 May 2026 22:12:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 15 May 2026 22:12:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 15 May 2026 22:12:17 GMT
ENV DOCKER_VERSION=29.5.0
# Fri, 15 May 2026 22:12:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 15 May 2026 22:12:17 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Fri, 15 May 2026 22:12:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-amd64'; 			sha256='0144479d5a1cd710be3464ae898628cfa68033e16b225aef52f81930c45ac9b5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v6'; 			sha256='1f34337385921c5da43d63452282726b062aa887fda975f96dd3d6e869648bc6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v7'; 			sha256='3560b5b6fd3485f4d0bd160e7edf56cc1f08f0cb5852c9af28bf3fab9973c7c2'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm64'; 			sha256='565605fe0bb393ed5d11771e5b52fc7ef05c701868861fa85609747c9d74a440'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-ppc64le'; 			sha256='c5ef8012f48a518e1c235ad408d26cd424d7b5fa87eaf78cb2ff4b9048730120'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-riscv64'; 			sha256='80b27d5f3a346591a5045b81217ee5be578ed151ef8cbd883a892c0ec0ac33f1'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-s390x'; 			sha256='04f5bd0d389f682c7e9287a3b3a1777b0848f8e10d58cbf9d4d12c9002bbb378'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 15 May 2026 22:12:18 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Fri, 15 May 2026 22:12:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 15 May 2026 22:12:19 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 15 May 2026 22:12:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 22:12:19 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 15 May 2026 22:12:19 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 15 May 2026 22:12:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2026 22:12:19 GMT
CMD ["sh"]
# Fri, 15 May 2026 22:46:13 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 15 May 2026 22:46:14 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 15 May 2026 22:46:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 15 May 2026 22:46:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 15 May 2026 22:46:17 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 15 May 2026 22:46:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 15 May 2026 22:46:17 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 22:46:17 GMT
VOLUME [/var/lib/docker]
# Fri, 15 May 2026 22:46:17 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 15 May 2026 22:46:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 15 May 2026 22:46:17 GMT
CMD []
# Sat, 16 May 2026 00:10:04 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Sat, 16 May 2026 00:10:04 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Sat, 16 May 2026 00:10:04 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Sat, 16 May 2026 00:10:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 	; 	rm rootless.tgz; 		rootlesskit --version # buildkit
# Sat, 16 May 2026 00:10:05 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Sat, 16 May 2026 00:10:05 GMT
VOLUME [/home/rootless/.local/share/docker]
# Sat, 16 May 2026 00:10:05 GMT
USER rootless
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd51147f6d8210f56d90e095c69db7468c6a7f4c96b15954bec62a38d029c230`  
		Last Modified: Fri, 15 May 2026 22:12:26 GMT  
		Size: 8.4 MB (8368382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca485120792b1bdb82820fd08df20937c87c36c02b044d113785a278f04c9c5e`  
		Last Modified: Fri, 15 May 2026 22:12:25 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76be2953b1820f6b03454f4cc64611d855fbccf3feb3c9d49c80e129eddcad5`  
		Last Modified: Fri, 15 May 2026 22:12:26 GMT  
		Size: 18.0 MB (18003835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc8387c97690c1e6db50aa3de5c90f1742500af7c360287ddfe4acd0578e0eb`  
		Last Modified: Fri, 15 May 2026 22:12:26 GMT  
		Size: 20.8 MB (20815340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3087ee8252be9dcbda43072f57a958f8f37983b3932bdca55c49fc7420da93f`  
		Last Modified: Fri, 15 May 2026 22:12:26 GMT  
		Size: 10.2 MB (10243274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027710042ccab2488d5291cd625bb62305844954e320f530f618c56b53ef928c`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0557313fec61d76b6a60306c806eb278032cfc80335daa86db37ad9979e81756`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9074eaed06bf00c4914e361b510e55cd12bb8b0305b732d777ef95e01914b4f4`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43b2d205b3daf8cb2c6ef3c0e0999b4106fc7a6595ba5568e8605a7e7b0722d8`  
		Last Modified: Fri, 15 May 2026 22:46:26 GMT  
		Size: 7.2 MB (7219897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0304531f0ed7ae27db4e86f747d65dfef2567fd5f396a4b3922c5ff5780d1f2`  
		Last Modified: Fri, 15 May 2026 22:46:26 GMT  
		Size: 100.9 KB (100934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95e602dc9bf9e82e229534494ecc27788dfc15984a25ad6683a47603dfb112ff`  
		Last Modified: Fri, 15 May 2026 22:46:26 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb752877659a29a329ac376438ffc77fd5832ef8ec7713badc224dc70797bd6`  
		Last Modified: Fri, 15 May 2026 22:46:29 GMT  
		Size: 62.1 MB (62129016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1ca5de4993dc83a36fb35a72b4fedf78533c646f254850669127c3e34a022a`  
		Last Modified: Fri, 15 May 2026 22:46:27 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27981b508a5db9a4e2a2c0b87eb0017d532fc5cc5bd11529ba120cd1e843ae91`  
		Last Modified: Fri, 15 May 2026 22:46:28 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1a7270b72b7f3e2799e7c141f64461907402307eab0e5a25271d1e2b47c44ee`  
		Last Modified: Sat, 16 May 2026 00:10:10 GMT  
		Size: 3.4 MB (3394559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5f6bb10aafb4e20e513a5cc5d9a7e3481a971f0433332b50708cd61bc4df70`  
		Last Modified: Sat, 16 May 2026 00:10:10 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c4e8ff9e0e4eab7d4814e9d39e6a4c25f79d76d2979f00a78de155911ef2ddd`  
		Last Modified: Sat, 16 May 2026 00:10:10 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91aab9887dd46e6f833ba3ffff294c32d59299ab8d4a3847194a60a227c55b0`  
		Last Modified: Sat, 16 May 2026 00:10:10 GMT  
		Size: 11.2 MB (11236505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3459fdc6872a7acd1e3b7884a28a60561f9e3488cf19f8437a3b11c8e09a6d8`  
		Last Modified: Sat, 16 May 2026 00:10:11 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:58ffdbbba10f97b2d1ef33dbfbdf016c2844506424a34f22333f5597310a7fab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 KB (30663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a11fccc6bc4fd79d54dca7d1d3ed318788c65b63d3184fbb73c400cadceb60f`

```dockerfile
```

-	Layers:
	-	`sha256:fc110ccff973a2ba6b5d21f0f1f25d79b12b82a863abcabd81b546d627bb598c`  
		Last Modified: Sat, 16 May 2026 00:10:09 GMT  
		Size: 30.7 KB (30663 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-windowsservercore`

```console
$ docker pull docker@sha256:3268bde2385bb80b1e442f6c04799dd7619f785c63be6c4dccb6831a144f3043
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32860; amd64
	-	windows version 10.0.20348.5139; amd64

### `docker:29-windowsservercore` - windows version 10.0.26100.32860; amd64

```console
$ docker pull docker@sha256:e4420a2945552c16d362b8472d0182a0ec134ce320f2233ec15e93015e599e8f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2262478653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90d0a0d1bad4f84f1fbcaf6c1e419ce3a0952a03ed6d4582f9767303292ca6c6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 10 May 2026 10:08:54 GMT
RUN Install update 10.0.26100.32860
# Fri, 15 May 2026 22:15:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 15 May 2026 22:16:21 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 15 May 2026 22:16:22 GMT
ENV DOCKER_VERSION=29.5.0
# Fri, 15 May 2026 22:16:23 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.5.0.zip
# Fri, 15 May 2026 22:16:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 15 May 2026 22:16:39 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Fri, 15 May 2026 22:16:40 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.windows-amd64.exe
# Fri, 15 May 2026 22:16:40 GMT
ENV DOCKER_BUILDX_SHA256=96a10e259fa1380e7bbf9a3cb04872f201a6e7e331ddeeec8d3e38aa2650ddc5
# Fri, 15 May 2026 22:16:50 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 15 May 2026 22:16:51 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Fri, 15 May 2026 22:16:51 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-windows-x86_64.exe
# Fri, 15 May 2026 22:16:52 GMT
ENV DOCKER_COMPOSE_SHA256=5e6d72612b3165be9fea4ae889435fec76979a9779b6f62f4efee99dd5f41ea1
# Fri, 15 May 2026 22:17:01 GMT
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
	-	`sha256:74b535a51fd23dbc5005aa72b61e95ad333b54b6b5276fd600c8f26dc1ec6379`  
		Last Modified: Fri, 15 May 2026 22:17:10 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f1111f6cb7254129e7ea39ba28883376409a104ffda0b87a45a420ceee27fcb`  
		Last Modified: Fri, 15 May 2026 22:17:10 GMT  
		Size: 392.8 KB (392802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2db17ecf93e3efdbccd835fd5d408afb7a3351f7597a48a1ad636c01794ebe04`  
		Last Modified: Fri, 15 May 2026 22:17:09 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c83f256bcd38582b57bb91e485a2d85240d5f2ae45b27c9afa7a9a5f44ebed73`  
		Last Modified: Fri, 15 May 2026 22:17:09 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cdc10f672c38740ac0512c480a10fe4b0dc1658659e00513da102771c2e3e40`  
		Last Modified: Fri, 15 May 2026 22:17:11 GMT  
		Size: 20.3 MB (20260443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e77a9dc340d0bdbccbce6b57c4d89cad2a1db92d89f7c2649002da080b5334bd`  
		Last Modified: Fri, 15 May 2026 22:17:07 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2309766ee1a21f57c947e3ef48cf4592eb1c12fb99926f92dc710c73dff7b930`  
		Last Modified: Fri, 15 May 2026 22:17:07 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9e8a3c0bbacac0c1695cff5c5e5eeefe513850e0a04322d018dfc23f9317a07`  
		Last Modified: Fri, 15 May 2026 22:17:07 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2562224ef98ba779eb91088241d392cb2a71abbc685b008022439f669f7686d6`  
		Last Modified: Fri, 15 May 2026 22:17:09 GMT  
		Size: 23.9 MB (23920245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6af350faa47b96f1766ca0debecbe39139716c8b55ae988b2528535eed60cca`  
		Last Modified: Fri, 15 May 2026 22:17:05 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:780002467e4bb1a15f8748b2ea889bc85483b2d7ddb96b528e3b32c982692e19`  
		Last Modified: Fri, 15 May 2026 22:17:05 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47e3ee62773736f785dc51e4bc1a7e48595fe0afed17ab1d89154d1e06595d11`  
		Last Modified: Fri, 15 May 2026 22:17:05 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d076a230450a0b438ed3c7d1ee23904031d66dddd7e9ee8ac765637eb942ff8`  
		Last Modified: Fri, 15 May 2026 22:17:07 GMT  
		Size: 12.0 MB (11951730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:29-windowsservercore` - windows version 10.0.20348.5139; amd64

```console
$ docker pull docker@sha256:08c5da38b0e30b8a83bf89e16eff7a1292d6948010a051f9310d6e9511e6423f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2178998545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c8a2de39d58f5e39341f81d00642352c6b050887b387821ad49ffd590b688ad`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Fri, 15 May 2026 22:15:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 15 May 2026 22:16:42 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 15 May 2026 22:16:43 GMT
ENV DOCKER_VERSION=29.5.0
# Fri, 15 May 2026 22:16:43 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.5.0.zip
# Fri, 15 May 2026 22:16:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 15 May 2026 22:16:57 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Fri, 15 May 2026 22:16:57 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.windows-amd64.exe
# Fri, 15 May 2026 22:16:58 GMT
ENV DOCKER_BUILDX_SHA256=96a10e259fa1380e7bbf9a3cb04872f201a6e7e331ddeeec8d3e38aa2650ddc5
# Fri, 15 May 2026 22:17:07 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 15 May 2026 22:17:08 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Fri, 15 May 2026 22:17:08 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-windows-x86_64.exe
# Fri, 15 May 2026 22:17:09 GMT
ENV DOCKER_COMPOSE_SHA256=5e6d72612b3165be9fea4ae889435fec76979a9779b6f62f4efee99dd5f41ea1
# Fri, 15 May 2026 22:17:16 GMT
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
	-	`sha256:5961f3afdef68ce25fa592066416467d81416df4b1af2537087f1c9150afb728`  
		Last Modified: Fri, 15 May 2026 22:17:25 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae47499b6a77bf67c8fc4c6163dd490f816d5ea9168dfad57664888a82963cd`  
		Last Modified: Fri, 15 May 2026 22:17:25 GMT  
		Size: 506.6 KB (506623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1a50c6ae3a4766042c073c45ffd8a1c5d67595c9c560f65c76492d18a12fd50`  
		Last Modified: Fri, 15 May 2026 22:17:24 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:756530867ead10020116e1f2f106664f6fed6cae2160122fc6ec372b43fd678b`  
		Last Modified: Fri, 15 May 2026 22:17:24 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203d6d943b8fa9b8934a5ce05bf2893265e234366a62bf9ea3a09f77d5608167`  
		Last Modified: Fri, 15 May 2026 22:17:26 GMT  
		Size: 20.2 MB (20232134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f38228e51f50d7a28325477b370bd57476f2a6883a023e98c0d628bc22295ad4`  
		Last Modified: Fri, 15 May 2026 22:17:22 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f7fe5a6a8d2169e19d30f03057f1cf4e3dfa71a14a9e3e2572a95d5246c205`  
		Last Modified: Fri, 15 May 2026 22:17:22 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa5b9407c6ba09fc25979a724f032914bee3ded478b4366b26a09de96ef0c80`  
		Last Modified: Fri, 15 May 2026 22:17:22 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60bb62b675b679633b1a24e24b203fa8ed15d941f3bbb283bae34df7d68c50af`  
		Last Modified: Fri, 15 May 2026 22:17:24 GMT  
		Size: 23.9 MB (23901135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8874726604cb50cc54f506879180a624b7e0fc0e3ad5a8a7063d89505fd60ea`  
		Last Modified: Fri, 15 May 2026 22:17:20 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c7b4c5d7c92d0e67fbdf7582c6455934c8b5f3b3a8c849173931adad0837ca3`  
		Last Modified: Fri, 15 May 2026 22:17:20 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efe6f324d4756f3cd5de0642c06bbc7c60c070aa7a512c8682d7e2232291ae8b`  
		Last Modified: Fri, 15 May 2026 22:17:20 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:487382c6166366ea2b9acbadbf146f8443b6a756bfb7678718eb9c7383bc4a2c`  
		Last Modified: Fri, 15 May 2026 22:17:22 GMT  
		Size: 11.9 MB (11926255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:1c7ad5b5ef3c89a3bdc56e2574cbfe03b7327d744f4266d72447109f574789c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `docker:29-windowsservercore-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull docker@sha256:08c5da38b0e30b8a83bf89e16eff7a1292d6948010a051f9310d6e9511e6423f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2178998545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c8a2de39d58f5e39341f81d00642352c6b050887b387821ad49ffd590b688ad`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Fri, 15 May 2026 22:15:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 15 May 2026 22:16:42 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 15 May 2026 22:16:43 GMT
ENV DOCKER_VERSION=29.5.0
# Fri, 15 May 2026 22:16:43 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.5.0.zip
# Fri, 15 May 2026 22:16:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 15 May 2026 22:16:57 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Fri, 15 May 2026 22:16:57 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.windows-amd64.exe
# Fri, 15 May 2026 22:16:58 GMT
ENV DOCKER_BUILDX_SHA256=96a10e259fa1380e7bbf9a3cb04872f201a6e7e331ddeeec8d3e38aa2650ddc5
# Fri, 15 May 2026 22:17:07 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 15 May 2026 22:17:08 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Fri, 15 May 2026 22:17:08 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-windows-x86_64.exe
# Fri, 15 May 2026 22:17:09 GMT
ENV DOCKER_COMPOSE_SHA256=5e6d72612b3165be9fea4ae889435fec76979a9779b6f62f4efee99dd5f41ea1
# Fri, 15 May 2026 22:17:16 GMT
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
	-	`sha256:5961f3afdef68ce25fa592066416467d81416df4b1af2537087f1c9150afb728`  
		Last Modified: Fri, 15 May 2026 22:17:25 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae47499b6a77bf67c8fc4c6163dd490f816d5ea9168dfad57664888a82963cd`  
		Last Modified: Fri, 15 May 2026 22:17:25 GMT  
		Size: 506.6 KB (506623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1a50c6ae3a4766042c073c45ffd8a1c5d67595c9c560f65c76492d18a12fd50`  
		Last Modified: Fri, 15 May 2026 22:17:24 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:756530867ead10020116e1f2f106664f6fed6cae2160122fc6ec372b43fd678b`  
		Last Modified: Fri, 15 May 2026 22:17:24 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203d6d943b8fa9b8934a5ce05bf2893265e234366a62bf9ea3a09f77d5608167`  
		Last Modified: Fri, 15 May 2026 22:17:26 GMT  
		Size: 20.2 MB (20232134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f38228e51f50d7a28325477b370bd57476f2a6883a023e98c0d628bc22295ad4`  
		Last Modified: Fri, 15 May 2026 22:17:22 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f7fe5a6a8d2169e19d30f03057f1cf4e3dfa71a14a9e3e2572a95d5246c205`  
		Last Modified: Fri, 15 May 2026 22:17:22 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa5b9407c6ba09fc25979a724f032914bee3ded478b4366b26a09de96ef0c80`  
		Last Modified: Fri, 15 May 2026 22:17:22 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60bb62b675b679633b1a24e24b203fa8ed15d941f3bbb283bae34df7d68c50af`  
		Last Modified: Fri, 15 May 2026 22:17:24 GMT  
		Size: 23.9 MB (23901135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8874726604cb50cc54f506879180a624b7e0fc0e3ad5a8a7063d89505fd60ea`  
		Last Modified: Fri, 15 May 2026 22:17:20 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c7b4c5d7c92d0e67fbdf7582c6455934c8b5f3b3a8c849173931adad0837ca3`  
		Last Modified: Fri, 15 May 2026 22:17:20 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efe6f324d4756f3cd5de0642c06bbc7c60c070aa7a512c8682d7e2232291ae8b`  
		Last Modified: Fri, 15 May 2026 22:17:20 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:487382c6166366ea2b9acbadbf146f8443b6a756bfb7678718eb9c7383bc4a2c`  
		Last Modified: Fri, 15 May 2026 22:17:22 GMT  
		Size: 11.9 MB (11926255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:d385e3828e8366b07bd0af1a4b025c4feb365a506fedb8e307acaae417e63f72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32860; amd64

### `docker:29-windowsservercore-ltsc2025` - windows version 10.0.26100.32860; amd64

```console
$ docker pull docker@sha256:e4420a2945552c16d362b8472d0182a0ec134ce320f2233ec15e93015e599e8f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2262478653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90d0a0d1bad4f84f1fbcaf6c1e419ce3a0952a03ed6d4582f9767303292ca6c6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 10 May 2026 10:08:54 GMT
RUN Install update 10.0.26100.32860
# Fri, 15 May 2026 22:15:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 15 May 2026 22:16:21 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 15 May 2026 22:16:22 GMT
ENV DOCKER_VERSION=29.5.0
# Fri, 15 May 2026 22:16:23 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.5.0.zip
# Fri, 15 May 2026 22:16:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 15 May 2026 22:16:39 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Fri, 15 May 2026 22:16:40 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.windows-amd64.exe
# Fri, 15 May 2026 22:16:40 GMT
ENV DOCKER_BUILDX_SHA256=96a10e259fa1380e7bbf9a3cb04872f201a6e7e331ddeeec8d3e38aa2650ddc5
# Fri, 15 May 2026 22:16:50 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 15 May 2026 22:16:51 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Fri, 15 May 2026 22:16:51 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-windows-x86_64.exe
# Fri, 15 May 2026 22:16:52 GMT
ENV DOCKER_COMPOSE_SHA256=5e6d72612b3165be9fea4ae889435fec76979a9779b6f62f4efee99dd5f41ea1
# Fri, 15 May 2026 22:17:01 GMT
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
	-	`sha256:74b535a51fd23dbc5005aa72b61e95ad333b54b6b5276fd600c8f26dc1ec6379`  
		Last Modified: Fri, 15 May 2026 22:17:10 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f1111f6cb7254129e7ea39ba28883376409a104ffda0b87a45a420ceee27fcb`  
		Last Modified: Fri, 15 May 2026 22:17:10 GMT  
		Size: 392.8 KB (392802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2db17ecf93e3efdbccd835fd5d408afb7a3351f7597a48a1ad636c01794ebe04`  
		Last Modified: Fri, 15 May 2026 22:17:09 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c83f256bcd38582b57bb91e485a2d85240d5f2ae45b27c9afa7a9a5f44ebed73`  
		Last Modified: Fri, 15 May 2026 22:17:09 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cdc10f672c38740ac0512c480a10fe4b0dc1658659e00513da102771c2e3e40`  
		Last Modified: Fri, 15 May 2026 22:17:11 GMT  
		Size: 20.3 MB (20260443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e77a9dc340d0bdbccbce6b57c4d89cad2a1db92d89f7c2649002da080b5334bd`  
		Last Modified: Fri, 15 May 2026 22:17:07 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2309766ee1a21f57c947e3ef48cf4592eb1c12fb99926f92dc710c73dff7b930`  
		Last Modified: Fri, 15 May 2026 22:17:07 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9e8a3c0bbacac0c1695cff5c5e5eeefe513850e0a04322d018dfc23f9317a07`  
		Last Modified: Fri, 15 May 2026 22:17:07 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2562224ef98ba779eb91088241d392cb2a71abbc685b008022439f669f7686d6`  
		Last Modified: Fri, 15 May 2026 22:17:09 GMT  
		Size: 23.9 MB (23920245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6af350faa47b96f1766ca0debecbe39139716c8b55ae988b2528535eed60cca`  
		Last Modified: Fri, 15 May 2026 22:17:05 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:780002467e4bb1a15f8748b2ea889bc85483b2d7ddb96b528e3b32c982692e19`  
		Last Modified: Fri, 15 May 2026 22:17:05 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47e3ee62773736f785dc51e4bc1a7e48595fe0afed17ab1d89154d1e06595d11`  
		Last Modified: Fri, 15 May 2026 22:17:05 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d076a230450a0b438ed3c7d1ee23904031d66dddd7e9ee8ac765637eb942ff8`  
		Last Modified: Fri, 15 May 2026 22:17:07 GMT  
		Size: 12.0 MB (11951730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.5`

```console
$ docker pull docker@sha256:d0c942e5e2c14a74da706cff670ea2449fb57f9bc6abae7164461d0c6322b8b4
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
$ docker pull docker@sha256:74328f9b3824edb27d1c5b57abfa5765aa1742806ad77e3e90b2ee328aba8301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.7 MB (141655694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71837a59b95c3653383ca90ce81fbcee4f34adb0fbbf8b357e75da9affc77579`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Fri, 15 May 2026 22:12:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 15 May 2026 22:12:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 15 May 2026 22:12:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 15 May 2026 22:12:17 GMT
ENV DOCKER_VERSION=29.5.0
# Fri, 15 May 2026 22:12:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 15 May 2026 22:12:17 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Fri, 15 May 2026 22:12:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-amd64'; 			sha256='0144479d5a1cd710be3464ae898628cfa68033e16b225aef52f81930c45ac9b5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v6'; 			sha256='1f34337385921c5da43d63452282726b062aa887fda975f96dd3d6e869648bc6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v7'; 			sha256='3560b5b6fd3485f4d0bd160e7edf56cc1f08f0cb5852c9af28bf3fab9973c7c2'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm64'; 			sha256='565605fe0bb393ed5d11771e5b52fc7ef05c701868861fa85609747c9d74a440'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-ppc64le'; 			sha256='c5ef8012f48a518e1c235ad408d26cd424d7b5fa87eaf78cb2ff4b9048730120'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-riscv64'; 			sha256='80b27d5f3a346591a5045b81217ee5be578ed151ef8cbd883a892c0ec0ac33f1'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-s390x'; 			sha256='04f5bd0d389f682c7e9287a3b3a1777b0848f8e10d58cbf9d4d12c9002bbb378'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 15 May 2026 22:12:18 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Fri, 15 May 2026 22:12:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 15 May 2026 22:12:19 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 15 May 2026 22:12:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 22:12:19 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 15 May 2026 22:12:19 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 15 May 2026 22:12:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2026 22:12:19 GMT
CMD ["sh"]
# Fri, 15 May 2026 22:45:52 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 15 May 2026 22:45:52 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 15 May 2026 22:45:52 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 15 May 2026 22:45:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 15 May 2026 22:45:55 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 15 May 2026 22:45:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 15 May 2026 22:45:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 22:45:55 GMT
VOLUME [/var/lib/docker]
# Fri, 15 May 2026 22:45:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 15 May 2026 22:45:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 15 May 2026 22:45:55 GMT
CMD []
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2240a8f6be9241c8313b7887a9f6b272758fa6f323a29ae88da91f004c59d0d6`  
		Last Modified: Fri, 15 May 2026 22:12:26 GMT  
		Size: 8.3 MB (8311611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee8f29570b73bc6fb95364db2374f726e9b921827f4d1383a6d310769c050e2`  
		Last Modified: Fri, 15 May 2026 22:12:26 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb157a4a9b724e516e2a50f94be797a8145642f3c45f0f8d7bc236aa4848960`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 19.5 MB (19549502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f6e87dc813cb0ce7fd8d1277ed2d283a03d11b6492284e50fc16c959ccf8cb1`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 23.0 MB (22988578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4642ba5a86eb9921fd340045e353c9b3723a87f535731ae12659016c86bd3a48`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 11.2 MB (11243758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53d662cd1653019365b80d59af307d893de60a95d5d03aa7faddf0654b0162a7`  
		Last Modified: Fri, 15 May 2026 22:12:28 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45636b869c7065c939fb09da20708b05eb4bffe960ae3cb0102e1101147bf702`  
		Last Modified: Fri, 15 May 2026 22:12:28 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9074eaed06bf00c4914e361b510e55cd12bb8b0305b732d777ef95e01914b4f4`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f0de530d70a206bbf99372d4e80b56da6aa52a05b01bd6390d3bb3f4317466`  
		Last Modified: Fri, 15 May 2026 22:46:06 GMT  
		Size: 6.9 MB (6941385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc4ad90df2e9375f24da713fdbd03d16ffd44bcab544ed61a9d388fcc342e85`  
		Last Modified: Fri, 15 May 2026 22:46:06 GMT  
		Size: 92.2 KB (92210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f7d81cca6c2e02237a63044b96fc4e4432bffd61e595b15c8c2d952370deeed`  
		Last Modified: Fri, 15 May 2026 22:46:06 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb7196e21df03c1f04999bead8f104980dd964263cd7b78f05f013ad70dc5e2`  
		Last Modified: Fri, 15 May 2026 22:46:08 GMT  
		Size: 68.7 MB (68656308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403fc89c99ec573758e84c2e171afabefeec367c0c3ac712710c2c280fac6f51`  
		Last Modified: Fri, 15 May 2026 22:46:07 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6ba97049938b6a09c6a9ac2e32cd77fd36080fff06433e8e5f31af12220583`  
		Last Modified: Fri, 15 May 2026 22:46:07 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.5` - unknown; unknown

```console
$ docker pull docker@sha256:bd3f7470c6236fcdb2cf1e2c99310e54bbd3ad7060762321c8003d30700a4adf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c743ab7cd39dee28326b6ff67c26d9c04b6169c89078262749d30845200dbb5b`

```dockerfile
```

-	Layers:
	-	`sha256:d84803d0d069e3f761b94992b6e3e50d1af7858113038a4930bde2b44ff43a64`  
		Last Modified: Fri, 15 May 2026 22:46:06 GMT  
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
$ docker pull docker@sha256:ef239f5a75ebd13a6e3a3ab62b4968537548555442e51b74688fefeee15455d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.7 MB (131665508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e6993f94a7073e22d9d8fa213b4f91cc953dac434c0511af155e03ba2bbbd8c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Fri, 15 May 2026 22:11:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 15 May 2026 22:11:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 15 May 2026 22:12:00 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 15 May 2026 22:12:04 GMT
ENV DOCKER_VERSION=29.5.0
# Fri, 15 May 2026 22:12:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 15 May 2026 22:12:04 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Fri, 15 May 2026 22:12:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-amd64'; 			sha256='0144479d5a1cd710be3464ae898628cfa68033e16b225aef52f81930c45ac9b5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v6'; 			sha256='1f34337385921c5da43d63452282726b062aa887fda975f96dd3d6e869648bc6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v7'; 			sha256='3560b5b6fd3485f4d0bd160e7edf56cc1f08f0cb5852c9af28bf3fab9973c7c2'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm64'; 			sha256='565605fe0bb393ed5d11771e5b52fc7ef05c701868861fa85609747c9d74a440'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-ppc64le'; 			sha256='c5ef8012f48a518e1c235ad408d26cd424d7b5fa87eaf78cb2ff4b9048730120'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-riscv64'; 			sha256='80b27d5f3a346591a5045b81217ee5be578ed151ef8cbd883a892c0ec0ac33f1'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-s390x'; 			sha256='04f5bd0d389f682c7e9287a3b3a1777b0848f8e10d58cbf9d4d12c9002bbb378'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 15 May 2026 22:12:07 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Fri, 15 May 2026 22:12:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 15 May 2026 22:12:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 15 May 2026 22:12:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 22:12:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 15 May 2026 22:12:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 15 May 2026 22:12:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2026 22:12:10 GMT
CMD ["sh"]
# Fri, 15 May 2026 22:14:39 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 15 May 2026 22:14:40 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 15 May 2026 22:14:40 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 15 May 2026 22:14:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 15 May 2026 22:14:43 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 15 May 2026 22:14:43 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 15 May 2026 22:14:43 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 22:14:43 GMT
VOLUME [/var/lib/docker]
# Fri, 15 May 2026 22:14:43 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 15 May 2026 22:14:43 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 15 May 2026 22:14:43 GMT
CMD []
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb53acd779ed72fcbca92822c9c8dca72fc19b59b4367fc8edbe5c8edd184829`  
		Last Modified: Fri, 15 May 2026 22:12:16 GMT  
		Size: 7.5 MB (7520515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3717dbbea465f22997cb871db7b421cb78bfc5d2353e0fbb9c24a4d7f4eead8b`  
		Last Modified: Fri, 15 May 2026 22:12:16 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2765ebda46cc899cbdd1066e7e900d81e9e6227536c38218d156a6c6ffc93324`  
		Last Modified: Fri, 15 May 2026 22:12:17 GMT  
		Size: 18.2 MB (18172266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8e62c2751306352d388df5f6ed3f91e4f160f2da7a249168dc387777896b44`  
		Last Modified: Fri, 15 May 2026 22:12:17 GMT  
		Size: 21.6 MB (21600397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e74677ed12033b201cddf684740d6f5f9540e22ab253c874ab4d21644f5b592`  
		Last Modified: Fri, 15 May 2026 22:12:17 GMT  
		Size: 10.6 MB (10637133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d76fc015f6b878f4335aa2e01b8ef18fcc9e9b2cb962b48d46350deb994e02d`  
		Last Modified: Fri, 15 May 2026 22:12:17 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad7ca5f5e6e176e7d1835e181fe35affc2155c45a6a1148aa7f18ea76d9d05e`  
		Last Modified: Fri, 15 May 2026 22:12:18 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdab469dc84864d9800ae053f9d87586d2515da2b650cf6f13f5ee84e15b2276`  
		Last Modified: Fri, 15 May 2026 22:12:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e61fa784a50d39d698bb4131e0cdda87523cb190f1d964d336a0eb9670b6fd`  
		Last Modified: Fri, 15 May 2026 22:14:53 GMT  
		Size: 6.6 MB (6577169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6091cd81f80a383632ea922a26439e61a5003e64d76dfc3d4bfec40420f0f921`  
		Last Modified: Fri, 15 May 2026 22:14:53 GMT  
		Size: 87.8 KB (87833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:858404ad7c646164306853c3153ee071dd35b14abaf989078b504a287c341dec`  
		Last Modified: Fri, 15 May 2026 22:14:53 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4328aaffaeedc3768196c5928da4c98cee1bfc491c8e951d2dc43da2d38acd04`  
		Last Modified: Fri, 15 May 2026 22:14:55 GMT  
		Size: 63.8 MB (63778918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f84fcf533486742f994566043a25c7a7c23e263cd00704b53a1653242d0b0b8`  
		Last Modified: Fri, 15 May 2026 22:14:55 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95db86311c1bf70966aa5d474d44b82d7521ce7b749c0450d9a393fc88161168`  
		Last Modified: Fri, 15 May 2026 22:14:55 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.5` - unknown; unknown

```console
$ docker pull docker@sha256:6b79b3ac684b96301be66c5f36fd56c5a6c5756cf5a41c478f6d1945686b8349
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:709fc5e54befeab0806a68f4887f40378c59005ec285f228919d0e515f79e46b`

```dockerfile
```

-	Layers:
	-	`sha256:0107810b79e283361584a1b052454ef6bbd5468de93976e803fe7b0ac4ee3336`  
		Last Modified: Fri, 15 May 2026 22:14:53 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.5` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:6271c82062c42bdbc409cb458dce06d11f74ce961c30a90c6eb58a998c28afee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.1 MB (131088703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e575b474f12e2e286b308aeaf79fda6e9fec3855a23edec1474dc5b5b8dd4427`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Fri, 15 May 2026 22:12:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 15 May 2026 22:12:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 15 May 2026 22:12:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 15 May 2026 22:12:17 GMT
ENV DOCKER_VERSION=29.5.0
# Fri, 15 May 2026 22:12:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 15 May 2026 22:12:17 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Fri, 15 May 2026 22:12:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-amd64'; 			sha256='0144479d5a1cd710be3464ae898628cfa68033e16b225aef52f81930c45ac9b5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v6'; 			sha256='1f34337385921c5da43d63452282726b062aa887fda975f96dd3d6e869648bc6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v7'; 			sha256='3560b5b6fd3485f4d0bd160e7edf56cc1f08f0cb5852c9af28bf3fab9973c7c2'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm64'; 			sha256='565605fe0bb393ed5d11771e5b52fc7ef05c701868861fa85609747c9d74a440'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-ppc64le'; 			sha256='c5ef8012f48a518e1c235ad408d26cd424d7b5fa87eaf78cb2ff4b9048730120'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-riscv64'; 			sha256='80b27d5f3a346591a5045b81217ee5be578ed151ef8cbd883a892c0ec0ac33f1'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-s390x'; 			sha256='04f5bd0d389f682c7e9287a3b3a1777b0848f8e10d58cbf9d4d12c9002bbb378'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 15 May 2026 22:12:18 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Fri, 15 May 2026 22:12:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 15 May 2026 22:12:19 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 15 May 2026 22:12:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 22:12:19 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 15 May 2026 22:12:19 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 15 May 2026 22:12:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2026 22:12:19 GMT
CMD ["sh"]
# Fri, 15 May 2026 22:46:13 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 15 May 2026 22:46:14 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 15 May 2026 22:46:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 15 May 2026 22:46:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 15 May 2026 22:46:17 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 15 May 2026 22:46:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 15 May 2026 22:46:17 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 22:46:17 GMT
VOLUME [/var/lib/docker]
# Fri, 15 May 2026 22:46:17 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 15 May 2026 22:46:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 15 May 2026 22:46:17 GMT
CMD []
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd51147f6d8210f56d90e095c69db7468c6a7f4c96b15954bec62a38d029c230`  
		Last Modified: Fri, 15 May 2026 22:12:26 GMT  
		Size: 8.4 MB (8368382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca485120792b1bdb82820fd08df20937c87c36c02b044d113785a278f04c9c5e`  
		Last Modified: Fri, 15 May 2026 22:12:25 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76be2953b1820f6b03454f4cc64611d855fbccf3feb3c9d49c80e129eddcad5`  
		Last Modified: Fri, 15 May 2026 22:12:26 GMT  
		Size: 18.0 MB (18003835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc8387c97690c1e6db50aa3de5c90f1742500af7c360287ddfe4acd0578e0eb`  
		Last Modified: Fri, 15 May 2026 22:12:26 GMT  
		Size: 20.8 MB (20815340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3087ee8252be9dcbda43072f57a958f8f37983b3932bdca55c49fc7420da93f`  
		Last Modified: Fri, 15 May 2026 22:12:26 GMT  
		Size: 10.2 MB (10243274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027710042ccab2488d5291cd625bb62305844954e320f530f618c56b53ef928c`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0557313fec61d76b6a60306c806eb278032cfc80335daa86db37ad9979e81756`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9074eaed06bf00c4914e361b510e55cd12bb8b0305b732d777ef95e01914b4f4`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43b2d205b3daf8cb2c6ef3c0e0999b4106fc7a6595ba5568e8605a7e7b0722d8`  
		Last Modified: Fri, 15 May 2026 22:46:26 GMT  
		Size: 7.2 MB (7219897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0304531f0ed7ae27db4e86f747d65dfef2567fd5f396a4b3922c5ff5780d1f2`  
		Last Modified: Fri, 15 May 2026 22:46:26 GMT  
		Size: 100.9 KB (100934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95e602dc9bf9e82e229534494ecc27788dfc15984a25ad6683a47603dfb112ff`  
		Last Modified: Fri, 15 May 2026 22:46:26 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb752877659a29a329ac376438ffc77fd5832ef8ec7713badc224dc70797bd6`  
		Last Modified: Fri, 15 May 2026 22:46:29 GMT  
		Size: 62.1 MB (62129016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1ca5de4993dc83a36fb35a72b4fedf78533c646f254850669127c3e34a022a`  
		Last Modified: Fri, 15 May 2026 22:46:27 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27981b508a5db9a4e2a2c0b87eb0017d532fc5cc5bd11529ba120cd1e843ae91`  
		Last Modified: Fri, 15 May 2026 22:46:28 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.5` - unknown; unknown

```console
$ docker pull docker@sha256:75f2ca4085188952af0189876ba5792cdd9148db56893b95a052e1a878bd4763
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9a506d026912de6f5e76fbcaf2f074cae0ccb50f7496d643ebb7bb3454ee5b0`

```dockerfile
```

-	Layers:
	-	`sha256:8cf936b97b7e42d4fcbb8824339486e8226b6af0c069484bcb894b3a1d54a301`  
		Last Modified: Fri, 15 May 2026 22:46:26 GMT  
		Size: 34.8 KB (34782 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.5-cli`

```console
$ docker pull docker@sha256:22eb9db6081c0bc3c05137a5e8f26720e1b09aaafd3f18b923b494bcd6283a3a
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
$ docker pull docker@sha256:93afea9ac780f8706540408cba1e801ba285071476b0c2bff424a0ca0037869c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.0 MB (65959799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54560465c89852384428d8b003c70278f2a11fdee74fde28173fea1077416da9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:29.5-cli` - unknown; unknown

```console
$ docker pull docker@sha256:e6e636232d7064d32da9c46ef93c11a565c43d61068daa1785a2d63bb664c190
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:973ee0a24a2536030656c4b9be0b463122f73df6150f6b0949b3d3601798afd1`

```dockerfile
```

-	Layers:
	-	`sha256:dbed7195f208034adcef893e2efc57ce071c5d914a8a9624d5a8a7fbb1a9f99e`  
		Last Modified: Tue, 19 May 2026 18:44:01 GMT  
		Size: 38.1 KB (38056 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.5-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:663439730373cf7597a3f83ae50ab11f8a171b59b1e9ce95a730be4c0b42eb22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62234030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f0de2aee792b8ce4ffb303432b131ae0026fdd58af954221ecf5bcb4f293705`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:29.5-cli` - unknown; unknown

```console
$ docker pull docker@sha256:866404ab9edde4226ee79d91959d86956cc3fe71a933e10c9c282f3bb9fe1e24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1f84764e1609e718085281484003ba89b5bd9d8cbb6984808cae3079115e48a`

```dockerfile
```

-	Layers:
	-	`sha256:60a6451bb1e2eecccb01163a32454bf66adbc39c153e56f1b682485c3f73fbc4`  
		Last Modified: Tue, 19 May 2026 18:46:40 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.5-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:9ec11722eadaf4ecb19592ea19d512fc17ef941738677435dc52f1f70e3b4da2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61215589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:376a20891ab4edb0bcada5d8b3ba3f89f105c6351ce5368f2cafee22c9c2e764`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Fri, 15 May 2026 22:11:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 15 May 2026 22:11:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 15 May 2026 22:12:00 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 15 May 2026 22:12:04 GMT
ENV DOCKER_VERSION=29.5.0
# Fri, 15 May 2026 22:12:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 15 May 2026 22:12:04 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Fri, 15 May 2026 22:12:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-amd64'; 			sha256='0144479d5a1cd710be3464ae898628cfa68033e16b225aef52f81930c45ac9b5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v6'; 			sha256='1f34337385921c5da43d63452282726b062aa887fda975f96dd3d6e869648bc6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v7'; 			sha256='3560b5b6fd3485f4d0bd160e7edf56cc1f08f0cb5852c9af28bf3fab9973c7c2'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm64'; 			sha256='565605fe0bb393ed5d11771e5b52fc7ef05c701868861fa85609747c9d74a440'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-ppc64le'; 			sha256='c5ef8012f48a518e1c235ad408d26cd424d7b5fa87eaf78cb2ff4b9048730120'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-riscv64'; 			sha256='80b27d5f3a346591a5045b81217ee5be578ed151ef8cbd883a892c0ec0ac33f1'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-s390x'; 			sha256='04f5bd0d389f682c7e9287a3b3a1777b0848f8e10d58cbf9d4d12c9002bbb378'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 15 May 2026 22:12:07 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Fri, 15 May 2026 22:12:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 15 May 2026 22:12:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 15 May 2026 22:12:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 22:12:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 15 May 2026 22:12:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 15 May 2026 22:12:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2026 22:12:10 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb53acd779ed72fcbca92822c9c8dca72fc19b59b4367fc8edbe5c8edd184829`  
		Last Modified: Fri, 15 May 2026 22:12:16 GMT  
		Size: 7.5 MB (7520515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3717dbbea465f22997cb871db7b421cb78bfc5d2353e0fbb9c24a4d7f4eead8b`  
		Last Modified: Fri, 15 May 2026 22:12:16 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2765ebda46cc899cbdd1066e7e900d81e9e6227536c38218d156a6c6ffc93324`  
		Last Modified: Fri, 15 May 2026 22:12:17 GMT  
		Size: 18.2 MB (18172266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8e62c2751306352d388df5f6ed3f91e4f160f2da7a249168dc387777896b44`  
		Last Modified: Fri, 15 May 2026 22:12:17 GMT  
		Size: 21.6 MB (21600397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e74677ed12033b201cddf684740d6f5f9540e22ab253c874ab4d21644f5b592`  
		Last Modified: Fri, 15 May 2026 22:12:17 GMT  
		Size: 10.6 MB (10637133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d76fc015f6b878f4335aa2e01b8ef18fcc9e9b2cb962b48d46350deb994e02d`  
		Last Modified: Fri, 15 May 2026 22:12:17 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad7ca5f5e6e176e7d1835e181fe35affc2155c45a6a1148aa7f18ea76d9d05e`  
		Last Modified: Fri, 15 May 2026 22:12:18 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdab469dc84864d9800ae053f9d87586d2515da2b650cf6f13f5ee84e15b2276`  
		Last Modified: Fri, 15 May 2026 22:12:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.5-cli` - unknown; unknown

```console
$ docker pull docker@sha256:3733f58f759836ce9f96949b34cf083d5873acad577a5181e080afb4bf3249f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14f8c9cf97e3e4d9ec70c8edcea1d71eca3c988ea012b28acc4d35eea629ae37`

```dockerfile
```

-	Layers:
	-	`sha256:7ce1554139b841ff42f6ca82b422a07755ca34b9f40a43a8f69db42b7b360f47`  
		Last Modified: Fri, 15 May 2026 22:12:16 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.5-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e211ecf9a3c37d57418eef652252ba0ca62fc942cdfa0d8dec160bc3086bd9c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61632856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee4f6ad10554b836d3f6dad4bf015212f96fc505f746c44c549df3e29d3fd2a2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Fri, 15 May 2026 22:12:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 15 May 2026 22:12:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 15 May 2026 22:12:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 15 May 2026 22:12:17 GMT
ENV DOCKER_VERSION=29.5.0
# Fri, 15 May 2026 22:12:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 15 May 2026 22:12:17 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Fri, 15 May 2026 22:12:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-amd64'; 			sha256='0144479d5a1cd710be3464ae898628cfa68033e16b225aef52f81930c45ac9b5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v6'; 			sha256='1f34337385921c5da43d63452282726b062aa887fda975f96dd3d6e869648bc6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v7'; 			sha256='3560b5b6fd3485f4d0bd160e7edf56cc1f08f0cb5852c9af28bf3fab9973c7c2'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm64'; 			sha256='565605fe0bb393ed5d11771e5b52fc7ef05c701868861fa85609747c9d74a440'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-ppc64le'; 			sha256='c5ef8012f48a518e1c235ad408d26cd424d7b5fa87eaf78cb2ff4b9048730120'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-riscv64'; 			sha256='80b27d5f3a346591a5045b81217ee5be578ed151ef8cbd883a892c0ec0ac33f1'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-s390x'; 			sha256='04f5bd0d389f682c7e9287a3b3a1777b0848f8e10d58cbf9d4d12c9002bbb378'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 15 May 2026 22:12:18 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Fri, 15 May 2026 22:12:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 15 May 2026 22:12:19 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 15 May 2026 22:12:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 22:12:19 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 15 May 2026 22:12:19 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 15 May 2026 22:12:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2026 22:12:19 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd51147f6d8210f56d90e095c69db7468c6a7f4c96b15954bec62a38d029c230`  
		Last Modified: Fri, 15 May 2026 22:12:26 GMT  
		Size: 8.4 MB (8368382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca485120792b1bdb82820fd08df20937c87c36c02b044d113785a278f04c9c5e`  
		Last Modified: Fri, 15 May 2026 22:12:25 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76be2953b1820f6b03454f4cc64611d855fbccf3feb3c9d49c80e129eddcad5`  
		Last Modified: Fri, 15 May 2026 22:12:26 GMT  
		Size: 18.0 MB (18003835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc8387c97690c1e6db50aa3de5c90f1742500af7c360287ddfe4acd0578e0eb`  
		Last Modified: Fri, 15 May 2026 22:12:26 GMT  
		Size: 20.8 MB (20815340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3087ee8252be9dcbda43072f57a958f8f37983b3932bdca55c49fc7420da93f`  
		Last Modified: Fri, 15 May 2026 22:12:26 GMT  
		Size: 10.2 MB (10243274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027710042ccab2488d5291cd625bb62305844954e320f530f618c56b53ef928c`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0557313fec61d76b6a60306c806eb278032cfc80335daa86db37ad9979e81756`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9074eaed06bf00c4914e361b510e55cd12bb8b0305b732d777ef95e01914b4f4`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.5-cli` - unknown; unknown

```console
$ docker pull docker@sha256:06da91c70ff029cd54c906f93a84997c38caa126b495b2f94c29d83561aa534a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c299b9b46a49c14a1255ad31a3c17438482a28e9408b1dcd36db58d87d66247`

```dockerfile
```

-	Layers:
	-	`sha256:912e2047614870aa935e1c45fd05fb52050a876007557a6795c50c8237ff6549`  
		Last Modified: Fri, 15 May 2026 22:12:24 GMT  
		Size: 38.3 KB (38262 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.5-dind`

```console
$ docker pull docker@sha256:d0c942e5e2c14a74da706cff670ea2449fb57f9bc6abae7164461d0c6322b8b4
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
$ docker pull docker@sha256:74328f9b3824edb27d1c5b57abfa5765aa1742806ad77e3e90b2ee328aba8301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.7 MB (141655694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71837a59b95c3653383ca90ce81fbcee4f34adb0fbbf8b357e75da9affc77579`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Fri, 15 May 2026 22:12:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 15 May 2026 22:12:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 15 May 2026 22:12:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 15 May 2026 22:12:17 GMT
ENV DOCKER_VERSION=29.5.0
# Fri, 15 May 2026 22:12:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 15 May 2026 22:12:17 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Fri, 15 May 2026 22:12:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-amd64'; 			sha256='0144479d5a1cd710be3464ae898628cfa68033e16b225aef52f81930c45ac9b5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v6'; 			sha256='1f34337385921c5da43d63452282726b062aa887fda975f96dd3d6e869648bc6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v7'; 			sha256='3560b5b6fd3485f4d0bd160e7edf56cc1f08f0cb5852c9af28bf3fab9973c7c2'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm64'; 			sha256='565605fe0bb393ed5d11771e5b52fc7ef05c701868861fa85609747c9d74a440'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-ppc64le'; 			sha256='c5ef8012f48a518e1c235ad408d26cd424d7b5fa87eaf78cb2ff4b9048730120'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-riscv64'; 			sha256='80b27d5f3a346591a5045b81217ee5be578ed151ef8cbd883a892c0ec0ac33f1'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-s390x'; 			sha256='04f5bd0d389f682c7e9287a3b3a1777b0848f8e10d58cbf9d4d12c9002bbb378'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 15 May 2026 22:12:18 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Fri, 15 May 2026 22:12:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 15 May 2026 22:12:19 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 15 May 2026 22:12:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 22:12:19 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 15 May 2026 22:12:19 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 15 May 2026 22:12:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2026 22:12:19 GMT
CMD ["sh"]
# Fri, 15 May 2026 22:45:52 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 15 May 2026 22:45:52 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 15 May 2026 22:45:52 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 15 May 2026 22:45:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 15 May 2026 22:45:55 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 15 May 2026 22:45:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 15 May 2026 22:45:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 22:45:55 GMT
VOLUME [/var/lib/docker]
# Fri, 15 May 2026 22:45:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 15 May 2026 22:45:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 15 May 2026 22:45:55 GMT
CMD []
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2240a8f6be9241c8313b7887a9f6b272758fa6f323a29ae88da91f004c59d0d6`  
		Last Modified: Fri, 15 May 2026 22:12:26 GMT  
		Size: 8.3 MB (8311611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee8f29570b73bc6fb95364db2374f726e9b921827f4d1383a6d310769c050e2`  
		Last Modified: Fri, 15 May 2026 22:12:26 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb157a4a9b724e516e2a50f94be797a8145642f3c45f0f8d7bc236aa4848960`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 19.5 MB (19549502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f6e87dc813cb0ce7fd8d1277ed2d283a03d11b6492284e50fc16c959ccf8cb1`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 23.0 MB (22988578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4642ba5a86eb9921fd340045e353c9b3723a87f535731ae12659016c86bd3a48`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 11.2 MB (11243758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53d662cd1653019365b80d59af307d893de60a95d5d03aa7faddf0654b0162a7`  
		Last Modified: Fri, 15 May 2026 22:12:28 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45636b869c7065c939fb09da20708b05eb4bffe960ae3cb0102e1101147bf702`  
		Last Modified: Fri, 15 May 2026 22:12:28 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9074eaed06bf00c4914e361b510e55cd12bb8b0305b732d777ef95e01914b4f4`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f0de530d70a206bbf99372d4e80b56da6aa52a05b01bd6390d3bb3f4317466`  
		Last Modified: Fri, 15 May 2026 22:46:06 GMT  
		Size: 6.9 MB (6941385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc4ad90df2e9375f24da713fdbd03d16ffd44bcab544ed61a9d388fcc342e85`  
		Last Modified: Fri, 15 May 2026 22:46:06 GMT  
		Size: 92.2 KB (92210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f7d81cca6c2e02237a63044b96fc4e4432bffd61e595b15c8c2d952370deeed`  
		Last Modified: Fri, 15 May 2026 22:46:06 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb7196e21df03c1f04999bead8f104980dd964263cd7b78f05f013ad70dc5e2`  
		Last Modified: Fri, 15 May 2026 22:46:08 GMT  
		Size: 68.7 MB (68656308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403fc89c99ec573758e84c2e171afabefeec367c0c3ac712710c2c280fac6f51`  
		Last Modified: Fri, 15 May 2026 22:46:07 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6ba97049938b6a09c6a9ac2e32cd77fd36080fff06433e8e5f31af12220583`  
		Last Modified: Fri, 15 May 2026 22:46:07 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.5-dind` - unknown; unknown

```console
$ docker pull docker@sha256:bd3f7470c6236fcdb2cf1e2c99310e54bbd3ad7060762321c8003d30700a4adf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c743ab7cd39dee28326b6ff67c26d9c04b6169c89078262749d30845200dbb5b`

```dockerfile
```

-	Layers:
	-	`sha256:d84803d0d069e3f761b94992b6e3e50d1af7858113038a4930bde2b44ff43a64`  
		Last Modified: Fri, 15 May 2026 22:46:06 GMT  
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
$ docker pull docker@sha256:ef239f5a75ebd13a6e3a3ab62b4968537548555442e51b74688fefeee15455d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.7 MB (131665508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e6993f94a7073e22d9d8fa213b4f91cc953dac434c0511af155e03ba2bbbd8c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Fri, 15 May 2026 22:11:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 15 May 2026 22:11:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 15 May 2026 22:12:00 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 15 May 2026 22:12:04 GMT
ENV DOCKER_VERSION=29.5.0
# Fri, 15 May 2026 22:12:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 15 May 2026 22:12:04 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Fri, 15 May 2026 22:12:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-amd64'; 			sha256='0144479d5a1cd710be3464ae898628cfa68033e16b225aef52f81930c45ac9b5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v6'; 			sha256='1f34337385921c5da43d63452282726b062aa887fda975f96dd3d6e869648bc6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v7'; 			sha256='3560b5b6fd3485f4d0bd160e7edf56cc1f08f0cb5852c9af28bf3fab9973c7c2'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm64'; 			sha256='565605fe0bb393ed5d11771e5b52fc7ef05c701868861fa85609747c9d74a440'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-ppc64le'; 			sha256='c5ef8012f48a518e1c235ad408d26cd424d7b5fa87eaf78cb2ff4b9048730120'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-riscv64'; 			sha256='80b27d5f3a346591a5045b81217ee5be578ed151ef8cbd883a892c0ec0ac33f1'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-s390x'; 			sha256='04f5bd0d389f682c7e9287a3b3a1777b0848f8e10d58cbf9d4d12c9002bbb378'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 15 May 2026 22:12:07 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Fri, 15 May 2026 22:12:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 15 May 2026 22:12:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 15 May 2026 22:12:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 22:12:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 15 May 2026 22:12:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 15 May 2026 22:12:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2026 22:12:10 GMT
CMD ["sh"]
# Fri, 15 May 2026 22:14:39 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 15 May 2026 22:14:40 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 15 May 2026 22:14:40 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 15 May 2026 22:14:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 15 May 2026 22:14:43 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 15 May 2026 22:14:43 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 15 May 2026 22:14:43 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 22:14:43 GMT
VOLUME [/var/lib/docker]
# Fri, 15 May 2026 22:14:43 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 15 May 2026 22:14:43 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 15 May 2026 22:14:43 GMT
CMD []
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb53acd779ed72fcbca92822c9c8dca72fc19b59b4367fc8edbe5c8edd184829`  
		Last Modified: Fri, 15 May 2026 22:12:16 GMT  
		Size: 7.5 MB (7520515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3717dbbea465f22997cb871db7b421cb78bfc5d2353e0fbb9c24a4d7f4eead8b`  
		Last Modified: Fri, 15 May 2026 22:12:16 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2765ebda46cc899cbdd1066e7e900d81e9e6227536c38218d156a6c6ffc93324`  
		Last Modified: Fri, 15 May 2026 22:12:17 GMT  
		Size: 18.2 MB (18172266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8e62c2751306352d388df5f6ed3f91e4f160f2da7a249168dc387777896b44`  
		Last Modified: Fri, 15 May 2026 22:12:17 GMT  
		Size: 21.6 MB (21600397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e74677ed12033b201cddf684740d6f5f9540e22ab253c874ab4d21644f5b592`  
		Last Modified: Fri, 15 May 2026 22:12:17 GMT  
		Size: 10.6 MB (10637133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d76fc015f6b878f4335aa2e01b8ef18fcc9e9b2cb962b48d46350deb994e02d`  
		Last Modified: Fri, 15 May 2026 22:12:17 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad7ca5f5e6e176e7d1835e181fe35affc2155c45a6a1148aa7f18ea76d9d05e`  
		Last Modified: Fri, 15 May 2026 22:12:18 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdab469dc84864d9800ae053f9d87586d2515da2b650cf6f13f5ee84e15b2276`  
		Last Modified: Fri, 15 May 2026 22:12:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e61fa784a50d39d698bb4131e0cdda87523cb190f1d964d336a0eb9670b6fd`  
		Last Modified: Fri, 15 May 2026 22:14:53 GMT  
		Size: 6.6 MB (6577169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6091cd81f80a383632ea922a26439e61a5003e64d76dfc3d4bfec40420f0f921`  
		Last Modified: Fri, 15 May 2026 22:14:53 GMT  
		Size: 87.8 KB (87833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:858404ad7c646164306853c3153ee071dd35b14abaf989078b504a287c341dec`  
		Last Modified: Fri, 15 May 2026 22:14:53 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4328aaffaeedc3768196c5928da4c98cee1bfc491c8e951d2dc43da2d38acd04`  
		Last Modified: Fri, 15 May 2026 22:14:55 GMT  
		Size: 63.8 MB (63778918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f84fcf533486742f994566043a25c7a7c23e263cd00704b53a1653242d0b0b8`  
		Last Modified: Fri, 15 May 2026 22:14:55 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95db86311c1bf70966aa5d474d44b82d7521ce7b749c0450d9a393fc88161168`  
		Last Modified: Fri, 15 May 2026 22:14:55 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.5-dind` - unknown; unknown

```console
$ docker pull docker@sha256:6b79b3ac684b96301be66c5f36fd56c5a6c5756cf5a41c478f6d1945686b8349
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:709fc5e54befeab0806a68f4887f40378c59005ec285f228919d0e515f79e46b`

```dockerfile
```

-	Layers:
	-	`sha256:0107810b79e283361584a1b052454ef6bbd5468de93976e803fe7b0ac4ee3336`  
		Last Modified: Fri, 15 May 2026 22:14:53 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.5-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:6271c82062c42bdbc409cb458dce06d11f74ce961c30a90c6eb58a998c28afee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.1 MB (131088703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e575b474f12e2e286b308aeaf79fda6e9fec3855a23edec1474dc5b5b8dd4427`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Fri, 15 May 2026 22:12:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 15 May 2026 22:12:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 15 May 2026 22:12:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 15 May 2026 22:12:17 GMT
ENV DOCKER_VERSION=29.5.0
# Fri, 15 May 2026 22:12:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 15 May 2026 22:12:17 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Fri, 15 May 2026 22:12:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-amd64'; 			sha256='0144479d5a1cd710be3464ae898628cfa68033e16b225aef52f81930c45ac9b5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v6'; 			sha256='1f34337385921c5da43d63452282726b062aa887fda975f96dd3d6e869648bc6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v7'; 			sha256='3560b5b6fd3485f4d0bd160e7edf56cc1f08f0cb5852c9af28bf3fab9973c7c2'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm64'; 			sha256='565605fe0bb393ed5d11771e5b52fc7ef05c701868861fa85609747c9d74a440'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-ppc64le'; 			sha256='c5ef8012f48a518e1c235ad408d26cd424d7b5fa87eaf78cb2ff4b9048730120'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-riscv64'; 			sha256='80b27d5f3a346591a5045b81217ee5be578ed151ef8cbd883a892c0ec0ac33f1'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-s390x'; 			sha256='04f5bd0d389f682c7e9287a3b3a1777b0848f8e10d58cbf9d4d12c9002bbb378'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 15 May 2026 22:12:18 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Fri, 15 May 2026 22:12:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 15 May 2026 22:12:19 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 15 May 2026 22:12:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 22:12:19 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 15 May 2026 22:12:19 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 15 May 2026 22:12:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2026 22:12:19 GMT
CMD ["sh"]
# Fri, 15 May 2026 22:46:13 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 15 May 2026 22:46:14 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 15 May 2026 22:46:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 15 May 2026 22:46:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 15 May 2026 22:46:17 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 15 May 2026 22:46:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 15 May 2026 22:46:17 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 22:46:17 GMT
VOLUME [/var/lib/docker]
# Fri, 15 May 2026 22:46:17 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 15 May 2026 22:46:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 15 May 2026 22:46:17 GMT
CMD []
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd51147f6d8210f56d90e095c69db7468c6a7f4c96b15954bec62a38d029c230`  
		Last Modified: Fri, 15 May 2026 22:12:26 GMT  
		Size: 8.4 MB (8368382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca485120792b1bdb82820fd08df20937c87c36c02b044d113785a278f04c9c5e`  
		Last Modified: Fri, 15 May 2026 22:12:25 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76be2953b1820f6b03454f4cc64611d855fbccf3feb3c9d49c80e129eddcad5`  
		Last Modified: Fri, 15 May 2026 22:12:26 GMT  
		Size: 18.0 MB (18003835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc8387c97690c1e6db50aa3de5c90f1742500af7c360287ddfe4acd0578e0eb`  
		Last Modified: Fri, 15 May 2026 22:12:26 GMT  
		Size: 20.8 MB (20815340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3087ee8252be9dcbda43072f57a958f8f37983b3932bdca55c49fc7420da93f`  
		Last Modified: Fri, 15 May 2026 22:12:26 GMT  
		Size: 10.2 MB (10243274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027710042ccab2488d5291cd625bb62305844954e320f530f618c56b53ef928c`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0557313fec61d76b6a60306c806eb278032cfc80335daa86db37ad9979e81756`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9074eaed06bf00c4914e361b510e55cd12bb8b0305b732d777ef95e01914b4f4`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43b2d205b3daf8cb2c6ef3c0e0999b4106fc7a6595ba5568e8605a7e7b0722d8`  
		Last Modified: Fri, 15 May 2026 22:46:26 GMT  
		Size: 7.2 MB (7219897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0304531f0ed7ae27db4e86f747d65dfef2567fd5f396a4b3922c5ff5780d1f2`  
		Last Modified: Fri, 15 May 2026 22:46:26 GMT  
		Size: 100.9 KB (100934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95e602dc9bf9e82e229534494ecc27788dfc15984a25ad6683a47603dfb112ff`  
		Last Modified: Fri, 15 May 2026 22:46:26 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb752877659a29a329ac376438ffc77fd5832ef8ec7713badc224dc70797bd6`  
		Last Modified: Fri, 15 May 2026 22:46:29 GMT  
		Size: 62.1 MB (62129016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1ca5de4993dc83a36fb35a72b4fedf78533c646f254850669127c3e34a022a`  
		Last Modified: Fri, 15 May 2026 22:46:27 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27981b508a5db9a4e2a2c0b87eb0017d532fc5cc5bd11529ba120cd1e843ae91`  
		Last Modified: Fri, 15 May 2026 22:46:28 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.5-dind` - unknown; unknown

```console
$ docker pull docker@sha256:75f2ca4085188952af0189876ba5792cdd9148db56893b95a052e1a878bd4763
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9a506d026912de6f5e76fbcaf2f074cae0ccb50f7496d643ebb7bb3454ee5b0`

```dockerfile
```

-	Layers:
	-	`sha256:8cf936b97b7e42d4fcbb8824339486e8226b6af0c069484bcb894b3a1d54a301`  
		Last Modified: Fri, 15 May 2026 22:46:26 GMT  
		Size: 34.8 KB (34782 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.5-dind-rootless`

```console
$ docker pull docker@sha256:2379588ca8e9ed0d452464f4aed5361da6361791ec1a2111d44515c3985b2659
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:29.5-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:86dd1e4303fe60a2cd5f155db3c77e30011cfd8aaa9950188cece42d5e9f8ac3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157179647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f66937a706e25d69d45209cbd13b73c920e1d5ae4415214c93da738b95c779a0`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Fri, 15 May 2026 22:12:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 15 May 2026 22:12:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 15 May 2026 22:12:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 15 May 2026 22:12:17 GMT
ENV DOCKER_VERSION=29.5.0
# Fri, 15 May 2026 22:12:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 15 May 2026 22:12:17 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Fri, 15 May 2026 22:12:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-amd64'; 			sha256='0144479d5a1cd710be3464ae898628cfa68033e16b225aef52f81930c45ac9b5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v6'; 			sha256='1f34337385921c5da43d63452282726b062aa887fda975f96dd3d6e869648bc6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v7'; 			sha256='3560b5b6fd3485f4d0bd160e7edf56cc1f08f0cb5852c9af28bf3fab9973c7c2'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm64'; 			sha256='565605fe0bb393ed5d11771e5b52fc7ef05c701868861fa85609747c9d74a440'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-ppc64le'; 			sha256='c5ef8012f48a518e1c235ad408d26cd424d7b5fa87eaf78cb2ff4b9048730120'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-riscv64'; 			sha256='80b27d5f3a346591a5045b81217ee5be578ed151ef8cbd883a892c0ec0ac33f1'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-s390x'; 			sha256='04f5bd0d389f682c7e9287a3b3a1777b0848f8e10d58cbf9d4d12c9002bbb378'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 15 May 2026 22:12:18 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Fri, 15 May 2026 22:12:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 15 May 2026 22:12:19 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 15 May 2026 22:12:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 22:12:19 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 15 May 2026 22:12:19 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 15 May 2026 22:12:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2026 22:12:19 GMT
CMD ["sh"]
# Fri, 15 May 2026 22:45:52 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 15 May 2026 22:45:52 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 15 May 2026 22:45:52 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 15 May 2026 22:45:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 15 May 2026 22:45:55 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 15 May 2026 22:45:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 15 May 2026 22:45:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 22:45:55 GMT
VOLUME [/var/lib/docker]
# Fri, 15 May 2026 22:45:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 15 May 2026 22:45:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 15 May 2026 22:45:55 GMT
CMD []
# Sat, 16 May 2026 00:10:18 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Sat, 16 May 2026 00:10:18 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Sat, 16 May 2026 00:10:18 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Sat, 16 May 2026 00:10:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 	; 	rm rootless.tgz; 		rootlesskit --version # buildkit
# Sat, 16 May 2026 00:10:18 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Sat, 16 May 2026 00:10:18 GMT
VOLUME [/home/rootless/.local/share/docker]
# Sat, 16 May 2026 00:10:18 GMT
USER rootless
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2240a8f6be9241c8313b7887a9f6b272758fa6f323a29ae88da91f004c59d0d6`  
		Last Modified: Fri, 15 May 2026 22:12:26 GMT  
		Size: 8.3 MB (8311611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee8f29570b73bc6fb95364db2374f726e9b921827f4d1383a6d310769c050e2`  
		Last Modified: Fri, 15 May 2026 22:12:26 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb157a4a9b724e516e2a50f94be797a8145642f3c45f0f8d7bc236aa4848960`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 19.5 MB (19549502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f6e87dc813cb0ce7fd8d1277ed2d283a03d11b6492284e50fc16c959ccf8cb1`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 23.0 MB (22988578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4642ba5a86eb9921fd340045e353c9b3723a87f535731ae12659016c86bd3a48`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 11.2 MB (11243758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53d662cd1653019365b80d59af307d893de60a95d5d03aa7faddf0654b0162a7`  
		Last Modified: Fri, 15 May 2026 22:12:28 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45636b869c7065c939fb09da20708b05eb4bffe960ae3cb0102e1101147bf702`  
		Last Modified: Fri, 15 May 2026 22:12:28 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9074eaed06bf00c4914e361b510e55cd12bb8b0305b732d777ef95e01914b4f4`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f0de530d70a206bbf99372d4e80b56da6aa52a05b01bd6390d3bb3f4317466`  
		Last Modified: Fri, 15 May 2026 22:46:06 GMT  
		Size: 6.9 MB (6941385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc4ad90df2e9375f24da713fdbd03d16ffd44bcab544ed61a9d388fcc342e85`  
		Last Modified: Fri, 15 May 2026 22:46:06 GMT  
		Size: 92.2 KB (92210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f7d81cca6c2e02237a63044b96fc4e4432bffd61e595b15c8c2d952370deeed`  
		Last Modified: Fri, 15 May 2026 22:46:06 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb7196e21df03c1f04999bead8f104980dd964263cd7b78f05f013ad70dc5e2`  
		Last Modified: Fri, 15 May 2026 22:46:08 GMT  
		Size: 68.7 MB (68656308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403fc89c99ec573758e84c2e171afabefeec367c0c3ac712710c2c280fac6f51`  
		Last Modified: Fri, 15 May 2026 22:46:07 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6ba97049938b6a09c6a9ac2e32cd77fd36080fff06433e8e5f31af12220583`  
		Last Modified: Fri, 15 May 2026 22:46:07 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3aecd32c9a7b429826161d546e29c1dff0ac6eea914337b0b9d0a168b785fe5`  
		Last Modified: Sat, 16 May 2026 00:10:24 GMT  
		Size: 3.4 MB (3420116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75a1fd367a70907870ec61c5541633c1016315039aa85446173764ece77df84`  
		Last Modified: Sat, 16 May 2026 00:10:23 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896453e7017b28888cd072db72945d8e744a934faf06c8d0afe071918a3ab492`  
		Last Modified: Sat, 16 May 2026 00:10:23 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8de78d541dc09dba7c55cf30b416cc37bf4cadc540afd919f470b8c6ea68c5`  
		Last Modified: Sat, 16 May 2026 00:10:24 GMT  
		Size: 12.1 MB (12102497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307ee9ce5b3abe899d1554ebbfe999955a855268f925239ee277ff0542c7424f`  
		Last Modified: Sat, 16 May 2026 00:10:25 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.5-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:a928bb65ab1afe6b79776cfe5fec97b7de2ce78299935d0f2a6d93a022bbf33d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10081df2ff0f054ec55a6ba8b0e73f3f8660a710ebcd84146466c7e415b001f2`

```dockerfile
```

-	Layers:
	-	`sha256:ef654a1e85deabbd5d572b1aa6d9feaba8a368d7af558b844574a48c0af89e2c`  
		Last Modified: Sat, 16 May 2026 00:10:23 GMT  
		Size: 30.5 KB (30492 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.5-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:beddbc20555efb8bc7641a98e7a58a5104329118a81b075bd2373de0e1dca5c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.7 MB (145721108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7cb4b74b39f9eb3c077215fb0f4c6f7d8395bd86b29015b4743c1a5b13d2f24`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Fri, 15 May 2026 22:12:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 15 May 2026 22:12:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 15 May 2026 22:12:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 15 May 2026 22:12:17 GMT
ENV DOCKER_VERSION=29.5.0
# Fri, 15 May 2026 22:12:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 15 May 2026 22:12:17 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Fri, 15 May 2026 22:12:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-amd64'; 			sha256='0144479d5a1cd710be3464ae898628cfa68033e16b225aef52f81930c45ac9b5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v6'; 			sha256='1f34337385921c5da43d63452282726b062aa887fda975f96dd3d6e869648bc6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v7'; 			sha256='3560b5b6fd3485f4d0bd160e7edf56cc1f08f0cb5852c9af28bf3fab9973c7c2'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm64'; 			sha256='565605fe0bb393ed5d11771e5b52fc7ef05c701868861fa85609747c9d74a440'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-ppc64le'; 			sha256='c5ef8012f48a518e1c235ad408d26cd424d7b5fa87eaf78cb2ff4b9048730120'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-riscv64'; 			sha256='80b27d5f3a346591a5045b81217ee5be578ed151ef8cbd883a892c0ec0ac33f1'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-s390x'; 			sha256='04f5bd0d389f682c7e9287a3b3a1777b0848f8e10d58cbf9d4d12c9002bbb378'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 15 May 2026 22:12:18 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Fri, 15 May 2026 22:12:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 15 May 2026 22:12:19 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 15 May 2026 22:12:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 22:12:19 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 15 May 2026 22:12:19 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 15 May 2026 22:12:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2026 22:12:19 GMT
CMD ["sh"]
# Fri, 15 May 2026 22:46:13 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 15 May 2026 22:46:14 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 15 May 2026 22:46:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 15 May 2026 22:46:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 15 May 2026 22:46:17 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 15 May 2026 22:46:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 15 May 2026 22:46:17 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 22:46:17 GMT
VOLUME [/var/lib/docker]
# Fri, 15 May 2026 22:46:17 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 15 May 2026 22:46:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 15 May 2026 22:46:17 GMT
CMD []
# Sat, 16 May 2026 00:10:04 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Sat, 16 May 2026 00:10:04 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Sat, 16 May 2026 00:10:04 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Sat, 16 May 2026 00:10:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 	; 	rm rootless.tgz; 		rootlesskit --version # buildkit
# Sat, 16 May 2026 00:10:05 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Sat, 16 May 2026 00:10:05 GMT
VOLUME [/home/rootless/.local/share/docker]
# Sat, 16 May 2026 00:10:05 GMT
USER rootless
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd51147f6d8210f56d90e095c69db7468c6a7f4c96b15954bec62a38d029c230`  
		Last Modified: Fri, 15 May 2026 22:12:26 GMT  
		Size: 8.4 MB (8368382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca485120792b1bdb82820fd08df20937c87c36c02b044d113785a278f04c9c5e`  
		Last Modified: Fri, 15 May 2026 22:12:25 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76be2953b1820f6b03454f4cc64611d855fbccf3feb3c9d49c80e129eddcad5`  
		Last Modified: Fri, 15 May 2026 22:12:26 GMT  
		Size: 18.0 MB (18003835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc8387c97690c1e6db50aa3de5c90f1742500af7c360287ddfe4acd0578e0eb`  
		Last Modified: Fri, 15 May 2026 22:12:26 GMT  
		Size: 20.8 MB (20815340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3087ee8252be9dcbda43072f57a958f8f37983b3932bdca55c49fc7420da93f`  
		Last Modified: Fri, 15 May 2026 22:12:26 GMT  
		Size: 10.2 MB (10243274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027710042ccab2488d5291cd625bb62305844954e320f530f618c56b53ef928c`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0557313fec61d76b6a60306c806eb278032cfc80335daa86db37ad9979e81756`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9074eaed06bf00c4914e361b510e55cd12bb8b0305b732d777ef95e01914b4f4`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43b2d205b3daf8cb2c6ef3c0e0999b4106fc7a6595ba5568e8605a7e7b0722d8`  
		Last Modified: Fri, 15 May 2026 22:46:26 GMT  
		Size: 7.2 MB (7219897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0304531f0ed7ae27db4e86f747d65dfef2567fd5f396a4b3922c5ff5780d1f2`  
		Last Modified: Fri, 15 May 2026 22:46:26 GMT  
		Size: 100.9 KB (100934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95e602dc9bf9e82e229534494ecc27788dfc15984a25ad6683a47603dfb112ff`  
		Last Modified: Fri, 15 May 2026 22:46:26 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb752877659a29a329ac376438ffc77fd5832ef8ec7713badc224dc70797bd6`  
		Last Modified: Fri, 15 May 2026 22:46:29 GMT  
		Size: 62.1 MB (62129016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1ca5de4993dc83a36fb35a72b4fedf78533c646f254850669127c3e34a022a`  
		Last Modified: Fri, 15 May 2026 22:46:27 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27981b508a5db9a4e2a2c0b87eb0017d532fc5cc5bd11529ba120cd1e843ae91`  
		Last Modified: Fri, 15 May 2026 22:46:28 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1a7270b72b7f3e2799e7c141f64461907402307eab0e5a25271d1e2b47c44ee`  
		Last Modified: Sat, 16 May 2026 00:10:10 GMT  
		Size: 3.4 MB (3394559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5f6bb10aafb4e20e513a5cc5d9a7e3481a971f0433332b50708cd61bc4df70`  
		Last Modified: Sat, 16 May 2026 00:10:10 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c4e8ff9e0e4eab7d4814e9d39e6a4c25f79d76d2979f00a78de155911ef2ddd`  
		Last Modified: Sat, 16 May 2026 00:10:10 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91aab9887dd46e6f833ba3ffff294c32d59299ab8d4a3847194a60a227c55b0`  
		Last Modified: Sat, 16 May 2026 00:10:10 GMT  
		Size: 11.2 MB (11236505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3459fdc6872a7acd1e3b7884a28a60561f9e3488cf19f8437a3b11c8e09a6d8`  
		Last Modified: Sat, 16 May 2026 00:10:11 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.5-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:58ffdbbba10f97b2d1ef33dbfbdf016c2844506424a34f22333f5597310a7fab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 KB (30663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a11fccc6bc4fd79d54dca7d1d3ed318788c65b63d3184fbb73c400cadceb60f`

```dockerfile
```

-	Layers:
	-	`sha256:fc110ccff973a2ba6b5d21f0f1f25d79b12b82a863abcabd81b546d627bb598c`  
		Last Modified: Sat, 16 May 2026 00:10:09 GMT  
		Size: 30.7 KB (30663 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.5-windowsservercore`

```console
$ docker pull docker@sha256:3268bde2385bb80b1e442f6c04799dd7619f785c63be6c4dccb6831a144f3043
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32860; amd64
	-	windows version 10.0.20348.5139; amd64

### `docker:29.5-windowsservercore` - windows version 10.0.26100.32860; amd64

```console
$ docker pull docker@sha256:e4420a2945552c16d362b8472d0182a0ec134ce320f2233ec15e93015e599e8f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2262478653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90d0a0d1bad4f84f1fbcaf6c1e419ce3a0952a03ed6d4582f9767303292ca6c6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 10 May 2026 10:08:54 GMT
RUN Install update 10.0.26100.32860
# Fri, 15 May 2026 22:15:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 15 May 2026 22:16:21 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 15 May 2026 22:16:22 GMT
ENV DOCKER_VERSION=29.5.0
# Fri, 15 May 2026 22:16:23 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.5.0.zip
# Fri, 15 May 2026 22:16:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 15 May 2026 22:16:39 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Fri, 15 May 2026 22:16:40 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.windows-amd64.exe
# Fri, 15 May 2026 22:16:40 GMT
ENV DOCKER_BUILDX_SHA256=96a10e259fa1380e7bbf9a3cb04872f201a6e7e331ddeeec8d3e38aa2650ddc5
# Fri, 15 May 2026 22:16:50 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 15 May 2026 22:16:51 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Fri, 15 May 2026 22:16:51 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-windows-x86_64.exe
# Fri, 15 May 2026 22:16:52 GMT
ENV DOCKER_COMPOSE_SHA256=5e6d72612b3165be9fea4ae889435fec76979a9779b6f62f4efee99dd5f41ea1
# Fri, 15 May 2026 22:17:01 GMT
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
	-	`sha256:74b535a51fd23dbc5005aa72b61e95ad333b54b6b5276fd600c8f26dc1ec6379`  
		Last Modified: Fri, 15 May 2026 22:17:10 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f1111f6cb7254129e7ea39ba28883376409a104ffda0b87a45a420ceee27fcb`  
		Last Modified: Fri, 15 May 2026 22:17:10 GMT  
		Size: 392.8 KB (392802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2db17ecf93e3efdbccd835fd5d408afb7a3351f7597a48a1ad636c01794ebe04`  
		Last Modified: Fri, 15 May 2026 22:17:09 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c83f256bcd38582b57bb91e485a2d85240d5f2ae45b27c9afa7a9a5f44ebed73`  
		Last Modified: Fri, 15 May 2026 22:17:09 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cdc10f672c38740ac0512c480a10fe4b0dc1658659e00513da102771c2e3e40`  
		Last Modified: Fri, 15 May 2026 22:17:11 GMT  
		Size: 20.3 MB (20260443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e77a9dc340d0bdbccbce6b57c4d89cad2a1db92d89f7c2649002da080b5334bd`  
		Last Modified: Fri, 15 May 2026 22:17:07 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2309766ee1a21f57c947e3ef48cf4592eb1c12fb99926f92dc710c73dff7b930`  
		Last Modified: Fri, 15 May 2026 22:17:07 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9e8a3c0bbacac0c1695cff5c5e5eeefe513850e0a04322d018dfc23f9317a07`  
		Last Modified: Fri, 15 May 2026 22:17:07 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2562224ef98ba779eb91088241d392cb2a71abbc685b008022439f669f7686d6`  
		Last Modified: Fri, 15 May 2026 22:17:09 GMT  
		Size: 23.9 MB (23920245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6af350faa47b96f1766ca0debecbe39139716c8b55ae988b2528535eed60cca`  
		Last Modified: Fri, 15 May 2026 22:17:05 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:780002467e4bb1a15f8748b2ea889bc85483b2d7ddb96b528e3b32c982692e19`  
		Last Modified: Fri, 15 May 2026 22:17:05 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47e3ee62773736f785dc51e4bc1a7e48595fe0afed17ab1d89154d1e06595d11`  
		Last Modified: Fri, 15 May 2026 22:17:05 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d076a230450a0b438ed3c7d1ee23904031d66dddd7e9ee8ac765637eb942ff8`  
		Last Modified: Fri, 15 May 2026 22:17:07 GMT  
		Size: 12.0 MB (11951730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:29.5-windowsservercore` - windows version 10.0.20348.5139; amd64

```console
$ docker pull docker@sha256:08c5da38b0e30b8a83bf89e16eff7a1292d6948010a051f9310d6e9511e6423f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2178998545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c8a2de39d58f5e39341f81d00642352c6b050887b387821ad49ffd590b688ad`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Fri, 15 May 2026 22:15:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 15 May 2026 22:16:42 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 15 May 2026 22:16:43 GMT
ENV DOCKER_VERSION=29.5.0
# Fri, 15 May 2026 22:16:43 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.5.0.zip
# Fri, 15 May 2026 22:16:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 15 May 2026 22:16:57 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Fri, 15 May 2026 22:16:57 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.windows-amd64.exe
# Fri, 15 May 2026 22:16:58 GMT
ENV DOCKER_BUILDX_SHA256=96a10e259fa1380e7bbf9a3cb04872f201a6e7e331ddeeec8d3e38aa2650ddc5
# Fri, 15 May 2026 22:17:07 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 15 May 2026 22:17:08 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Fri, 15 May 2026 22:17:08 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-windows-x86_64.exe
# Fri, 15 May 2026 22:17:09 GMT
ENV DOCKER_COMPOSE_SHA256=5e6d72612b3165be9fea4ae889435fec76979a9779b6f62f4efee99dd5f41ea1
# Fri, 15 May 2026 22:17:16 GMT
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
	-	`sha256:5961f3afdef68ce25fa592066416467d81416df4b1af2537087f1c9150afb728`  
		Last Modified: Fri, 15 May 2026 22:17:25 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae47499b6a77bf67c8fc4c6163dd490f816d5ea9168dfad57664888a82963cd`  
		Last Modified: Fri, 15 May 2026 22:17:25 GMT  
		Size: 506.6 KB (506623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1a50c6ae3a4766042c073c45ffd8a1c5d67595c9c560f65c76492d18a12fd50`  
		Last Modified: Fri, 15 May 2026 22:17:24 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:756530867ead10020116e1f2f106664f6fed6cae2160122fc6ec372b43fd678b`  
		Last Modified: Fri, 15 May 2026 22:17:24 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203d6d943b8fa9b8934a5ce05bf2893265e234366a62bf9ea3a09f77d5608167`  
		Last Modified: Fri, 15 May 2026 22:17:26 GMT  
		Size: 20.2 MB (20232134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f38228e51f50d7a28325477b370bd57476f2a6883a023e98c0d628bc22295ad4`  
		Last Modified: Fri, 15 May 2026 22:17:22 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f7fe5a6a8d2169e19d30f03057f1cf4e3dfa71a14a9e3e2572a95d5246c205`  
		Last Modified: Fri, 15 May 2026 22:17:22 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa5b9407c6ba09fc25979a724f032914bee3ded478b4366b26a09de96ef0c80`  
		Last Modified: Fri, 15 May 2026 22:17:22 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60bb62b675b679633b1a24e24b203fa8ed15d941f3bbb283bae34df7d68c50af`  
		Last Modified: Fri, 15 May 2026 22:17:24 GMT  
		Size: 23.9 MB (23901135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8874726604cb50cc54f506879180a624b7e0fc0e3ad5a8a7063d89505fd60ea`  
		Last Modified: Fri, 15 May 2026 22:17:20 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c7b4c5d7c92d0e67fbdf7582c6455934c8b5f3b3a8c849173931adad0837ca3`  
		Last Modified: Fri, 15 May 2026 22:17:20 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efe6f324d4756f3cd5de0642c06bbc7c60c070aa7a512c8682d7e2232291ae8b`  
		Last Modified: Fri, 15 May 2026 22:17:20 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:487382c6166366ea2b9acbadbf146f8443b6a756bfb7678718eb9c7383bc4a2c`  
		Last Modified: Fri, 15 May 2026 22:17:22 GMT  
		Size: 11.9 MB (11926255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.5-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:1c7ad5b5ef3c89a3bdc56e2574cbfe03b7327d744f4266d72447109f574789c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `docker:29.5-windowsservercore-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull docker@sha256:08c5da38b0e30b8a83bf89e16eff7a1292d6948010a051f9310d6e9511e6423f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2178998545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c8a2de39d58f5e39341f81d00642352c6b050887b387821ad49ffd590b688ad`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Fri, 15 May 2026 22:15:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 15 May 2026 22:16:42 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 15 May 2026 22:16:43 GMT
ENV DOCKER_VERSION=29.5.0
# Fri, 15 May 2026 22:16:43 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.5.0.zip
# Fri, 15 May 2026 22:16:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 15 May 2026 22:16:57 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Fri, 15 May 2026 22:16:57 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.windows-amd64.exe
# Fri, 15 May 2026 22:16:58 GMT
ENV DOCKER_BUILDX_SHA256=96a10e259fa1380e7bbf9a3cb04872f201a6e7e331ddeeec8d3e38aa2650ddc5
# Fri, 15 May 2026 22:17:07 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 15 May 2026 22:17:08 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Fri, 15 May 2026 22:17:08 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-windows-x86_64.exe
# Fri, 15 May 2026 22:17:09 GMT
ENV DOCKER_COMPOSE_SHA256=5e6d72612b3165be9fea4ae889435fec76979a9779b6f62f4efee99dd5f41ea1
# Fri, 15 May 2026 22:17:16 GMT
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
	-	`sha256:5961f3afdef68ce25fa592066416467d81416df4b1af2537087f1c9150afb728`  
		Last Modified: Fri, 15 May 2026 22:17:25 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae47499b6a77bf67c8fc4c6163dd490f816d5ea9168dfad57664888a82963cd`  
		Last Modified: Fri, 15 May 2026 22:17:25 GMT  
		Size: 506.6 KB (506623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1a50c6ae3a4766042c073c45ffd8a1c5d67595c9c560f65c76492d18a12fd50`  
		Last Modified: Fri, 15 May 2026 22:17:24 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:756530867ead10020116e1f2f106664f6fed6cae2160122fc6ec372b43fd678b`  
		Last Modified: Fri, 15 May 2026 22:17:24 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203d6d943b8fa9b8934a5ce05bf2893265e234366a62bf9ea3a09f77d5608167`  
		Last Modified: Fri, 15 May 2026 22:17:26 GMT  
		Size: 20.2 MB (20232134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f38228e51f50d7a28325477b370bd57476f2a6883a023e98c0d628bc22295ad4`  
		Last Modified: Fri, 15 May 2026 22:17:22 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f7fe5a6a8d2169e19d30f03057f1cf4e3dfa71a14a9e3e2572a95d5246c205`  
		Last Modified: Fri, 15 May 2026 22:17:22 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa5b9407c6ba09fc25979a724f032914bee3ded478b4366b26a09de96ef0c80`  
		Last Modified: Fri, 15 May 2026 22:17:22 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60bb62b675b679633b1a24e24b203fa8ed15d941f3bbb283bae34df7d68c50af`  
		Last Modified: Fri, 15 May 2026 22:17:24 GMT  
		Size: 23.9 MB (23901135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8874726604cb50cc54f506879180a624b7e0fc0e3ad5a8a7063d89505fd60ea`  
		Last Modified: Fri, 15 May 2026 22:17:20 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c7b4c5d7c92d0e67fbdf7582c6455934c8b5f3b3a8c849173931adad0837ca3`  
		Last Modified: Fri, 15 May 2026 22:17:20 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efe6f324d4756f3cd5de0642c06bbc7c60c070aa7a512c8682d7e2232291ae8b`  
		Last Modified: Fri, 15 May 2026 22:17:20 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:487382c6166366ea2b9acbadbf146f8443b6a756bfb7678718eb9c7383bc4a2c`  
		Last Modified: Fri, 15 May 2026 22:17:22 GMT  
		Size: 11.9 MB (11926255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.5-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:d385e3828e8366b07bd0af1a4b025c4feb365a506fedb8e307acaae417e63f72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32860; amd64

### `docker:29.5-windowsservercore-ltsc2025` - windows version 10.0.26100.32860; amd64

```console
$ docker pull docker@sha256:e4420a2945552c16d362b8472d0182a0ec134ce320f2233ec15e93015e599e8f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2262478653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90d0a0d1bad4f84f1fbcaf6c1e419ce3a0952a03ed6d4582f9767303292ca6c6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 10 May 2026 10:08:54 GMT
RUN Install update 10.0.26100.32860
# Fri, 15 May 2026 22:15:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 15 May 2026 22:16:21 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 15 May 2026 22:16:22 GMT
ENV DOCKER_VERSION=29.5.0
# Fri, 15 May 2026 22:16:23 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.5.0.zip
# Fri, 15 May 2026 22:16:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 15 May 2026 22:16:39 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Fri, 15 May 2026 22:16:40 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.windows-amd64.exe
# Fri, 15 May 2026 22:16:40 GMT
ENV DOCKER_BUILDX_SHA256=96a10e259fa1380e7bbf9a3cb04872f201a6e7e331ddeeec8d3e38aa2650ddc5
# Fri, 15 May 2026 22:16:50 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 15 May 2026 22:16:51 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Fri, 15 May 2026 22:16:51 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-windows-x86_64.exe
# Fri, 15 May 2026 22:16:52 GMT
ENV DOCKER_COMPOSE_SHA256=5e6d72612b3165be9fea4ae889435fec76979a9779b6f62f4efee99dd5f41ea1
# Fri, 15 May 2026 22:17:01 GMT
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
	-	`sha256:74b535a51fd23dbc5005aa72b61e95ad333b54b6b5276fd600c8f26dc1ec6379`  
		Last Modified: Fri, 15 May 2026 22:17:10 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f1111f6cb7254129e7ea39ba28883376409a104ffda0b87a45a420ceee27fcb`  
		Last Modified: Fri, 15 May 2026 22:17:10 GMT  
		Size: 392.8 KB (392802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2db17ecf93e3efdbccd835fd5d408afb7a3351f7597a48a1ad636c01794ebe04`  
		Last Modified: Fri, 15 May 2026 22:17:09 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c83f256bcd38582b57bb91e485a2d85240d5f2ae45b27c9afa7a9a5f44ebed73`  
		Last Modified: Fri, 15 May 2026 22:17:09 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cdc10f672c38740ac0512c480a10fe4b0dc1658659e00513da102771c2e3e40`  
		Last Modified: Fri, 15 May 2026 22:17:11 GMT  
		Size: 20.3 MB (20260443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e77a9dc340d0bdbccbce6b57c4d89cad2a1db92d89f7c2649002da080b5334bd`  
		Last Modified: Fri, 15 May 2026 22:17:07 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2309766ee1a21f57c947e3ef48cf4592eb1c12fb99926f92dc710c73dff7b930`  
		Last Modified: Fri, 15 May 2026 22:17:07 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9e8a3c0bbacac0c1695cff5c5e5eeefe513850e0a04322d018dfc23f9317a07`  
		Last Modified: Fri, 15 May 2026 22:17:07 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2562224ef98ba779eb91088241d392cb2a71abbc685b008022439f669f7686d6`  
		Last Modified: Fri, 15 May 2026 22:17:09 GMT  
		Size: 23.9 MB (23920245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6af350faa47b96f1766ca0debecbe39139716c8b55ae988b2528535eed60cca`  
		Last Modified: Fri, 15 May 2026 22:17:05 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:780002467e4bb1a15f8748b2ea889bc85483b2d7ddb96b528e3b32c982692e19`  
		Last Modified: Fri, 15 May 2026 22:17:05 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47e3ee62773736f785dc51e4bc1a7e48595fe0afed17ab1d89154d1e06595d11`  
		Last Modified: Fri, 15 May 2026 22:17:05 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d076a230450a0b438ed3c7d1ee23904031d66dddd7e9ee8ac765637eb942ff8`  
		Last Modified: Fri, 15 May 2026 22:17:07 GMT  
		Size: 12.0 MB (11951730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.5.1`

```console
$ docker pull docker@sha256:5d0f434af43d0c804c0d67f663bfc07f762eceecf3df6f774b9f4570a65c2f8b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm variant v6
	-	unknown; unknown

### `docker:29.5.1` - linux; arm variant v6

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

### `docker:29.5.1` - unknown; unknown

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

## `docker:29.5.1-alpine3.23`

```console
$ docker pull docker@sha256:5d0f434af43d0c804c0d67f663bfc07f762eceecf3df6f774b9f4570a65c2f8b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm variant v6
	-	unknown; unknown

### `docker:29.5.1-alpine3.23` - linux; arm variant v6

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

### `docker:29.5.1-alpine3.23` - unknown; unknown

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

## `docker:29.5.1-cli`

```console
$ docker pull docker@sha256:2d75c2033986586a89e1a49b99c665066ee5744b54038d2445c1509b48924d89
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown

### `docker:29.5.1-cli` - linux; amd64

```console
$ docker pull docker@sha256:93afea9ac780f8706540408cba1e801ba285071476b0c2bff424a0ca0037869c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.0 MB (65959799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54560465c89852384428d8b003c70278f2a11fdee74fde28173fea1077416da9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:29.5.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:e6e636232d7064d32da9c46ef93c11a565c43d61068daa1785a2d63bb664c190
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:973ee0a24a2536030656c4b9be0b463122f73df6150f6b0949b3d3601798afd1`

```dockerfile
```

-	Layers:
	-	`sha256:dbed7195f208034adcef893e2efc57ce071c5d914a8a9624d5a8a7fbb1a9f99e`  
		Last Modified: Tue, 19 May 2026 18:44:01 GMT  
		Size: 38.1 KB (38056 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.5.1-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:663439730373cf7597a3f83ae50ab11f8a171b59b1e9ce95a730be4c0b42eb22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62234030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f0de2aee792b8ce4ffb303432b131ae0026fdd58af954221ecf5bcb4f293705`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:29.5.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:866404ab9edde4226ee79d91959d86956cc3fe71a933e10c9c282f3bb9fe1e24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1f84764e1609e718085281484003ba89b5bd9d8cbb6984808cae3079115e48a`

```dockerfile
```

-	Layers:
	-	`sha256:60a6451bb1e2eecccb01163a32454bf66adbc39c153e56f1b682485c3f73fbc4`  
		Last Modified: Tue, 19 May 2026 18:46:40 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.5.1-cli-alpine3.23`

```console
$ docker pull docker@sha256:2d75c2033986586a89e1a49b99c665066ee5744b54038d2445c1509b48924d89
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown

### `docker:29.5.1-cli-alpine3.23` - linux; amd64

```console
$ docker pull docker@sha256:93afea9ac780f8706540408cba1e801ba285071476b0c2bff424a0ca0037869c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.0 MB (65959799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54560465c89852384428d8b003c70278f2a11fdee74fde28173fea1077416da9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:29.5.1-cli-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:e6e636232d7064d32da9c46ef93c11a565c43d61068daa1785a2d63bb664c190
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:973ee0a24a2536030656c4b9be0b463122f73df6150f6b0949b3d3601798afd1`

```dockerfile
```

-	Layers:
	-	`sha256:dbed7195f208034adcef893e2efc57ce071c5d914a8a9624d5a8a7fbb1a9f99e`  
		Last Modified: Tue, 19 May 2026 18:44:01 GMT  
		Size: 38.1 KB (38056 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.5.1-cli-alpine3.23` - linux; arm variant v6

```console
$ docker pull docker@sha256:663439730373cf7597a3f83ae50ab11f8a171b59b1e9ce95a730be4c0b42eb22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62234030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f0de2aee792b8ce4ffb303432b131ae0026fdd58af954221ecf5bcb4f293705`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:29.5.1-cli-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:866404ab9edde4226ee79d91959d86956cc3fe71a933e10c9c282f3bb9fe1e24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1f84764e1609e718085281484003ba89b5bd9d8cbb6984808cae3079115e48a`

```dockerfile
```

-	Layers:
	-	`sha256:60a6451bb1e2eecccb01163a32454bf66adbc39c153e56f1b682485c3f73fbc4`  
		Last Modified: Tue, 19 May 2026 18:46:40 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.5.1-dind`

```console
$ docker pull docker@sha256:5d0f434af43d0c804c0d67f663bfc07f762eceecf3df6f774b9f4570a65c2f8b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm variant v6
	-	unknown; unknown

### `docker:29.5.1-dind` - linux; arm variant v6

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

### `docker:29.5.1-dind` - unknown; unknown

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

## `docker:29.5.1-dind-alpine3.23`

```console
$ docker pull docker@sha256:5d0f434af43d0c804c0d67f663bfc07f762eceecf3df6f774b9f4570a65c2f8b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm variant v6
	-	unknown; unknown

### `docker:29.5.1-dind-alpine3.23` - linux; arm variant v6

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

### `docker:29.5.1-dind-alpine3.23` - unknown; unknown

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

## `docker:29.5.1-dind-rootless`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:29.5.1-windowsservercore`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:29.5.1-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:29.5.1-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:cli`

```console
$ docker pull docker@sha256:22eb9db6081c0bc3c05137a5e8f26720e1b09aaafd3f18b923b494bcd6283a3a
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
$ docker pull docker@sha256:93afea9ac780f8706540408cba1e801ba285071476b0c2bff424a0ca0037869c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.0 MB (65959799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54560465c89852384428d8b003c70278f2a11fdee74fde28173fea1077416da9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:e6e636232d7064d32da9c46ef93c11a565c43d61068daa1785a2d63bb664c190
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:973ee0a24a2536030656c4b9be0b463122f73df6150f6b0949b3d3601798afd1`

```dockerfile
```

-	Layers:
	-	`sha256:dbed7195f208034adcef893e2efc57ce071c5d914a8a9624d5a8a7fbb1a9f99e`  
		Last Modified: Tue, 19 May 2026 18:44:01 GMT  
		Size: 38.1 KB (38056 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:663439730373cf7597a3f83ae50ab11f8a171b59b1e9ce95a730be4c0b42eb22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62234030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f0de2aee792b8ce4ffb303432b131ae0026fdd58af954221ecf5bcb4f293705`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:866404ab9edde4226ee79d91959d86956cc3fe71a933e10c9c282f3bb9fe1e24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1f84764e1609e718085281484003ba89b5bd9d8cbb6984808cae3079115e48a`

```dockerfile
```

-	Layers:
	-	`sha256:60a6451bb1e2eecccb01163a32454bf66adbc39c153e56f1b682485c3f73fbc4`  
		Last Modified: Tue, 19 May 2026 18:46:40 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:9ec11722eadaf4ecb19592ea19d512fc17ef941738677435dc52f1f70e3b4da2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61215589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:376a20891ab4edb0bcada5d8b3ba3f89f105c6351ce5368f2cafee22c9c2e764`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Fri, 15 May 2026 22:11:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 15 May 2026 22:11:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 15 May 2026 22:12:00 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 15 May 2026 22:12:04 GMT
ENV DOCKER_VERSION=29.5.0
# Fri, 15 May 2026 22:12:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 15 May 2026 22:12:04 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Fri, 15 May 2026 22:12:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-amd64'; 			sha256='0144479d5a1cd710be3464ae898628cfa68033e16b225aef52f81930c45ac9b5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v6'; 			sha256='1f34337385921c5da43d63452282726b062aa887fda975f96dd3d6e869648bc6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v7'; 			sha256='3560b5b6fd3485f4d0bd160e7edf56cc1f08f0cb5852c9af28bf3fab9973c7c2'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm64'; 			sha256='565605fe0bb393ed5d11771e5b52fc7ef05c701868861fa85609747c9d74a440'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-ppc64le'; 			sha256='c5ef8012f48a518e1c235ad408d26cd424d7b5fa87eaf78cb2ff4b9048730120'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-riscv64'; 			sha256='80b27d5f3a346591a5045b81217ee5be578ed151ef8cbd883a892c0ec0ac33f1'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-s390x'; 			sha256='04f5bd0d389f682c7e9287a3b3a1777b0848f8e10d58cbf9d4d12c9002bbb378'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 15 May 2026 22:12:07 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Fri, 15 May 2026 22:12:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 15 May 2026 22:12:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 15 May 2026 22:12:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 22:12:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 15 May 2026 22:12:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 15 May 2026 22:12:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2026 22:12:10 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb53acd779ed72fcbca92822c9c8dca72fc19b59b4367fc8edbe5c8edd184829`  
		Last Modified: Fri, 15 May 2026 22:12:16 GMT  
		Size: 7.5 MB (7520515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3717dbbea465f22997cb871db7b421cb78bfc5d2353e0fbb9c24a4d7f4eead8b`  
		Last Modified: Fri, 15 May 2026 22:12:16 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2765ebda46cc899cbdd1066e7e900d81e9e6227536c38218d156a6c6ffc93324`  
		Last Modified: Fri, 15 May 2026 22:12:17 GMT  
		Size: 18.2 MB (18172266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8e62c2751306352d388df5f6ed3f91e4f160f2da7a249168dc387777896b44`  
		Last Modified: Fri, 15 May 2026 22:12:17 GMT  
		Size: 21.6 MB (21600397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e74677ed12033b201cddf684740d6f5f9540e22ab253c874ab4d21644f5b592`  
		Last Modified: Fri, 15 May 2026 22:12:17 GMT  
		Size: 10.6 MB (10637133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d76fc015f6b878f4335aa2e01b8ef18fcc9e9b2cb962b48d46350deb994e02d`  
		Last Modified: Fri, 15 May 2026 22:12:17 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad7ca5f5e6e176e7d1835e181fe35affc2155c45a6a1148aa7f18ea76d9d05e`  
		Last Modified: Fri, 15 May 2026 22:12:18 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdab469dc84864d9800ae053f9d87586d2515da2b650cf6f13f5ee84e15b2276`  
		Last Modified: Fri, 15 May 2026 22:12:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:3733f58f759836ce9f96949b34cf083d5873acad577a5181e080afb4bf3249f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14f8c9cf97e3e4d9ec70c8edcea1d71eca3c988ea012b28acc4d35eea629ae37`

```dockerfile
```

-	Layers:
	-	`sha256:7ce1554139b841ff42f6ca82b422a07755ca34b9f40a43a8f69db42b7b360f47`  
		Last Modified: Fri, 15 May 2026 22:12:16 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e211ecf9a3c37d57418eef652252ba0ca62fc942cdfa0d8dec160bc3086bd9c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61632856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee4f6ad10554b836d3f6dad4bf015212f96fc505f746c44c549df3e29d3fd2a2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Fri, 15 May 2026 22:12:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 15 May 2026 22:12:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 15 May 2026 22:12:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 15 May 2026 22:12:17 GMT
ENV DOCKER_VERSION=29.5.0
# Fri, 15 May 2026 22:12:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 15 May 2026 22:12:17 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Fri, 15 May 2026 22:12:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-amd64'; 			sha256='0144479d5a1cd710be3464ae898628cfa68033e16b225aef52f81930c45ac9b5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v6'; 			sha256='1f34337385921c5da43d63452282726b062aa887fda975f96dd3d6e869648bc6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v7'; 			sha256='3560b5b6fd3485f4d0bd160e7edf56cc1f08f0cb5852c9af28bf3fab9973c7c2'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm64'; 			sha256='565605fe0bb393ed5d11771e5b52fc7ef05c701868861fa85609747c9d74a440'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-ppc64le'; 			sha256='c5ef8012f48a518e1c235ad408d26cd424d7b5fa87eaf78cb2ff4b9048730120'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-riscv64'; 			sha256='80b27d5f3a346591a5045b81217ee5be578ed151ef8cbd883a892c0ec0ac33f1'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-s390x'; 			sha256='04f5bd0d389f682c7e9287a3b3a1777b0848f8e10d58cbf9d4d12c9002bbb378'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 15 May 2026 22:12:18 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Fri, 15 May 2026 22:12:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 15 May 2026 22:12:19 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 15 May 2026 22:12:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 22:12:19 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 15 May 2026 22:12:19 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 15 May 2026 22:12:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2026 22:12:19 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd51147f6d8210f56d90e095c69db7468c6a7f4c96b15954bec62a38d029c230`  
		Last Modified: Fri, 15 May 2026 22:12:26 GMT  
		Size: 8.4 MB (8368382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca485120792b1bdb82820fd08df20937c87c36c02b044d113785a278f04c9c5e`  
		Last Modified: Fri, 15 May 2026 22:12:25 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76be2953b1820f6b03454f4cc64611d855fbccf3feb3c9d49c80e129eddcad5`  
		Last Modified: Fri, 15 May 2026 22:12:26 GMT  
		Size: 18.0 MB (18003835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc8387c97690c1e6db50aa3de5c90f1742500af7c360287ddfe4acd0578e0eb`  
		Last Modified: Fri, 15 May 2026 22:12:26 GMT  
		Size: 20.8 MB (20815340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3087ee8252be9dcbda43072f57a958f8f37983b3932bdca55c49fc7420da93f`  
		Last Modified: Fri, 15 May 2026 22:12:26 GMT  
		Size: 10.2 MB (10243274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027710042ccab2488d5291cd625bb62305844954e320f530f618c56b53ef928c`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0557313fec61d76b6a60306c806eb278032cfc80335daa86db37ad9979e81756`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9074eaed06bf00c4914e361b510e55cd12bb8b0305b732d777ef95e01914b4f4`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:06da91c70ff029cd54c906f93a84997c38caa126b495b2f94c29d83561aa534a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c299b9b46a49c14a1255ad31a3c17438482a28e9408b1dcd36db58d87d66247`

```dockerfile
```

-	Layers:
	-	`sha256:912e2047614870aa935e1c45fd05fb52050a876007557a6795c50c8237ff6549`  
		Last Modified: Fri, 15 May 2026 22:12:24 GMT  
		Size: 38.3 KB (38262 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind`

```console
$ docker pull docker@sha256:d0c942e5e2c14a74da706cff670ea2449fb57f9bc6abae7164461d0c6322b8b4
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
$ docker pull docker@sha256:74328f9b3824edb27d1c5b57abfa5765aa1742806ad77e3e90b2ee328aba8301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.7 MB (141655694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71837a59b95c3653383ca90ce81fbcee4f34adb0fbbf8b357e75da9affc77579`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Fri, 15 May 2026 22:12:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 15 May 2026 22:12:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 15 May 2026 22:12:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 15 May 2026 22:12:17 GMT
ENV DOCKER_VERSION=29.5.0
# Fri, 15 May 2026 22:12:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 15 May 2026 22:12:17 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Fri, 15 May 2026 22:12:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-amd64'; 			sha256='0144479d5a1cd710be3464ae898628cfa68033e16b225aef52f81930c45ac9b5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v6'; 			sha256='1f34337385921c5da43d63452282726b062aa887fda975f96dd3d6e869648bc6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v7'; 			sha256='3560b5b6fd3485f4d0bd160e7edf56cc1f08f0cb5852c9af28bf3fab9973c7c2'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm64'; 			sha256='565605fe0bb393ed5d11771e5b52fc7ef05c701868861fa85609747c9d74a440'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-ppc64le'; 			sha256='c5ef8012f48a518e1c235ad408d26cd424d7b5fa87eaf78cb2ff4b9048730120'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-riscv64'; 			sha256='80b27d5f3a346591a5045b81217ee5be578ed151ef8cbd883a892c0ec0ac33f1'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-s390x'; 			sha256='04f5bd0d389f682c7e9287a3b3a1777b0848f8e10d58cbf9d4d12c9002bbb378'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 15 May 2026 22:12:18 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Fri, 15 May 2026 22:12:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 15 May 2026 22:12:19 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 15 May 2026 22:12:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 22:12:19 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 15 May 2026 22:12:19 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 15 May 2026 22:12:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2026 22:12:19 GMT
CMD ["sh"]
# Fri, 15 May 2026 22:45:52 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 15 May 2026 22:45:52 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 15 May 2026 22:45:52 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 15 May 2026 22:45:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 15 May 2026 22:45:55 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 15 May 2026 22:45:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 15 May 2026 22:45:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 22:45:55 GMT
VOLUME [/var/lib/docker]
# Fri, 15 May 2026 22:45:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 15 May 2026 22:45:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 15 May 2026 22:45:55 GMT
CMD []
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2240a8f6be9241c8313b7887a9f6b272758fa6f323a29ae88da91f004c59d0d6`  
		Last Modified: Fri, 15 May 2026 22:12:26 GMT  
		Size: 8.3 MB (8311611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee8f29570b73bc6fb95364db2374f726e9b921827f4d1383a6d310769c050e2`  
		Last Modified: Fri, 15 May 2026 22:12:26 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb157a4a9b724e516e2a50f94be797a8145642f3c45f0f8d7bc236aa4848960`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 19.5 MB (19549502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f6e87dc813cb0ce7fd8d1277ed2d283a03d11b6492284e50fc16c959ccf8cb1`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 23.0 MB (22988578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4642ba5a86eb9921fd340045e353c9b3723a87f535731ae12659016c86bd3a48`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 11.2 MB (11243758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53d662cd1653019365b80d59af307d893de60a95d5d03aa7faddf0654b0162a7`  
		Last Modified: Fri, 15 May 2026 22:12:28 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45636b869c7065c939fb09da20708b05eb4bffe960ae3cb0102e1101147bf702`  
		Last Modified: Fri, 15 May 2026 22:12:28 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9074eaed06bf00c4914e361b510e55cd12bb8b0305b732d777ef95e01914b4f4`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f0de530d70a206bbf99372d4e80b56da6aa52a05b01bd6390d3bb3f4317466`  
		Last Modified: Fri, 15 May 2026 22:46:06 GMT  
		Size: 6.9 MB (6941385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc4ad90df2e9375f24da713fdbd03d16ffd44bcab544ed61a9d388fcc342e85`  
		Last Modified: Fri, 15 May 2026 22:46:06 GMT  
		Size: 92.2 KB (92210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f7d81cca6c2e02237a63044b96fc4e4432bffd61e595b15c8c2d952370deeed`  
		Last Modified: Fri, 15 May 2026 22:46:06 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb7196e21df03c1f04999bead8f104980dd964263cd7b78f05f013ad70dc5e2`  
		Last Modified: Fri, 15 May 2026 22:46:08 GMT  
		Size: 68.7 MB (68656308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403fc89c99ec573758e84c2e171afabefeec367c0c3ac712710c2c280fac6f51`  
		Last Modified: Fri, 15 May 2026 22:46:07 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6ba97049938b6a09c6a9ac2e32cd77fd36080fff06433e8e5f31af12220583`  
		Last Modified: Fri, 15 May 2026 22:46:07 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:bd3f7470c6236fcdb2cf1e2c99310e54bbd3ad7060762321c8003d30700a4adf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c743ab7cd39dee28326b6ff67c26d9c04b6169c89078262749d30845200dbb5b`

```dockerfile
```

-	Layers:
	-	`sha256:d84803d0d069e3f761b94992b6e3e50d1af7858113038a4930bde2b44ff43a64`  
		Last Modified: Fri, 15 May 2026 22:46:06 GMT  
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
$ docker pull docker@sha256:ef239f5a75ebd13a6e3a3ab62b4968537548555442e51b74688fefeee15455d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.7 MB (131665508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e6993f94a7073e22d9d8fa213b4f91cc953dac434c0511af155e03ba2bbbd8c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Fri, 15 May 2026 22:11:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 15 May 2026 22:11:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 15 May 2026 22:12:00 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 15 May 2026 22:12:04 GMT
ENV DOCKER_VERSION=29.5.0
# Fri, 15 May 2026 22:12:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 15 May 2026 22:12:04 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Fri, 15 May 2026 22:12:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-amd64'; 			sha256='0144479d5a1cd710be3464ae898628cfa68033e16b225aef52f81930c45ac9b5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v6'; 			sha256='1f34337385921c5da43d63452282726b062aa887fda975f96dd3d6e869648bc6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v7'; 			sha256='3560b5b6fd3485f4d0bd160e7edf56cc1f08f0cb5852c9af28bf3fab9973c7c2'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm64'; 			sha256='565605fe0bb393ed5d11771e5b52fc7ef05c701868861fa85609747c9d74a440'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-ppc64le'; 			sha256='c5ef8012f48a518e1c235ad408d26cd424d7b5fa87eaf78cb2ff4b9048730120'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-riscv64'; 			sha256='80b27d5f3a346591a5045b81217ee5be578ed151ef8cbd883a892c0ec0ac33f1'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-s390x'; 			sha256='04f5bd0d389f682c7e9287a3b3a1777b0848f8e10d58cbf9d4d12c9002bbb378'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 15 May 2026 22:12:07 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Fri, 15 May 2026 22:12:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 15 May 2026 22:12:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 15 May 2026 22:12:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 22:12:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 15 May 2026 22:12:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 15 May 2026 22:12:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2026 22:12:10 GMT
CMD ["sh"]
# Fri, 15 May 2026 22:14:39 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 15 May 2026 22:14:40 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 15 May 2026 22:14:40 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 15 May 2026 22:14:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 15 May 2026 22:14:43 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 15 May 2026 22:14:43 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 15 May 2026 22:14:43 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 22:14:43 GMT
VOLUME [/var/lib/docker]
# Fri, 15 May 2026 22:14:43 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 15 May 2026 22:14:43 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 15 May 2026 22:14:43 GMT
CMD []
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb53acd779ed72fcbca92822c9c8dca72fc19b59b4367fc8edbe5c8edd184829`  
		Last Modified: Fri, 15 May 2026 22:12:16 GMT  
		Size: 7.5 MB (7520515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3717dbbea465f22997cb871db7b421cb78bfc5d2353e0fbb9c24a4d7f4eead8b`  
		Last Modified: Fri, 15 May 2026 22:12:16 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2765ebda46cc899cbdd1066e7e900d81e9e6227536c38218d156a6c6ffc93324`  
		Last Modified: Fri, 15 May 2026 22:12:17 GMT  
		Size: 18.2 MB (18172266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8e62c2751306352d388df5f6ed3f91e4f160f2da7a249168dc387777896b44`  
		Last Modified: Fri, 15 May 2026 22:12:17 GMT  
		Size: 21.6 MB (21600397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e74677ed12033b201cddf684740d6f5f9540e22ab253c874ab4d21644f5b592`  
		Last Modified: Fri, 15 May 2026 22:12:17 GMT  
		Size: 10.6 MB (10637133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d76fc015f6b878f4335aa2e01b8ef18fcc9e9b2cb962b48d46350deb994e02d`  
		Last Modified: Fri, 15 May 2026 22:12:17 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad7ca5f5e6e176e7d1835e181fe35affc2155c45a6a1148aa7f18ea76d9d05e`  
		Last Modified: Fri, 15 May 2026 22:12:18 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdab469dc84864d9800ae053f9d87586d2515da2b650cf6f13f5ee84e15b2276`  
		Last Modified: Fri, 15 May 2026 22:12:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e61fa784a50d39d698bb4131e0cdda87523cb190f1d964d336a0eb9670b6fd`  
		Last Modified: Fri, 15 May 2026 22:14:53 GMT  
		Size: 6.6 MB (6577169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6091cd81f80a383632ea922a26439e61a5003e64d76dfc3d4bfec40420f0f921`  
		Last Modified: Fri, 15 May 2026 22:14:53 GMT  
		Size: 87.8 KB (87833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:858404ad7c646164306853c3153ee071dd35b14abaf989078b504a287c341dec`  
		Last Modified: Fri, 15 May 2026 22:14:53 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4328aaffaeedc3768196c5928da4c98cee1bfc491c8e951d2dc43da2d38acd04`  
		Last Modified: Fri, 15 May 2026 22:14:55 GMT  
		Size: 63.8 MB (63778918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f84fcf533486742f994566043a25c7a7c23e263cd00704b53a1653242d0b0b8`  
		Last Modified: Fri, 15 May 2026 22:14:55 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95db86311c1bf70966aa5d474d44b82d7521ce7b749c0450d9a393fc88161168`  
		Last Modified: Fri, 15 May 2026 22:14:55 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:6b79b3ac684b96301be66c5f36fd56c5a6c5756cf5a41c478f6d1945686b8349
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:709fc5e54befeab0806a68f4887f40378c59005ec285f228919d0e515f79e46b`

```dockerfile
```

-	Layers:
	-	`sha256:0107810b79e283361584a1b052454ef6bbd5468de93976e803fe7b0ac4ee3336`  
		Last Modified: Fri, 15 May 2026 22:14:53 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:6271c82062c42bdbc409cb458dce06d11f74ce961c30a90c6eb58a998c28afee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.1 MB (131088703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e575b474f12e2e286b308aeaf79fda6e9fec3855a23edec1474dc5b5b8dd4427`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Fri, 15 May 2026 22:12:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 15 May 2026 22:12:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 15 May 2026 22:12:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 15 May 2026 22:12:17 GMT
ENV DOCKER_VERSION=29.5.0
# Fri, 15 May 2026 22:12:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 15 May 2026 22:12:17 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Fri, 15 May 2026 22:12:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-amd64'; 			sha256='0144479d5a1cd710be3464ae898628cfa68033e16b225aef52f81930c45ac9b5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v6'; 			sha256='1f34337385921c5da43d63452282726b062aa887fda975f96dd3d6e869648bc6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v7'; 			sha256='3560b5b6fd3485f4d0bd160e7edf56cc1f08f0cb5852c9af28bf3fab9973c7c2'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm64'; 			sha256='565605fe0bb393ed5d11771e5b52fc7ef05c701868861fa85609747c9d74a440'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-ppc64le'; 			sha256='c5ef8012f48a518e1c235ad408d26cd424d7b5fa87eaf78cb2ff4b9048730120'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-riscv64'; 			sha256='80b27d5f3a346591a5045b81217ee5be578ed151ef8cbd883a892c0ec0ac33f1'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-s390x'; 			sha256='04f5bd0d389f682c7e9287a3b3a1777b0848f8e10d58cbf9d4d12c9002bbb378'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 15 May 2026 22:12:18 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Fri, 15 May 2026 22:12:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 15 May 2026 22:12:19 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 15 May 2026 22:12:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 22:12:19 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 15 May 2026 22:12:19 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 15 May 2026 22:12:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2026 22:12:19 GMT
CMD ["sh"]
# Fri, 15 May 2026 22:46:13 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 15 May 2026 22:46:14 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 15 May 2026 22:46:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 15 May 2026 22:46:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 15 May 2026 22:46:17 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 15 May 2026 22:46:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 15 May 2026 22:46:17 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 22:46:17 GMT
VOLUME [/var/lib/docker]
# Fri, 15 May 2026 22:46:17 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 15 May 2026 22:46:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 15 May 2026 22:46:17 GMT
CMD []
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd51147f6d8210f56d90e095c69db7468c6a7f4c96b15954bec62a38d029c230`  
		Last Modified: Fri, 15 May 2026 22:12:26 GMT  
		Size: 8.4 MB (8368382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca485120792b1bdb82820fd08df20937c87c36c02b044d113785a278f04c9c5e`  
		Last Modified: Fri, 15 May 2026 22:12:25 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76be2953b1820f6b03454f4cc64611d855fbccf3feb3c9d49c80e129eddcad5`  
		Last Modified: Fri, 15 May 2026 22:12:26 GMT  
		Size: 18.0 MB (18003835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc8387c97690c1e6db50aa3de5c90f1742500af7c360287ddfe4acd0578e0eb`  
		Last Modified: Fri, 15 May 2026 22:12:26 GMT  
		Size: 20.8 MB (20815340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3087ee8252be9dcbda43072f57a958f8f37983b3932bdca55c49fc7420da93f`  
		Last Modified: Fri, 15 May 2026 22:12:26 GMT  
		Size: 10.2 MB (10243274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027710042ccab2488d5291cd625bb62305844954e320f530f618c56b53ef928c`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0557313fec61d76b6a60306c806eb278032cfc80335daa86db37ad9979e81756`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9074eaed06bf00c4914e361b510e55cd12bb8b0305b732d777ef95e01914b4f4`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43b2d205b3daf8cb2c6ef3c0e0999b4106fc7a6595ba5568e8605a7e7b0722d8`  
		Last Modified: Fri, 15 May 2026 22:46:26 GMT  
		Size: 7.2 MB (7219897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0304531f0ed7ae27db4e86f747d65dfef2567fd5f396a4b3922c5ff5780d1f2`  
		Last Modified: Fri, 15 May 2026 22:46:26 GMT  
		Size: 100.9 KB (100934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95e602dc9bf9e82e229534494ecc27788dfc15984a25ad6683a47603dfb112ff`  
		Last Modified: Fri, 15 May 2026 22:46:26 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb752877659a29a329ac376438ffc77fd5832ef8ec7713badc224dc70797bd6`  
		Last Modified: Fri, 15 May 2026 22:46:29 GMT  
		Size: 62.1 MB (62129016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1ca5de4993dc83a36fb35a72b4fedf78533c646f254850669127c3e34a022a`  
		Last Modified: Fri, 15 May 2026 22:46:27 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27981b508a5db9a4e2a2c0b87eb0017d532fc5cc5bd11529ba120cd1e843ae91`  
		Last Modified: Fri, 15 May 2026 22:46:28 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:75f2ca4085188952af0189876ba5792cdd9148db56893b95a052e1a878bd4763
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9a506d026912de6f5e76fbcaf2f074cae0ccb50f7496d643ebb7bb3454ee5b0`

```dockerfile
```

-	Layers:
	-	`sha256:8cf936b97b7e42d4fcbb8824339486e8226b6af0c069484bcb894b3a1d54a301`  
		Last Modified: Fri, 15 May 2026 22:46:26 GMT  
		Size: 34.8 KB (34782 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind-rootless`

```console
$ docker pull docker@sha256:2379588ca8e9ed0d452464f4aed5361da6361791ec1a2111d44515c3985b2659
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:86dd1e4303fe60a2cd5f155db3c77e30011cfd8aaa9950188cece42d5e9f8ac3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157179647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f66937a706e25d69d45209cbd13b73c920e1d5ae4415214c93da738b95c779a0`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Fri, 15 May 2026 22:12:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 15 May 2026 22:12:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 15 May 2026 22:12:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 15 May 2026 22:12:17 GMT
ENV DOCKER_VERSION=29.5.0
# Fri, 15 May 2026 22:12:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 15 May 2026 22:12:17 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Fri, 15 May 2026 22:12:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-amd64'; 			sha256='0144479d5a1cd710be3464ae898628cfa68033e16b225aef52f81930c45ac9b5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v6'; 			sha256='1f34337385921c5da43d63452282726b062aa887fda975f96dd3d6e869648bc6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v7'; 			sha256='3560b5b6fd3485f4d0bd160e7edf56cc1f08f0cb5852c9af28bf3fab9973c7c2'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm64'; 			sha256='565605fe0bb393ed5d11771e5b52fc7ef05c701868861fa85609747c9d74a440'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-ppc64le'; 			sha256='c5ef8012f48a518e1c235ad408d26cd424d7b5fa87eaf78cb2ff4b9048730120'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-riscv64'; 			sha256='80b27d5f3a346591a5045b81217ee5be578ed151ef8cbd883a892c0ec0ac33f1'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-s390x'; 			sha256='04f5bd0d389f682c7e9287a3b3a1777b0848f8e10d58cbf9d4d12c9002bbb378'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 15 May 2026 22:12:18 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Fri, 15 May 2026 22:12:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 15 May 2026 22:12:19 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 15 May 2026 22:12:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 22:12:19 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 15 May 2026 22:12:19 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 15 May 2026 22:12:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2026 22:12:19 GMT
CMD ["sh"]
# Fri, 15 May 2026 22:45:52 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 15 May 2026 22:45:52 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 15 May 2026 22:45:52 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 15 May 2026 22:45:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 15 May 2026 22:45:55 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 15 May 2026 22:45:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 15 May 2026 22:45:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 22:45:55 GMT
VOLUME [/var/lib/docker]
# Fri, 15 May 2026 22:45:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 15 May 2026 22:45:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 15 May 2026 22:45:55 GMT
CMD []
# Sat, 16 May 2026 00:10:18 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Sat, 16 May 2026 00:10:18 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Sat, 16 May 2026 00:10:18 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Sat, 16 May 2026 00:10:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 	; 	rm rootless.tgz; 		rootlesskit --version # buildkit
# Sat, 16 May 2026 00:10:18 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Sat, 16 May 2026 00:10:18 GMT
VOLUME [/home/rootless/.local/share/docker]
# Sat, 16 May 2026 00:10:18 GMT
USER rootless
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2240a8f6be9241c8313b7887a9f6b272758fa6f323a29ae88da91f004c59d0d6`  
		Last Modified: Fri, 15 May 2026 22:12:26 GMT  
		Size: 8.3 MB (8311611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee8f29570b73bc6fb95364db2374f726e9b921827f4d1383a6d310769c050e2`  
		Last Modified: Fri, 15 May 2026 22:12:26 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb157a4a9b724e516e2a50f94be797a8145642f3c45f0f8d7bc236aa4848960`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 19.5 MB (19549502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f6e87dc813cb0ce7fd8d1277ed2d283a03d11b6492284e50fc16c959ccf8cb1`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 23.0 MB (22988578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4642ba5a86eb9921fd340045e353c9b3723a87f535731ae12659016c86bd3a48`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 11.2 MB (11243758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53d662cd1653019365b80d59af307d893de60a95d5d03aa7faddf0654b0162a7`  
		Last Modified: Fri, 15 May 2026 22:12:28 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45636b869c7065c939fb09da20708b05eb4bffe960ae3cb0102e1101147bf702`  
		Last Modified: Fri, 15 May 2026 22:12:28 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9074eaed06bf00c4914e361b510e55cd12bb8b0305b732d777ef95e01914b4f4`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f0de530d70a206bbf99372d4e80b56da6aa52a05b01bd6390d3bb3f4317466`  
		Last Modified: Fri, 15 May 2026 22:46:06 GMT  
		Size: 6.9 MB (6941385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc4ad90df2e9375f24da713fdbd03d16ffd44bcab544ed61a9d388fcc342e85`  
		Last Modified: Fri, 15 May 2026 22:46:06 GMT  
		Size: 92.2 KB (92210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f7d81cca6c2e02237a63044b96fc4e4432bffd61e595b15c8c2d952370deeed`  
		Last Modified: Fri, 15 May 2026 22:46:06 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb7196e21df03c1f04999bead8f104980dd964263cd7b78f05f013ad70dc5e2`  
		Last Modified: Fri, 15 May 2026 22:46:08 GMT  
		Size: 68.7 MB (68656308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403fc89c99ec573758e84c2e171afabefeec367c0c3ac712710c2c280fac6f51`  
		Last Modified: Fri, 15 May 2026 22:46:07 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6ba97049938b6a09c6a9ac2e32cd77fd36080fff06433e8e5f31af12220583`  
		Last Modified: Fri, 15 May 2026 22:46:07 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3aecd32c9a7b429826161d546e29c1dff0ac6eea914337b0b9d0a168b785fe5`  
		Last Modified: Sat, 16 May 2026 00:10:24 GMT  
		Size: 3.4 MB (3420116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75a1fd367a70907870ec61c5541633c1016315039aa85446173764ece77df84`  
		Last Modified: Sat, 16 May 2026 00:10:23 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896453e7017b28888cd072db72945d8e744a934faf06c8d0afe071918a3ab492`  
		Last Modified: Sat, 16 May 2026 00:10:23 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8de78d541dc09dba7c55cf30b416cc37bf4cadc540afd919f470b8c6ea68c5`  
		Last Modified: Sat, 16 May 2026 00:10:24 GMT  
		Size: 12.1 MB (12102497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307ee9ce5b3abe899d1554ebbfe999955a855268f925239ee277ff0542c7424f`  
		Last Modified: Sat, 16 May 2026 00:10:25 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:a928bb65ab1afe6b79776cfe5fec97b7de2ce78299935d0f2a6d93a022bbf33d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10081df2ff0f054ec55a6ba8b0e73f3f8660a710ebcd84146466c7e415b001f2`

```dockerfile
```

-	Layers:
	-	`sha256:ef654a1e85deabbd5d572b1aa6d9feaba8a368d7af558b844574a48c0af89e2c`  
		Last Modified: Sat, 16 May 2026 00:10:23 GMT  
		Size: 30.5 KB (30492 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:beddbc20555efb8bc7641a98e7a58a5104329118a81b075bd2373de0e1dca5c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.7 MB (145721108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7cb4b74b39f9eb3c077215fb0f4c6f7d8395bd86b29015b4743c1a5b13d2f24`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Fri, 15 May 2026 22:12:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 15 May 2026 22:12:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 15 May 2026 22:12:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 15 May 2026 22:12:17 GMT
ENV DOCKER_VERSION=29.5.0
# Fri, 15 May 2026 22:12:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 15 May 2026 22:12:17 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Fri, 15 May 2026 22:12:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-amd64'; 			sha256='0144479d5a1cd710be3464ae898628cfa68033e16b225aef52f81930c45ac9b5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v6'; 			sha256='1f34337385921c5da43d63452282726b062aa887fda975f96dd3d6e869648bc6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v7'; 			sha256='3560b5b6fd3485f4d0bd160e7edf56cc1f08f0cb5852c9af28bf3fab9973c7c2'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm64'; 			sha256='565605fe0bb393ed5d11771e5b52fc7ef05c701868861fa85609747c9d74a440'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-ppc64le'; 			sha256='c5ef8012f48a518e1c235ad408d26cd424d7b5fa87eaf78cb2ff4b9048730120'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-riscv64'; 			sha256='80b27d5f3a346591a5045b81217ee5be578ed151ef8cbd883a892c0ec0ac33f1'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-s390x'; 			sha256='04f5bd0d389f682c7e9287a3b3a1777b0848f8e10d58cbf9d4d12c9002bbb378'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 15 May 2026 22:12:18 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Fri, 15 May 2026 22:12:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 15 May 2026 22:12:19 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 15 May 2026 22:12:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 22:12:19 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 15 May 2026 22:12:19 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 15 May 2026 22:12:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2026 22:12:19 GMT
CMD ["sh"]
# Fri, 15 May 2026 22:46:13 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 15 May 2026 22:46:14 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 15 May 2026 22:46:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 15 May 2026 22:46:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 15 May 2026 22:46:17 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 15 May 2026 22:46:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 15 May 2026 22:46:17 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 22:46:17 GMT
VOLUME [/var/lib/docker]
# Fri, 15 May 2026 22:46:17 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 15 May 2026 22:46:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 15 May 2026 22:46:17 GMT
CMD []
# Sat, 16 May 2026 00:10:04 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Sat, 16 May 2026 00:10:04 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Sat, 16 May 2026 00:10:04 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Sat, 16 May 2026 00:10:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 	; 	rm rootless.tgz; 		rootlesskit --version # buildkit
# Sat, 16 May 2026 00:10:05 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Sat, 16 May 2026 00:10:05 GMT
VOLUME [/home/rootless/.local/share/docker]
# Sat, 16 May 2026 00:10:05 GMT
USER rootless
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd51147f6d8210f56d90e095c69db7468c6a7f4c96b15954bec62a38d029c230`  
		Last Modified: Fri, 15 May 2026 22:12:26 GMT  
		Size: 8.4 MB (8368382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca485120792b1bdb82820fd08df20937c87c36c02b044d113785a278f04c9c5e`  
		Last Modified: Fri, 15 May 2026 22:12:25 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76be2953b1820f6b03454f4cc64611d855fbccf3feb3c9d49c80e129eddcad5`  
		Last Modified: Fri, 15 May 2026 22:12:26 GMT  
		Size: 18.0 MB (18003835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc8387c97690c1e6db50aa3de5c90f1742500af7c360287ddfe4acd0578e0eb`  
		Last Modified: Fri, 15 May 2026 22:12:26 GMT  
		Size: 20.8 MB (20815340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3087ee8252be9dcbda43072f57a958f8f37983b3932bdca55c49fc7420da93f`  
		Last Modified: Fri, 15 May 2026 22:12:26 GMT  
		Size: 10.2 MB (10243274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027710042ccab2488d5291cd625bb62305844954e320f530f618c56b53ef928c`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0557313fec61d76b6a60306c806eb278032cfc80335daa86db37ad9979e81756`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9074eaed06bf00c4914e361b510e55cd12bb8b0305b732d777ef95e01914b4f4`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43b2d205b3daf8cb2c6ef3c0e0999b4106fc7a6595ba5568e8605a7e7b0722d8`  
		Last Modified: Fri, 15 May 2026 22:46:26 GMT  
		Size: 7.2 MB (7219897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0304531f0ed7ae27db4e86f747d65dfef2567fd5f396a4b3922c5ff5780d1f2`  
		Last Modified: Fri, 15 May 2026 22:46:26 GMT  
		Size: 100.9 KB (100934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95e602dc9bf9e82e229534494ecc27788dfc15984a25ad6683a47603dfb112ff`  
		Last Modified: Fri, 15 May 2026 22:46:26 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb752877659a29a329ac376438ffc77fd5832ef8ec7713badc224dc70797bd6`  
		Last Modified: Fri, 15 May 2026 22:46:29 GMT  
		Size: 62.1 MB (62129016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1ca5de4993dc83a36fb35a72b4fedf78533c646f254850669127c3e34a022a`  
		Last Modified: Fri, 15 May 2026 22:46:27 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27981b508a5db9a4e2a2c0b87eb0017d532fc5cc5bd11529ba120cd1e843ae91`  
		Last Modified: Fri, 15 May 2026 22:46:28 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1a7270b72b7f3e2799e7c141f64461907402307eab0e5a25271d1e2b47c44ee`  
		Last Modified: Sat, 16 May 2026 00:10:10 GMT  
		Size: 3.4 MB (3394559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5f6bb10aafb4e20e513a5cc5d9a7e3481a971f0433332b50708cd61bc4df70`  
		Last Modified: Sat, 16 May 2026 00:10:10 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c4e8ff9e0e4eab7d4814e9d39e6a4c25f79d76d2979f00a78de155911ef2ddd`  
		Last Modified: Sat, 16 May 2026 00:10:10 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91aab9887dd46e6f833ba3ffff294c32d59299ab8d4a3847194a60a227c55b0`  
		Last Modified: Sat, 16 May 2026 00:10:10 GMT  
		Size: 11.2 MB (11236505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3459fdc6872a7acd1e3b7884a28a60561f9e3488cf19f8437a3b11c8e09a6d8`  
		Last Modified: Sat, 16 May 2026 00:10:11 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:58ffdbbba10f97b2d1ef33dbfbdf016c2844506424a34f22333f5597310a7fab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 KB (30663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a11fccc6bc4fd79d54dca7d1d3ed318788c65b63d3184fbb73c400cadceb60f`

```dockerfile
```

-	Layers:
	-	`sha256:fc110ccff973a2ba6b5d21f0f1f25d79b12b82a863abcabd81b546d627bb598c`  
		Last Modified: Sat, 16 May 2026 00:10:09 GMT  
		Size: 30.7 KB (30663 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:latest`

```console
$ docker pull docker@sha256:d0c942e5e2c14a74da706cff670ea2449fb57f9bc6abae7164461d0c6322b8b4
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
$ docker pull docker@sha256:74328f9b3824edb27d1c5b57abfa5765aa1742806ad77e3e90b2ee328aba8301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.7 MB (141655694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71837a59b95c3653383ca90ce81fbcee4f34adb0fbbf8b357e75da9affc77579`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Fri, 15 May 2026 22:12:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 15 May 2026 22:12:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 15 May 2026 22:12:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 15 May 2026 22:12:17 GMT
ENV DOCKER_VERSION=29.5.0
# Fri, 15 May 2026 22:12:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 15 May 2026 22:12:17 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Fri, 15 May 2026 22:12:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-amd64'; 			sha256='0144479d5a1cd710be3464ae898628cfa68033e16b225aef52f81930c45ac9b5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v6'; 			sha256='1f34337385921c5da43d63452282726b062aa887fda975f96dd3d6e869648bc6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v7'; 			sha256='3560b5b6fd3485f4d0bd160e7edf56cc1f08f0cb5852c9af28bf3fab9973c7c2'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm64'; 			sha256='565605fe0bb393ed5d11771e5b52fc7ef05c701868861fa85609747c9d74a440'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-ppc64le'; 			sha256='c5ef8012f48a518e1c235ad408d26cd424d7b5fa87eaf78cb2ff4b9048730120'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-riscv64'; 			sha256='80b27d5f3a346591a5045b81217ee5be578ed151ef8cbd883a892c0ec0ac33f1'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-s390x'; 			sha256='04f5bd0d389f682c7e9287a3b3a1777b0848f8e10d58cbf9d4d12c9002bbb378'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 15 May 2026 22:12:18 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Fri, 15 May 2026 22:12:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 15 May 2026 22:12:19 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 15 May 2026 22:12:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 22:12:19 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 15 May 2026 22:12:19 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 15 May 2026 22:12:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2026 22:12:19 GMT
CMD ["sh"]
# Fri, 15 May 2026 22:45:52 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 15 May 2026 22:45:52 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 15 May 2026 22:45:52 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 15 May 2026 22:45:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 15 May 2026 22:45:55 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 15 May 2026 22:45:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 15 May 2026 22:45:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 22:45:55 GMT
VOLUME [/var/lib/docker]
# Fri, 15 May 2026 22:45:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 15 May 2026 22:45:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 15 May 2026 22:45:55 GMT
CMD []
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2240a8f6be9241c8313b7887a9f6b272758fa6f323a29ae88da91f004c59d0d6`  
		Last Modified: Fri, 15 May 2026 22:12:26 GMT  
		Size: 8.3 MB (8311611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee8f29570b73bc6fb95364db2374f726e9b921827f4d1383a6d310769c050e2`  
		Last Modified: Fri, 15 May 2026 22:12:26 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb157a4a9b724e516e2a50f94be797a8145642f3c45f0f8d7bc236aa4848960`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 19.5 MB (19549502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f6e87dc813cb0ce7fd8d1277ed2d283a03d11b6492284e50fc16c959ccf8cb1`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 23.0 MB (22988578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4642ba5a86eb9921fd340045e353c9b3723a87f535731ae12659016c86bd3a48`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 11.2 MB (11243758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53d662cd1653019365b80d59af307d893de60a95d5d03aa7faddf0654b0162a7`  
		Last Modified: Fri, 15 May 2026 22:12:28 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45636b869c7065c939fb09da20708b05eb4bffe960ae3cb0102e1101147bf702`  
		Last Modified: Fri, 15 May 2026 22:12:28 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9074eaed06bf00c4914e361b510e55cd12bb8b0305b732d777ef95e01914b4f4`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f0de530d70a206bbf99372d4e80b56da6aa52a05b01bd6390d3bb3f4317466`  
		Last Modified: Fri, 15 May 2026 22:46:06 GMT  
		Size: 6.9 MB (6941385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc4ad90df2e9375f24da713fdbd03d16ffd44bcab544ed61a9d388fcc342e85`  
		Last Modified: Fri, 15 May 2026 22:46:06 GMT  
		Size: 92.2 KB (92210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f7d81cca6c2e02237a63044b96fc4e4432bffd61e595b15c8c2d952370deeed`  
		Last Modified: Fri, 15 May 2026 22:46:06 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb7196e21df03c1f04999bead8f104980dd964263cd7b78f05f013ad70dc5e2`  
		Last Modified: Fri, 15 May 2026 22:46:08 GMT  
		Size: 68.7 MB (68656308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403fc89c99ec573758e84c2e171afabefeec367c0c3ac712710c2c280fac6f51`  
		Last Modified: Fri, 15 May 2026 22:46:07 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6ba97049938b6a09c6a9ac2e32cd77fd36080fff06433e8e5f31af12220583`  
		Last Modified: Fri, 15 May 2026 22:46:07 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:bd3f7470c6236fcdb2cf1e2c99310e54bbd3ad7060762321c8003d30700a4adf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c743ab7cd39dee28326b6ff67c26d9c04b6169c89078262749d30845200dbb5b`

```dockerfile
```

-	Layers:
	-	`sha256:d84803d0d069e3f761b94992b6e3e50d1af7858113038a4930bde2b44ff43a64`  
		Last Modified: Fri, 15 May 2026 22:46:06 GMT  
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
$ docker pull docker@sha256:ef239f5a75ebd13a6e3a3ab62b4968537548555442e51b74688fefeee15455d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.7 MB (131665508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e6993f94a7073e22d9d8fa213b4f91cc953dac434c0511af155e03ba2bbbd8c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Fri, 15 May 2026 22:11:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 15 May 2026 22:11:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 15 May 2026 22:12:00 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 15 May 2026 22:12:04 GMT
ENV DOCKER_VERSION=29.5.0
# Fri, 15 May 2026 22:12:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 15 May 2026 22:12:04 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Fri, 15 May 2026 22:12:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-amd64'; 			sha256='0144479d5a1cd710be3464ae898628cfa68033e16b225aef52f81930c45ac9b5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v6'; 			sha256='1f34337385921c5da43d63452282726b062aa887fda975f96dd3d6e869648bc6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v7'; 			sha256='3560b5b6fd3485f4d0bd160e7edf56cc1f08f0cb5852c9af28bf3fab9973c7c2'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm64'; 			sha256='565605fe0bb393ed5d11771e5b52fc7ef05c701868861fa85609747c9d74a440'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-ppc64le'; 			sha256='c5ef8012f48a518e1c235ad408d26cd424d7b5fa87eaf78cb2ff4b9048730120'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-riscv64'; 			sha256='80b27d5f3a346591a5045b81217ee5be578ed151ef8cbd883a892c0ec0ac33f1'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-s390x'; 			sha256='04f5bd0d389f682c7e9287a3b3a1777b0848f8e10d58cbf9d4d12c9002bbb378'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 15 May 2026 22:12:07 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Fri, 15 May 2026 22:12:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 15 May 2026 22:12:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 15 May 2026 22:12:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 22:12:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 15 May 2026 22:12:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 15 May 2026 22:12:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2026 22:12:10 GMT
CMD ["sh"]
# Fri, 15 May 2026 22:14:39 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 15 May 2026 22:14:40 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 15 May 2026 22:14:40 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 15 May 2026 22:14:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 15 May 2026 22:14:43 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 15 May 2026 22:14:43 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 15 May 2026 22:14:43 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 22:14:43 GMT
VOLUME [/var/lib/docker]
# Fri, 15 May 2026 22:14:43 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 15 May 2026 22:14:43 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 15 May 2026 22:14:43 GMT
CMD []
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb53acd779ed72fcbca92822c9c8dca72fc19b59b4367fc8edbe5c8edd184829`  
		Last Modified: Fri, 15 May 2026 22:12:16 GMT  
		Size: 7.5 MB (7520515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3717dbbea465f22997cb871db7b421cb78bfc5d2353e0fbb9c24a4d7f4eead8b`  
		Last Modified: Fri, 15 May 2026 22:12:16 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2765ebda46cc899cbdd1066e7e900d81e9e6227536c38218d156a6c6ffc93324`  
		Last Modified: Fri, 15 May 2026 22:12:17 GMT  
		Size: 18.2 MB (18172266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8e62c2751306352d388df5f6ed3f91e4f160f2da7a249168dc387777896b44`  
		Last Modified: Fri, 15 May 2026 22:12:17 GMT  
		Size: 21.6 MB (21600397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e74677ed12033b201cddf684740d6f5f9540e22ab253c874ab4d21644f5b592`  
		Last Modified: Fri, 15 May 2026 22:12:17 GMT  
		Size: 10.6 MB (10637133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d76fc015f6b878f4335aa2e01b8ef18fcc9e9b2cb962b48d46350deb994e02d`  
		Last Modified: Fri, 15 May 2026 22:12:17 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad7ca5f5e6e176e7d1835e181fe35affc2155c45a6a1148aa7f18ea76d9d05e`  
		Last Modified: Fri, 15 May 2026 22:12:18 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdab469dc84864d9800ae053f9d87586d2515da2b650cf6f13f5ee84e15b2276`  
		Last Modified: Fri, 15 May 2026 22:12:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e61fa784a50d39d698bb4131e0cdda87523cb190f1d964d336a0eb9670b6fd`  
		Last Modified: Fri, 15 May 2026 22:14:53 GMT  
		Size: 6.6 MB (6577169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6091cd81f80a383632ea922a26439e61a5003e64d76dfc3d4bfec40420f0f921`  
		Last Modified: Fri, 15 May 2026 22:14:53 GMT  
		Size: 87.8 KB (87833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:858404ad7c646164306853c3153ee071dd35b14abaf989078b504a287c341dec`  
		Last Modified: Fri, 15 May 2026 22:14:53 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4328aaffaeedc3768196c5928da4c98cee1bfc491c8e951d2dc43da2d38acd04`  
		Last Modified: Fri, 15 May 2026 22:14:55 GMT  
		Size: 63.8 MB (63778918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f84fcf533486742f994566043a25c7a7c23e263cd00704b53a1653242d0b0b8`  
		Last Modified: Fri, 15 May 2026 22:14:55 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95db86311c1bf70966aa5d474d44b82d7521ce7b749c0450d9a393fc88161168`  
		Last Modified: Fri, 15 May 2026 22:14:55 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:6b79b3ac684b96301be66c5f36fd56c5a6c5756cf5a41c478f6d1945686b8349
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:709fc5e54befeab0806a68f4887f40378c59005ec285f228919d0e515f79e46b`

```dockerfile
```

-	Layers:
	-	`sha256:0107810b79e283361584a1b052454ef6bbd5468de93976e803fe7b0ac4ee3336`  
		Last Modified: Fri, 15 May 2026 22:14:53 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:6271c82062c42bdbc409cb458dce06d11f74ce961c30a90c6eb58a998c28afee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.1 MB (131088703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e575b474f12e2e286b308aeaf79fda6e9fec3855a23edec1474dc5b5b8dd4427`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Fri, 15 May 2026 22:12:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 15 May 2026 22:12:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 15 May 2026 22:12:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 15 May 2026 22:12:17 GMT
ENV DOCKER_VERSION=29.5.0
# Fri, 15 May 2026 22:12:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 15 May 2026 22:12:17 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Fri, 15 May 2026 22:12:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-amd64'; 			sha256='0144479d5a1cd710be3464ae898628cfa68033e16b225aef52f81930c45ac9b5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v6'; 			sha256='1f34337385921c5da43d63452282726b062aa887fda975f96dd3d6e869648bc6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v7'; 			sha256='3560b5b6fd3485f4d0bd160e7edf56cc1f08f0cb5852c9af28bf3fab9973c7c2'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm64'; 			sha256='565605fe0bb393ed5d11771e5b52fc7ef05c701868861fa85609747c9d74a440'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-ppc64le'; 			sha256='c5ef8012f48a518e1c235ad408d26cd424d7b5fa87eaf78cb2ff4b9048730120'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-riscv64'; 			sha256='80b27d5f3a346591a5045b81217ee5be578ed151ef8cbd883a892c0ec0ac33f1'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-s390x'; 			sha256='04f5bd0d389f682c7e9287a3b3a1777b0848f8e10d58cbf9d4d12c9002bbb378'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 15 May 2026 22:12:18 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Fri, 15 May 2026 22:12:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 15 May 2026 22:12:19 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 15 May 2026 22:12:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 22:12:19 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 15 May 2026 22:12:19 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 15 May 2026 22:12:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2026 22:12:19 GMT
CMD ["sh"]
# Fri, 15 May 2026 22:46:13 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 15 May 2026 22:46:14 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 15 May 2026 22:46:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 15 May 2026 22:46:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 15 May 2026 22:46:17 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 15 May 2026 22:46:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 15 May 2026 22:46:17 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 22:46:17 GMT
VOLUME [/var/lib/docker]
# Fri, 15 May 2026 22:46:17 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 15 May 2026 22:46:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 15 May 2026 22:46:17 GMT
CMD []
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd51147f6d8210f56d90e095c69db7468c6a7f4c96b15954bec62a38d029c230`  
		Last Modified: Fri, 15 May 2026 22:12:26 GMT  
		Size: 8.4 MB (8368382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca485120792b1bdb82820fd08df20937c87c36c02b044d113785a278f04c9c5e`  
		Last Modified: Fri, 15 May 2026 22:12:25 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76be2953b1820f6b03454f4cc64611d855fbccf3feb3c9d49c80e129eddcad5`  
		Last Modified: Fri, 15 May 2026 22:12:26 GMT  
		Size: 18.0 MB (18003835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc8387c97690c1e6db50aa3de5c90f1742500af7c360287ddfe4acd0578e0eb`  
		Last Modified: Fri, 15 May 2026 22:12:26 GMT  
		Size: 20.8 MB (20815340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3087ee8252be9dcbda43072f57a958f8f37983b3932bdca55c49fc7420da93f`  
		Last Modified: Fri, 15 May 2026 22:12:26 GMT  
		Size: 10.2 MB (10243274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027710042ccab2488d5291cd625bb62305844954e320f530f618c56b53ef928c`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0557313fec61d76b6a60306c806eb278032cfc80335daa86db37ad9979e81756`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9074eaed06bf00c4914e361b510e55cd12bb8b0305b732d777ef95e01914b4f4`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43b2d205b3daf8cb2c6ef3c0e0999b4106fc7a6595ba5568e8605a7e7b0722d8`  
		Last Modified: Fri, 15 May 2026 22:46:26 GMT  
		Size: 7.2 MB (7219897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0304531f0ed7ae27db4e86f747d65dfef2567fd5f396a4b3922c5ff5780d1f2`  
		Last Modified: Fri, 15 May 2026 22:46:26 GMT  
		Size: 100.9 KB (100934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95e602dc9bf9e82e229534494ecc27788dfc15984a25ad6683a47603dfb112ff`  
		Last Modified: Fri, 15 May 2026 22:46:26 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb752877659a29a329ac376438ffc77fd5832ef8ec7713badc224dc70797bd6`  
		Last Modified: Fri, 15 May 2026 22:46:29 GMT  
		Size: 62.1 MB (62129016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1ca5de4993dc83a36fb35a72b4fedf78533c646f254850669127c3e34a022a`  
		Last Modified: Fri, 15 May 2026 22:46:27 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27981b508a5db9a4e2a2c0b87eb0017d532fc5cc5bd11529ba120cd1e843ae91`  
		Last Modified: Fri, 15 May 2026 22:46:28 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:75f2ca4085188952af0189876ba5792cdd9148db56893b95a052e1a878bd4763
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9a506d026912de6f5e76fbcaf2f074cae0ccb50f7496d643ebb7bb3454ee5b0`

```dockerfile
```

-	Layers:
	-	`sha256:8cf936b97b7e42d4fcbb8824339486e8226b6af0c069484bcb894b3a1d54a301`  
		Last Modified: Fri, 15 May 2026 22:46:26 GMT  
		Size: 34.8 KB (34782 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:windowsservercore`

```console
$ docker pull docker@sha256:3268bde2385bb80b1e442f6c04799dd7619f785c63be6c4dccb6831a144f3043
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32860; amd64
	-	windows version 10.0.20348.5139; amd64

### `docker:windowsservercore` - windows version 10.0.26100.32860; amd64

```console
$ docker pull docker@sha256:e4420a2945552c16d362b8472d0182a0ec134ce320f2233ec15e93015e599e8f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2262478653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90d0a0d1bad4f84f1fbcaf6c1e419ce3a0952a03ed6d4582f9767303292ca6c6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 10 May 2026 10:08:54 GMT
RUN Install update 10.0.26100.32860
# Fri, 15 May 2026 22:15:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 15 May 2026 22:16:21 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 15 May 2026 22:16:22 GMT
ENV DOCKER_VERSION=29.5.0
# Fri, 15 May 2026 22:16:23 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.5.0.zip
# Fri, 15 May 2026 22:16:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 15 May 2026 22:16:39 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Fri, 15 May 2026 22:16:40 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.windows-amd64.exe
# Fri, 15 May 2026 22:16:40 GMT
ENV DOCKER_BUILDX_SHA256=96a10e259fa1380e7bbf9a3cb04872f201a6e7e331ddeeec8d3e38aa2650ddc5
# Fri, 15 May 2026 22:16:50 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 15 May 2026 22:16:51 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Fri, 15 May 2026 22:16:51 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-windows-x86_64.exe
# Fri, 15 May 2026 22:16:52 GMT
ENV DOCKER_COMPOSE_SHA256=5e6d72612b3165be9fea4ae889435fec76979a9779b6f62f4efee99dd5f41ea1
# Fri, 15 May 2026 22:17:01 GMT
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
	-	`sha256:74b535a51fd23dbc5005aa72b61e95ad333b54b6b5276fd600c8f26dc1ec6379`  
		Last Modified: Fri, 15 May 2026 22:17:10 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f1111f6cb7254129e7ea39ba28883376409a104ffda0b87a45a420ceee27fcb`  
		Last Modified: Fri, 15 May 2026 22:17:10 GMT  
		Size: 392.8 KB (392802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2db17ecf93e3efdbccd835fd5d408afb7a3351f7597a48a1ad636c01794ebe04`  
		Last Modified: Fri, 15 May 2026 22:17:09 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c83f256bcd38582b57bb91e485a2d85240d5f2ae45b27c9afa7a9a5f44ebed73`  
		Last Modified: Fri, 15 May 2026 22:17:09 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cdc10f672c38740ac0512c480a10fe4b0dc1658659e00513da102771c2e3e40`  
		Last Modified: Fri, 15 May 2026 22:17:11 GMT  
		Size: 20.3 MB (20260443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e77a9dc340d0bdbccbce6b57c4d89cad2a1db92d89f7c2649002da080b5334bd`  
		Last Modified: Fri, 15 May 2026 22:17:07 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2309766ee1a21f57c947e3ef48cf4592eb1c12fb99926f92dc710c73dff7b930`  
		Last Modified: Fri, 15 May 2026 22:17:07 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9e8a3c0bbacac0c1695cff5c5e5eeefe513850e0a04322d018dfc23f9317a07`  
		Last Modified: Fri, 15 May 2026 22:17:07 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2562224ef98ba779eb91088241d392cb2a71abbc685b008022439f669f7686d6`  
		Last Modified: Fri, 15 May 2026 22:17:09 GMT  
		Size: 23.9 MB (23920245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6af350faa47b96f1766ca0debecbe39139716c8b55ae988b2528535eed60cca`  
		Last Modified: Fri, 15 May 2026 22:17:05 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:780002467e4bb1a15f8748b2ea889bc85483b2d7ddb96b528e3b32c982692e19`  
		Last Modified: Fri, 15 May 2026 22:17:05 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47e3ee62773736f785dc51e4bc1a7e48595fe0afed17ab1d89154d1e06595d11`  
		Last Modified: Fri, 15 May 2026 22:17:05 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d076a230450a0b438ed3c7d1ee23904031d66dddd7e9ee8ac765637eb942ff8`  
		Last Modified: Fri, 15 May 2026 22:17:07 GMT  
		Size: 12.0 MB (11951730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.20348.5139; amd64

```console
$ docker pull docker@sha256:08c5da38b0e30b8a83bf89e16eff7a1292d6948010a051f9310d6e9511e6423f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2178998545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c8a2de39d58f5e39341f81d00642352c6b050887b387821ad49ffd590b688ad`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Fri, 15 May 2026 22:15:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 15 May 2026 22:16:42 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 15 May 2026 22:16:43 GMT
ENV DOCKER_VERSION=29.5.0
# Fri, 15 May 2026 22:16:43 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.5.0.zip
# Fri, 15 May 2026 22:16:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 15 May 2026 22:16:57 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Fri, 15 May 2026 22:16:57 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.windows-amd64.exe
# Fri, 15 May 2026 22:16:58 GMT
ENV DOCKER_BUILDX_SHA256=96a10e259fa1380e7bbf9a3cb04872f201a6e7e331ddeeec8d3e38aa2650ddc5
# Fri, 15 May 2026 22:17:07 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 15 May 2026 22:17:08 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Fri, 15 May 2026 22:17:08 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-windows-x86_64.exe
# Fri, 15 May 2026 22:17:09 GMT
ENV DOCKER_COMPOSE_SHA256=5e6d72612b3165be9fea4ae889435fec76979a9779b6f62f4efee99dd5f41ea1
# Fri, 15 May 2026 22:17:16 GMT
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
	-	`sha256:5961f3afdef68ce25fa592066416467d81416df4b1af2537087f1c9150afb728`  
		Last Modified: Fri, 15 May 2026 22:17:25 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae47499b6a77bf67c8fc4c6163dd490f816d5ea9168dfad57664888a82963cd`  
		Last Modified: Fri, 15 May 2026 22:17:25 GMT  
		Size: 506.6 KB (506623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1a50c6ae3a4766042c073c45ffd8a1c5d67595c9c560f65c76492d18a12fd50`  
		Last Modified: Fri, 15 May 2026 22:17:24 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:756530867ead10020116e1f2f106664f6fed6cae2160122fc6ec372b43fd678b`  
		Last Modified: Fri, 15 May 2026 22:17:24 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203d6d943b8fa9b8934a5ce05bf2893265e234366a62bf9ea3a09f77d5608167`  
		Last Modified: Fri, 15 May 2026 22:17:26 GMT  
		Size: 20.2 MB (20232134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f38228e51f50d7a28325477b370bd57476f2a6883a023e98c0d628bc22295ad4`  
		Last Modified: Fri, 15 May 2026 22:17:22 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f7fe5a6a8d2169e19d30f03057f1cf4e3dfa71a14a9e3e2572a95d5246c205`  
		Last Modified: Fri, 15 May 2026 22:17:22 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa5b9407c6ba09fc25979a724f032914bee3ded478b4366b26a09de96ef0c80`  
		Last Modified: Fri, 15 May 2026 22:17:22 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60bb62b675b679633b1a24e24b203fa8ed15d941f3bbb283bae34df7d68c50af`  
		Last Modified: Fri, 15 May 2026 22:17:24 GMT  
		Size: 23.9 MB (23901135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8874726604cb50cc54f506879180a624b7e0fc0e3ad5a8a7063d89505fd60ea`  
		Last Modified: Fri, 15 May 2026 22:17:20 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c7b4c5d7c92d0e67fbdf7582c6455934c8b5f3b3a8c849173931adad0837ca3`  
		Last Modified: Fri, 15 May 2026 22:17:20 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efe6f324d4756f3cd5de0642c06bbc7c60c070aa7a512c8682d7e2232291ae8b`  
		Last Modified: Fri, 15 May 2026 22:17:20 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:487382c6166366ea2b9acbadbf146f8443b6a756bfb7678718eb9c7383bc4a2c`  
		Last Modified: Fri, 15 May 2026 22:17:22 GMT  
		Size: 11.9 MB (11926255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:1c7ad5b5ef3c89a3bdc56e2574cbfe03b7327d744f4266d72447109f574789c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull docker@sha256:08c5da38b0e30b8a83bf89e16eff7a1292d6948010a051f9310d6e9511e6423f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2178998545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c8a2de39d58f5e39341f81d00642352c6b050887b387821ad49ffd590b688ad`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Fri, 15 May 2026 22:15:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 15 May 2026 22:16:42 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 15 May 2026 22:16:43 GMT
ENV DOCKER_VERSION=29.5.0
# Fri, 15 May 2026 22:16:43 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.5.0.zip
# Fri, 15 May 2026 22:16:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 15 May 2026 22:16:57 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Fri, 15 May 2026 22:16:57 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.windows-amd64.exe
# Fri, 15 May 2026 22:16:58 GMT
ENV DOCKER_BUILDX_SHA256=96a10e259fa1380e7bbf9a3cb04872f201a6e7e331ddeeec8d3e38aa2650ddc5
# Fri, 15 May 2026 22:17:07 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 15 May 2026 22:17:08 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Fri, 15 May 2026 22:17:08 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-windows-x86_64.exe
# Fri, 15 May 2026 22:17:09 GMT
ENV DOCKER_COMPOSE_SHA256=5e6d72612b3165be9fea4ae889435fec76979a9779b6f62f4efee99dd5f41ea1
# Fri, 15 May 2026 22:17:16 GMT
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
	-	`sha256:5961f3afdef68ce25fa592066416467d81416df4b1af2537087f1c9150afb728`  
		Last Modified: Fri, 15 May 2026 22:17:25 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae47499b6a77bf67c8fc4c6163dd490f816d5ea9168dfad57664888a82963cd`  
		Last Modified: Fri, 15 May 2026 22:17:25 GMT  
		Size: 506.6 KB (506623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1a50c6ae3a4766042c073c45ffd8a1c5d67595c9c560f65c76492d18a12fd50`  
		Last Modified: Fri, 15 May 2026 22:17:24 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:756530867ead10020116e1f2f106664f6fed6cae2160122fc6ec372b43fd678b`  
		Last Modified: Fri, 15 May 2026 22:17:24 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203d6d943b8fa9b8934a5ce05bf2893265e234366a62bf9ea3a09f77d5608167`  
		Last Modified: Fri, 15 May 2026 22:17:26 GMT  
		Size: 20.2 MB (20232134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f38228e51f50d7a28325477b370bd57476f2a6883a023e98c0d628bc22295ad4`  
		Last Modified: Fri, 15 May 2026 22:17:22 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f7fe5a6a8d2169e19d30f03057f1cf4e3dfa71a14a9e3e2572a95d5246c205`  
		Last Modified: Fri, 15 May 2026 22:17:22 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa5b9407c6ba09fc25979a724f032914bee3ded478b4366b26a09de96ef0c80`  
		Last Modified: Fri, 15 May 2026 22:17:22 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60bb62b675b679633b1a24e24b203fa8ed15d941f3bbb283bae34df7d68c50af`  
		Last Modified: Fri, 15 May 2026 22:17:24 GMT  
		Size: 23.9 MB (23901135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8874726604cb50cc54f506879180a624b7e0fc0e3ad5a8a7063d89505fd60ea`  
		Last Modified: Fri, 15 May 2026 22:17:20 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c7b4c5d7c92d0e67fbdf7582c6455934c8b5f3b3a8c849173931adad0837ca3`  
		Last Modified: Fri, 15 May 2026 22:17:20 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efe6f324d4756f3cd5de0642c06bbc7c60c070aa7a512c8682d7e2232291ae8b`  
		Last Modified: Fri, 15 May 2026 22:17:20 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:487382c6166366ea2b9acbadbf146f8443b6a756bfb7678718eb9c7383bc4a2c`  
		Last Modified: Fri, 15 May 2026 22:17:22 GMT  
		Size: 11.9 MB (11926255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:d385e3828e8366b07bd0af1a4b025c4feb365a506fedb8e307acaae417e63f72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32860; amd64

### `docker:windowsservercore-ltsc2025` - windows version 10.0.26100.32860; amd64

```console
$ docker pull docker@sha256:e4420a2945552c16d362b8472d0182a0ec134ce320f2233ec15e93015e599e8f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2262478653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90d0a0d1bad4f84f1fbcaf6c1e419ce3a0952a03ed6d4582f9767303292ca6c6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 10 May 2026 10:08:54 GMT
RUN Install update 10.0.26100.32860
# Fri, 15 May 2026 22:15:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 15 May 2026 22:16:21 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 15 May 2026 22:16:22 GMT
ENV DOCKER_VERSION=29.5.0
# Fri, 15 May 2026 22:16:23 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.5.0.zip
# Fri, 15 May 2026 22:16:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 15 May 2026 22:16:39 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Fri, 15 May 2026 22:16:40 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.windows-amd64.exe
# Fri, 15 May 2026 22:16:40 GMT
ENV DOCKER_BUILDX_SHA256=96a10e259fa1380e7bbf9a3cb04872f201a6e7e331ddeeec8d3e38aa2650ddc5
# Fri, 15 May 2026 22:16:50 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 15 May 2026 22:16:51 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Fri, 15 May 2026 22:16:51 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-windows-x86_64.exe
# Fri, 15 May 2026 22:16:52 GMT
ENV DOCKER_COMPOSE_SHA256=5e6d72612b3165be9fea4ae889435fec76979a9779b6f62f4efee99dd5f41ea1
# Fri, 15 May 2026 22:17:01 GMT
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
	-	`sha256:74b535a51fd23dbc5005aa72b61e95ad333b54b6b5276fd600c8f26dc1ec6379`  
		Last Modified: Fri, 15 May 2026 22:17:10 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f1111f6cb7254129e7ea39ba28883376409a104ffda0b87a45a420ceee27fcb`  
		Last Modified: Fri, 15 May 2026 22:17:10 GMT  
		Size: 392.8 KB (392802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2db17ecf93e3efdbccd835fd5d408afb7a3351f7597a48a1ad636c01794ebe04`  
		Last Modified: Fri, 15 May 2026 22:17:09 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c83f256bcd38582b57bb91e485a2d85240d5f2ae45b27c9afa7a9a5f44ebed73`  
		Last Modified: Fri, 15 May 2026 22:17:09 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cdc10f672c38740ac0512c480a10fe4b0dc1658659e00513da102771c2e3e40`  
		Last Modified: Fri, 15 May 2026 22:17:11 GMT  
		Size: 20.3 MB (20260443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e77a9dc340d0bdbccbce6b57c4d89cad2a1db92d89f7c2649002da080b5334bd`  
		Last Modified: Fri, 15 May 2026 22:17:07 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2309766ee1a21f57c947e3ef48cf4592eb1c12fb99926f92dc710c73dff7b930`  
		Last Modified: Fri, 15 May 2026 22:17:07 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9e8a3c0bbacac0c1695cff5c5e5eeefe513850e0a04322d018dfc23f9317a07`  
		Last Modified: Fri, 15 May 2026 22:17:07 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2562224ef98ba779eb91088241d392cb2a71abbc685b008022439f669f7686d6`  
		Last Modified: Fri, 15 May 2026 22:17:09 GMT  
		Size: 23.9 MB (23920245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6af350faa47b96f1766ca0debecbe39139716c8b55ae988b2528535eed60cca`  
		Last Modified: Fri, 15 May 2026 22:17:05 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:780002467e4bb1a15f8748b2ea889bc85483b2d7ddb96b528e3b32c982692e19`  
		Last Modified: Fri, 15 May 2026 22:17:05 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47e3ee62773736f785dc51e4bc1a7e48595fe0afed17ab1d89154d1e06595d11`  
		Last Modified: Fri, 15 May 2026 22:17:05 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d076a230450a0b438ed3c7d1ee23904031d66dddd7e9ee8ac765637eb942ff8`  
		Last Modified: Fri, 15 May 2026 22:17:07 GMT  
		Size: 12.0 MB (11951730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
