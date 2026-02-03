<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `docker`

-	[`docker:29`](#docker29)
-	[`docker:29-cli`](#docker29-cli)
-	[`docker:29-dind`](#docker29-dind)
-	[`docker:29-dind-rootless`](#docker29-dind-rootless)
-	[`docker:29-windowsservercore`](#docker29-windowsservercore)
-	[`docker:29-windowsservercore-ltsc2022`](#docker29-windowsservercore-ltsc2022)
-	[`docker:29-windowsservercore-ltsc2025`](#docker29-windowsservercore-ltsc2025)
-	[`docker:29.2`](#docker292)
-	[`docker:29.2-cli`](#docker292-cli)
-	[`docker:29.2-dind`](#docker292-dind)
-	[`docker:29.2-dind-rootless`](#docker292-dind-rootless)
-	[`docker:29.2-windowsservercore`](#docker292-windowsservercore)
-	[`docker:29.2-windowsservercore-ltsc2022`](#docker292-windowsservercore-ltsc2022)
-	[`docker:29.2-windowsservercore-ltsc2025`](#docker292-windowsservercore-ltsc2025)
-	[`docker:29.2.1`](#docker2921)
-	[`docker:29.2.1-alpine3.23`](#docker2921-alpine323)
-	[`docker:29.2.1-cli`](#docker2921-cli)
-	[`docker:29.2.1-cli-alpine3.23`](#docker2921-cli-alpine323)
-	[`docker:29.2.1-dind`](#docker2921-dind)
-	[`docker:29.2.1-dind-alpine3.23`](#docker2921-dind-alpine323)
-	[`docker:29.2.1-dind-rootless`](#docker2921-dind-rootless)
-	[`docker:29.2.1-windowsservercore`](#docker2921-windowsservercore)
-	[`docker:29.2.1-windowsservercore-ltsc2022`](#docker2921-windowsservercore-ltsc2022)
-	[`docker:29.2.1-windowsservercore-ltsc2025`](#docker2921-windowsservercore-ltsc2025)
-	[`docker:cli`](#dockercli)
-	[`docker:dind`](#dockerdind)
-	[`docker:dind-rootless`](#dockerdind-rootless)
-	[`docker:latest`](#dockerlatest)
-	[`docker:windowsservercore`](#dockerwindowsservercore)
-	[`docker:windowsservercore-ltsc2022`](#dockerwindowsservercore-ltsc2022)
-	[`docker:windowsservercore-ltsc2025`](#dockerwindowsservercore-ltsc2025)

## `docker:29`

```console
$ docker pull docker@sha256:a284d31e4db9a9916fd9be44380263eaeafedf0e3048a859f978922b5a0c16fc
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
$ docker pull docker@sha256:99aa88f75d8d401c30e395db1d2e679a89ff0be9b415f020b8e2383c517e1fda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.8 MB (143799092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ca04087ca24aa6deade38370d033555d14dacd022c6a5d275f038b89eaf131`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:15:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:15:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:15:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:15:17 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:15:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:15:17 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:15:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:15:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:15:19 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:15:19 GMT
CMD ["sh"]
# Wed, 28 Jan 2026 03:58:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 Jan 2026 03:58:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 Jan 2026 03:58:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 Jan 2026 03:58:45 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
VOLUME [/var/lib/docker]
# Wed, 28 Jan 2026 03:58:45 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 Jan 2026 03:58:45 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 Jan 2026 03:58:45 GMT
CMD []
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03ce8e2700f1129dc15f38a5e1e7d27cdd2b98175c4d9ac08dc5646c3c35ba4`  
		Last Modified: Wed, 28 Jan 2026 02:15:26 GMT  
		Size: 8.4 MB (8399638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dabc00febb6a9a0d9954ef0b62272b11dabac7697dd7a0f94f9a96e241fbfd2`  
		Last Modified: Wed, 28 Jan 2026 02:15:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9408125f9d0c694cc95efc06409f73e6d6907c853a7f861c85b36824fb02ed25`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 18.8 MB (18774054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1765bbbd236eff12d3ecffaab470c2a8ade7f1432cbf0f1efe2f520cb9d74bfc`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 28.3 MB (28308902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d4f1a3f89cb924cc72cf031843e7490b98f39a276e6628c0ef444a871ff92f`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 10.8 MB (10799762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ca730a0591b75f8b903f70ff08c4b2959f397bd8775ba1a873cbb344b15c1a0`  
		Last Modified: Wed, 28 Jan 2026 02:15:28 GMT  
		Size: 533.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc93a580b636b3173550ee5a31a23ae95eb17558288345a26091285a5f477d5`  
		Last Modified: Wed, 28 Jan 2026 02:15:28 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9745309fb9885c647e35e9d55ab83308f9c212460ad5f9b73c2e518179059b72`  
		Last Modified: Wed, 28 Jan 2026 02:15:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:effa5c3a383e3a584de2fe9ef352f8fcde727e8db088492f0c8e49fc27f7abaa`  
		Last Modified: Wed, 28 Jan 2026 03:58:56 GMT  
		Size: 6.9 MB (6934734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a8f8addf621601263b2bfea9efe7ffac5903b85bfe7b9f628f7a2ff6bd4fce`  
		Last Modified: Wed, 28 Jan 2026 03:58:55 GMT  
		Size: 92.5 KB (92460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:396bcb1ae646a1eb234538a6bf406490001b6067e5626f4858b3d3ab115a1338`  
		Last Modified: Wed, 28 Jan 2026 03:58:56 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636ece6788bea2909cc3a17231a1a4827c4db266c991df7770a909ecdb8d3fd0`  
		Last Modified: Wed, 28 Jan 2026 03:58:57 GMT  
		Size: 66.6 MB (66619579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb2987d59bbd2b711c1759725d9ccc5891b03def0602234c4f49beb1e5c2be1`  
		Last Modified: Wed, 28 Jan 2026 03:58:57 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ac6a5de045400bc7b163e70c2cd9429f6202144cb50ed4b85688aded44f58e`  
		Last Modified: Wed, 28 Jan 2026 03:58:57 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:2d2c0973782cdccc69752fb841755627c37546ebbf2f68f0bf070bf51d23ec60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0784b32a62dac2ebed2ad0ae726d2901f105b39654d58a2d2d351b4eaea7d818`

```dockerfile
```

-	Layers:
	-	`sha256:161b2e45f0098aead317dd0674b614a4e1252835a147f30b88ddc0667bf7ba93`  
		Last Modified: Wed, 28 Jan 2026 03:58:55 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29` - linux; arm variant v6

```console
$ docker pull docker@sha256:70dcad0b903a121c11d71a23834267a49327cd21053d8a2a83529cf94a2d9fbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135630532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:438bd2c6733062a94188c3067ba6118e7dda4560c7d7eb98ecec81192d5273b2`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:19:28 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:19:29 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:19:29 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:19:32 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:19:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:19:32 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:19:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:19:34 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:19:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:19:36 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:19:36 GMT
CMD ["sh"]
# Wed, 28 Jan 2026 03:49:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 Jan 2026 03:49:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 Jan 2026 03:49:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 03:49:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 Jan 2026 03:49:21 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 Jan 2026 03:49:21 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 Jan 2026 03:49:21 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:49:21 GMT
VOLUME [/var/lib/docker]
# Wed, 28 Jan 2026 03:49:21 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 Jan 2026 03:49:21 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 Jan 2026 03:49:21 GMT
CMD []
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08efb619161971b8dbf3d2d18d22c25f3caf7baea4b18537b77a961fee285e4d`  
		Last Modified: Wed, 28 Jan 2026 02:19:43 GMT  
		Size: 8.3 MB (8301019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11eae5034a08f196af9949aec8c0d0a5c776062160fbfa6839f4e91eb25c523`  
		Last Modified: Wed, 28 Jan 2026 02:19:42 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b811dd811e1e6a5a185faf36f1f9dd7bd483290fc51d98ccb7f5014b5bd19ab`  
		Last Modified: Wed, 28 Jan 2026 02:19:43 GMT  
		Size: 17.6 MB (17576540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395a6e19e8b08ce81dbf6939f7000c5eaaa78657497cffd3559c4d3586ad6f25`  
		Last Modified: Wed, 28 Jan 2026 02:19:44 GMT  
		Size: 26.6 MB (26570467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b3f84acb2b12fc7c649c003ff8e9348dabfff644a17daad4b02eef0bd9b40b6`  
		Last Modified: Wed, 28 Jan 2026 02:19:44 GMT  
		Size: 10.2 MB (10213042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746007c626ec304c1dfcf1e9084f31b26345a6079f9efe6f265b8fa508abf11a`  
		Last Modified: Wed, 28 Jan 2026 02:19:44 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f144bc5ce89728429c7674f4da3e2efbf3439669eae61e270d13a77809b4b9b7`  
		Last Modified: Wed, 28 Jan 2026 02:19:45 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b078b00f266ba4e03e79da886e567e61c21f493be073a7001f1e3db1345ccf57`  
		Last Modified: Wed, 28 Jan 2026 02:19:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6f4b2cf4256d701c8e551ce6b913b60516e7a6812dd2a6b150737145528fdf`  
		Last Modified: Wed, 28 Jan 2026 03:49:31 GMT  
		Size: 7.3 MB (7271609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b290e764c28e19f2f21aa7790d801cc6056a53cd51c8fb1bb6faf2e2346d4145`  
		Last Modified: Wed, 28 Jan 2026 03:49:30 GMT  
		Size: 91.8 KB (91775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:894eda0b2167abb0c583bbf993071a8d219941e2dd3bc2fcd1f8bfd8ca024a34`  
		Last Modified: Wed, 28 Jan 2026 03:49:30 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661a756971591996ae71af31b4d76fd40c1ba5140d25d52487a63a2ce33123b3`  
		Last Modified: Wed, 28 Jan 2026 03:49:32 GMT  
		Size: 62.0 MB (62028111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0fea802a7e013543afeb57c94b421ff42c6cc94e875a7a48079633d5b32cf0`  
		Last Modified: Wed, 28 Jan 2026 03:49:31 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89262e7e7a4c52344f56768909e409e4d52e23b7e5f872f34c6f8f05f600ced1`  
		Last Modified: Wed, 28 Jan 2026 03:49:32 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:77efd8773fd21feb58c996858580a066f8336af75ce15a65d1e94fbfc662939f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8937de610607274348941cf30b97eee5b16a47a2a3e355daae965571f78e1b8e`

```dockerfile
```

-	Layers:
	-	`sha256:b2c9967356bfd5048f745045eb7a61d4c51f3b8a396da52f925736b964896609`  
		Last Modified: Wed, 28 Jan 2026 03:49:30 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29` - linux; arm variant v7

```console
$ docker pull docker@sha256:136f2e805834a4247060b8060063ba782a2fdce6083a3cb47d02e83936623504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133715469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a4604f36042cbaaba3fd792ec4e26bfaf62d2d45b48d38a8697760ddf3306fa`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:19:33 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:19:33 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:19:34 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:19:37 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:19:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:19:37 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:19:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:19:39 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:19:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:19:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:19:41 GMT
CMD ["sh"]
# Wed, 28 Jan 2026 03:51:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 Jan 2026 03:51:44 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 Jan 2026 03:51:44 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 03:51:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 Jan 2026 03:51:47 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 Jan 2026 03:51:47 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 Jan 2026 03:51:47 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:51:47 GMT
VOLUME [/var/lib/docker]
# Wed, 28 Jan 2026 03:51:47 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 Jan 2026 03:51:47 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 Jan 2026 03:51:47 GMT
CMD []
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef74ac3c65992e7acddcc2a2c02498d51d5fda8b771538e5411d2d5f3a3e9eec`  
		Last Modified: Wed, 28 Jan 2026 02:19:47 GMT  
		Size: 7.6 MB (7597810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01925faabefdbedf8efebb820b152e94fb287b72138d282a76557993132623ca`  
		Last Modified: Wed, 28 Jan 2026 02:19:47 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ad13ec2588fba164870da3d93ba8b5ad34e242b5bc6fb7b5df1bd055e194e0`  
		Last Modified: Wed, 28 Jan 2026 02:19:48 GMT  
		Size: 17.6 MB (17566458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc3d6d20d26654203dbb33aecb823850102a06ee1d8826eeea313f51053947d`  
		Last Modified: Wed, 28 Jan 2026 02:19:48 GMT  
		Size: 26.5 MB (26544669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309b43a06105801e72a4057c9a98aa39f845292f118ed5364be6f2c58fff6fb2`  
		Last Modified: Wed, 28 Jan 2026 02:19:48 GMT  
		Size: 10.2 MB (10198593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c018df83e09983e9c86c614e37738e0c9913c07f571d99ca7464a8eead3114`  
		Last Modified: Wed, 28 Jan 2026 02:19:49 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff08fbe96bdc955d67587b7154a9e64b5fd0933ad18112a10502a2d2ee351334`  
		Last Modified: Wed, 28 Jan 2026 02:19:49 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82766871530b6d5c5faaefb052706696dbc1f4936a761d57fe77b41476c57e81`  
		Last Modified: Wed, 28 Jan 2026 02:19:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966fa3b3930581a719871ad9cc50569b5b949938c666c5f604128567586dcc98`  
		Last Modified: Wed, 28 Jan 2026 03:51:58 GMT  
		Size: 6.6 MB (6572989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8288f87d3ec8e6d2c73fad07643b43f2c5a333b046f21c81531e877d6eaf19d4`  
		Last Modified: Wed, 28 Jan 2026 03:51:58 GMT  
		Size: 88.1 KB (88136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd5922158e4b006788c6366971c7c91cc1404b01a100da81d4c9a0477a74027`  
		Last Modified: Wed, 28 Jan 2026 03:51:58 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842a3b5326d8c1c6b696edd5624246ed13391ce31743771eb92561f224c0e672`  
		Last Modified: Wed, 28 Jan 2026 03:52:00 GMT  
		Size: 61.9 MB (61856931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f666916210054b0fd5f72affa9ac152fa7c42d927442f2dd309d354e89b9277`  
		Last Modified: Wed, 28 Jan 2026 03:51:59 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cf19ee261d3469335adb02771df03de4d7bd57f3cb5c06bb5841ae7b93697c`  
		Last Modified: Wed, 28 Jan 2026 03:51:59 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:8457bbc8972fac13450e367c97a9a1b851c44540331c9f631abe6ecc6da554fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d30df9382a2c15c97b7086f993412c3a0f44e8ed81f835508748d782eabe5345`

```dockerfile
```

-	Layers:
	-	`sha256:0a1c8b9290fc1e34c2f218c7730ca8fc83fc55704982e288265ea392b6f0447c`  
		Last Modified: Wed, 28 Jan 2026 03:51:58 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:2cd37b1da26b3d7bdae2014ffafb6543a3c40f32973395bdf6e402afc6818e38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.2 MB (133249301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a287877d76e510dc36d4294bef0d4540628445c54cbf477d32ad4aef68e7bb0a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:15:20 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:15:20 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:15:20 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:15:22 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:15:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:15:22 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:15:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:15:23 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:15:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:15:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:15:24 GMT
CMD ["sh"]
# Wed, 28 Jan 2026 04:19:44 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 Jan 2026 04:19:44 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 Jan 2026 04:19:45 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 04:19:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 Jan 2026 04:19:48 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 Jan 2026 04:19:48 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 Jan 2026 04:19:48 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 04:19:48 GMT
VOLUME [/var/lib/docker]
# Wed, 28 Jan 2026 04:19:48 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 Jan 2026 04:19:48 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 Jan 2026 04:19:48 GMT
CMD []
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23cd2c872bdff3a89f69a977eea6049f005ee667e33468764b0584c9a8959fe3`  
		Last Modified: Wed, 28 Jan 2026 02:15:31 GMT  
		Size: 8.5 MB (8453525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a2f891a573bd6b7ff30782766b7564cfd2718e91c2399081bdf0ffb44fabba`  
		Last Modified: Wed, 28 Jan 2026 02:15:30 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f26d33b7e75cf64b24043a967d4288b682c0eba3866ed27897136240d3f4cbe`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 17.3 MB (17349909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fadf59f99eaf4a5457883e92f5eb0e9f05304f32b91ff429c77b5d12c399d17`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 25.5 MB (25539742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bbb75472d83a88fcf93366d31a9685491eaee5051b271d7e9822962477745c`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 10.0 MB (9954517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982182610648dbb0778b184ecff3e692201a2114ba00657d6fd977582e60c802`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c47f152455dabd15e5d73f9f555e031f1bf91be0a42bb7899543ca32f4be842`  
		Last Modified: Wed, 28 Jan 2026 02:15:34 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d60b69639960857109359648f1dd0dd6cb3d2cce9bdd6b1a594fd99159bf8f`  
		Last Modified: Wed, 28 Jan 2026 02:15:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf3426000179b3492ca41ec23019609bae7bd020884ba682b730f4920dcdadd`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 7.2 MB (7213335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d0c859c41e3ca1cc276016f6151a0a02e77f672f849df7d283d4657b2fd464`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 101.3 KB (101289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6748b522881f24eb97f2eed26e32bdb49ae5819b2477eae3a4976874142ff758`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:407dff81deac15d5750c410b3b45d2888514fd7173fad465cdb860a9e18a068c`  
		Last Modified: Wed, 28 Jan 2026 04:19:59 GMT  
		Size: 60.4 MB (60431745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae84a81436627202044f15c8bfbb21c37acd9371efb16eac52fa88d19fd035c`  
		Last Modified: Wed, 28 Jan 2026 04:19:58 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66e9c5f6367f5ce3bcd7921fbcd7ecdee44c87e2b3fb4e91c0953fdefb902bb`  
		Last Modified: Wed, 28 Jan 2026 04:19:58 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:76d7445bd6915a9080071a3680a3a2dd3bfb0697d214d61d429692ed178b2519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee53cf6ac36a1613efdfec96533f5b66f1bac362f162eeed2703924705574c2d`

```dockerfile
```

-	Layers:
	-	`sha256:51f7535efd28fb94f257372f96380d2a49634a8b4664d35a295a7201ee67d470`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-cli`

```console
$ docker pull docker@sha256:1d6d751f1d68d1a5142c23c730ef5ecc976a8e050fa08c3cdb09f7e2e54a4439
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
$ docker pull docker@sha256:0c04277b44d1d448d40238faa142c2edf21d4a90dc0d61486c32056bbf11572a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70148082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90fa388e81d5f66d9d9ee840c5375a0801629a980c3d9657463257b2c863f324`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:25:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:25:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:25:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:25:58 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:25:58 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:25:58 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:25:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:25:59 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:26:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:26:00 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:26:00 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ffbc9e9d61a3a427749366541c9e55c1440658b296b288726282a7e3a200f3`  
		Last Modified: Tue, 03 Feb 2026 17:26:07 GMT  
		Size: 8.4 MB (8399657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9130c567f6fc24a30ebaa5979b9c6700d6c174c3a52a1e753c42621bfb1a32d9`  
		Last Modified: Tue, 03 Feb 2026 17:26:07 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b75aa627f4cd980f8d8c3e7be1834e54e286a6499508105b6f72c4a373c7a6e`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 18.8 MB (18773130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c979ccecd955439750b7f01789bf427e4c8d60acbf2b4a12100ff3173aea9b`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 28.3 MB (28311545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217f84c60501e3b3fb548f194b2861bfcb2a70aa12a9abe9b0d4ee342d75a7b5`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 10.8 MB (10799774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bf8952411ee385ba36420d9b6bdcc36594a8be8bdace8fe62d7d97f81322411`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f757cc0a441eaf36dbebd029cb42e59a8c463fb4ea19e2ec6bf557d5a981dc2`  
		Last Modified: Tue, 03 Feb 2026 17:26:09 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7358b0dc3398fd6f4c32455892c6ab6fbc099f1a8e62df04445dec7663a095`  
		Last Modified: Tue, 03 Feb 2026 17:26:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:c1620c41ed6e739f033f9e98a5bba1cb95e1ea6a093197beb216823c8c93ce72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c5f4666aeb7f994fb855d5fb4b289608e198a0a0b59b25161f28433aeb36364`

```dockerfile
```

-	Layers:
	-	`sha256:19b63918903a6b77f5af72e60038c44df3a84e5a4563b3db3d54ef79567b8195`  
		Last Modified: Tue, 03 Feb 2026 17:26:07 GMT  
		Size: 38.1 KB (38056 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:cf09d93cea103396a11b1b12c36c15b6b93d367c0c80cce733f00214c71c92e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66235505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4367f8d4a4b3fc3d463d69bca54b902b58d4792ccf8967224e2ec3dd7aa4afb4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:25:26 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:25:26 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:25:26 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:25:31 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:25:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:25:31 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:25:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:25:33 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:25:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:25:35 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:25:35 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ed7f28a4b26e2736ceb8045d972a5f166880f3b93b1ce13d7cb7710819f7c0`  
		Last Modified: Tue, 03 Feb 2026 17:25:42 GMT  
		Size: 8.3 MB (8300971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59982a56599ba445b45c1ff95a9bf2efe937cb3105d8107453c37e42aa96ab06`  
		Last Modified: Tue, 03 Feb 2026 17:25:41 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627db20a49a4f2be2d19fe161406f293a8b8804c985028e04c1cd95f0c40d96e`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 17.6 MB (17575014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acd42cfefd8cbfbea51ccc805027f78eefae1b3ad5cb91c207ebf9578a6a855`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 26.6 MB (26574500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac22564cea85937e49534e5ef435197d6c83fb053c5aa91ffddb70acae2ff81`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 10.2 MB (10213046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8735f9cb2ee8a9b930cd6b2bf3885083108a83a3707f302210e9bb0a138c15ec`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf43e9302aee150c8b25e6f5c53d2eb8642dd7db31500f8f7e980a6639b3d75`  
		Last Modified: Tue, 03 Feb 2026 17:25:44 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52ca294aaca561ae37709af7d9406792302f6ac4cfe16d2068ba04176c0aa2a`  
		Last Modified: Tue, 03 Feb 2026 17:25:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:fbcdf3246eea54b7103bc19f384cd3f454538bd499af80a1566455c68e652971
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f63de4e3179da9faef11522e19444ae1387215588371c787a0b6852c464dcd77`

```dockerfile
```

-	Layers:
	-	`sha256:97d51d656e276dcee240923733068124918a337234be2ffb56edcdb70a458855`  
		Last Modified: Tue, 03 Feb 2026 17:25:41 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:ba03aff6e89a96861c91cbe97855b49f31e816c782afaa8225043cb76f7ae372
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65192844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:985b778ba8e60d8ceaa28fed60316b7c31c5ff3e18d6afb37619d388a8da92b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:26:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:26:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:26:11 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:26:15 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:26:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:26:15 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:26:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:26:19 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:26:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:26:20 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:26:20 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb5af91453d1293030fbe90db4c6166609f99510d3fcec579be00a21249cbf2`  
		Last Modified: Tue, 03 Feb 2026 17:26:28 GMT  
		Size: 7.6 MB (7597849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7fbe9447e7591ff3854f01ba9776952a93a9c4f22447067e6a9e1c3f93c760`  
		Last Modified: Tue, 03 Feb 2026 17:26:27 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ffc7844b3d362e6b692567d2587e4fd19b348dff44182f52019fdefe7ab344`  
		Last Modified: Tue, 03 Feb 2026 17:26:28 GMT  
		Size: 17.6 MB (17566404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9111fb63645fb502831d395247748514cc38c89a036c0c80ac0d68172af396`  
		Last Modified: Tue, 03 Feb 2026 17:26:29 GMT  
		Size: 26.5 MB (26546121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17318896bc84227a623de0b09b1c19d9ba46473321e3c6ef037516d813f8da1`  
		Last Modified: Tue, 03 Feb 2026 17:26:29 GMT  
		Size: 10.2 MB (10198592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f58cddeebb4c56cedfe3c4d3406be79ac683f61f8d149db919627222cd847dae`  
		Last Modified: Tue, 03 Feb 2026 17:26:29 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45cca7f5e3f5fc71d61ff7160fba4b5af52d1d5c1376ef27109056ee0bd35891`  
		Last Modified: Tue, 03 Feb 2026 17:26:30 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68671e7ea5f72eebefa27db844dfc891bba0667adb87fda60be5a0a78a9e0af3`  
		Last Modified: Tue, 03 Feb 2026 17:26:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:725c7ed6fedc0c78099cca969de9d894742913605a635c1d1ae732d243e1f9d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a2b7afca7a73cadfc121038f2cb596614c4eff15299359ccc0fe5915a333dfa`

```dockerfile
```

-	Layers:
	-	`sha256:9fd463f063b0e999eee86b191492b64c48293c00436e4b777db697007872a8d6`  
		Last Modified: Tue, 03 Feb 2026 17:26:27 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:2bef500bc870e9a4eef5ac67cf6fef451c072f77b7351b207d74a3463c80e455
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.5 MB (65497196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cffbe99c0e2eadb1b2dd8830a3ecddedf95c08183d497287cb048586c0c94905`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:26:35 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:26:35 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:26:35 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:26:37 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:26:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:26:37 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:26:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:26:38 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:26:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:26:39 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:26:39 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42a77f5fc93e1d6c642b2eb20bac67ddedc3fa614973ecad5d2425aa529cc7f`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 8.5 MB (8453512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9817403955ea5ea2eedc37cde61397fd369d7b07e3863286754b4989d443759a`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d23c75ff3415b6637326f398bd112a7ec4373805d39318b94b65c8ff6ce7538`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 17.3 MB (17349111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfca817951310f1a68cb06e3fe0f27540e7d76c61b144cbbb1ebaa04308c8233`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 25.5 MB (25540815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7af456c729c76507dbf99635546e893dd549241c3157a2a655f1a7472544d6`  
		Last Modified: Tue, 03 Feb 2026 17:26:47 GMT  
		Size: 10.0 MB (9954516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72242c4fb87c9ebb62312863874911bfe531f06775fe6a90aa5c937db6274442`  
		Last Modified: Tue, 03 Feb 2026 17:26:47 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e91b41b56d8ea2c6e69d6ed8a929177b21cc4e84b65284dd552f20cda40c3dd`  
		Last Modified: Tue, 03 Feb 2026 17:26:48 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66fa267764c487b75a914eae88e45afb0bdd82be8b4c090d4af5946454d79964`  
		Last Modified: Tue, 03 Feb 2026 17:26:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:22956d1b0f85ed3aaf3fbd162a232fd08241684704dc328c469298a7a60f924e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa0c6c28d5d6436cdecdceb1ee544bccb64c7a75c45b13de36e354116226cab3`

```dockerfile
```

-	Layers:
	-	`sha256:0c689b61e422b3962e7df2e52b56054a4e453d576da33fd3b1d6f7dca26d06b6`  
		Last Modified: Tue, 03 Feb 2026 17:26:45 GMT  
		Size: 38.3 KB (38258 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-dind`

```console
$ docker pull docker@sha256:a284d31e4db9a9916fd9be44380263eaeafedf0e3048a859f978922b5a0c16fc
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
$ docker pull docker@sha256:99aa88f75d8d401c30e395db1d2e679a89ff0be9b415f020b8e2383c517e1fda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.8 MB (143799092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ca04087ca24aa6deade38370d033555d14dacd022c6a5d275f038b89eaf131`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:15:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:15:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:15:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:15:17 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:15:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:15:17 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:15:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:15:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:15:19 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:15:19 GMT
CMD ["sh"]
# Wed, 28 Jan 2026 03:58:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 Jan 2026 03:58:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 Jan 2026 03:58:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 Jan 2026 03:58:45 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
VOLUME [/var/lib/docker]
# Wed, 28 Jan 2026 03:58:45 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 Jan 2026 03:58:45 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 Jan 2026 03:58:45 GMT
CMD []
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03ce8e2700f1129dc15f38a5e1e7d27cdd2b98175c4d9ac08dc5646c3c35ba4`  
		Last Modified: Wed, 28 Jan 2026 02:15:26 GMT  
		Size: 8.4 MB (8399638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dabc00febb6a9a0d9954ef0b62272b11dabac7697dd7a0f94f9a96e241fbfd2`  
		Last Modified: Wed, 28 Jan 2026 02:15:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9408125f9d0c694cc95efc06409f73e6d6907c853a7f861c85b36824fb02ed25`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 18.8 MB (18774054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1765bbbd236eff12d3ecffaab470c2a8ade7f1432cbf0f1efe2f520cb9d74bfc`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 28.3 MB (28308902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d4f1a3f89cb924cc72cf031843e7490b98f39a276e6628c0ef444a871ff92f`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 10.8 MB (10799762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ca730a0591b75f8b903f70ff08c4b2959f397bd8775ba1a873cbb344b15c1a0`  
		Last Modified: Wed, 28 Jan 2026 02:15:28 GMT  
		Size: 533.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc93a580b636b3173550ee5a31a23ae95eb17558288345a26091285a5f477d5`  
		Last Modified: Wed, 28 Jan 2026 02:15:28 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9745309fb9885c647e35e9d55ab83308f9c212460ad5f9b73c2e518179059b72`  
		Last Modified: Wed, 28 Jan 2026 02:15:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:effa5c3a383e3a584de2fe9ef352f8fcde727e8db088492f0c8e49fc27f7abaa`  
		Last Modified: Wed, 28 Jan 2026 03:58:56 GMT  
		Size: 6.9 MB (6934734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a8f8addf621601263b2bfea9efe7ffac5903b85bfe7b9f628f7a2ff6bd4fce`  
		Last Modified: Wed, 28 Jan 2026 03:58:55 GMT  
		Size: 92.5 KB (92460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:396bcb1ae646a1eb234538a6bf406490001b6067e5626f4858b3d3ab115a1338`  
		Last Modified: Wed, 28 Jan 2026 03:58:56 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636ece6788bea2909cc3a17231a1a4827c4db266c991df7770a909ecdb8d3fd0`  
		Last Modified: Wed, 28 Jan 2026 03:58:57 GMT  
		Size: 66.6 MB (66619579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb2987d59bbd2b711c1759725d9ccc5891b03def0602234c4f49beb1e5c2be1`  
		Last Modified: Wed, 28 Jan 2026 03:58:57 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ac6a5de045400bc7b163e70c2cd9429f6202144cb50ed4b85688aded44f58e`  
		Last Modified: Wed, 28 Jan 2026 03:58:57 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:2d2c0973782cdccc69752fb841755627c37546ebbf2f68f0bf070bf51d23ec60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0784b32a62dac2ebed2ad0ae726d2901f105b39654d58a2d2d351b4eaea7d818`

```dockerfile
```

-	Layers:
	-	`sha256:161b2e45f0098aead317dd0674b614a4e1252835a147f30b88ddc0667bf7ba93`  
		Last Modified: Wed, 28 Jan 2026 03:58:55 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:70dcad0b903a121c11d71a23834267a49327cd21053d8a2a83529cf94a2d9fbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135630532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:438bd2c6733062a94188c3067ba6118e7dda4560c7d7eb98ecec81192d5273b2`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:19:28 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:19:29 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:19:29 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:19:32 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:19:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:19:32 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:19:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:19:34 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:19:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:19:36 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:19:36 GMT
CMD ["sh"]
# Wed, 28 Jan 2026 03:49:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 Jan 2026 03:49:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 Jan 2026 03:49:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 03:49:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 Jan 2026 03:49:21 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 Jan 2026 03:49:21 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 Jan 2026 03:49:21 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:49:21 GMT
VOLUME [/var/lib/docker]
# Wed, 28 Jan 2026 03:49:21 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 Jan 2026 03:49:21 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 Jan 2026 03:49:21 GMT
CMD []
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08efb619161971b8dbf3d2d18d22c25f3caf7baea4b18537b77a961fee285e4d`  
		Last Modified: Wed, 28 Jan 2026 02:19:43 GMT  
		Size: 8.3 MB (8301019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11eae5034a08f196af9949aec8c0d0a5c776062160fbfa6839f4e91eb25c523`  
		Last Modified: Wed, 28 Jan 2026 02:19:42 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b811dd811e1e6a5a185faf36f1f9dd7bd483290fc51d98ccb7f5014b5bd19ab`  
		Last Modified: Wed, 28 Jan 2026 02:19:43 GMT  
		Size: 17.6 MB (17576540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395a6e19e8b08ce81dbf6939f7000c5eaaa78657497cffd3559c4d3586ad6f25`  
		Last Modified: Wed, 28 Jan 2026 02:19:44 GMT  
		Size: 26.6 MB (26570467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b3f84acb2b12fc7c649c003ff8e9348dabfff644a17daad4b02eef0bd9b40b6`  
		Last Modified: Wed, 28 Jan 2026 02:19:44 GMT  
		Size: 10.2 MB (10213042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746007c626ec304c1dfcf1e9084f31b26345a6079f9efe6f265b8fa508abf11a`  
		Last Modified: Wed, 28 Jan 2026 02:19:44 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f144bc5ce89728429c7674f4da3e2efbf3439669eae61e270d13a77809b4b9b7`  
		Last Modified: Wed, 28 Jan 2026 02:19:45 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b078b00f266ba4e03e79da886e567e61c21f493be073a7001f1e3db1345ccf57`  
		Last Modified: Wed, 28 Jan 2026 02:19:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6f4b2cf4256d701c8e551ce6b913b60516e7a6812dd2a6b150737145528fdf`  
		Last Modified: Wed, 28 Jan 2026 03:49:31 GMT  
		Size: 7.3 MB (7271609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b290e764c28e19f2f21aa7790d801cc6056a53cd51c8fb1bb6faf2e2346d4145`  
		Last Modified: Wed, 28 Jan 2026 03:49:30 GMT  
		Size: 91.8 KB (91775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:894eda0b2167abb0c583bbf993071a8d219941e2dd3bc2fcd1f8bfd8ca024a34`  
		Last Modified: Wed, 28 Jan 2026 03:49:30 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661a756971591996ae71af31b4d76fd40c1ba5140d25d52487a63a2ce33123b3`  
		Last Modified: Wed, 28 Jan 2026 03:49:32 GMT  
		Size: 62.0 MB (62028111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0fea802a7e013543afeb57c94b421ff42c6cc94e875a7a48079633d5b32cf0`  
		Last Modified: Wed, 28 Jan 2026 03:49:31 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89262e7e7a4c52344f56768909e409e4d52e23b7e5f872f34c6f8f05f600ced1`  
		Last Modified: Wed, 28 Jan 2026 03:49:32 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:77efd8773fd21feb58c996858580a066f8336af75ce15a65d1e94fbfc662939f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8937de610607274348941cf30b97eee5b16a47a2a3e355daae965571f78e1b8e`

```dockerfile
```

-	Layers:
	-	`sha256:b2c9967356bfd5048f745045eb7a61d4c51f3b8a396da52f925736b964896609`  
		Last Modified: Wed, 28 Jan 2026 03:49:30 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:136f2e805834a4247060b8060063ba782a2fdce6083a3cb47d02e83936623504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133715469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a4604f36042cbaaba3fd792ec4e26bfaf62d2d45b48d38a8697760ddf3306fa`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:19:33 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:19:33 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:19:34 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:19:37 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:19:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:19:37 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:19:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:19:39 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:19:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:19:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:19:41 GMT
CMD ["sh"]
# Wed, 28 Jan 2026 03:51:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 Jan 2026 03:51:44 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 Jan 2026 03:51:44 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 03:51:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 Jan 2026 03:51:47 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 Jan 2026 03:51:47 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 Jan 2026 03:51:47 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:51:47 GMT
VOLUME [/var/lib/docker]
# Wed, 28 Jan 2026 03:51:47 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 Jan 2026 03:51:47 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 Jan 2026 03:51:47 GMT
CMD []
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef74ac3c65992e7acddcc2a2c02498d51d5fda8b771538e5411d2d5f3a3e9eec`  
		Last Modified: Wed, 28 Jan 2026 02:19:47 GMT  
		Size: 7.6 MB (7597810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01925faabefdbedf8efebb820b152e94fb287b72138d282a76557993132623ca`  
		Last Modified: Wed, 28 Jan 2026 02:19:47 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ad13ec2588fba164870da3d93ba8b5ad34e242b5bc6fb7b5df1bd055e194e0`  
		Last Modified: Wed, 28 Jan 2026 02:19:48 GMT  
		Size: 17.6 MB (17566458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc3d6d20d26654203dbb33aecb823850102a06ee1d8826eeea313f51053947d`  
		Last Modified: Wed, 28 Jan 2026 02:19:48 GMT  
		Size: 26.5 MB (26544669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309b43a06105801e72a4057c9a98aa39f845292f118ed5364be6f2c58fff6fb2`  
		Last Modified: Wed, 28 Jan 2026 02:19:48 GMT  
		Size: 10.2 MB (10198593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c018df83e09983e9c86c614e37738e0c9913c07f571d99ca7464a8eead3114`  
		Last Modified: Wed, 28 Jan 2026 02:19:49 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff08fbe96bdc955d67587b7154a9e64b5fd0933ad18112a10502a2d2ee351334`  
		Last Modified: Wed, 28 Jan 2026 02:19:49 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82766871530b6d5c5faaefb052706696dbc1f4936a761d57fe77b41476c57e81`  
		Last Modified: Wed, 28 Jan 2026 02:19:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966fa3b3930581a719871ad9cc50569b5b949938c666c5f604128567586dcc98`  
		Last Modified: Wed, 28 Jan 2026 03:51:58 GMT  
		Size: 6.6 MB (6572989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8288f87d3ec8e6d2c73fad07643b43f2c5a333b046f21c81531e877d6eaf19d4`  
		Last Modified: Wed, 28 Jan 2026 03:51:58 GMT  
		Size: 88.1 KB (88136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd5922158e4b006788c6366971c7c91cc1404b01a100da81d4c9a0477a74027`  
		Last Modified: Wed, 28 Jan 2026 03:51:58 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842a3b5326d8c1c6b696edd5624246ed13391ce31743771eb92561f224c0e672`  
		Last Modified: Wed, 28 Jan 2026 03:52:00 GMT  
		Size: 61.9 MB (61856931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f666916210054b0fd5f72affa9ac152fa7c42d927442f2dd309d354e89b9277`  
		Last Modified: Wed, 28 Jan 2026 03:51:59 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cf19ee261d3469335adb02771df03de4d7bd57f3cb5c06bb5841ae7b93697c`  
		Last Modified: Wed, 28 Jan 2026 03:51:59 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:8457bbc8972fac13450e367c97a9a1b851c44540331c9f631abe6ecc6da554fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d30df9382a2c15c97b7086f993412c3a0f44e8ed81f835508748d782eabe5345`

```dockerfile
```

-	Layers:
	-	`sha256:0a1c8b9290fc1e34c2f218c7730ca8fc83fc55704982e288265ea392b6f0447c`  
		Last Modified: Wed, 28 Jan 2026 03:51:58 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:2cd37b1da26b3d7bdae2014ffafb6543a3c40f32973395bdf6e402afc6818e38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.2 MB (133249301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a287877d76e510dc36d4294bef0d4540628445c54cbf477d32ad4aef68e7bb0a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:15:20 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:15:20 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:15:20 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:15:22 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:15:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:15:22 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:15:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:15:23 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:15:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:15:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:15:24 GMT
CMD ["sh"]
# Wed, 28 Jan 2026 04:19:44 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 Jan 2026 04:19:44 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 Jan 2026 04:19:45 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 04:19:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 Jan 2026 04:19:48 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 Jan 2026 04:19:48 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 Jan 2026 04:19:48 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 04:19:48 GMT
VOLUME [/var/lib/docker]
# Wed, 28 Jan 2026 04:19:48 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 Jan 2026 04:19:48 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 Jan 2026 04:19:48 GMT
CMD []
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23cd2c872bdff3a89f69a977eea6049f005ee667e33468764b0584c9a8959fe3`  
		Last Modified: Wed, 28 Jan 2026 02:15:31 GMT  
		Size: 8.5 MB (8453525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a2f891a573bd6b7ff30782766b7564cfd2718e91c2399081bdf0ffb44fabba`  
		Last Modified: Wed, 28 Jan 2026 02:15:30 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f26d33b7e75cf64b24043a967d4288b682c0eba3866ed27897136240d3f4cbe`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 17.3 MB (17349909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fadf59f99eaf4a5457883e92f5eb0e9f05304f32b91ff429c77b5d12c399d17`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 25.5 MB (25539742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bbb75472d83a88fcf93366d31a9685491eaee5051b271d7e9822962477745c`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 10.0 MB (9954517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982182610648dbb0778b184ecff3e692201a2114ba00657d6fd977582e60c802`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c47f152455dabd15e5d73f9f555e031f1bf91be0a42bb7899543ca32f4be842`  
		Last Modified: Wed, 28 Jan 2026 02:15:34 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d60b69639960857109359648f1dd0dd6cb3d2cce9bdd6b1a594fd99159bf8f`  
		Last Modified: Wed, 28 Jan 2026 02:15:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf3426000179b3492ca41ec23019609bae7bd020884ba682b730f4920dcdadd`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 7.2 MB (7213335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d0c859c41e3ca1cc276016f6151a0a02e77f672f849df7d283d4657b2fd464`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 101.3 KB (101289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6748b522881f24eb97f2eed26e32bdb49ae5819b2477eae3a4976874142ff758`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:407dff81deac15d5750c410b3b45d2888514fd7173fad465cdb860a9e18a068c`  
		Last Modified: Wed, 28 Jan 2026 04:19:59 GMT  
		Size: 60.4 MB (60431745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae84a81436627202044f15c8bfbb21c37acd9371efb16eac52fa88d19fd035c`  
		Last Modified: Wed, 28 Jan 2026 04:19:58 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66e9c5f6367f5ce3bcd7921fbcd7ecdee44c87e2b3fb4e91c0953fdefb902bb`  
		Last Modified: Wed, 28 Jan 2026 04:19:58 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:76d7445bd6915a9080071a3680a3a2dd3bfb0697d214d61d429692ed178b2519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee53cf6ac36a1613efdfec96533f5b66f1bac362f162eeed2703924705574c2d`

```dockerfile
```

-	Layers:
	-	`sha256:51f7535efd28fb94f257372f96380d2a49634a8b4664d35a295a7201ee67d470`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-dind-rootless`

```console
$ docker pull docker@sha256:e2256cccf0a81babdf6b0715edc84299976eea749dc373de1d4c4b98f38be576
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:29-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:6e740431e7ec02952bcba763683de89ae7c38ed168d0cfc4b875ffc2cc94eb01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.6 MB (164596244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:893377b7f16e5efd1e758a1c978a11516ff914ffd6896497463fae305e6732d9`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:15:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:15:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:15:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:15:17 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:15:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:15:17 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:15:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:15:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:15:19 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:15:19 GMT
CMD ["sh"]
# Wed, 28 Jan 2026 03:58:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 Jan 2026 03:58:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 Jan 2026 03:58:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 Jan 2026 03:58:45 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
VOLUME [/var/lib/docker]
# Wed, 28 Jan 2026 03:58:45 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 Jan 2026 03:58:45 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 Jan 2026 03:58:45 GMT
CMD []
# Wed, 28 Jan 2026 04:49:51 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Wed, 28 Jan 2026 04:49:51 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 28 Jan 2026 04:49:51 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 04:49:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 28 Jan 2026 04:49:52 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 28 Jan 2026 04:49:52 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 28 Jan 2026 04:49:52 GMT
USER rootless
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03ce8e2700f1129dc15f38a5e1e7d27cdd2b98175c4d9ac08dc5646c3c35ba4`  
		Last Modified: Wed, 28 Jan 2026 02:15:26 GMT  
		Size: 8.4 MB (8399638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dabc00febb6a9a0d9954ef0b62272b11dabac7697dd7a0f94f9a96e241fbfd2`  
		Last Modified: Wed, 28 Jan 2026 02:15:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9408125f9d0c694cc95efc06409f73e6d6907c853a7f861c85b36824fb02ed25`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 18.8 MB (18774054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1765bbbd236eff12d3ecffaab470c2a8ade7f1432cbf0f1efe2f520cb9d74bfc`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 28.3 MB (28308902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d4f1a3f89cb924cc72cf031843e7490b98f39a276e6628c0ef444a871ff92f`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 10.8 MB (10799762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ca730a0591b75f8b903f70ff08c4b2959f397bd8775ba1a873cbb344b15c1a0`  
		Last Modified: Wed, 28 Jan 2026 02:15:28 GMT  
		Size: 533.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc93a580b636b3173550ee5a31a23ae95eb17558288345a26091285a5f477d5`  
		Last Modified: Wed, 28 Jan 2026 02:15:28 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9745309fb9885c647e35e9d55ab83308f9c212460ad5f9b73c2e518179059b72`  
		Last Modified: Wed, 28 Jan 2026 02:15:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:effa5c3a383e3a584de2fe9ef352f8fcde727e8db088492f0c8e49fc27f7abaa`  
		Last Modified: Wed, 28 Jan 2026 03:58:56 GMT  
		Size: 6.9 MB (6934734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a8f8addf621601263b2bfea9efe7ffac5903b85bfe7b9f628f7a2ff6bd4fce`  
		Last Modified: Wed, 28 Jan 2026 03:58:55 GMT  
		Size: 92.5 KB (92460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:396bcb1ae646a1eb234538a6bf406490001b6067e5626f4858b3d3ab115a1338`  
		Last Modified: Wed, 28 Jan 2026 03:58:56 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636ece6788bea2909cc3a17231a1a4827c4db266c991df7770a909ecdb8d3fd0`  
		Last Modified: Wed, 28 Jan 2026 03:58:57 GMT  
		Size: 66.6 MB (66619579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb2987d59bbd2b711c1759725d9ccc5891b03def0602234c4f49beb1e5c2be1`  
		Last Modified: Wed, 28 Jan 2026 03:58:57 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ac6a5de045400bc7b163e70c2cd9429f6202144cb50ed4b85688aded44f58e`  
		Last Modified: Wed, 28 Jan 2026 03:58:57 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:733f26c740596bada2273b63c30df575d6fe75108c34ae59cf6cce23eb6fde38`  
		Last Modified: Wed, 28 Jan 2026 04:49:58 GMT  
		Size: 3.4 MB (3419936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9b0d647df5d90a456bfb18e7fe3512570e5501e17a96c28d0673f36c7de2ab`  
		Last Modified: Wed, 28 Jan 2026 04:49:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2266ba1a98fbf4bf56e7477a64291015ffc22febbdef7b5c52756c0bccea91bc`  
		Last Modified: Wed, 28 Jan 2026 04:49:58 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e7bef04bfc2f8ecbd179e44e594aea6870289cac0095619a71f9ae48c070b2`  
		Last Modified: Wed, 28 Jan 2026 04:49:59 GMT  
		Size: 17.4 MB (17375872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de36060bb1e57bb0070a546b5af68c0c667dfc7c88ad9c5e0b4b58cd903fdd5f`  
		Last Modified: Wed, 28 Jan 2026 04:49:59 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:304a9bab4d48983bd4f25caa7723d4ff17feec1769ef4b9d815a85818b33f85a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18a9fa96564b6f3cbe5f035361ffe48a58c26e0d28c673a4517c0afb4d19bd17`

```dockerfile
```

-	Layers:
	-	`sha256:f20e17ed780eccbdcae7df7f23b087c7750a8fca8f1ef231ace886ff1ec41145`  
		Last Modified: Wed, 28 Jan 2026 04:49:58 GMT  
		Size: 30.6 KB (30589 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:10185cf7e9ecf2d725eabaed0f994c40d28c4ca77f04234d07c2bb0efcd4c588
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154355521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f80a4777f73ae85118338e6c79bca8a28937df9dc8a5f912a5066951db75e2a7`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:15:20 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:15:20 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:15:20 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:15:22 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:15:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:15:22 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:15:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:15:23 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:15:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:15:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:15:24 GMT
CMD ["sh"]
# Wed, 28 Jan 2026 04:19:44 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 Jan 2026 04:19:44 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 Jan 2026 04:19:45 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 04:19:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 Jan 2026 04:19:48 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 Jan 2026 04:19:48 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 Jan 2026 04:19:48 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 04:19:48 GMT
VOLUME [/var/lib/docker]
# Wed, 28 Jan 2026 04:19:48 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 Jan 2026 04:19:48 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 Jan 2026 04:19:48 GMT
CMD []
# Wed, 28 Jan 2026 05:26:30 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Wed, 28 Jan 2026 05:26:30 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 28 Jan 2026 05:26:30 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 05:26:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 28 Jan 2026 05:26:31 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 28 Jan 2026 05:26:31 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 28 Jan 2026 05:26:31 GMT
USER rootless
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23cd2c872bdff3a89f69a977eea6049f005ee667e33468764b0584c9a8959fe3`  
		Last Modified: Wed, 28 Jan 2026 02:15:31 GMT  
		Size: 8.5 MB (8453525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a2f891a573bd6b7ff30782766b7564cfd2718e91c2399081bdf0ffb44fabba`  
		Last Modified: Wed, 28 Jan 2026 02:15:30 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f26d33b7e75cf64b24043a967d4288b682c0eba3866ed27897136240d3f4cbe`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 17.3 MB (17349909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fadf59f99eaf4a5457883e92f5eb0e9f05304f32b91ff429c77b5d12c399d17`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 25.5 MB (25539742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bbb75472d83a88fcf93366d31a9685491eaee5051b271d7e9822962477745c`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 10.0 MB (9954517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982182610648dbb0778b184ecff3e692201a2114ba00657d6fd977582e60c802`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c47f152455dabd15e5d73f9f555e031f1bf91be0a42bb7899543ca32f4be842`  
		Last Modified: Wed, 28 Jan 2026 02:15:34 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d60b69639960857109359648f1dd0dd6cb3d2cce9bdd6b1a594fd99159bf8f`  
		Last Modified: Wed, 28 Jan 2026 02:15:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf3426000179b3492ca41ec23019609bae7bd020884ba682b730f4920dcdadd`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 7.2 MB (7213335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d0c859c41e3ca1cc276016f6151a0a02e77f672f849df7d283d4657b2fd464`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 101.3 KB (101289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6748b522881f24eb97f2eed26e32bdb49ae5819b2477eae3a4976874142ff758`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:407dff81deac15d5750c410b3b45d2888514fd7173fad465cdb860a9e18a068c`  
		Last Modified: Wed, 28 Jan 2026 04:19:59 GMT  
		Size: 60.4 MB (60431745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae84a81436627202044f15c8bfbb21c37acd9371efb16eac52fa88d19fd035c`  
		Last Modified: Wed, 28 Jan 2026 04:19:58 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66e9c5f6367f5ce3bcd7921fbcd7ecdee44c87e2b3fb4e91c0953fdefb902bb`  
		Last Modified: Wed, 28 Jan 2026 04:19:58 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b2ca6f15a1175824a8ac624e8e96c03e577d7045335b3b8da66fa925ac730e`  
		Last Modified: Wed, 28 Jan 2026 05:26:37 GMT  
		Size: 3.4 MB (3394379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aae4fb46b816b0c2dabc0ce7fb6de979a1297033cfc1d63f2330898b865858f`  
		Last Modified: Wed, 28 Jan 2026 05:26:37 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0ee34b605800e64fa4c7d8ae1e8b3a28b7a99fb9273d49a13ddc555bda1daa5`  
		Last Modified: Wed, 28 Jan 2026 05:26:37 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4850780d6ebb6a4c34ff107ae6908c6afecf589851309b1c501eea08aadde6b2`  
		Last Modified: Wed, 28 Jan 2026 05:26:38 GMT  
		Size: 17.7 MB (17710501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b19d5a6a20d8289c916e7596e72a2d20595e4e8c11ae662f0ce57a9c05814f1`  
		Last Modified: Wed, 28 Jan 2026 05:26:38 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:c4559aefd8beb1182fc0607820b2e0c38fe82f9a6af4f47c78173a966859ba4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50641e7994aded7de3b8033e71f36c7fa1b0b852dc54cb3365dbfd3de2e376b6`

```dockerfile
```

-	Layers:
	-	`sha256:2e936dbc59719f822df84bc05b46cb1f559506d9e7912ed2c9c670c5b0a6d64c`  
		Last Modified: Wed, 28 Jan 2026 05:26:37 GMT  
		Size: 30.8 KB (30753 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-windowsservercore`

```console
$ docker pull docker@sha256:79cb1793605b4f2d7317cea6706862e4b002e6ace6375912bab555eebfdf6ed2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `docker:29-windowsservercore` - windows version 10.0.26100.32230; amd64

```console
$ docker pull docker@sha256:c5d3ecbfcaeb424c90459ac8317405555d19b1b8b3e578390234d4a8e7c24c64
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1556599774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d647b193ba9f5cb583f9fb294f2d532c6d85295880ef0649d60793cc309abcd1`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Tue, 03 Feb 2026 17:28:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 03 Feb 2026 17:29:28 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 03 Feb 2026 17:29:30 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:29:32 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.1.zip
# Tue, 03 Feb 2026 17:29:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 03 Feb 2026 17:29:46 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:29:48 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.windows-amd64.exe
# Tue, 03 Feb 2026 17:29:48 GMT
ENV DOCKER_BUILDX_SHA256=b49832d4ac46bde05006f7ad3506b9d5060b60e5c566545d8e10c1a80df08a4a
# Tue, 03 Feb 2026 17:29:59 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 03 Feb 2026 17:30:00 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:30:01 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Tue, 03 Feb 2026 17:30:01 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Tue, 03 Feb 2026 17:30:08 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3345d2727a1883e3d335172c07a1f0f478ed9c744e1aa4ec455219fd5b041b31`  
		Last Modified: Tue, 03 Feb 2026 17:30:17 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c2b758f14303d714990de0fad8eacb8f18d18925809a064fa024e0a8203573a`  
		Last Modified: Tue, 03 Feb 2026 17:30:16 GMT  
		Size: 402.8 KB (402791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c544aebc260938057720752277d7e0b5a599ebf13c36d8be0403e694d8929db8`  
		Last Modified: Tue, 03 Feb 2026 17:30:15 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54275eb139ff712b0a5f139cdba772a69cd2371fcb0b65f6371b8d8b22f92c19`  
		Last Modified: Tue, 03 Feb 2026 17:30:15 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff99eb3d4bee14899afa2383e60cfa18a0f63d88f5c759afcbfa0cef9bae50bb`  
		Last Modified: Tue, 03 Feb 2026 17:30:18 GMT  
		Size: 19.5 MB (19477937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d8a57f5276cfc049bae3b7a853039be549c9bada93ef2e8d868ea54e9c04236`  
		Last Modified: Tue, 03 Feb 2026 17:30:14 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be178348f9fba72db323ad766660239b1363bbe80d1f01cf90cd2531b5f01b03`  
		Last Modified: Tue, 03 Feb 2026 17:30:14 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca77ca63bd7d4b72f07134cb3691a9edeba02acdb61fb8ff15a7f6c7f44734ce`  
		Last Modified: Tue, 03 Feb 2026 17:30:14 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51aa328a4c51fa2977445e97c24b485b2fbf132d207a9adfa58cf7406f3f8a1f`  
		Last Modified: Tue, 03 Feb 2026 17:30:30 GMT  
		Size: 29.5 MB (29453041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c300d10089e1c370f164537efd3c43df949644198f422eb4863dccfe9930a4f`  
		Last Modified: Tue, 03 Feb 2026 17:30:12 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5356d434dcd14c58d539907321e96d2a0e794ac74a29c08aa2df1dbaa611e231`  
		Last Modified: Tue, 03 Feb 2026 17:30:12 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b03bbb60e30cb160ee1c1c6844849f758718d7111a7cb510a1b0ec1702120fd`  
		Last Modified: Tue, 03 Feb 2026 17:30:12 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2d04ad8db9950e63dbd9118d08d70484b5aed5cf9dadf9591e16f2a8339e8e`  
		Last Modified: Tue, 03 Feb 2026 17:30:14 GMT  
		Size: 11.5 MB (11493926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:29-windowsservercore` - windows version 10.0.20348.4648; amd64

```console
$ docker pull docker@sha256:ba1e9a93d62651a48e0592e4a6010300708e2422e46df2b25d54b1d2f1e7fb47
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1896494534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a09c7520bcdba0cceb87d9e1fe705ea6641137be025705d09eaba1893561ddea`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Tue, 03 Feb 2026 17:28:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 03 Feb 2026 17:29:49 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 03 Feb 2026 17:29:49 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:29:50 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.1.zip
# Tue, 03 Feb 2026 17:30:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 03 Feb 2026 17:30:17 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:30:18 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.windows-amd64.exe
# Tue, 03 Feb 2026 17:30:18 GMT
ENV DOCKER_BUILDX_SHA256=b49832d4ac46bde05006f7ad3506b9d5060b60e5c566545d8e10c1a80df08a4a
# Tue, 03 Feb 2026 17:30:49 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 03 Feb 2026 17:30:50 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:30:52 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Tue, 03 Feb 2026 17:30:52 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Tue, 03 Feb 2026 17:31:09 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1610c61d22cce1c0da1f89bcf2b2b93db5d1ee6703ddda8c50c992a55a3a3273`  
		Last Modified: Tue, 03 Feb 2026 17:31:19 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35301633ca92d436f45505192a1ef4f18618178fd179a0275e79d55f1cdba61d`  
		Last Modified: Tue, 03 Feb 2026 17:31:19 GMT  
		Size: 502.0 KB (501985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc76ce47c4de88873c339dee382928f8c2afe957a1f67eaa1bc1745de35e796e`  
		Last Modified: Tue, 03 Feb 2026 17:31:18 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c0a93da300b8f2017782995a21ddcc03360f0068884e95f2c90a34943b5a853`  
		Last Modified: Tue, 03 Feb 2026 17:31:18 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4642a451e4aa3a689441cf53a384a5333b79045931964aecc32acb75dab6242f`  
		Last Modified: Tue, 03 Feb 2026 17:31:20 GMT  
		Size: 19.4 MB (19440499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f80fcdb722aba8bdf0a57b047c109edce18d999e3bc1649781fa0d3de37c6e29`  
		Last Modified: Tue, 03 Feb 2026 17:31:16 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52573eb20ed9e08365fa5f5e972f07f60f80fd44870b2c8c2e00435b86e529d7`  
		Last Modified: Tue, 03 Feb 2026 17:31:16 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc93a0644ac21577feac91654ceef3e9cb714742257794765b8f41f26967f84e`  
		Last Modified: Tue, 03 Feb 2026 17:31:16 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c020b7de7a60805f5e0f214c5933b5730ce1e22475c6c0637dbe59005c03baa4`  
		Last Modified: Tue, 03 Feb 2026 17:31:33 GMT  
		Size: 29.4 MB (29425091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:538b00d976a03c45b55d387636033ba066f8d59660d195f26399a156232cb079`  
		Last Modified: Tue, 03 Feb 2026 17:31:14 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f8c0456ab18eeca4e06f6a4f1edc155807d2fd8565b3c71217f4895c0778536`  
		Last Modified: Tue, 03 Feb 2026 17:31:14 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525c0f16947c0cc46484ca50b3cbe0be998327c9e218a8f15dd79b3752be1f84`  
		Last Modified: Tue, 03 Feb 2026 17:31:14 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f29f86a605fc1d2ecf16f261c2beeb1261773d00bba4c7341e76d2363f15db4a`  
		Last Modified: Tue, 03 Feb 2026 17:31:16 GMT  
		Size: 11.5 MB (11456032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:315827d701f9fef8731fca2a65b1c5960422bfb5d0e6f335995310b4c2c2bf07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `docker:29-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull docker@sha256:ba1e9a93d62651a48e0592e4a6010300708e2422e46df2b25d54b1d2f1e7fb47
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1896494534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a09c7520bcdba0cceb87d9e1fe705ea6641137be025705d09eaba1893561ddea`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Tue, 03 Feb 2026 17:28:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 03 Feb 2026 17:29:49 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 03 Feb 2026 17:29:49 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:29:50 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.1.zip
# Tue, 03 Feb 2026 17:30:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 03 Feb 2026 17:30:17 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:30:18 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.windows-amd64.exe
# Tue, 03 Feb 2026 17:30:18 GMT
ENV DOCKER_BUILDX_SHA256=b49832d4ac46bde05006f7ad3506b9d5060b60e5c566545d8e10c1a80df08a4a
# Tue, 03 Feb 2026 17:30:49 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 03 Feb 2026 17:30:50 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:30:52 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Tue, 03 Feb 2026 17:30:52 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Tue, 03 Feb 2026 17:31:09 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1610c61d22cce1c0da1f89bcf2b2b93db5d1ee6703ddda8c50c992a55a3a3273`  
		Last Modified: Tue, 03 Feb 2026 17:31:19 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35301633ca92d436f45505192a1ef4f18618178fd179a0275e79d55f1cdba61d`  
		Last Modified: Tue, 03 Feb 2026 17:31:19 GMT  
		Size: 502.0 KB (501985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc76ce47c4de88873c339dee382928f8c2afe957a1f67eaa1bc1745de35e796e`  
		Last Modified: Tue, 03 Feb 2026 17:31:18 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c0a93da300b8f2017782995a21ddcc03360f0068884e95f2c90a34943b5a853`  
		Last Modified: Tue, 03 Feb 2026 17:31:18 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4642a451e4aa3a689441cf53a384a5333b79045931964aecc32acb75dab6242f`  
		Last Modified: Tue, 03 Feb 2026 17:31:20 GMT  
		Size: 19.4 MB (19440499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f80fcdb722aba8bdf0a57b047c109edce18d999e3bc1649781fa0d3de37c6e29`  
		Last Modified: Tue, 03 Feb 2026 17:31:16 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52573eb20ed9e08365fa5f5e972f07f60f80fd44870b2c8c2e00435b86e529d7`  
		Last Modified: Tue, 03 Feb 2026 17:31:16 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc93a0644ac21577feac91654ceef3e9cb714742257794765b8f41f26967f84e`  
		Last Modified: Tue, 03 Feb 2026 17:31:16 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c020b7de7a60805f5e0f214c5933b5730ce1e22475c6c0637dbe59005c03baa4`  
		Last Modified: Tue, 03 Feb 2026 17:31:33 GMT  
		Size: 29.4 MB (29425091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:538b00d976a03c45b55d387636033ba066f8d59660d195f26399a156232cb079`  
		Last Modified: Tue, 03 Feb 2026 17:31:14 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f8c0456ab18eeca4e06f6a4f1edc155807d2fd8565b3c71217f4895c0778536`  
		Last Modified: Tue, 03 Feb 2026 17:31:14 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525c0f16947c0cc46484ca50b3cbe0be998327c9e218a8f15dd79b3752be1f84`  
		Last Modified: Tue, 03 Feb 2026 17:31:14 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f29f86a605fc1d2ecf16f261c2beeb1261773d00bba4c7341e76d2363f15db4a`  
		Last Modified: Tue, 03 Feb 2026 17:31:16 GMT  
		Size: 11.5 MB (11456032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:ed671d3152d0f57a459cd9f0838f7e48071ccef5c71ad1188693f4540f24cf19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32230; amd64

### `docker:29-windowsservercore-ltsc2025` - windows version 10.0.26100.32230; amd64

```console
$ docker pull docker@sha256:c5d3ecbfcaeb424c90459ac8317405555d19b1b8b3e578390234d4a8e7c24c64
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1556599774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d647b193ba9f5cb583f9fb294f2d532c6d85295880ef0649d60793cc309abcd1`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Tue, 03 Feb 2026 17:28:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 03 Feb 2026 17:29:28 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 03 Feb 2026 17:29:30 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:29:32 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.1.zip
# Tue, 03 Feb 2026 17:29:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 03 Feb 2026 17:29:46 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:29:48 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.windows-amd64.exe
# Tue, 03 Feb 2026 17:29:48 GMT
ENV DOCKER_BUILDX_SHA256=b49832d4ac46bde05006f7ad3506b9d5060b60e5c566545d8e10c1a80df08a4a
# Tue, 03 Feb 2026 17:29:59 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 03 Feb 2026 17:30:00 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:30:01 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Tue, 03 Feb 2026 17:30:01 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Tue, 03 Feb 2026 17:30:08 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3345d2727a1883e3d335172c07a1f0f478ed9c744e1aa4ec455219fd5b041b31`  
		Last Modified: Tue, 03 Feb 2026 17:30:17 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c2b758f14303d714990de0fad8eacb8f18d18925809a064fa024e0a8203573a`  
		Last Modified: Tue, 03 Feb 2026 17:30:16 GMT  
		Size: 402.8 KB (402791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c544aebc260938057720752277d7e0b5a599ebf13c36d8be0403e694d8929db8`  
		Last Modified: Tue, 03 Feb 2026 17:30:15 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54275eb139ff712b0a5f139cdba772a69cd2371fcb0b65f6371b8d8b22f92c19`  
		Last Modified: Tue, 03 Feb 2026 17:30:15 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff99eb3d4bee14899afa2383e60cfa18a0f63d88f5c759afcbfa0cef9bae50bb`  
		Last Modified: Tue, 03 Feb 2026 17:30:18 GMT  
		Size: 19.5 MB (19477937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d8a57f5276cfc049bae3b7a853039be549c9bada93ef2e8d868ea54e9c04236`  
		Last Modified: Tue, 03 Feb 2026 17:30:14 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be178348f9fba72db323ad766660239b1363bbe80d1f01cf90cd2531b5f01b03`  
		Last Modified: Tue, 03 Feb 2026 17:30:14 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca77ca63bd7d4b72f07134cb3691a9edeba02acdb61fb8ff15a7f6c7f44734ce`  
		Last Modified: Tue, 03 Feb 2026 17:30:14 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51aa328a4c51fa2977445e97c24b485b2fbf132d207a9adfa58cf7406f3f8a1f`  
		Last Modified: Tue, 03 Feb 2026 17:30:30 GMT  
		Size: 29.5 MB (29453041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c300d10089e1c370f164537efd3c43df949644198f422eb4863dccfe9930a4f`  
		Last Modified: Tue, 03 Feb 2026 17:30:12 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5356d434dcd14c58d539907321e96d2a0e794ac74a29c08aa2df1dbaa611e231`  
		Last Modified: Tue, 03 Feb 2026 17:30:12 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b03bbb60e30cb160ee1c1c6844849f758718d7111a7cb510a1b0ec1702120fd`  
		Last Modified: Tue, 03 Feb 2026 17:30:12 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2d04ad8db9950e63dbd9118d08d70484b5aed5cf9dadf9591e16f2a8339e8e`  
		Last Modified: Tue, 03 Feb 2026 17:30:14 GMT  
		Size: 11.5 MB (11493926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.2`

```console
$ docker pull docker@sha256:a284d31e4db9a9916fd9be44380263eaeafedf0e3048a859f978922b5a0c16fc
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

### `docker:29.2` - linux; amd64

```console
$ docker pull docker@sha256:99aa88f75d8d401c30e395db1d2e679a89ff0be9b415f020b8e2383c517e1fda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.8 MB (143799092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ca04087ca24aa6deade38370d033555d14dacd022c6a5d275f038b89eaf131`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:15:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:15:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:15:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:15:17 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:15:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:15:17 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:15:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:15:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:15:19 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:15:19 GMT
CMD ["sh"]
# Wed, 28 Jan 2026 03:58:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 Jan 2026 03:58:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 Jan 2026 03:58:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 Jan 2026 03:58:45 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
VOLUME [/var/lib/docker]
# Wed, 28 Jan 2026 03:58:45 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 Jan 2026 03:58:45 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 Jan 2026 03:58:45 GMT
CMD []
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03ce8e2700f1129dc15f38a5e1e7d27cdd2b98175c4d9ac08dc5646c3c35ba4`  
		Last Modified: Wed, 28 Jan 2026 02:15:26 GMT  
		Size: 8.4 MB (8399638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dabc00febb6a9a0d9954ef0b62272b11dabac7697dd7a0f94f9a96e241fbfd2`  
		Last Modified: Wed, 28 Jan 2026 02:15:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9408125f9d0c694cc95efc06409f73e6d6907c853a7f861c85b36824fb02ed25`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 18.8 MB (18774054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1765bbbd236eff12d3ecffaab470c2a8ade7f1432cbf0f1efe2f520cb9d74bfc`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 28.3 MB (28308902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d4f1a3f89cb924cc72cf031843e7490b98f39a276e6628c0ef444a871ff92f`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 10.8 MB (10799762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ca730a0591b75f8b903f70ff08c4b2959f397bd8775ba1a873cbb344b15c1a0`  
		Last Modified: Wed, 28 Jan 2026 02:15:28 GMT  
		Size: 533.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc93a580b636b3173550ee5a31a23ae95eb17558288345a26091285a5f477d5`  
		Last Modified: Wed, 28 Jan 2026 02:15:28 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9745309fb9885c647e35e9d55ab83308f9c212460ad5f9b73c2e518179059b72`  
		Last Modified: Wed, 28 Jan 2026 02:15:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:effa5c3a383e3a584de2fe9ef352f8fcde727e8db088492f0c8e49fc27f7abaa`  
		Last Modified: Wed, 28 Jan 2026 03:58:56 GMT  
		Size: 6.9 MB (6934734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a8f8addf621601263b2bfea9efe7ffac5903b85bfe7b9f628f7a2ff6bd4fce`  
		Last Modified: Wed, 28 Jan 2026 03:58:55 GMT  
		Size: 92.5 KB (92460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:396bcb1ae646a1eb234538a6bf406490001b6067e5626f4858b3d3ab115a1338`  
		Last Modified: Wed, 28 Jan 2026 03:58:56 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636ece6788bea2909cc3a17231a1a4827c4db266c991df7770a909ecdb8d3fd0`  
		Last Modified: Wed, 28 Jan 2026 03:58:57 GMT  
		Size: 66.6 MB (66619579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb2987d59bbd2b711c1759725d9ccc5891b03def0602234c4f49beb1e5c2be1`  
		Last Modified: Wed, 28 Jan 2026 03:58:57 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ac6a5de045400bc7b163e70c2cd9429f6202144cb50ed4b85688aded44f58e`  
		Last Modified: Wed, 28 Jan 2026 03:58:57 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2` - unknown; unknown

```console
$ docker pull docker@sha256:2d2c0973782cdccc69752fb841755627c37546ebbf2f68f0bf070bf51d23ec60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0784b32a62dac2ebed2ad0ae726d2901f105b39654d58a2d2d351b4eaea7d818`

```dockerfile
```

-	Layers:
	-	`sha256:161b2e45f0098aead317dd0674b614a4e1252835a147f30b88ddc0667bf7ba93`  
		Last Modified: Wed, 28 Jan 2026 03:58:55 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2` - linux; arm variant v6

```console
$ docker pull docker@sha256:70dcad0b903a121c11d71a23834267a49327cd21053d8a2a83529cf94a2d9fbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135630532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:438bd2c6733062a94188c3067ba6118e7dda4560c7d7eb98ecec81192d5273b2`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:19:28 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:19:29 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:19:29 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:19:32 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:19:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:19:32 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:19:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:19:34 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:19:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:19:36 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:19:36 GMT
CMD ["sh"]
# Wed, 28 Jan 2026 03:49:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 Jan 2026 03:49:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 Jan 2026 03:49:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 03:49:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 Jan 2026 03:49:21 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 Jan 2026 03:49:21 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 Jan 2026 03:49:21 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:49:21 GMT
VOLUME [/var/lib/docker]
# Wed, 28 Jan 2026 03:49:21 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 Jan 2026 03:49:21 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 Jan 2026 03:49:21 GMT
CMD []
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08efb619161971b8dbf3d2d18d22c25f3caf7baea4b18537b77a961fee285e4d`  
		Last Modified: Wed, 28 Jan 2026 02:19:43 GMT  
		Size: 8.3 MB (8301019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11eae5034a08f196af9949aec8c0d0a5c776062160fbfa6839f4e91eb25c523`  
		Last Modified: Wed, 28 Jan 2026 02:19:42 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b811dd811e1e6a5a185faf36f1f9dd7bd483290fc51d98ccb7f5014b5bd19ab`  
		Last Modified: Wed, 28 Jan 2026 02:19:43 GMT  
		Size: 17.6 MB (17576540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395a6e19e8b08ce81dbf6939f7000c5eaaa78657497cffd3559c4d3586ad6f25`  
		Last Modified: Wed, 28 Jan 2026 02:19:44 GMT  
		Size: 26.6 MB (26570467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b3f84acb2b12fc7c649c003ff8e9348dabfff644a17daad4b02eef0bd9b40b6`  
		Last Modified: Wed, 28 Jan 2026 02:19:44 GMT  
		Size: 10.2 MB (10213042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746007c626ec304c1dfcf1e9084f31b26345a6079f9efe6f265b8fa508abf11a`  
		Last Modified: Wed, 28 Jan 2026 02:19:44 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f144bc5ce89728429c7674f4da3e2efbf3439669eae61e270d13a77809b4b9b7`  
		Last Modified: Wed, 28 Jan 2026 02:19:45 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b078b00f266ba4e03e79da886e567e61c21f493be073a7001f1e3db1345ccf57`  
		Last Modified: Wed, 28 Jan 2026 02:19:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6f4b2cf4256d701c8e551ce6b913b60516e7a6812dd2a6b150737145528fdf`  
		Last Modified: Wed, 28 Jan 2026 03:49:31 GMT  
		Size: 7.3 MB (7271609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b290e764c28e19f2f21aa7790d801cc6056a53cd51c8fb1bb6faf2e2346d4145`  
		Last Modified: Wed, 28 Jan 2026 03:49:30 GMT  
		Size: 91.8 KB (91775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:894eda0b2167abb0c583bbf993071a8d219941e2dd3bc2fcd1f8bfd8ca024a34`  
		Last Modified: Wed, 28 Jan 2026 03:49:30 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661a756971591996ae71af31b4d76fd40c1ba5140d25d52487a63a2ce33123b3`  
		Last Modified: Wed, 28 Jan 2026 03:49:32 GMT  
		Size: 62.0 MB (62028111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0fea802a7e013543afeb57c94b421ff42c6cc94e875a7a48079633d5b32cf0`  
		Last Modified: Wed, 28 Jan 2026 03:49:31 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89262e7e7a4c52344f56768909e409e4d52e23b7e5f872f34c6f8f05f600ced1`  
		Last Modified: Wed, 28 Jan 2026 03:49:32 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2` - unknown; unknown

```console
$ docker pull docker@sha256:77efd8773fd21feb58c996858580a066f8336af75ce15a65d1e94fbfc662939f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8937de610607274348941cf30b97eee5b16a47a2a3e355daae965571f78e1b8e`

```dockerfile
```

-	Layers:
	-	`sha256:b2c9967356bfd5048f745045eb7a61d4c51f3b8a396da52f925736b964896609`  
		Last Modified: Wed, 28 Jan 2026 03:49:30 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2` - linux; arm variant v7

```console
$ docker pull docker@sha256:136f2e805834a4247060b8060063ba782a2fdce6083a3cb47d02e83936623504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133715469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a4604f36042cbaaba3fd792ec4e26bfaf62d2d45b48d38a8697760ddf3306fa`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:19:33 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:19:33 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:19:34 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:19:37 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:19:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:19:37 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:19:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:19:39 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:19:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:19:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:19:41 GMT
CMD ["sh"]
# Wed, 28 Jan 2026 03:51:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 Jan 2026 03:51:44 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 Jan 2026 03:51:44 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 03:51:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 Jan 2026 03:51:47 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 Jan 2026 03:51:47 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 Jan 2026 03:51:47 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:51:47 GMT
VOLUME [/var/lib/docker]
# Wed, 28 Jan 2026 03:51:47 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 Jan 2026 03:51:47 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 Jan 2026 03:51:47 GMT
CMD []
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef74ac3c65992e7acddcc2a2c02498d51d5fda8b771538e5411d2d5f3a3e9eec`  
		Last Modified: Wed, 28 Jan 2026 02:19:47 GMT  
		Size: 7.6 MB (7597810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01925faabefdbedf8efebb820b152e94fb287b72138d282a76557993132623ca`  
		Last Modified: Wed, 28 Jan 2026 02:19:47 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ad13ec2588fba164870da3d93ba8b5ad34e242b5bc6fb7b5df1bd055e194e0`  
		Last Modified: Wed, 28 Jan 2026 02:19:48 GMT  
		Size: 17.6 MB (17566458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc3d6d20d26654203dbb33aecb823850102a06ee1d8826eeea313f51053947d`  
		Last Modified: Wed, 28 Jan 2026 02:19:48 GMT  
		Size: 26.5 MB (26544669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309b43a06105801e72a4057c9a98aa39f845292f118ed5364be6f2c58fff6fb2`  
		Last Modified: Wed, 28 Jan 2026 02:19:48 GMT  
		Size: 10.2 MB (10198593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c018df83e09983e9c86c614e37738e0c9913c07f571d99ca7464a8eead3114`  
		Last Modified: Wed, 28 Jan 2026 02:19:49 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff08fbe96bdc955d67587b7154a9e64b5fd0933ad18112a10502a2d2ee351334`  
		Last Modified: Wed, 28 Jan 2026 02:19:49 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82766871530b6d5c5faaefb052706696dbc1f4936a761d57fe77b41476c57e81`  
		Last Modified: Wed, 28 Jan 2026 02:19:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966fa3b3930581a719871ad9cc50569b5b949938c666c5f604128567586dcc98`  
		Last Modified: Wed, 28 Jan 2026 03:51:58 GMT  
		Size: 6.6 MB (6572989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8288f87d3ec8e6d2c73fad07643b43f2c5a333b046f21c81531e877d6eaf19d4`  
		Last Modified: Wed, 28 Jan 2026 03:51:58 GMT  
		Size: 88.1 KB (88136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd5922158e4b006788c6366971c7c91cc1404b01a100da81d4c9a0477a74027`  
		Last Modified: Wed, 28 Jan 2026 03:51:58 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842a3b5326d8c1c6b696edd5624246ed13391ce31743771eb92561f224c0e672`  
		Last Modified: Wed, 28 Jan 2026 03:52:00 GMT  
		Size: 61.9 MB (61856931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f666916210054b0fd5f72affa9ac152fa7c42d927442f2dd309d354e89b9277`  
		Last Modified: Wed, 28 Jan 2026 03:51:59 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cf19ee261d3469335adb02771df03de4d7bd57f3cb5c06bb5841ae7b93697c`  
		Last Modified: Wed, 28 Jan 2026 03:51:59 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2` - unknown; unknown

```console
$ docker pull docker@sha256:8457bbc8972fac13450e367c97a9a1b851c44540331c9f631abe6ecc6da554fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d30df9382a2c15c97b7086f993412c3a0f44e8ed81f835508748d782eabe5345`

```dockerfile
```

-	Layers:
	-	`sha256:0a1c8b9290fc1e34c2f218c7730ca8fc83fc55704982e288265ea392b6f0447c`  
		Last Modified: Wed, 28 Jan 2026 03:51:58 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:2cd37b1da26b3d7bdae2014ffafb6543a3c40f32973395bdf6e402afc6818e38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.2 MB (133249301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a287877d76e510dc36d4294bef0d4540628445c54cbf477d32ad4aef68e7bb0a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:15:20 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:15:20 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:15:20 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:15:22 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:15:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:15:22 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:15:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:15:23 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:15:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:15:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:15:24 GMT
CMD ["sh"]
# Wed, 28 Jan 2026 04:19:44 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 Jan 2026 04:19:44 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 Jan 2026 04:19:45 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 04:19:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 Jan 2026 04:19:48 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 Jan 2026 04:19:48 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 Jan 2026 04:19:48 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 04:19:48 GMT
VOLUME [/var/lib/docker]
# Wed, 28 Jan 2026 04:19:48 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 Jan 2026 04:19:48 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 Jan 2026 04:19:48 GMT
CMD []
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23cd2c872bdff3a89f69a977eea6049f005ee667e33468764b0584c9a8959fe3`  
		Last Modified: Wed, 28 Jan 2026 02:15:31 GMT  
		Size: 8.5 MB (8453525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a2f891a573bd6b7ff30782766b7564cfd2718e91c2399081bdf0ffb44fabba`  
		Last Modified: Wed, 28 Jan 2026 02:15:30 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f26d33b7e75cf64b24043a967d4288b682c0eba3866ed27897136240d3f4cbe`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 17.3 MB (17349909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fadf59f99eaf4a5457883e92f5eb0e9f05304f32b91ff429c77b5d12c399d17`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 25.5 MB (25539742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bbb75472d83a88fcf93366d31a9685491eaee5051b271d7e9822962477745c`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 10.0 MB (9954517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982182610648dbb0778b184ecff3e692201a2114ba00657d6fd977582e60c802`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c47f152455dabd15e5d73f9f555e031f1bf91be0a42bb7899543ca32f4be842`  
		Last Modified: Wed, 28 Jan 2026 02:15:34 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d60b69639960857109359648f1dd0dd6cb3d2cce9bdd6b1a594fd99159bf8f`  
		Last Modified: Wed, 28 Jan 2026 02:15:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf3426000179b3492ca41ec23019609bae7bd020884ba682b730f4920dcdadd`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 7.2 MB (7213335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d0c859c41e3ca1cc276016f6151a0a02e77f672f849df7d283d4657b2fd464`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 101.3 KB (101289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6748b522881f24eb97f2eed26e32bdb49ae5819b2477eae3a4976874142ff758`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:407dff81deac15d5750c410b3b45d2888514fd7173fad465cdb860a9e18a068c`  
		Last Modified: Wed, 28 Jan 2026 04:19:59 GMT  
		Size: 60.4 MB (60431745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae84a81436627202044f15c8bfbb21c37acd9371efb16eac52fa88d19fd035c`  
		Last Modified: Wed, 28 Jan 2026 04:19:58 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66e9c5f6367f5ce3bcd7921fbcd7ecdee44c87e2b3fb4e91c0953fdefb902bb`  
		Last Modified: Wed, 28 Jan 2026 04:19:58 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2` - unknown; unknown

```console
$ docker pull docker@sha256:76d7445bd6915a9080071a3680a3a2dd3bfb0697d214d61d429692ed178b2519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee53cf6ac36a1613efdfec96533f5b66f1bac362f162eeed2703924705574c2d`

```dockerfile
```

-	Layers:
	-	`sha256:51f7535efd28fb94f257372f96380d2a49634a8b4664d35a295a7201ee67d470`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.2-cli`

```console
$ docker pull docker@sha256:1d6d751f1d68d1a5142c23c730ef5ecc976a8e050fa08c3cdb09f7e2e54a4439
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

### `docker:29.2-cli` - linux; amd64

```console
$ docker pull docker@sha256:0c04277b44d1d448d40238faa142c2edf21d4a90dc0d61486c32056bbf11572a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70148082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90fa388e81d5f66d9d9ee840c5375a0801629a980c3d9657463257b2c863f324`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:25:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:25:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:25:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:25:58 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:25:58 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:25:58 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:25:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:25:59 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:26:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:26:00 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:26:00 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ffbc9e9d61a3a427749366541c9e55c1440658b296b288726282a7e3a200f3`  
		Last Modified: Tue, 03 Feb 2026 17:26:07 GMT  
		Size: 8.4 MB (8399657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9130c567f6fc24a30ebaa5979b9c6700d6c174c3a52a1e753c42621bfb1a32d9`  
		Last Modified: Tue, 03 Feb 2026 17:26:07 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b75aa627f4cd980f8d8c3e7be1834e54e286a6499508105b6f72c4a373c7a6e`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 18.8 MB (18773130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c979ccecd955439750b7f01789bf427e4c8d60acbf2b4a12100ff3173aea9b`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 28.3 MB (28311545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217f84c60501e3b3fb548f194b2861bfcb2a70aa12a9abe9b0d4ee342d75a7b5`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 10.8 MB (10799774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bf8952411ee385ba36420d9b6bdcc36594a8be8bdace8fe62d7d97f81322411`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f757cc0a441eaf36dbebd029cb42e59a8c463fb4ea19e2ec6bf557d5a981dc2`  
		Last Modified: Tue, 03 Feb 2026 17:26:09 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7358b0dc3398fd6f4c32455892c6ab6fbc099f1a8e62df04445dec7663a095`  
		Last Modified: Tue, 03 Feb 2026 17:26:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2-cli` - unknown; unknown

```console
$ docker pull docker@sha256:c1620c41ed6e739f033f9e98a5bba1cb95e1ea6a093197beb216823c8c93ce72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c5f4666aeb7f994fb855d5fb4b289608e198a0a0b59b25161f28433aeb36364`

```dockerfile
```

-	Layers:
	-	`sha256:19b63918903a6b77f5af72e60038c44df3a84e5a4563b3db3d54ef79567b8195`  
		Last Modified: Tue, 03 Feb 2026 17:26:07 GMT  
		Size: 38.1 KB (38056 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:cf09d93cea103396a11b1b12c36c15b6b93d367c0c80cce733f00214c71c92e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66235505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4367f8d4a4b3fc3d463d69bca54b902b58d4792ccf8967224e2ec3dd7aa4afb4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:25:26 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:25:26 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:25:26 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:25:31 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:25:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:25:31 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:25:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:25:33 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:25:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:25:35 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:25:35 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ed7f28a4b26e2736ceb8045d972a5f166880f3b93b1ce13d7cb7710819f7c0`  
		Last Modified: Tue, 03 Feb 2026 17:25:42 GMT  
		Size: 8.3 MB (8300971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59982a56599ba445b45c1ff95a9bf2efe937cb3105d8107453c37e42aa96ab06`  
		Last Modified: Tue, 03 Feb 2026 17:25:41 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627db20a49a4f2be2d19fe161406f293a8b8804c985028e04c1cd95f0c40d96e`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 17.6 MB (17575014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acd42cfefd8cbfbea51ccc805027f78eefae1b3ad5cb91c207ebf9578a6a855`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 26.6 MB (26574500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac22564cea85937e49534e5ef435197d6c83fb053c5aa91ffddb70acae2ff81`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 10.2 MB (10213046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8735f9cb2ee8a9b930cd6b2bf3885083108a83a3707f302210e9bb0a138c15ec`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf43e9302aee150c8b25e6f5c53d2eb8642dd7db31500f8f7e980a6639b3d75`  
		Last Modified: Tue, 03 Feb 2026 17:25:44 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52ca294aaca561ae37709af7d9406792302f6ac4cfe16d2068ba04176c0aa2a`  
		Last Modified: Tue, 03 Feb 2026 17:25:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2-cli` - unknown; unknown

```console
$ docker pull docker@sha256:fbcdf3246eea54b7103bc19f384cd3f454538bd499af80a1566455c68e652971
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f63de4e3179da9faef11522e19444ae1387215588371c787a0b6852c464dcd77`

```dockerfile
```

-	Layers:
	-	`sha256:97d51d656e276dcee240923733068124918a337234be2ffb56edcdb70a458855`  
		Last Modified: Tue, 03 Feb 2026 17:25:41 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:ba03aff6e89a96861c91cbe97855b49f31e816c782afaa8225043cb76f7ae372
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65192844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:985b778ba8e60d8ceaa28fed60316b7c31c5ff3e18d6afb37619d388a8da92b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:26:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:26:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:26:11 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:26:15 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:26:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:26:15 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:26:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:26:19 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:26:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:26:20 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:26:20 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb5af91453d1293030fbe90db4c6166609f99510d3fcec579be00a21249cbf2`  
		Last Modified: Tue, 03 Feb 2026 17:26:28 GMT  
		Size: 7.6 MB (7597849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7fbe9447e7591ff3854f01ba9776952a93a9c4f22447067e6a9e1c3f93c760`  
		Last Modified: Tue, 03 Feb 2026 17:26:27 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ffc7844b3d362e6b692567d2587e4fd19b348dff44182f52019fdefe7ab344`  
		Last Modified: Tue, 03 Feb 2026 17:26:28 GMT  
		Size: 17.6 MB (17566404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9111fb63645fb502831d395247748514cc38c89a036c0c80ac0d68172af396`  
		Last Modified: Tue, 03 Feb 2026 17:26:29 GMT  
		Size: 26.5 MB (26546121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17318896bc84227a623de0b09b1c19d9ba46473321e3c6ef037516d813f8da1`  
		Last Modified: Tue, 03 Feb 2026 17:26:29 GMT  
		Size: 10.2 MB (10198592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f58cddeebb4c56cedfe3c4d3406be79ac683f61f8d149db919627222cd847dae`  
		Last Modified: Tue, 03 Feb 2026 17:26:29 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45cca7f5e3f5fc71d61ff7160fba4b5af52d1d5c1376ef27109056ee0bd35891`  
		Last Modified: Tue, 03 Feb 2026 17:26:30 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68671e7ea5f72eebefa27db844dfc891bba0667adb87fda60be5a0a78a9e0af3`  
		Last Modified: Tue, 03 Feb 2026 17:26:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2-cli` - unknown; unknown

```console
$ docker pull docker@sha256:725c7ed6fedc0c78099cca969de9d894742913605a635c1d1ae732d243e1f9d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a2b7afca7a73cadfc121038f2cb596614c4eff15299359ccc0fe5915a333dfa`

```dockerfile
```

-	Layers:
	-	`sha256:9fd463f063b0e999eee86b191492b64c48293c00436e4b777db697007872a8d6`  
		Last Modified: Tue, 03 Feb 2026 17:26:27 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:2bef500bc870e9a4eef5ac67cf6fef451c072f77b7351b207d74a3463c80e455
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.5 MB (65497196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cffbe99c0e2eadb1b2dd8830a3ecddedf95c08183d497287cb048586c0c94905`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:26:35 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:26:35 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:26:35 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:26:37 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:26:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:26:37 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:26:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:26:38 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:26:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:26:39 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:26:39 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42a77f5fc93e1d6c642b2eb20bac67ddedc3fa614973ecad5d2425aa529cc7f`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 8.5 MB (8453512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9817403955ea5ea2eedc37cde61397fd369d7b07e3863286754b4989d443759a`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d23c75ff3415b6637326f398bd112a7ec4373805d39318b94b65c8ff6ce7538`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 17.3 MB (17349111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfca817951310f1a68cb06e3fe0f27540e7d76c61b144cbbb1ebaa04308c8233`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 25.5 MB (25540815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7af456c729c76507dbf99635546e893dd549241c3157a2a655f1a7472544d6`  
		Last Modified: Tue, 03 Feb 2026 17:26:47 GMT  
		Size: 10.0 MB (9954516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72242c4fb87c9ebb62312863874911bfe531f06775fe6a90aa5c937db6274442`  
		Last Modified: Tue, 03 Feb 2026 17:26:47 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e91b41b56d8ea2c6e69d6ed8a929177b21cc4e84b65284dd552f20cda40c3dd`  
		Last Modified: Tue, 03 Feb 2026 17:26:48 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66fa267764c487b75a914eae88e45afb0bdd82be8b4c090d4af5946454d79964`  
		Last Modified: Tue, 03 Feb 2026 17:26:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2-cli` - unknown; unknown

```console
$ docker pull docker@sha256:22956d1b0f85ed3aaf3fbd162a232fd08241684704dc328c469298a7a60f924e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa0c6c28d5d6436cdecdceb1ee544bccb64c7a75c45b13de36e354116226cab3`

```dockerfile
```

-	Layers:
	-	`sha256:0c689b61e422b3962e7df2e52b56054a4e453d576da33fd3b1d6f7dca26d06b6`  
		Last Modified: Tue, 03 Feb 2026 17:26:45 GMT  
		Size: 38.3 KB (38258 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.2-dind`

```console
$ docker pull docker@sha256:a284d31e4db9a9916fd9be44380263eaeafedf0e3048a859f978922b5a0c16fc
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

### `docker:29.2-dind` - linux; amd64

```console
$ docker pull docker@sha256:99aa88f75d8d401c30e395db1d2e679a89ff0be9b415f020b8e2383c517e1fda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.8 MB (143799092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ca04087ca24aa6deade38370d033555d14dacd022c6a5d275f038b89eaf131`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:15:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:15:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:15:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:15:17 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:15:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:15:17 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:15:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:15:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:15:19 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:15:19 GMT
CMD ["sh"]
# Wed, 28 Jan 2026 03:58:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 Jan 2026 03:58:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 Jan 2026 03:58:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 Jan 2026 03:58:45 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
VOLUME [/var/lib/docker]
# Wed, 28 Jan 2026 03:58:45 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 Jan 2026 03:58:45 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 Jan 2026 03:58:45 GMT
CMD []
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03ce8e2700f1129dc15f38a5e1e7d27cdd2b98175c4d9ac08dc5646c3c35ba4`  
		Last Modified: Wed, 28 Jan 2026 02:15:26 GMT  
		Size: 8.4 MB (8399638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dabc00febb6a9a0d9954ef0b62272b11dabac7697dd7a0f94f9a96e241fbfd2`  
		Last Modified: Wed, 28 Jan 2026 02:15:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9408125f9d0c694cc95efc06409f73e6d6907c853a7f861c85b36824fb02ed25`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 18.8 MB (18774054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1765bbbd236eff12d3ecffaab470c2a8ade7f1432cbf0f1efe2f520cb9d74bfc`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 28.3 MB (28308902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d4f1a3f89cb924cc72cf031843e7490b98f39a276e6628c0ef444a871ff92f`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 10.8 MB (10799762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ca730a0591b75f8b903f70ff08c4b2959f397bd8775ba1a873cbb344b15c1a0`  
		Last Modified: Wed, 28 Jan 2026 02:15:28 GMT  
		Size: 533.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc93a580b636b3173550ee5a31a23ae95eb17558288345a26091285a5f477d5`  
		Last Modified: Wed, 28 Jan 2026 02:15:28 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9745309fb9885c647e35e9d55ab83308f9c212460ad5f9b73c2e518179059b72`  
		Last Modified: Wed, 28 Jan 2026 02:15:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:effa5c3a383e3a584de2fe9ef352f8fcde727e8db088492f0c8e49fc27f7abaa`  
		Last Modified: Wed, 28 Jan 2026 03:58:56 GMT  
		Size: 6.9 MB (6934734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a8f8addf621601263b2bfea9efe7ffac5903b85bfe7b9f628f7a2ff6bd4fce`  
		Last Modified: Wed, 28 Jan 2026 03:58:55 GMT  
		Size: 92.5 KB (92460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:396bcb1ae646a1eb234538a6bf406490001b6067e5626f4858b3d3ab115a1338`  
		Last Modified: Wed, 28 Jan 2026 03:58:56 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636ece6788bea2909cc3a17231a1a4827c4db266c991df7770a909ecdb8d3fd0`  
		Last Modified: Wed, 28 Jan 2026 03:58:57 GMT  
		Size: 66.6 MB (66619579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb2987d59bbd2b711c1759725d9ccc5891b03def0602234c4f49beb1e5c2be1`  
		Last Modified: Wed, 28 Jan 2026 03:58:57 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ac6a5de045400bc7b163e70c2cd9429f6202144cb50ed4b85688aded44f58e`  
		Last Modified: Wed, 28 Jan 2026 03:58:57 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2-dind` - unknown; unknown

```console
$ docker pull docker@sha256:2d2c0973782cdccc69752fb841755627c37546ebbf2f68f0bf070bf51d23ec60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0784b32a62dac2ebed2ad0ae726d2901f105b39654d58a2d2d351b4eaea7d818`

```dockerfile
```

-	Layers:
	-	`sha256:161b2e45f0098aead317dd0674b614a4e1252835a147f30b88ddc0667bf7ba93`  
		Last Modified: Wed, 28 Jan 2026 03:58:55 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:70dcad0b903a121c11d71a23834267a49327cd21053d8a2a83529cf94a2d9fbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135630532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:438bd2c6733062a94188c3067ba6118e7dda4560c7d7eb98ecec81192d5273b2`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:19:28 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:19:29 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:19:29 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:19:32 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:19:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:19:32 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:19:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:19:34 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:19:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:19:36 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:19:36 GMT
CMD ["sh"]
# Wed, 28 Jan 2026 03:49:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 Jan 2026 03:49:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 Jan 2026 03:49:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 03:49:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 Jan 2026 03:49:21 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 Jan 2026 03:49:21 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 Jan 2026 03:49:21 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:49:21 GMT
VOLUME [/var/lib/docker]
# Wed, 28 Jan 2026 03:49:21 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 Jan 2026 03:49:21 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 Jan 2026 03:49:21 GMT
CMD []
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08efb619161971b8dbf3d2d18d22c25f3caf7baea4b18537b77a961fee285e4d`  
		Last Modified: Wed, 28 Jan 2026 02:19:43 GMT  
		Size: 8.3 MB (8301019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11eae5034a08f196af9949aec8c0d0a5c776062160fbfa6839f4e91eb25c523`  
		Last Modified: Wed, 28 Jan 2026 02:19:42 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b811dd811e1e6a5a185faf36f1f9dd7bd483290fc51d98ccb7f5014b5bd19ab`  
		Last Modified: Wed, 28 Jan 2026 02:19:43 GMT  
		Size: 17.6 MB (17576540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395a6e19e8b08ce81dbf6939f7000c5eaaa78657497cffd3559c4d3586ad6f25`  
		Last Modified: Wed, 28 Jan 2026 02:19:44 GMT  
		Size: 26.6 MB (26570467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b3f84acb2b12fc7c649c003ff8e9348dabfff644a17daad4b02eef0bd9b40b6`  
		Last Modified: Wed, 28 Jan 2026 02:19:44 GMT  
		Size: 10.2 MB (10213042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746007c626ec304c1dfcf1e9084f31b26345a6079f9efe6f265b8fa508abf11a`  
		Last Modified: Wed, 28 Jan 2026 02:19:44 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f144bc5ce89728429c7674f4da3e2efbf3439669eae61e270d13a77809b4b9b7`  
		Last Modified: Wed, 28 Jan 2026 02:19:45 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b078b00f266ba4e03e79da886e567e61c21f493be073a7001f1e3db1345ccf57`  
		Last Modified: Wed, 28 Jan 2026 02:19:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6f4b2cf4256d701c8e551ce6b913b60516e7a6812dd2a6b150737145528fdf`  
		Last Modified: Wed, 28 Jan 2026 03:49:31 GMT  
		Size: 7.3 MB (7271609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b290e764c28e19f2f21aa7790d801cc6056a53cd51c8fb1bb6faf2e2346d4145`  
		Last Modified: Wed, 28 Jan 2026 03:49:30 GMT  
		Size: 91.8 KB (91775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:894eda0b2167abb0c583bbf993071a8d219941e2dd3bc2fcd1f8bfd8ca024a34`  
		Last Modified: Wed, 28 Jan 2026 03:49:30 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661a756971591996ae71af31b4d76fd40c1ba5140d25d52487a63a2ce33123b3`  
		Last Modified: Wed, 28 Jan 2026 03:49:32 GMT  
		Size: 62.0 MB (62028111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0fea802a7e013543afeb57c94b421ff42c6cc94e875a7a48079633d5b32cf0`  
		Last Modified: Wed, 28 Jan 2026 03:49:31 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89262e7e7a4c52344f56768909e409e4d52e23b7e5f872f34c6f8f05f600ced1`  
		Last Modified: Wed, 28 Jan 2026 03:49:32 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2-dind` - unknown; unknown

```console
$ docker pull docker@sha256:77efd8773fd21feb58c996858580a066f8336af75ce15a65d1e94fbfc662939f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8937de610607274348941cf30b97eee5b16a47a2a3e355daae965571f78e1b8e`

```dockerfile
```

-	Layers:
	-	`sha256:b2c9967356bfd5048f745045eb7a61d4c51f3b8a396da52f925736b964896609`  
		Last Modified: Wed, 28 Jan 2026 03:49:30 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:136f2e805834a4247060b8060063ba782a2fdce6083a3cb47d02e83936623504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133715469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a4604f36042cbaaba3fd792ec4e26bfaf62d2d45b48d38a8697760ddf3306fa`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:19:33 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:19:33 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:19:34 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:19:37 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:19:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:19:37 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:19:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:19:39 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:19:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:19:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:19:41 GMT
CMD ["sh"]
# Wed, 28 Jan 2026 03:51:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 Jan 2026 03:51:44 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 Jan 2026 03:51:44 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 03:51:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 Jan 2026 03:51:47 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 Jan 2026 03:51:47 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 Jan 2026 03:51:47 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:51:47 GMT
VOLUME [/var/lib/docker]
# Wed, 28 Jan 2026 03:51:47 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 Jan 2026 03:51:47 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 Jan 2026 03:51:47 GMT
CMD []
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef74ac3c65992e7acddcc2a2c02498d51d5fda8b771538e5411d2d5f3a3e9eec`  
		Last Modified: Wed, 28 Jan 2026 02:19:47 GMT  
		Size: 7.6 MB (7597810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01925faabefdbedf8efebb820b152e94fb287b72138d282a76557993132623ca`  
		Last Modified: Wed, 28 Jan 2026 02:19:47 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ad13ec2588fba164870da3d93ba8b5ad34e242b5bc6fb7b5df1bd055e194e0`  
		Last Modified: Wed, 28 Jan 2026 02:19:48 GMT  
		Size: 17.6 MB (17566458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc3d6d20d26654203dbb33aecb823850102a06ee1d8826eeea313f51053947d`  
		Last Modified: Wed, 28 Jan 2026 02:19:48 GMT  
		Size: 26.5 MB (26544669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309b43a06105801e72a4057c9a98aa39f845292f118ed5364be6f2c58fff6fb2`  
		Last Modified: Wed, 28 Jan 2026 02:19:48 GMT  
		Size: 10.2 MB (10198593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c018df83e09983e9c86c614e37738e0c9913c07f571d99ca7464a8eead3114`  
		Last Modified: Wed, 28 Jan 2026 02:19:49 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff08fbe96bdc955d67587b7154a9e64b5fd0933ad18112a10502a2d2ee351334`  
		Last Modified: Wed, 28 Jan 2026 02:19:49 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82766871530b6d5c5faaefb052706696dbc1f4936a761d57fe77b41476c57e81`  
		Last Modified: Wed, 28 Jan 2026 02:19:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966fa3b3930581a719871ad9cc50569b5b949938c666c5f604128567586dcc98`  
		Last Modified: Wed, 28 Jan 2026 03:51:58 GMT  
		Size: 6.6 MB (6572989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8288f87d3ec8e6d2c73fad07643b43f2c5a333b046f21c81531e877d6eaf19d4`  
		Last Modified: Wed, 28 Jan 2026 03:51:58 GMT  
		Size: 88.1 KB (88136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd5922158e4b006788c6366971c7c91cc1404b01a100da81d4c9a0477a74027`  
		Last Modified: Wed, 28 Jan 2026 03:51:58 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842a3b5326d8c1c6b696edd5624246ed13391ce31743771eb92561f224c0e672`  
		Last Modified: Wed, 28 Jan 2026 03:52:00 GMT  
		Size: 61.9 MB (61856931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f666916210054b0fd5f72affa9ac152fa7c42d927442f2dd309d354e89b9277`  
		Last Modified: Wed, 28 Jan 2026 03:51:59 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cf19ee261d3469335adb02771df03de4d7bd57f3cb5c06bb5841ae7b93697c`  
		Last Modified: Wed, 28 Jan 2026 03:51:59 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2-dind` - unknown; unknown

```console
$ docker pull docker@sha256:8457bbc8972fac13450e367c97a9a1b851c44540331c9f631abe6ecc6da554fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d30df9382a2c15c97b7086f993412c3a0f44e8ed81f835508748d782eabe5345`

```dockerfile
```

-	Layers:
	-	`sha256:0a1c8b9290fc1e34c2f218c7730ca8fc83fc55704982e288265ea392b6f0447c`  
		Last Modified: Wed, 28 Jan 2026 03:51:58 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:2cd37b1da26b3d7bdae2014ffafb6543a3c40f32973395bdf6e402afc6818e38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.2 MB (133249301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a287877d76e510dc36d4294bef0d4540628445c54cbf477d32ad4aef68e7bb0a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:15:20 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:15:20 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:15:20 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:15:22 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:15:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:15:22 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:15:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:15:23 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:15:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:15:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:15:24 GMT
CMD ["sh"]
# Wed, 28 Jan 2026 04:19:44 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 Jan 2026 04:19:44 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 Jan 2026 04:19:45 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 04:19:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 Jan 2026 04:19:48 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 Jan 2026 04:19:48 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 Jan 2026 04:19:48 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 04:19:48 GMT
VOLUME [/var/lib/docker]
# Wed, 28 Jan 2026 04:19:48 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 Jan 2026 04:19:48 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 Jan 2026 04:19:48 GMT
CMD []
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23cd2c872bdff3a89f69a977eea6049f005ee667e33468764b0584c9a8959fe3`  
		Last Modified: Wed, 28 Jan 2026 02:15:31 GMT  
		Size: 8.5 MB (8453525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a2f891a573bd6b7ff30782766b7564cfd2718e91c2399081bdf0ffb44fabba`  
		Last Modified: Wed, 28 Jan 2026 02:15:30 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f26d33b7e75cf64b24043a967d4288b682c0eba3866ed27897136240d3f4cbe`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 17.3 MB (17349909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fadf59f99eaf4a5457883e92f5eb0e9f05304f32b91ff429c77b5d12c399d17`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 25.5 MB (25539742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bbb75472d83a88fcf93366d31a9685491eaee5051b271d7e9822962477745c`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 10.0 MB (9954517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982182610648dbb0778b184ecff3e692201a2114ba00657d6fd977582e60c802`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c47f152455dabd15e5d73f9f555e031f1bf91be0a42bb7899543ca32f4be842`  
		Last Modified: Wed, 28 Jan 2026 02:15:34 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d60b69639960857109359648f1dd0dd6cb3d2cce9bdd6b1a594fd99159bf8f`  
		Last Modified: Wed, 28 Jan 2026 02:15:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf3426000179b3492ca41ec23019609bae7bd020884ba682b730f4920dcdadd`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 7.2 MB (7213335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d0c859c41e3ca1cc276016f6151a0a02e77f672f849df7d283d4657b2fd464`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 101.3 KB (101289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6748b522881f24eb97f2eed26e32bdb49ae5819b2477eae3a4976874142ff758`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:407dff81deac15d5750c410b3b45d2888514fd7173fad465cdb860a9e18a068c`  
		Last Modified: Wed, 28 Jan 2026 04:19:59 GMT  
		Size: 60.4 MB (60431745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae84a81436627202044f15c8bfbb21c37acd9371efb16eac52fa88d19fd035c`  
		Last Modified: Wed, 28 Jan 2026 04:19:58 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66e9c5f6367f5ce3bcd7921fbcd7ecdee44c87e2b3fb4e91c0953fdefb902bb`  
		Last Modified: Wed, 28 Jan 2026 04:19:58 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2-dind` - unknown; unknown

```console
$ docker pull docker@sha256:76d7445bd6915a9080071a3680a3a2dd3bfb0697d214d61d429692ed178b2519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee53cf6ac36a1613efdfec96533f5b66f1bac362f162eeed2703924705574c2d`

```dockerfile
```

-	Layers:
	-	`sha256:51f7535efd28fb94f257372f96380d2a49634a8b4664d35a295a7201ee67d470`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.2-dind-rootless`

```console
$ docker pull docker@sha256:e2256cccf0a81babdf6b0715edc84299976eea749dc373de1d4c4b98f38be576
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:29.2-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:6e740431e7ec02952bcba763683de89ae7c38ed168d0cfc4b875ffc2cc94eb01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.6 MB (164596244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:893377b7f16e5efd1e758a1c978a11516ff914ffd6896497463fae305e6732d9`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:15:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:15:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:15:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:15:17 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:15:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:15:17 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:15:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:15:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:15:19 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:15:19 GMT
CMD ["sh"]
# Wed, 28 Jan 2026 03:58:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 Jan 2026 03:58:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 Jan 2026 03:58:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 Jan 2026 03:58:45 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
VOLUME [/var/lib/docker]
# Wed, 28 Jan 2026 03:58:45 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 Jan 2026 03:58:45 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 Jan 2026 03:58:45 GMT
CMD []
# Wed, 28 Jan 2026 04:49:51 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Wed, 28 Jan 2026 04:49:51 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 28 Jan 2026 04:49:51 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 04:49:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 28 Jan 2026 04:49:52 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 28 Jan 2026 04:49:52 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 28 Jan 2026 04:49:52 GMT
USER rootless
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03ce8e2700f1129dc15f38a5e1e7d27cdd2b98175c4d9ac08dc5646c3c35ba4`  
		Last Modified: Wed, 28 Jan 2026 02:15:26 GMT  
		Size: 8.4 MB (8399638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dabc00febb6a9a0d9954ef0b62272b11dabac7697dd7a0f94f9a96e241fbfd2`  
		Last Modified: Wed, 28 Jan 2026 02:15:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9408125f9d0c694cc95efc06409f73e6d6907c853a7f861c85b36824fb02ed25`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 18.8 MB (18774054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1765bbbd236eff12d3ecffaab470c2a8ade7f1432cbf0f1efe2f520cb9d74bfc`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 28.3 MB (28308902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d4f1a3f89cb924cc72cf031843e7490b98f39a276e6628c0ef444a871ff92f`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 10.8 MB (10799762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ca730a0591b75f8b903f70ff08c4b2959f397bd8775ba1a873cbb344b15c1a0`  
		Last Modified: Wed, 28 Jan 2026 02:15:28 GMT  
		Size: 533.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc93a580b636b3173550ee5a31a23ae95eb17558288345a26091285a5f477d5`  
		Last Modified: Wed, 28 Jan 2026 02:15:28 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9745309fb9885c647e35e9d55ab83308f9c212460ad5f9b73c2e518179059b72`  
		Last Modified: Wed, 28 Jan 2026 02:15:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:effa5c3a383e3a584de2fe9ef352f8fcde727e8db088492f0c8e49fc27f7abaa`  
		Last Modified: Wed, 28 Jan 2026 03:58:56 GMT  
		Size: 6.9 MB (6934734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a8f8addf621601263b2bfea9efe7ffac5903b85bfe7b9f628f7a2ff6bd4fce`  
		Last Modified: Wed, 28 Jan 2026 03:58:55 GMT  
		Size: 92.5 KB (92460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:396bcb1ae646a1eb234538a6bf406490001b6067e5626f4858b3d3ab115a1338`  
		Last Modified: Wed, 28 Jan 2026 03:58:56 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636ece6788bea2909cc3a17231a1a4827c4db266c991df7770a909ecdb8d3fd0`  
		Last Modified: Wed, 28 Jan 2026 03:58:57 GMT  
		Size: 66.6 MB (66619579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb2987d59bbd2b711c1759725d9ccc5891b03def0602234c4f49beb1e5c2be1`  
		Last Modified: Wed, 28 Jan 2026 03:58:57 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ac6a5de045400bc7b163e70c2cd9429f6202144cb50ed4b85688aded44f58e`  
		Last Modified: Wed, 28 Jan 2026 03:58:57 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:733f26c740596bada2273b63c30df575d6fe75108c34ae59cf6cce23eb6fde38`  
		Last Modified: Wed, 28 Jan 2026 04:49:58 GMT  
		Size: 3.4 MB (3419936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9b0d647df5d90a456bfb18e7fe3512570e5501e17a96c28d0673f36c7de2ab`  
		Last Modified: Wed, 28 Jan 2026 04:49:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2266ba1a98fbf4bf56e7477a64291015ffc22febbdef7b5c52756c0bccea91bc`  
		Last Modified: Wed, 28 Jan 2026 04:49:58 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e7bef04bfc2f8ecbd179e44e594aea6870289cac0095619a71f9ae48c070b2`  
		Last Modified: Wed, 28 Jan 2026 04:49:59 GMT  
		Size: 17.4 MB (17375872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de36060bb1e57bb0070a546b5af68c0c667dfc7c88ad9c5e0b4b58cd903fdd5f`  
		Last Modified: Wed, 28 Jan 2026 04:49:59 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:304a9bab4d48983bd4f25caa7723d4ff17feec1769ef4b9d815a85818b33f85a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18a9fa96564b6f3cbe5f035361ffe48a58c26e0d28c673a4517c0afb4d19bd17`

```dockerfile
```

-	Layers:
	-	`sha256:f20e17ed780eccbdcae7df7f23b087c7750a8fca8f1ef231ace886ff1ec41145`  
		Last Modified: Wed, 28 Jan 2026 04:49:58 GMT  
		Size: 30.6 KB (30589 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:10185cf7e9ecf2d725eabaed0f994c40d28c4ca77f04234d07c2bb0efcd4c588
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154355521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f80a4777f73ae85118338e6c79bca8a28937df9dc8a5f912a5066951db75e2a7`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:15:20 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:15:20 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:15:20 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:15:22 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:15:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:15:22 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:15:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:15:23 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:15:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:15:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:15:24 GMT
CMD ["sh"]
# Wed, 28 Jan 2026 04:19:44 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 Jan 2026 04:19:44 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 Jan 2026 04:19:45 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 04:19:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 Jan 2026 04:19:48 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 Jan 2026 04:19:48 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 Jan 2026 04:19:48 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 04:19:48 GMT
VOLUME [/var/lib/docker]
# Wed, 28 Jan 2026 04:19:48 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 Jan 2026 04:19:48 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 Jan 2026 04:19:48 GMT
CMD []
# Wed, 28 Jan 2026 05:26:30 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Wed, 28 Jan 2026 05:26:30 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 28 Jan 2026 05:26:30 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 05:26:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 28 Jan 2026 05:26:31 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 28 Jan 2026 05:26:31 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 28 Jan 2026 05:26:31 GMT
USER rootless
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23cd2c872bdff3a89f69a977eea6049f005ee667e33468764b0584c9a8959fe3`  
		Last Modified: Wed, 28 Jan 2026 02:15:31 GMT  
		Size: 8.5 MB (8453525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a2f891a573bd6b7ff30782766b7564cfd2718e91c2399081bdf0ffb44fabba`  
		Last Modified: Wed, 28 Jan 2026 02:15:30 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f26d33b7e75cf64b24043a967d4288b682c0eba3866ed27897136240d3f4cbe`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 17.3 MB (17349909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fadf59f99eaf4a5457883e92f5eb0e9f05304f32b91ff429c77b5d12c399d17`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 25.5 MB (25539742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bbb75472d83a88fcf93366d31a9685491eaee5051b271d7e9822962477745c`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 10.0 MB (9954517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982182610648dbb0778b184ecff3e692201a2114ba00657d6fd977582e60c802`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c47f152455dabd15e5d73f9f555e031f1bf91be0a42bb7899543ca32f4be842`  
		Last Modified: Wed, 28 Jan 2026 02:15:34 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d60b69639960857109359648f1dd0dd6cb3d2cce9bdd6b1a594fd99159bf8f`  
		Last Modified: Wed, 28 Jan 2026 02:15:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf3426000179b3492ca41ec23019609bae7bd020884ba682b730f4920dcdadd`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 7.2 MB (7213335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d0c859c41e3ca1cc276016f6151a0a02e77f672f849df7d283d4657b2fd464`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 101.3 KB (101289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6748b522881f24eb97f2eed26e32bdb49ae5819b2477eae3a4976874142ff758`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:407dff81deac15d5750c410b3b45d2888514fd7173fad465cdb860a9e18a068c`  
		Last Modified: Wed, 28 Jan 2026 04:19:59 GMT  
		Size: 60.4 MB (60431745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae84a81436627202044f15c8bfbb21c37acd9371efb16eac52fa88d19fd035c`  
		Last Modified: Wed, 28 Jan 2026 04:19:58 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66e9c5f6367f5ce3bcd7921fbcd7ecdee44c87e2b3fb4e91c0953fdefb902bb`  
		Last Modified: Wed, 28 Jan 2026 04:19:58 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b2ca6f15a1175824a8ac624e8e96c03e577d7045335b3b8da66fa925ac730e`  
		Last Modified: Wed, 28 Jan 2026 05:26:37 GMT  
		Size: 3.4 MB (3394379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aae4fb46b816b0c2dabc0ce7fb6de979a1297033cfc1d63f2330898b865858f`  
		Last Modified: Wed, 28 Jan 2026 05:26:37 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0ee34b605800e64fa4c7d8ae1e8b3a28b7a99fb9273d49a13ddc555bda1daa5`  
		Last Modified: Wed, 28 Jan 2026 05:26:37 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4850780d6ebb6a4c34ff107ae6908c6afecf589851309b1c501eea08aadde6b2`  
		Last Modified: Wed, 28 Jan 2026 05:26:38 GMT  
		Size: 17.7 MB (17710501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b19d5a6a20d8289c916e7596e72a2d20595e4e8c11ae662f0ce57a9c05814f1`  
		Last Modified: Wed, 28 Jan 2026 05:26:38 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:c4559aefd8beb1182fc0607820b2e0c38fe82f9a6af4f47c78173a966859ba4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50641e7994aded7de3b8033e71f36c7fa1b0b852dc54cb3365dbfd3de2e376b6`

```dockerfile
```

-	Layers:
	-	`sha256:2e936dbc59719f822df84bc05b46cb1f559506d9e7912ed2c9c670c5b0a6d64c`  
		Last Modified: Wed, 28 Jan 2026 05:26:37 GMT  
		Size: 30.8 KB (30753 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.2-windowsservercore`

```console
$ docker pull docker@sha256:79cb1793605b4f2d7317cea6706862e4b002e6ace6375912bab555eebfdf6ed2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `docker:29.2-windowsservercore` - windows version 10.0.26100.32230; amd64

```console
$ docker pull docker@sha256:c5d3ecbfcaeb424c90459ac8317405555d19b1b8b3e578390234d4a8e7c24c64
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1556599774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d647b193ba9f5cb583f9fb294f2d532c6d85295880ef0649d60793cc309abcd1`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Tue, 03 Feb 2026 17:28:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 03 Feb 2026 17:29:28 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 03 Feb 2026 17:29:30 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:29:32 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.1.zip
# Tue, 03 Feb 2026 17:29:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 03 Feb 2026 17:29:46 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:29:48 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.windows-amd64.exe
# Tue, 03 Feb 2026 17:29:48 GMT
ENV DOCKER_BUILDX_SHA256=b49832d4ac46bde05006f7ad3506b9d5060b60e5c566545d8e10c1a80df08a4a
# Tue, 03 Feb 2026 17:29:59 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 03 Feb 2026 17:30:00 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:30:01 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Tue, 03 Feb 2026 17:30:01 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Tue, 03 Feb 2026 17:30:08 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3345d2727a1883e3d335172c07a1f0f478ed9c744e1aa4ec455219fd5b041b31`  
		Last Modified: Tue, 03 Feb 2026 17:30:17 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c2b758f14303d714990de0fad8eacb8f18d18925809a064fa024e0a8203573a`  
		Last Modified: Tue, 03 Feb 2026 17:30:16 GMT  
		Size: 402.8 KB (402791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c544aebc260938057720752277d7e0b5a599ebf13c36d8be0403e694d8929db8`  
		Last Modified: Tue, 03 Feb 2026 17:30:15 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54275eb139ff712b0a5f139cdba772a69cd2371fcb0b65f6371b8d8b22f92c19`  
		Last Modified: Tue, 03 Feb 2026 17:30:15 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff99eb3d4bee14899afa2383e60cfa18a0f63d88f5c759afcbfa0cef9bae50bb`  
		Last Modified: Tue, 03 Feb 2026 17:30:18 GMT  
		Size: 19.5 MB (19477937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d8a57f5276cfc049bae3b7a853039be549c9bada93ef2e8d868ea54e9c04236`  
		Last Modified: Tue, 03 Feb 2026 17:30:14 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be178348f9fba72db323ad766660239b1363bbe80d1f01cf90cd2531b5f01b03`  
		Last Modified: Tue, 03 Feb 2026 17:30:14 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca77ca63bd7d4b72f07134cb3691a9edeba02acdb61fb8ff15a7f6c7f44734ce`  
		Last Modified: Tue, 03 Feb 2026 17:30:14 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51aa328a4c51fa2977445e97c24b485b2fbf132d207a9adfa58cf7406f3f8a1f`  
		Last Modified: Tue, 03 Feb 2026 17:30:30 GMT  
		Size: 29.5 MB (29453041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c300d10089e1c370f164537efd3c43df949644198f422eb4863dccfe9930a4f`  
		Last Modified: Tue, 03 Feb 2026 17:30:12 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5356d434dcd14c58d539907321e96d2a0e794ac74a29c08aa2df1dbaa611e231`  
		Last Modified: Tue, 03 Feb 2026 17:30:12 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b03bbb60e30cb160ee1c1c6844849f758718d7111a7cb510a1b0ec1702120fd`  
		Last Modified: Tue, 03 Feb 2026 17:30:12 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2d04ad8db9950e63dbd9118d08d70484b5aed5cf9dadf9591e16f2a8339e8e`  
		Last Modified: Tue, 03 Feb 2026 17:30:14 GMT  
		Size: 11.5 MB (11493926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:29.2-windowsservercore` - windows version 10.0.20348.4648; amd64

```console
$ docker pull docker@sha256:ba1e9a93d62651a48e0592e4a6010300708e2422e46df2b25d54b1d2f1e7fb47
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1896494534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a09c7520bcdba0cceb87d9e1fe705ea6641137be025705d09eaba1893561ddea`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Tue, 03 Feb 2026 17:28:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 03 Feb 2026 17:29:49 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 03 Feb 2026 17:29:49 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:29:50 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.1.zip
# Tue, 03 Feb 2026 17:30:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 03 Feb 2026 17:30:17 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:30:18 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.windows-amd64.exe
# Tue, 03 Feb 2026 17:30:18 GMT
ENV DOCKER_BUILDX_SHA256=b49832d4ac46bde05006f7ad3506b9d5060b60e5c566545d8e10c1a80df08a4a
# Tue, 03 Feb 2026 17:30:49 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 03 Feb 2026 17:30:50 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:30:52 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Tue, 03 Feb 2026 17:30:52 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Tue, 03 Feb 2026 17:31:09 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1610c61d22cce1c0da1f89bcf2b2b93db5d1ee6703ddda8c50c992a55a3a3273`  
		Last Modified: Tue, 03 Feb 2026 17:31:19 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35301633ca92d436f45505192a1ef4f18618178fd179a0275e79d55f1cdba61d`  
		Last Modified: Tue, 03 Feb 2026 17:31:19 GMT  
		Size: 502.0 KB (501985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc76ce47c4de88873c339dee382928f8c2afe957a1f67eaa1bc1745de35e796e`  
		Last Modified: Tue, 03 Feb 2026 17:31:18 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c0a93da300b8f2017782995a21ddcc03360f0068884e95f2c90a34943b5a853`  
		Last Modified: Tue, 03 Feb 2026 17:31:18 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4642a451e4aa3a689441cf53a384a5333b79045931964aecc32acb75dab6242f`  
		Last Modified: Tue, 03 Feb 2026 17:31:20 GMT  
		Size: 19.4 MB (19440499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f80fcdb722aba8bdf0a57b047c109edce18d999e3bc1649781fa0d3de37c6e29`  
		Last Modified: Tue, 03 Feb 2026 17:31:16 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52573eb20ed9e08365fa5f5e972f07f60f80fd44870b2c8c2e00435b86e529d7`  
		Last Modified: Tue, 03 Feb 2026 17:31:16 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc93a0644ac21577feac91654ceef3e9cb714742257794765b8f41f26967f84e`  
		Last Modified: Tue, 03 Feb 2026 17:31:16 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c020b7de7a60805f5e0f214c5933b5730ce1e22475c6c0637dbe59005c03baa4`  
		Last Modified: Tue, 03 Feb 2026 17:31:33 GMT  
		Size: 29.4 MB (29425091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:538b00d976a03c45b55d387636033ba066f8d59660d195f26399a156232cb079`  
		Last Modified: Tue, 03 Feb 2026 17:31:14 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f8c0456ab18eeca4e06f6a4f1edc155807d2fd8565b3c71217f4895c0778536`  
		Last Modified: Tue, 03 Feb 2026 17:31:14 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525c0f16947c0cc46484ca50b3cbe0be998327c9e218a8f15dd79b3752be1f84`  
		Last Modified: Tue, 03 Feb 2026 17:31:14 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f29f86a605fc1d2ecf16f261c2beeb1261773d00bba4c7341e76d2363f15db4a`  
		Last Modified: Tue, 03 Feb 2026 17:31:16 GMT  
		Size: 11.5 MB (11456032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.2-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:315827d701f9fef8731fca2a65b1c5960422bfb5d0e6f335995310b4c2c2bf07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `docker:29.2-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull docker@sha256:ba1e9a93d62651a48e0592e4a6010300708e2422e46df2b25d54b1d2f1e7fb47
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1896494534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a09c7520bcdba0cceb87d9e1fe705ea6641137be025705d09eaba1893561ddea`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Tue, 03 Feb 2026 17:28:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 03 Feb 2026 17:29:49 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 03 Feb 2026 17:29:49 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:29:50 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.1.zip
# Tue, 03 Feb 2026 17:30:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 03 Feb 2026 17:30:17 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:30:18 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.windows-amd64.exe
# Tue, 03 Feb 2026 17:30:18 GMT
ENV DOCKER_BUILDX_SHA256=b49832d4ac46bde05006f7ad3506b9d5060b60e5c566545d8e10c1a80df08a4a
# Tue, 03 Feb 2026 17:30:49 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 03 Feb 2026 17:30:50 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:30:52 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Tue, 03 Feb 2026 17:30:52 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Tue, 03 Feb 2026 17:31:09 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1610c61d22cce1c0da1f89bcf2b2b93db5d1ee6703ddda8c50c992a55a3a3273`  
		Last Modified: Tue, 03 Feb 2026 17:31:19 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35301633ca92d436f45505192a1ef4f18618178fd179a0275e79d55f1cdba61d`  
		Last Modified: Tue, 03 Feb 2026 17:31:19 GMT  
		Size: 502.0 KB (501985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc76ce47c4de88873c339dee382928f8c2afe957a1f67eaa1bc1745de35e796e`  
		Last Modified: Tue, 03 Feb 2026 17:31:18 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c0a93da300b8f2017782995a21ddcc03360f0068884e95f2c90a34943b5a853`  
		Last Modified: Tue, 03 Feb 2026 17:31:18 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4642a451e4aa3a689441cf53a384a5333b79045931964aecc32acb75dab6242f`  
		Last Modified: Tue, 03 Feb 2026 17:31:20 GMT  
		Size: 19.4 MB (19440499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f80fcdb722aba8bdf0a57b047c109edce18d999e3bc1649781fa0d3de37c6e29`  
		Last Modified: Tue, 03 Feb 2026 17:31:16 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52573eb20ed9e08365fa5f5e972f07f60f80fd44870b2c8c2e00435b86e529d7`  
		Last Modified: Tue, 03 Feb 2026 17:31:16 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc93a0644ac21577feac91654ceef3e9cb714742257794765b8f41f26967f84e`  
		Last Modified: Tue, 03 Feb 2026 17:31:16 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c020b7de7a60805f5e0f214c5933b5730ce1e22475c6c0637dbe59005c03baa4`  
		Last Modified: Tue, 03 Feb 2026 17:31:33 GMT  
		Size: 29.4 MB (29425091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:538b00d976a03c45b55d387636033ba066f8d59660d195f26399a156232cb079`  
		Last Modified: Tue, 03 Feb 2026 17:31:14 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f8c0456ab18eeca4e06f6a4f1edc155807d2fd8565b3c71217f4895c0778536`  
		Last Modified: Tue, 03 Feb 2026 17:31:14 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525c0f16947c0cc46484ca50b3cbe0be998327c9e218a8f15dd79b3752be1f84`  
		Last Modified: Tue, 03 Feb 2026 17:31:14 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f29f86a605fc1d2ecf16f261c2beeb1261773d00bba4c7341e76d2363f15db4a`  
		Last Modified: Tue, 03 Feb 2026 17:31:16 GMT  
		Size: 11.5 MB (11456032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.2-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:ed671d3152d0f57a459cd9f0838f7e48071ccef5c71ad1188693f4540f24cf19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32230; amd64

### `docker:29.2-windowsservercore-ltsc2025` - windows version 10.0.26100.32230; amd64

```console
$ docker pull docker@sha256:c5d3ecbfcaeb424c90459ac8317405555d19b1b8b3e578390234d4a8e7c24c64
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1556599774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d647b193ba9f5cb583f9fb294f2d532c6d85295880ef0649d60793cc309abcd1`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Tue, 03 Feb 2026 17:28:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 03 Feb 2026 17:29:28 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 03 Feb 2026 17:29:30 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:29:32 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.1.zip
# Tue, 03 Feb 2026 17:29:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 03 Feb 2026 17:29:46 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:29:48 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.windows-amd64.exe
# Tue, 03 Feb 2026 17:29:48 GMT
ENV DOCKER_BUILDX_SHA256=b49832d4ac46bde05006f7ad3506b9d5060b60e5c566545d8e10c1a80df08a4a
# Tue, 03 Feb 2026 17:29:59 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 03 Feb 2026 17:30:00 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:30:01 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Tue, 03 Feb 2026 17:30:01 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Tue, 03 Feb 2026 17:30:08 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3345d2727a1883e3d335172c07a1f0f478ed9c744e1aa4ec455219fd5b041b31`  
		Last Modified: Tue, 03 Feb 2026 17:30:17 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c2b758f14303d714990de0fad8eacb8f18d18925809a064fa024e0a8203573a`  
		Last Modified: Tue, 03 Feb 2026 17:30:16 GMT  
		Size: 402.8 KB (402791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c544aebc260938057720752277d7e0b5a599ebf13c36d8be0403e694d8929db8`  
		Last Modified: Tue, 03 Feb 2026 17:30:15 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54275eb139ff712b0a5f139cdba772a69cd2371fcb0b65f6371b8d8b22f92c19`  
		Last Modified: Tue, 03 Feb 2026 17:30:15 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff99eb3d4bee14899afa2383e60cfa18a0f63d88f5c759afcbfa0cef9bae50bb`  
		Last Modified: Tue, 03 Feb 2026 17:30:18 GMT  
		Size: 19.5 MB (19477937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d8a57f5276cfc049bae3b7a853039be549c9bada93ef2e8d868ea54e9c04236`  
		Last Modified: Tue, 03 Feb 2026 17:30:14 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be178348f9fba72db323ad766660239b1363bbe80d1f01cf90cd2531b5f01b03`  
		Last Modified: Tue, 03 Feb 2026 17:30:14 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca77ca63bd7d4b72f07134cb3691a9edeba02acdb61fb8ff15a7f6c7f44734ce`  
		Last Modified: Tue, 03 Feb 2026 17:30:14 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51aa328a4c51fa2977445e97c24b485b2fbf132d207a9adfa58cf7406f3f8a1f`  
		Last Modified: Tue, 03 Feb 2026 17:30:30 GMT  
		Size: 29.5 MB (29453041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c300d10089e1c370f164537efd3c43df949644198f422eb4863dccfe9930a4f`  
		Last Modified: Tue, 03 Feb 2026 17:30:12 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5356d434dcd14c58d539907321e96d2a0e794ac74a29c08aa2df1dbaa611e231`  
		Last Modified: Tue, 03 Feb 2026 17:30:12 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b03bbb60e30cb160ee1c1c6844849f758718d7111a7cb510a1b0ec1702120fd`  
		Last Modified: Tue, 03 Feb 2026 17:30:12 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2d04ad8db9950e63dbd9118d08d70484b5aed5cf9dadf9591e16f2a8339e8e`  
		Last Modified: Tue, 03 Feb 2026 17:30:14 GMT  
		Size: 11.5 MB (11493926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.2.1`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:29.2.1-alpine3.23`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:29.2.1-cli`

```console
$ docker pull docker@sha256:1d6d751f1d68d1a5142c23c730ef5ecc976a8e050fa08c3cdb09f7e2e54a4439
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

### `docker:29.2.1-cli` - linux; amd64

```console
$ docker pull docker@sha256:0c04277b44d1d448d40238faa142c2edf21d4a90dc0d61486c32056bbf11572a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70148082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90fa388e81d5f66d9d9ee840c5375a0801629a980c3d9657463257b2c863f324`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:25:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:25:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:25:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:25:58 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:25:58 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:25:58 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:25:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:25:59 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:26:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:26:00 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:26:00 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ffbc9e9d61a3a427749366541c9e55c1440658b296b288726282a7e3a200f3`  
		Last Modified: Tue, 03 Feb 2026 17:26:07 GMT  
		Size: 8.4 MB (8399657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9130c567f6fc24a30ebaa5979b9c6700d6c174c3a52a1e753c42621bfb1a32d9`  
		Last Modified: Tue, 03 Feb 2026 17:26:07 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b75aa627f4cd980f8d8c3e7be1834e54e286a6499508105b6f72c4a373c7a6e`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 18.8 MB (18773130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c979ccecd955439750b7f01789bf427e4c8d60acbf2b4a12100ff3173aea9b`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 28.3 MB (28311545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217f84c60501e3b3fb548f194b2861bfcb2a70aa12a9abe9b0d4ee342d75a7b5`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 10.8 MB (10799774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bf8952411ee385ba36420d9b6bdcc36594a8be8bdace8fe62d7d97f81322411`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f757cc0a441eaf36dbebd029cb42e59a8c463fb4ea19e2ec6bf557d5a981dc2`  
		Last Modified: Tue, 03 Feb 2026 17:26:09 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7358b0dc3398fd6f4c32455892c6ab6fbc099f1a8e62df04445dec7663a095`  
		Last Modified: Tue, 03 Feb 2026 17:26:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:c1620c41ed6e739f033f9e98a5bba1cb95e1ea6a093197beb216823c8c93ce72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c5f4666aeb7f994fb855d5fb4b289608e198a0a0b59b25161f28433aeb36364`

```dockerfile
```

-	Layers:
	-	`sha256:19b63918903a6b77f5af72e60038c44df3a84e5a4563b3db3d54ef79567b8195`  
		Last Modified: Tue, 03 Feb 2026 17:26:07 GMT  
		Size: 38.1 KB (38056 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2.1-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:cf09d93cea103396a11b1b12c36c15b6b93d367c0c80cce733f00214c71c92e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66235505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4367f8d4a4b3fc3d463d69bca54b902b58d4792ccf8967224e2ec3dd7aa4afb4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:25:26 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:25:26 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:25:26 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:25:31 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:25:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:25:31 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:25:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:25:33 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:25:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:25:35 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:25:35 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ed7f28a4b26e2736ceb8045d972a5f166880f3b93b1ce13d7cb7710819f7c0`  
		Last Modified: Tue, 03 Feb 2026 17:25:42 GMT  
		Size: 8.3 MB (8300971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59982a56599ba445b45c1ff95a9bf2efe937cb3105d8107453c37e42aa96ab06`  
		Last Modified: Tue, 03 Feb 2026 17:25:41 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627db20a49a4f2be2d19fe161406f293a8b8804c985028e04c1cd95f0c40d96e`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 17.6 MB (17575014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acd42cfefd8cbfbea51ccc805027f78eefae1b3ad5cb91c207ebf9578a6a855`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 26.6 MB (26574500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac22564cea85937e49534e5ef435197d6c83fb053c5aa91ffddb70acae2ff81`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 10.2 MB (10213046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8735f9cb2ee8a9b930cd6b2bf3885083108a83a3707f302210e9bb0a138c15ec`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf43e9302aee150c8b25e6f5c53d2eb8642dd7db31500f8f7e980a6639b3d75`  
		Last Modified: Tue, 03 Feb 2026 17:25:44 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52ca294aaca561ae37709af7d9406792302f6ac4cfe16d2068ba04176c0aa2a`  
		Last Modified: Tue, 03 Feb 2026 17:25:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:fbcdf3246eea54b7103bc19f384cd3f454538bd499af80a1566455c68e652971
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f63de4e3179da9faef11522e19444ae1387215588371c787a0b6852c464dcd77`

```dockerfile
```

-	Layers:
	-	`sha256:97d51d656e276dcee240923733068124918a337234be2ffb56edcdb70a458855`  
		Last Modified: Tue, 03 Feb 2026 17:25:41 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2.1-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:ba03aff6e89a96861c91cbe97855b49f31e816c782afaa8225043cb76f7ae372
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65192844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:985b778ba8e60d8ceaa28fed60316b7c31c5ff3e18d6afb37619d388a8da92b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:26:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:26:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:26:11 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:26:15 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:26:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:26:15 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:26:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:26:19 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:26:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:26:20 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:26:20 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb5af91453d1293030fbe90db4c6166609f99510d3fcec579be00a21249cbf2`  
		Last Modified: Tue, 03 Feb 2026 17:26:28 GMT  
		Size: 7.6 MB (7597849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7fbe9447e7591ff3854f01ba9776952a93a9c4f22447067e6a9e1c3f93c760`  
		Last Modified: Tue, 03 Feb 2026 17:26:27 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ffc7844b3d362e6b692567d2587e4fd19b348dff44182f52019fdefe7ab344`  
		Last Modified: Tue, 03 Feb 2026 17:26:28 GMT  
		Size: 17.6 MB (17566404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9111fb63645fb502831d395247748514cc38c89a036c0c80ac0d68172af396`  
		Last Modified: Tue, 03 Feb 2026 17:26:29 GMT  
		Size: 26.5 MB (26546121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17318896bc84227a623de0b09b1c19d9ba46473321e3c6ef037516d813f8da1`  
		Last Modified: Tue, 03 Feb 2026 17:26:29 GMT  
		Size: 10.2 MB (10198592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f58cddeebb4c56cedfe3c4d3406be79ac683f61f8d149db919627222cd847dae`  
		Last Modified: Tue, 03 Feb 2026 17:26:29 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45cca7f5e3f5fc71d61ff7160fba4b5af52d1d5c1376ef27109056ee0bd35891`  
		Last Modified: Tue, 03 Feb 2026 17:26:30 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68671e7ea5f72eebefa27db844dfc891bba0667adb87fda60be5a0a78a9e0af3`  
		Last Modified: Tue, 03 Feb 2026 17:26:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:725c7ed6fedc0c78099cca969de9d894742913605a635c1d1ae732d243e1f9d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a2b7afca7a73cadfc121038f2cb596614c4eff15299359ccc0fe5915a333dfa`

```dockerfile
```

-	Layers:
	-	`sha256:9fd463f063b0e999eee86b191492b64c48293c00436e4b777db697007872a8d6`  
		Last Modified: Tue, 03 Feb 2026 17:26:27 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2.1-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:2bef500bc870e9a4eef5ac67cf6fef451c072f77b7351b207d74a3463c80e455
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.5 MB (65497196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cffbe99c0e2eadb1b2dd8830a3ecddedf95c08183d497287cb048586c0c94905`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:26:35 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:26:35 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:26:35 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:26:37 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:26:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:26:37 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:26:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:26:38 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:26:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:26:39 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:26:39 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42a77f5fc93e1d6c642b2eb20bac67ddedc3fa614973ecad5d2425aa529cc7f`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 8.5 MB (8453512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9817403955ea5ea2eedc37cde61397fd369d7b07e3863286754b4989d443759a`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d23c75ff3415b6637326f398bd112a7ec4373805d39318b94b65c8ff6ce7538`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 17.3 MB (17349111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfca817951310f1a68cb06e3fe0f27540e7d76c61b144cbbb1ebaa04308c8233`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 25.5 MB (25540815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7af456c729c76507dbf99635546e893dd549241c3157a2a655f1a7472544d6`  
		Last Modified: Tue, 03 Feb 2026 17:26:47 GMT  
		Size: 10.0 MB (9954516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72242c4fb87c9ebb62312863874911bfe531f06775fe6a90aa5c937db6274442`  
		Last Modified: Tue, 03 Feb 2026 17:26:47 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e91b41b56d8ea2c6e69d6ed8a929177b21cc4e84b65284dd552f20cda40c3dd`  
		Last Modified: Tue, 03 Feb 2026 17:26:48 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66fa267764c487b75a914eae88e45afb0bdd82be8b4c090d4af5946454d79964`  
		Last Modified: Tue, 03 Feb 2026 17:26:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:22956d1b0f85ed3aaf3fbd162a232fd08241684704dc328c469298a7a60f924e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa0c6c28d5d6436cdecdceb1ee544bccb64c7a75c45b13de36e354116226cab3`

```dockerfile
```

-	Layers:
	-	`sha256:0c689b61e422b3962e7df2e52b56054a4e453d576da33fd3b1d6f7dca26d06b6`  
		Last Modified: Tue, 03 Feb 2026 17:26:45 GMT  
		Size: 38.3 KB (38258 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.2.1-cli-alpine3.23`

```console
$ docker pull docker@sha256:1d6d751f1d68d1a5142c23c730ef5ecc976a8e050fa08c3cdb09f7e2e54a4439
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

### `docker:29.2.1-cli-alpine3.23` - linux; amd64

```console
$ docker pull docker@sha256:0c04277b44d1d448d40238faa142c2edf21d4a90dc0d61486c32056bbf11572a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70148082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90fa388e81d5f66d9d9ee840c5375a0801629a980c3d9657463257b2c863f324`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:25:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:25:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:25:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:25:58 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:25:58 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:25:58 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:25:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:25:59 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:26:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:26:00 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:26:00 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ffbc9e9d61a3a427749366541c9e55c1440658b296b288726282a7e3a200f3`  
		Last Modified: Tue, 03 Feb 2026 17:26:07 GMT  
		Size: 8.4 MB (8399657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9130c567f6fc24a30ebaa5979b9c6700d6c174c3a52a1e753c42621bfb1a32d9`  
		Last Modified: Tue, 03 Feb 2026 17:26:07 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b75aa627f4cd980f8d8c3e7be1834e54e286a6499508105b6f72c4a373c7a6e`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 18.8 MB (18773130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c979ccecd955439750b7f01789bf427e4c8d60acbf2b4a12100ff3173aea9b`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 28.3 MB (28311545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217f84c60501e3b3fb548f194b2861bfcb2a70aa12a9abe9b0d4ee342d75a7b5`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 10.8 MB (10799774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bf8952411ee385ba36420d9b6bdcc36594a8be8bdace8fe62d7d97f81322411`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f757cc0a441eaf36dbebd029cb42e59a8c463fb4ea19e2ec6bf557d5a981dc2`  
		Last Modified: Tue, 03 Feb 2026 17:26:09 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7358b0dc3398fd6f4c32455892c6ab6fbc099f1a8e62df04445dec7663a095`  
		Last Modified: Tue, 03 Feb 2026 17:26:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.1-cli-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:c1620c41ed6e739f033f9e98a5bba1cb95e1ea6a093197beb216823c8c93ce72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c5f4666aeb7f994fb855d5fb4b289608e198a0a0b59b25161f28433aeb36364`

```dockerfile
```

-	Layers:
	-	`sha256:19b63918903a6b77f5af72e60038c44df3a84e5a4563b3db3d54ef79567b8195`  
		Last Modified: Tue, 03 Feb 2026 17:26:07 GMT  
		Size: 38.1 KB (38056 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2.1-cli-alpine3.23` - linux; arm variant v6

```console
$ docker pull docker@sha256:cf09d93cea103396a11b1b12c36c15b6b93d367c0c80cce733f00214c71c92e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66235505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4367f8d4a4b3fc3d463d69bca54b902b58d4792ccf8967224e2ec3dd7aa4afb4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:25:26 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:25:26 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:25:26 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:25:31 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:25:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:25:31 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:25:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:25:33 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:25:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:25:35 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:25:35 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ed7f28a4b26e2736ceb8045d972a5f166880f3b93b1ce13d7cb7710819f7c0`  
		Last Modified: Tue, 03 Feb 2026 17:25:42 GMT  
		Size: 8.3 MB (8300971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59982a56599ba445b45c1ff95a9bf2efe937cb3105d8107453c37e42aa96ab06`  
		Last Modified: Tue, 03 Feb 2026 17:25:41 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627db20a49a4f2be2d19fe161406f293a8b8804c985028e04c1cd95f0c40d96e`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 17.6 MB (17575014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acd42cfefd8cbfbea51ccc805027f78eefae1b3ad5cb91c207ebf9578a6a855`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 26.6 MB (26574500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac22564cea85937e49534e5ef435197d6c83fb053c5aa91ffddb70acae2ff81`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 10.2 MB (10213046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8735f9cb2ee8a9b930cd6b2bf3885083108a83a3707f302210e9bb0a138c15ec`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf43e9302aee150c8b25e6f5c53d2eb8642dd7db31500f8f7e980a6639b3d75`  
		Last Modified: Tue, 03 Feb 2026 17:25:44 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52ca294aaca561ae37709af7d9406792302f6ac4cfe16d2068ba04176c0aa2a`  
		Last Modified: Tue, 03 Feb 2026 17:25:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.1-cli-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:fbcdf3246eea54b7103bc19f384cd3f454538bd499af80a1566455c68e652971
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f63de4e3179da9faef11522e19444ae1387215588371c787a0b6852c464dcd77`

```dockerfile
```

-	Layers:
	-	`sha256:97d51d656e276dcee240923733068124918a337234be2ffb56edcdb70a458855`  
		Last Modified: Tue, 03 Feb 2026 17:25:41 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2.1-cli-alpine3.23` - linux; arm variant v7

```console
$ docker pull docker@sha256:ba03aff6e89a96861c91cbe97855b49f31e816c782afaa8225043cb76f7ae372
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65192844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:985b778ba8e60d8ceaa28fed60316b7c31c5ff3e18d6afb37619d388a8da92b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:26:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:26:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:26:11 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:26:15 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:26:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:26:15 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:26:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:26:19 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:26:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:26:20 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:26:20 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb5af91453d1293030fbe90db4c6166609f99510d3fcec579be00a21249cbf2`  
		Last Modified: Tue, 03 Feb 2026 17:26:28 GMT  
		Size: 7.6 MB (7597849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7fbe9447e7591ff3854f01ba9776952a93a9c4f22447067e6a9e1c3f93c760`  
		Last Modified: Tue, 03 Feb 2026 17:26:27 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ffc7844b3d362e6b692567d2587e4fd19b348dff44182f52019fdefe7ab344`  
		Last Modified: Tue, 03 Feb 2026 17:26:28 GMT  
		Size: 17.6 MB (17566404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9111fb63645fb502831d395247748514cc38c89a036c0c80ac0d68172af396`  
		Last Modified: Tue, 03 Feb 2026 17:26:29 GMT  
		Size: 26.5 MB (26546121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17318896bc84227a623de0b09b1c19d9ba46473321e3c6ef037516d813f8da1`  
		Last Modified: Tue, 03 Feb 2026 17:26:29 GMT  
		Size: 10.2 MB (10198592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f58cddeebb4c56cedfe3c4d3406be79ac683f61f8d149db919627222cd847dae`  
		Last Modified: Tue, 03 Feb 2026 17:26:29 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45cca7f5e3f5fc71d61ff7160fba4b5af52d1d5c1376ef27109056ee0bd35891`  
		Last Modified: Tue, 03 Feb 2026 17:26:30 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68671e7ea5f72eebefa27db844dfc891bba0667adb87fda60be5a0a78a9e0af3`  
		Last Modified: Tue, 03 Feb 2026 17:26:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.1-cli-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:725c7ed6fedc0c78099cca969de9d894742913605a635c1d1ae732d243e1f9d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a2b7afca7a73cadfc121038f2cb596614c4eff15299359ccc0fe5915a333dfa`

```dockerfile
```

-	Layers:
	-	`sha256:9fd463f063b0e999eee86b191492b64c48293c00436e4b777db697007872a8d6`  
		Last Modified: Tue, 03 Feb 2026 17:26:27 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2.1-cli-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:2bef500bc870e9a4eef5ac67cf6fef451c072f77b7351b207d74a3463c80e455
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.5 MB (65497196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cffbe99c0e2eadb1b2dd8830a3ecddedf95c08183d497287cb048586c0c94905`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:26:35 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:26:35 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:26:35 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:26:37 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:26:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:26:37 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:26:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:26:38 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:26:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:26:39 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:26:39 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42a77f5fc93e1d6c642b2eb20bac67ddedc3fa614973ecad5d2425aa529cc7f`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 8.5 MB (8453512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9817403955ea5ea2eedc37cde61397fd369d7b07e3863286754b4989d443759a`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d23c75ff3415b6637326f398bd112a7ec4373805d39318b94b65c8ff6ce7538`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 17.3 MB (17349111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfca817951310f1a68cb06e3fe0f27540e7d76c61b144cbbb1ebaa04308c8233`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 25.5 MB (25540815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7af456c729c76507dbf99635546e893dd549241c3157a2a655f1a7472544d6`  
		Last Modified: Tue, 03 Feb 2026 17:26:47 GMT  
		Size: 10.0 MB (9954516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72242c4fb87c9ebb62312863874911bfe531f06775fe6a90aa5c937db6274442`  
		Last Modified: Tue, 03 Feb 2026 17:26:47 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e91b41b56d8ea2c6e69d6ed8a929177b21cc4e84b65284dd552f20cda40c3dd`  
		Last Modified: Tue, 03 Feb 2026 17:26:48 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66fa267764c487b75a914eae88e45afb0bdd82be8b4c090d4af5946454d79964`  
		Last Modified: Tue, 03 Feb 2026 17:26:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.1-cli-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:22956d1b0f85ed3aaf3fbd162a232fd08241684704dc328c469298a7a60f924e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa0c6c28d5d6436cdecdceb1ee544bccb64c7a75c45b13de36e354116226cab3`

```dockerfile
```

-	Layers:
	-	`sha256:0c689b61e422b3962e7df2e52b56054a4e453d576da33fd3b1d6f7dca26d06b6`  
		Last Modified: Tue, 03 Feb 2026 17:26:45 GMT  
		Size: 38.3 KB (38258 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.2.1-dind`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:29.2.1-dind-alpine3.23`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:29.2.1-dind-rootless`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:29.2.1-windowsservercore`

```console
$ docker pull docker@sha256:79cb1793605b4f2d7317cea6706862e4b002e6ace6375912bab555eebfdf6ed2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `docker:29.2.1-windowsservercore` - windows version 10.0.26100.32230; amd64

```console
$ docker pull docker@sha256:c5d3ecbfcaeb424c90459ac8317405555d19b1b8b3e578390234d4a8e7c24c64
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1556599774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d647b193ba9f5cb583f9fb294f2d532c6d85295880ef0649d60793cc309abcd1`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Tue, 03 Feb 2026 17:28:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 03 Feb 2026 17:29:28 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 03 Feb 2026 17:29:30 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:29:32 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.1.zip
# Tue, 03 Feb 2026 17:29:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 03 Feb 2026 17:29:46 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:29:48 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.windows-amd64.exe
# Tue, 03 Feb 2026 17:29:48 GMT
ENV DOCKER_BUILDX_SHA256=b49832d4ac46bde05006f7ad3506b9d5060b60e5c566545d8e10c1a80df08a4a
# Tue, 03 Feb 2026 17:29:59 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 03 Feb 2026 17:30:00 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:30:01 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Tue, 03 Feb 2026 17:30:01 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Tue, 03 Feb 2026 17:30:08 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3345d2727a1883e3d335172c07a1f0f478ed9c744e1aa4ec455219fd5b041b31`  
		Last Modified: Tue, 03 Feb 2026 17:30:17 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c2b758f14303d714990de0fad8eacb8f18d18925809a064fa024e0a8203573a`  
		Last Modified: Tue, 03 Feb 2026 17:30:16 GMT  
		Size: 402.8 KB (402791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c544aebc260938057720752277d7e0b5a599ebf13c36d8be0403e694d8929db8`  
		Last Modified: Tue, 03 Feb 2026 17:30:15 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54275eb139ff712b0a5f139cdba772a69cd2371fcb0b65f6371b8d8b22f92c19`  
		Last Modified: Tue, 03 Feb 2026 17:30:15 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff99eb3d4bee14899afa2383e60cfa18a0f63d88f5c759afcbfa0cef9bae50bb`  
		Last Modified: Tue, 03 Feb 2026 17:30:18 GMT  
		Size: 19.5 MB (19477937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d8a57f5276cfc049bae3b7a853039be549c9bada93ef2e8d868ea54e9c04236`  
		Last Modified: Tue, 03 Feb 2026 17:30:14 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be178348f9fba72db323ad766660239b1363bbe80d1f01cf90cd2531b5f01b03`  
		Last Modified: Tue, 03 Feb 2026 17:30:14 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca77ca63bd7d4b72f07134cb3691a9edeba02acdb61fb8ff15a7f6c7f44734ce`  
		Last Modified: Tue, 03 Feb 2026 17:30:14 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51aa328a4c51fa2977445e97c24b485b2fbf132d207a9adfa58cf7406f3f8a1f`  
		Last Modified: Tue, 03 Feb 2026 17:30:30 GMT  
		Size: 29.5 MB (29453041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c300d10089e1c370f164537efd3c43df949644198f422eb4863dccfe9930a4f`  
		Last Modified: Tue, 03 Feb 2026 17:30:12 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5356d434dcd14c58d539907321e96d2a0e794ac74a29c08aa2df1dbaa611e231`  
		Last Modified: Tue, 03 Feb 2026 17:30:12 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b03bbb60e30cb160ee1c1c6844849f758718d7111a7cb510a1b0ec1702120fd`  
		Last Modified: Tue, 03 Feb 2026 17:30:12 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2d04ad8db9950e63dbd9118d08d70484b5aed5cf9dadf9591e16f2a8339e8e`  
		Last Modified: Tue, 03 Feb 2026 17:30:14 GMT  
		Size: 11.5 MB (11493926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:29.2.1-windowsservercore` - windows version 10.0.20348.4648; amd64

```console
$ docker pull docker@sha256:ba1e9a93d62651a48e0592e4a6010300708e2422e46df2b25d54b1d2f1e7fb47
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1896494534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a09c7520bcdba0cceb87d9e1fe705ea6641137be025705d09eaba1893561ddea`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Tue, 03 Feb 2026 17:28:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 03 Feb 2026 17:29:49 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 03 Feb 2026 17:29:49 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:29:50 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.1.zip
# Tue, 03 Feb 2026 17:30:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 03 Feb 2026 17:30:17 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:30:18 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.windows-amd64.exe
# Tue, 03 Feb 2026 17:30:18 GMT
ENV DOCKER_BUILDX_SHA256=b49832d4ac46bde05006f7ad3506b9d5060b60e5c566545d8e10c1a80df08a4a
# Tue, 03 Feb 2026 17:30:49 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 03 Feb 2026 17:30:50 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:30:52 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Tue, 03 Feb 2026 17:30:52 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Tue, 03 Feb 2026 17:31:09 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1610c61d22cce1c0da1f89bcf2b2b93db5d1ee6703ddda8c50c992a55a3a3273`  
		Last Modified: Tue, 03 Feb 2026 17:31:19 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35301633ca92d436f45505192a1ef4f18618178fd179a0275e79d55f1cdba61d`  
		Last Modified: Tue, 03 Feb 2026 17:31:19 GMT  
		Size: 502.0 KB (501985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc76ce47c4de88873c339dee382928f8c2afe957a1f67eaa1bc1745de35e796e`  
		Last Modified: Tue, 03 Feb 2026 17:31:18 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c0a93da300b8f2017782995a21ddcc03360f0068884e95f2c90a34943b5a853`  
		Last Modified: Tue, 03 Feb 2026 17:31:18 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4642a451e4aa3a689441cf53a384a5333b79045931964aecc32acb75dab6242f`  
		Last Modified: Tue, 03 Feb 2026 17:31:20 GMT  
		Size: 19.4 MB (19440499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f80fcdb722aba8bdf0a57b047c109edce18d999e3bc1649781fa0d3de37c6e29`  
		Last Modified: Tue, 03 Feb 2026 17:31:16 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52573eb20ed9e08365fa5f5e972f07f60f80fd44870b2c8c2e00435b86e529d7`  
		Last Modified: Tue, 03 Feb 2026 17:31:16 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc93a0644ac21577feac91654ceef3e9cb714742257794765b8f41f26967f84e`  
		Last Modified: Tue, 03 Feb 2026 17:31:16 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c020b7de7a60805f5e0f214c5933b5730ce1e22475c6c0637dbe59005c03baa4`  
		Last Modified: Tue, 03 Feb 2026 17:31:33 GMT  
		Size: 29.4 MB (29425091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:538b00d976a03c45b55d387636033ba066f8d59660d195f26399a156232cb079`  
		Last Modified: Tue, 03 Feb 2026 17:31:14 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f8c0456ab18eeca4e06f6a4f1edc155807d2fd8565b3c71217f4895c0778536`  
		Last Modified: Tue, 03 Feb 2026 17:31:14 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525c0f16947c0cc46484ca50b3cbe0be998327c9e218a8f15dd79b3752be1f84`  
		Last Modified: Tue, 03 Feb 2026 17:31:14 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f29f86a605fc1d2ecf16f261c2beeb1261773d00bba4c7341e76d2363f15db4a`  
		Last Modified: Tue, 03 Feb 2026 17:31:16 GMT  
		Size: 11.5 MB (11456032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.2.1-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:315827d701f9fef8731fca2a65b1c5960422bfb5d0e6f335995310b4c2c2bf07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `docker:29.2.1-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull docker@sha256:ba1e9a93d62651a48e0592e4a6010300708e2422e46df2b25d54b1d2f1e7fb47
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1896494534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a09c7520bcdba0cceb87d9e1fe705ea6641137be025705d09eaba1893561ddea`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Tue, 03 Feb 2026 17:28:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 03 Feb 2026 17:29:49 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 03 Feb 2026 17:29:49 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:29:50 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.1.zip
# Tue, 03 Feb 2026 17:30:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 03 Feb 2026 17:30:17 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:30:18 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.windows-amd64.exe
# Tue, 03 Feb 2026 17:30:18 GMT
ENV DOCKER_BUILDX_SHA256=b49832d4ac46bde05006f7ad3506b9d5060b60e5c566545d8e10c1a80df08a4a
# Tue, 03 Feb 2026 17:30:49 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 03 Feb 2026 17:30:50 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:30:52 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Tue, 03 Feb 2026 17:30:52 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Tue, 03 Feb 2026 17:31:09 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1610c61d22cce1c0da1f89bcf2b2b93db5d1ee6703ddda8c50c992a55a3a3273`  
		Last Modified: Tue, 03 Feb 2026 17:31:19 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35301633ca92d436f45505192a1ef4f18618178fd179a0275e79d55f1cdba61d`  
		Last Modified: Tue, 03 Feb 2026 17:31:19 GMT  
		Size: 502.0 KB (501985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc76ce47c4de88873c339dee382928f8c2afe957a1f67eaa1bc1745de35e796e`  
		Last Modified: Tue, 03 Feb 2026 17:31:18 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c0a93da300b8f2017782995a21ddcc03360f0068884e95f2c90a34943b5a853`  
		Last Modified: Tue, 03 Feb 2026 17:31:18 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4642a451e4aa3a689441cf53a384a5333b79045931964aecc32acb75dab6242f`  
		Last Modified: Tue, 03 Feb 2026 17:31:20 GMT  
		Size: 19.4 MB (19440499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f80fcdb722aba8bdf0a57b047c109edce18d999e3bc1649781fa0d3de37c6e29`  
		Last Modified: Tue, 03 Feb 2026 17:31:16 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52573eb20ed9e08365fa5f5e972f07f60f80fd44870b2c8c2e00435b86e529d7`  
		Last Modified: Tue, 03 Feb 2026 17:31:16 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc93a0644ac21577feac91654ceef3e9cb714742257794765b8f41f26967f84e`  
		Last Modified: Tue, 03 Feb 2026 17:31:16 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c020b7de7a60805f5e0f214c5933b5730ce1e22475c6c0637dbe59005c03baa4`  
		Last Modified: Tue, 03 Feb 2026 17:31:33 GMT  
		Size: 29.4 MB (29425091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:538b00d976a03c45b55d387636033ba066f8d59660d195f26399a156232cb079`  
		Last Modified: Tue, 03 Feb 2026 17:31:14 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f8c0456ab18eeca4e06f6a4f1edc155807d2fd8565b3c71217f4895c0778536`  
		Last Modified: Tue, 03 Feb 2026 17:31:14 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525c0f16947c0cc46484ca50b3cbe0be998327c9e218a8f15dd79b3752be1f84`  
		Last Modified: Tue, 03 Feb 2026 17:31:14 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f29f86a605fc1d2ecf16f261c2beeb1261773d00bba4c7341e76d2363f15db4a`  
		Last Modified: Tue, 03 Feb 2026 17:31:16 GMT  
		Size: 11.5 MB (11456032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.2.1-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:ed671d3152d0f57a459cd9f0838f7e48071ccef5c71ad1188693f4540f24cf19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32230; amd64

### `docker:29.2.1-windowsservercore-ltsc2025` - windows version 10.0.26100.32230; amd64

```console
$ docker pull docker@sha256:c5d3ecbfcaeb424c90459ac8317405555d19b1b8b3e578390234d4a8e7c24c64
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1556599774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d647b193ba9f5cb583f9fb294f2d532c6d85295880ef0649d60793cc309abcd1`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Tue, 03 Feb 2026 17:28:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 03 Feb 2026 17:29:28 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 03 Feb 2026 17:29:30 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:29:32 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.1.zip
# Tue, 03 Feb 2026 17:29:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 03 Feb 2026 17:29:46 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:29:48 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.windows-amd64.exe
# Tue, 03 Feb 2026 17:29:48 GMT
ENV DOCKER_BUILDX_SHA256=b49832d4ac46bde05006f7ad3506b9d5060b60e5c566545d8e10c1a80df08a4a
# Tue, 03 Feb 2026 17:29:59 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 03 Feb 2026 17:30:00 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:30:01 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Tue, 03 Feb 2026 17:30:01 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Tue, 03 Feb 2026 17:30:08 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3345d2727a1883e3d335172c07a1f0f478ed9c744e1aa4ec455219fd5b041b31`  
		Last Modified: Tue, 03 Feb 2026 17:30:17 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c2b758f14303d714990de0fad8eacb8f18d18925809a064fa024e0a8203573a`  
		Last Modified: Tue, 03 Feb 2026 17:30:16 GMT  
		Size: 402.8 KB (402791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c544aebc260938057720752277d7e0b5a599ebf13c36d8be0403e694d8929db8`  
		Last Modified: Tue, 03 Feb 2026 17:30:15 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54275eb139ff712b0a5f139cdba772a69cd2371fcb0b65f6371b8d8b22f92c19`  
		Last Modified: Tue, 03 Feb 2026 17:30:15 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff99eb3d4bee14899afa2383e60cfa18a0f63d88f5c759afcbfa0cef9bae50bb`  
		Last Modified: Tue, 03 Feb 2026 17:30:18 GMT  
		Size: 19.5 MB (19477937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d8a57f5276cfc049bae3b7a853039be549c9bada93ef2e8d868ea54e9c04236`  
		Last Modified: Tue, 03 Feb 2026 17:30:14 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be178348f9fba72db323ad766660239b1363bbe80d1f01cf90cd2531b5f01b03`  
		Last Modified: Tue, 03 Feb 2026 17:30:14 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca77ca63bd7d4b72f07134cb3691a9edeba02acdb61fb8ff15a7f6c7f44734ce`  
		Last Modified: Tue, 03 Feb 2026 17:30:14 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51aa328a4c51fa2977445e97c24b485b2fbf132d207a9adfa58cf7406f3f8a1f`  
		Last Modified: Tue, 03 Feb 2026 17:30:30 GMT  
		Size: 29.5 MB (29453041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c300d10089e1c370f164537efd3c43df949644198f422eb4863dccfe9930a4f`  
		Last Modified: Tue, 03 Feb 2026 17:30:12 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5356d434dcd14c58d539907321e96d2a0e794ac74a29c08aa2df1dbaa611e231`  
		Last Modified: Tue, 03 Feb 2026 17:30:12 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b03bbb60e30cb160ee1c1c6844849f758718d7111a7cb510a1b0ec1702120fd`  
		Last Modified: Tue, 03 Feb 2026 17:30:12 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2d04ad8db9950e63dbd9118d08d70484b5aed5cf9dadf9591e16f2a8339e8e`  
		Last Modified: Tue, 03 Feb 2026 17:30:14 GMT  
		Size: 11.5 MB (11493926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:cli`

```console
$ docker pull docker@sha256:1d6d751f1d68d1a5142c23c730ef5ecc976a8e050fa08c3cdb09f7e2e54a4439
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
$ docker pull docker@sha256:0c04277b44d1d448d40238faa142c2edf21d4a90dc0d61486c32056bbf11572a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70148082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90fa388e81d5f66d9d9ee840c5375a0801629a980c3d9657463257b2c863f324`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:25:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:25:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:25:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:25:58 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:25:58 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:25:58 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:25:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:25:59 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:26:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:26:00 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:26:00 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ffbc9e9d61a3a427749366541c9e55c1440658b296b288726282a7e3a200f3`  
		Last Modified: Tue, 03 Feb 2026 17:26:07 GMT  
		Size: 8.4 MB (8399657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9130c567f6fc24a30ebaa5979b9c6700d6c174c3a52a1e753c42621bfb1a32d9`  
		Last Modified: Tue, 03 Feb 2026 17:26:07 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b75aa627f4cd980f8d8c3e7be1834e54e286a6499508105b6f72c4a373c7a6e`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 18.8 MB (18773130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c979ccecd955439750b7f01789bf427e4c8d60acbf2b4a12100ff3173aea9b`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 28.3 MB (28311545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217f84c60501e3b3fb548f194b2861bfcb2a70aa12a9abe9b0d4ee342d75a7b5`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 10.8 MB (10799774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bf8952411ee385ba36420d9b6bdcc36594a8be8bdace8fe62d7d97f81322411`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f757cc0a441eaf36dbebd029cb42e59a8c463fb4ea19e2ec6bf557d5a981dc2`  
		Last Modified: Tue, 03 Feb 2026 17:26:09 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7358b0dc3398fd6f4c32455892c6ab6fbc099f1a8e62df04445dec7663a095`  
		Last Modified: Tue, 03 Feb 2026 17:26:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:c1620c41ed6e739f033f9e98a5bba1cb95e1ea6a093197beb216823c8c93ce72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c5f4666aeb7f994fb855d5fb4b289608e198a0a0b59b25161f28433aeb36364`

```dockerfile
```

-	Layers:
	-	`sha256:19b63918903a6b77f5af72e60038c44df3a84e5a4563b3db3d54ef79567b8195`  
		Last Modified: Tue, 03 Feb 2026 17:26:07 GMT  
		Size: 38.1 KB (38056 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:cf09d93cea103396a11b1b12c36c15b6b93d367c0c80cce733f00214c71c92e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66235505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4367f8d4a4b3fc3d463d69bca54b902b58d4792ccf8967224e2ec3dd7aa4afb4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:25:26 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:25:26 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:25:26 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:25:31 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:25:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:25:31 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:25:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:25:33 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:25:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:25:35 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:25:35 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ed7f28a4b26e2736ceb8045d972a5f166880f3b93b1ce13d7cb7710819f7c0`  
		Last Modified: Tue, 03 Feb 2026 17:25:42 GMT  
		Size: 8.3 MB (8300971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59982a56599ba445b45c1ff95a9bf2efe937cb3105d8107453c37e42aa96ab06`  
		Last Modified: Tue, 03 Feb 2026 17:25:41 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627db20a49a4f2be2d19fe161406f293a8b8804c985028e04c1cd95f0c40d96e`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 17.6 MB (17575014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acd42cfefd8cbfbea51ccc805027f78eefae1b3ad5cb91c207ebf9578a6a855`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 26.6 MB (26574500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac22564cea85937e49534e5ef435197d6c83fb053c5aa91ffddb70acae2ff81`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 10.2 MB (10213046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8735f9cb2ee8a9b930cd6b2bf3885083108a83a3707f302210e9bb0a138c15ec`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf43e9302aee150c8b25e6f5c53d2eb8642dd7db31500f8f7e980a6639b3d75`  
		Last Modified: Tue, 03 Feb 2026 17:25:44 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52ca294aaca561ae37709af7d9406792302f6ac4cfe16d2068ba04176c0aa2a`  
		Last Modified: Tue, 03 Feb 2026 17:25:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:fbcdf3246eea54b7103bc19f384cd3f454538bd499af80a1566455c68e652971
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f63de4e3179da9faef11522e19444ae1387215588371c787a0b6852c464dcd77`

```dockerfile
```

-	Layers:
	-	`sha256:97d51d656e276dcee240923733068124918a337234be2ffb56edcdb70a458855`  
		Last Modified: Tue, 03 Feb 2026 17:25:41 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:ba03aff6e89a96861c91cbe97855b49f31e816c782afaa8225043cb76f7ae372
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65192844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:985b778ba8e60d8ceaa28fed60316b7c31c5ff3e18d6afb37619d388a8da92b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:26:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:26:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:26:11 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:26:15 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:26:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:26:15 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:26:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:26:19 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:26:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:26:20 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:26:20 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb5af91453d1293030fbe90db4c6166609f99510d3fcec579be00a21249cbf2`  
		Last Modified: Tue, 03 Feb 2026 17:26:28 GMT  
		Size: 7.6 MB (7597849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7fbe9447e7591ff3854f01ba9776952a93a9c4f22447067e6a9e1c3f93c760`  
		Last Modified: Tue, 03 Feb 2026 17:26:27 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ffc7844b3d362e6b692567d2587e4fd19b348dff44182f52019fdefe7ab344`  
		Last Modified: Tue, 03 Feb 2026 17:26:28 GMT  
		Size: 17.6 MB (17566404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9111fb63645fb502831d395247748514cc38c89a036c0c80ac0d68172af396`  
		Last Modified: Tue, 03 Feb 2026 17:26:29 GMT  
		Size: 26.5 MB (26546121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17318896bc84227a623de0b09b1c19d9ba46473321e3c6ef037516d813f8da1`  
		Last Modified: Tue, 03 Feb 2026 17:26:29 GMT  
		Size: 10.2 MB (10198592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f58cddeebb4c56cedfe3c4d3406be79ac683f61f8d149db919627222cd847dae`  
		Last Modified: Tue, 03 Feb 2026 17:26:29 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45cca7f5e3f5fc71d61ff7160fba4b5af52d1d5c1376ef27109056ee0bd35891`  
		Last Modified: Tue, 03 Feb 2026 17:26:30 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68671e7ea5f72eebefa27db844dfc891bba0667adb87fda60be5a0a78a9e0af3`  
		Last Modified: Tue, 03 Feb 2026 17:26:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:725c7ed6fedc0c78099cca969de9d894742913605a635c1d1ae732d243e1f9d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a2b7afca7a73cadfc121038f2cb596614c4eff15299359ccc0fe5915a333dfa`

```dockerfile
```

-	Layers:
	-	`sha256:9fd463f063b0e999eee86b191492b64c48293c00436e4b777db697007872a8d6`  
		Last Modified: Tue, 03 Feb 2026 17:26:27 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:2bef500bc870e9a4eef5ac67cf6fef451c072f77b7351b207d74a3463c80e455
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.5 MB (65497196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cffbe99c0e2eadb1b2dd8830a3ecddedf95c08183d497287cb048586c0c94905`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:26:35 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:26:35 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:26:35 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:26:37 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:26:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:26:37 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:26:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:26:38 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:26:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:26:39 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:26:39 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42a77f5fc93e1d6c642b2eb20bac67ddedc3fa614973ecad5d2425aa529cc7f`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 8.5 MB (8453512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9817403955ea5ea2eedc37cde61397fd369d7b07e3863286754b4989d443759a`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d23c75ff3415b6637326f398bd112a7ec4373805d39318b94b65c8ff6ce7538`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 17.3 MB (17349111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfca817951310f1a68cb06e3fe0f27540e7d76c61b144cbbb1ebaa04308c8233`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 25.5 MB (25540815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7af456c729c76507dbf99635546e893dd549241c3157a2a655f1a7472544d6`  
		Last Modified: Tue, 03 Feb 2026 17:26:47 GMT  
		Size: 10.0 MB (9954516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72242c4fb87c9ebb62312863874911bfe531f06775fe6a90aa5c937db6274442`  
		Last Modified: Tue, 03 Feb 2026 17:26:47 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e91b41b56d8ea2c6e69d6ed8a929177b21cc4e84b65284dd552f20cda40c3dd`  
		Last Modified: Tue, 03 Feb 2026 17:26:48 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66fa267764c487b75a914eae88e45afb0bdd82be8b4c090d4af5946454d79964`  
		Last Modified: Tue, 03 Feb 2026 17:26:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:22956d1b0f85ed3aaf3fbd162a232fd08241684704dc328c469298a7a60f924e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa0c6c28d5d6436cdecdceb1ee544bccb64c7a75c45b13de36e354116226cab3`

```dockerfile
```

-	Layers:
	-	`sha256:0c689b61e422b3962e7df2e52b56054a4e453d576da33fd3b1d6f7dca26d06b6`  
		Last Modified: Tue, 03 Feb 2026 17:26:45 GMT  
		Size: 38.3 KB (38258 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind`

```console
$ docker pull docker@sha256:a284d31e4db9a9916fd9be44380263eaeafedf0e3048a859f978922b5a0c16fc
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
$ docker pull docker@sha256:99aa88f75d8d401c30e395db1d2e679a89ff0be9b415f020b8e2383c517e1fda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.8 MB (143799092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ca04087ca24aa6deade38370d033555d14dacd022c6a5d275f038b89eaf131`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:15:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:15:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:15:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:15:17 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:15:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:15:17 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:15:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:15:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:15:19 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:15:19 GMT
CMD ["sh"]
# Wed, 28 Jan 2026 03:58:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 Jan 2026 03:58:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 Jan 2026 03:58:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 Jan 2026 03:58:45 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
VOLUME [/var/lib/docker]
# Wed, 28 Jan 2026 03:58:45 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 Jan 2026 03:58:45 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 Jan 2026 03:58:45 GMT
CMD []
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03ce8e2700f1129dc15f38a5e1e7d27cdd2b98175c4d9ac08dc5646c3c35ba4`  
		Last Modified: Wed, 28 Jan 2026 02:15:26 GMT  
		Size: 8.4 MB (8399638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dabc00febb6a9a0d9954ef0b62272b11dabac7697dd7a0f94f9a96e241fbfd2`  
		Last Modified: Wed, 28 Jan 2026 02:15:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9408125f9d0c694cc95efc06409f73e6d6907c853a7f861c85b36824fb02ed25`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 18.8 MB (18774054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1765bbbd236eff12d3ecffaab470c2a8ade7f1432cbf0f1efe2f520cb9d74bfc`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 28.3 MB (28308902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d4f1a3f89cb924cc72cf031843e7490b98f39a276e6628c0ef444a871ff92f`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 10.8 MB (10799762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ca730a0591b75f8b903f70ff08c4b2959f397bd8775ba1a873cbb344b15c1a0`  
		Last Modified: Wed, 28 Jan 2026 02:15:28 GMT  
		Size: 533.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc93a580b636b3173550ee5a31a23ae95eb17558288345a26091285a5f477d5`  
		Last Modified: Wed, 28 Jan 2026 02:15:28 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9745309fb9885c647e35e9d55ab83308f9c212460ad5f9b73c2e518179059b72`  
		Last Modified: Wed, 28 Jan 2026 02:15:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:effa5c3a383e3a584de2fe9ef352f8fcde727e8db088492f0c8e49fc27f7abaa`  
		Last Modified: Wed, 28 Jan 2026 03:58:56 GMT  
		Size: 6.9 MB (6934734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a8f8addf621601263b2bfea9efe7ffac5903b85bfe7b9f628f7a2ff6bd4fce`  
		Last Modified: Wed, 28 Jan 2026 03:58:55 GMT  
		Size: 92.5 KB (92460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:396bcb1ae646a1eb234538a6bf406490001b6067e5626f4858b3d3ab115a1338`  
		Last Modified: Wed, 28 Jan 2026 03:58:56 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636ece6788bea2909cc3a17231a1a4827c4db266c991df7770a909ecdb8d3fd0`  
		Last Modified: Wed, 28 Jan 2026 03:58:57 GMT  
		Size: 66.6 MB (66619579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb2987d59bbd2b711c1759725d9ccc5891b03def0602234c4f49beb1e5c2be1`  
		Last Modified: Wed, 28 Jan 2026 03:58:57 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ac6a5de045400bc7b163e70c2cd9429f6202144cb50ed4b85688aded44f58e`  
		Last Modified: Wed, 28 Jan 2026 03:58:57 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:2d2c0973782cdccc69752fb841755627c37546ebbf2f68f0bf070bf51d23ec60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0784b32a62dac2ebed2ad0ae726d2901f105b39654d58a2d2d351b4eaea7d818`

```dockerfile
```

-	Layers:
	-	`sha256:161b2e45f0098aead317dd0674b614a4e1252835a147f30b88ddc0667bf7ba93`  
		Last Modified: Wed, 28 Jan 2026 03:58:55 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:70dcad0b903a121c11d71a23834267a49327cd21053d8a2a83529cf94a2d9fbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135630532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:438bd2c6733062a94188c3067ba6118e7dda4560c7d7eb98ecec81192d5273b2`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:19:28 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:19:29 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:19:29 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:19:32 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:19:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:19:32 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:19:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:19:34 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:19:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:19:36 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:19:36 GMT
CMD ["sh"]
# Wed, 28 Jan 2026 03:49:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 Jan 2026 03:49:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 Jan 2026 03:49:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 03:49:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 Jan 2026 03:49:21 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 Jan 2026 03:49:21 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 Jan 2026 03:49:21 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:49:21 GMT
VOLUME [/var/lib/docker]
# Wed, 28 Jan 2026 03:49:21 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 Jan 2026 03:49:21 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 Jan 2026 03:49:21 GMT
CMD []
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08efb619161971b8dbf3d2d18d22c25f3caf7baea4b18537b77a961fee285e4d`  
		Last Modified: Wed, 28 Jan 2026 02:19:43 GMT  
		Size: 8.3 MB (8301019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11eae5034a08f196af9949aec8c0d0a5c776062160fbfa6839f4e91eb25c523`  
		Last Modified: Wed, 28 Jan 2026 02:19:42 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b811dd811e1e6a5a185faf36f1f9dd7bd483290fc51d98ccb7f5014b5bd19ab`  
		Last Modified: Wed, 28 Jan 2026 02:19:43 GMT  
		Size: 17.6 MB (17576540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395a6e19e8b08ce81dbf6939f7000c5eaaa78657497cffd3559c4d3586ad6f25`  
		Last Modified: Wed, 28 Jan 2026 02:19:44 GMT  
		Size: 26.6 MB (26570467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b3f84acb2b12fc7c649c003ff8e9348dabfff644a17daad4b02eef0bd9b40b6`  
		Last Modified: Wed, 28 Jan 2026 02:19:44 GMT  
		Size: 10.2 MB (10213042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746007c626ec304c1dfcf1e9084f31b26345a6079f9efe6f265b8fa508abf11a`  
		Last Modified: Wed, 28 Jan 2026 02:19:44 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f144bc5ce89728429c7674f4da3e2efbf3439669eae61e270d13a77809b4b9b7`  
		Last Modified: Wed, 28 Jan 2026 02:19:45 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b078b00f266ba4e03e79da886e567e61c21f493be073a7001f1e3db1345ccf57`  
		Last Modified: Wed, 28 Jan 2026 02:19:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6f4b2cf4256d701c8e551ce6b913b60516e7a6812dd2a6b150737145528fdf`  
		Last Modified: Wed, 28 Jan 2026 03:49:31 GMT  
		Size: 7.3 MB (7271609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b290e764c28e19f2f21aa7790d801cc6056a53cd51c8fb1bb6faf2e2346d4145`  
		Last Modified: Wed, 28 Jan 2026 03:49:30 GMT  
		Size: 91.8 KB (91775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:894eda0b2167abb0c583bbf993071a8d219941e2dd3bc2fcd1f8bfd8ca024a34`  
		Last Modified: Wed, 28 Jan 2026 03:49:30 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661a756971591996ae71af31b4d76fd40c1ba5140d25d52487a63a2ce33123b3`  
		Last Modified: Wed, 28 Jan 2026 03:49:32 GMT  
		Size: 62.0 MB (62028111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0fea802a7e013543afeb57c94b421ff42c6cc94e875a7a48079633d5b32cf0`  
		Last Modified: Wed, 28 Jan 2026 03:49:31 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89262e7e7a4c52344f56768909e409e4d52e23b7e5f872f34c6f8f05f600ced1`  
		Last Modified: Wed, 28 Jan 2026 03:49:32 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:77efd8773fd21feb58c996858580a066f8336af75ce15a65d1e94fbfc662939f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8937de610607274348941cf30b97eee5b16a47a2a3e355daae965571f78e1b8e`

```dockerfile
```

-	Layers:
	-	`sha256:b2c9967356bfd5048f745045eb7a61d4c51f3b8a396da52f925736b964896609`  
		Last Modified: Wed, 28 Jan 2026 03:49:30 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:136f2e805834a4247060b8060063ba782a2fdce6083a3cb47d02e83936623504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133715469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a4604f36042cbaaba3fd792ec4e26bfaf62d2d45b48d38a8697760ddf3306fa`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:19:33 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:19:33 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:19:34 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:19:37 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:19:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:19:37 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:19:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:19:39 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:19:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:19:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:19:41 GMT
CMD ["sh"]
# Wed, 28 Jan 2026 03:51:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 Jan 2026 03:51:44 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 Jan 2026 03:51:44 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 03:51:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 Jan 2026 03:51:47 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 Jan 2026 03:51:47 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 Jan 2026 03:51:47 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:51:47 GMT
VOLUME [/var/lib/docker]
# Wed, 28 Jan 2026 03:51:47 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 Jan 2026 03:51:47 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 Jan 2026 03:51:47 GMT
CMD []
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef74ac3c65992e7acddcc2a2c02498d51d5fda8b771538e5411d2d5f3a3e9eec`  
		Last Modified: Wed, 28 Jan 2026 02:19:47 GMT  
		Size: 7.6 MB (7597810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01925faabefdbedf8efebb820b152e94fb287b72138d282a76557993132623ca`  
		Last Modified: Wed, 28 Jan 2026 02:19:47 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ad13ec2588fba164870da3d93ba8b5ad34e242b5bc6fb7b5df1bd055e194e0`  
		Last Modified: Wed, 28 Jan 2026 02:19:48 GMT  
		Size: 17.6 MB (17566458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc3d6d20d26654203dbb33aecb823850102a06ee1d8826eeea313f51053947d`  
		Last Modified: Wed, 28 Jan 2026 02:19:48 GMT  
		Size: 26.5 MB (26544669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309b43a06105801e72a4057c9a98aa39f845292f118ed5364be6f2c58fff6fb2`  
		Last Modified: Wed, 28 Jan 2026 02:19:48 GMT  
		Size: 10.2 MB (10198593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c018df83e09983e9c86c614e37738e0c9913c07f571d99ca7464a8eead3114`  
		Last Modified: Wed, 28 Jan 2026 02:19:49 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff08fbe96bdc955d67587b7154a9e64b5fd0933ad18112a10502a2d2ee351334`  
		Last Modified: Wed, 28 Jan 2026 02:19:49 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82766871530b6d5c5faaefb052706696dbc1f4936a761d57fe77b41476c57e81`  
		Last Modified: Wed, 28 Jan 2026 02:19:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966fa3b3930581a719871ad9cc50569b5b949938c666c5f604128567586dcc98`  
		Last Modified: Wed, 28 Jan 2026 03:51:58 GMT  
		Size: 6.6 MB (6572989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8288f87d3ec8e6d2c73fad07643b43f2c5a333b046f21c81531e877d6eaf19d4`  
		Last Modified: Wed, 28 Jan 2026 03:51:58 GMT  
		Size: 88.1 KB (88136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd5922158e4b006788c6366971c7c91cc1404b01a100da81d4c9a0477a74027`  
		Last Modified: Wed, 28 Jan 2026 03:51:58 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842a3b5326d8c1c6b696edd5624246ed13391ce31743771eb92561f224c0e672`  
		Last Modified: Wed, 28 Jan 2026 03:52:00 GMT  
		Size: 61.9 MB (61856931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f666916210054b0fd5f72affa9ac152fa7c42d927442f2dd309d354e89b9277`  
		Last Modified: Wed, 28 Jan 2026 03:51:59 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cf19ee261d3469335adb02771df03de4d7bd57f3cb5c06bb5841ae7b93697c`  
		Last Modified: Wed, 28 Jan 2026 03:51:59 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:8457bbc8972fac13450e367c97a9a1b851c44540331c9f631abe6ecc6da554fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d30df9382a2c15c97b7086f993412c3a0f44e8ed81f835508748d782eabe5345`

```dockerfile
```

-	Layers:
	-	`sha256:0a1c8b9290fc1e34c2f218c7730ca8fc83fc55704982e288265ea392b6f0447c`  
		Last Modified: Wed, 28 Jan 2026 03:51:58 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:2cd37b1da26b3d7bdae2014ffafb6543a3c40f32973395bdf6e402afc6818e38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.2 MB (133249301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a287877d76e510dc36d4294bef0d4540628445c54cbf477d32ad4aef68e7bb0a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:15:20 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:15:20 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:15:20 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:15:22 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:15:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:15:22 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:15:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:15:23 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:15:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:15:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:15:24 GMT
CMD ["sh"]
# Wed, 28 Jan 2026 04:19:44 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 Jan 2026 04:19:44 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 Jan 2026 04:19:45 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 04:19:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 Jan 2026 04:19:48 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 Jan 2026 04:19:48 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 Jan 2026 04:19:48 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 04:19:48 GMT
VOLUME [/var/lib/docker]
# Wed, 28 Jan 2026 04:19:48 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 Jan 2026 04:19:48 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 Jan 2026 04:19:48 GMT
CMD []
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23cd2c872bdff3a89f69a977eea6049f005ee667e33468764b0584c9a8959fe3`  
		Last Modified: Wed, 28 Jan 2026 02:15:31 GMT  
		Size: 8.5 MB (8453525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a2f891a573bd6b7ff30782766b7564cfd2718e91c2399081bdf0ffb44fabba`  
		Last Modified: Wed, 28 Jan 2026 02:15:30 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f26d33b7e75cf64b24043a967d4288b682c0eba3866ed27897136240d3f4cbe`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 17.3 MB (17349909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fadf59f99eaf4a5457883e92f5eb0e9f05304f32b91ff429c77b5d12c399d17`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 25.5 MB (25539742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bbb75472d83a88fcf93366d31a9685491eaee5051b271d7e9822962477745c`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 10.0 MB (9954517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982182610648dbb0778b184ecff3e692201a2114ba00657d6fd977582e60c802`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c47f152455dabd15e5d73f9f555e031f1bf91be0a42bb7899543ca32f4be842`  
		Last Modified: Wed, 28 Jan 2026 02:15:34 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d60b69639960857109359648f1dd0dd6cb3d2cce9bdd6b1a594fd99159bf8f`  
		Last Modified: Wed, 28 Jan 2026 02:15:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf3426000179b3492ca41ec23019609bae7bd020884ba682b730f4920dcdadd`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 7.2 MB (7213335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d0c859c41e3ca1cc276016f6151a0a02e77f672f849df7d283d4657b2fd464`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 101.3 KB (101289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6748b522881f24eb97f2eed26e32bdb49ae5819b2477eae3a4976874142ff758`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:407dff81deac15d5750c410b3b45d2888514fd7173fad465cdb860a9e18a068c`  
		Last Modified: Wed, 28 Jan 2026 04:19:59 GMT  
		Size: 60.4 MB (60431745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae84a81436627202044f15c8bfbb21c37acd9371efb16eac52fa88d19fd035c`  
		Last Modified: Wed, 28 Jan 2026 04:19:58 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66e9c5f6367f5ce3bcd7921fbcd7ecdee44c87e2b3fb4e91c0953fdefb902bb`  
		Last Modified: Wed, 28 Jan 2026 04:19:58 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:76d7445bd6915a9080071a3680a3a2dd3bfb0697d214d61d429692ed178b2519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee53cf6ac36a1613efdfec96533f5b66f1bac362f162eeed2703924705574c2d`

```dockerfile
```

-	Layers:
	-	`sha256:51f7535efd28fb94f257372f96380d2a49634a8b4664d35a295a7201ee67d470`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind-rootless`

```console
$ docker pull docker@sha256:e2256cccf0a81babdf6b0715edc84299976eea749dc373de1d4c4b98f38be576
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:6e740431e7ec02952bcba763683de89ae7c38ed168d0cfc4b875ffc2cc94eb01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.6 MB (164596244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:893377b7f16e5efd1e758a1c978a11516ff914ffd6896497463fae305e6732d9`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:15:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:15:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:15:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:15:17 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:15:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:15:17 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:15:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:15:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:15:19 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:15:19 GMT
CMD ["sh"]
# Wed, 28 Jan 2026 03:58:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 Jan 2026 03:58:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 Jan 2026 03:58:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 Jan 2026 03:58:45 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
VOLUME [/var/lib/docker]
# Wed, 28 Jan 2026 03:58:45 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 Jan 2026 03:58:45 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 Jan 2026 03:58:45 GMT
CMD []
# Wed, 28 Jan 2026 04:49:51 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Wed, 28 Jan 2026 04:49:51 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 28 Jan 2026 04:49:51 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 04:49:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 28 Jan 2026 04:49:52 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 28 Jan 2026 04:49:52 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 28 Jan 2026 04:49:52 GMT
USER rootless
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03ce8e2700f1129dc15f38a5e1e7d27cdd2b98175c4d9ac08dc5646c3c35ba4`  
		Last Modified: Wed, 28 Jan 2026 02:15:26 GMT  
		Size: 8.4 MB (8399638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dabc00febb6a9a0d9954ef0b62272b11dabac7697dd7a0f94f9a96e241fbfd2`  
		Last Modified: Wed, 28 Jan 2026 02:15:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9408125f9d0c694cc95efc06409f73e6d6907c853a7f861c85b36824fb02ed25`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 18.8 MB (18774054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1765bbbd236eff12d3ecffaab470c2a8ade7f1432cbf0f1efe2f520cb9d74bfc`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 28.3 MB (28308902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d4f1a3f89cb924cc72cf031843e7490b98f39a276e6628c0ef444a871ff92f`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 10.8 MB (10799762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ca730a0591b75f8b903f70ff08c4b2959f397bd8775ba1a873cbb344b15c1a0`  
		Last Modified: Wed, 28 Jan 2026 02:15:28 GMT  
		Size: 533.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc93a580b636b3173550ee5a31a23ae95eb17558288345a26091285a5f477d5`  
		Last Modified: Wed, 28 Jan 2026 02:15:28 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9745309fb9885c647e35e9d55ab83308f9c212460ad5f9b73c2e518179059b72`  
		Last Modified: Wed, 28 Jan 2026 02:15:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:effa5c3a383e3a584de2fe9ef352f8fcde727e8db088492f0c8e49fc27f7abaa`  
		Last Modified: Wed, 28 Jan 2026 03:58:56 GMT  
		Size: 6.9 MB (6934734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a8f8addf621601263b2bfea9efe7ffac5903b85bfe7b9f628f7a2ff6bd4fce`  
		Last Modified: Wed, 28 Jan 2026 03:58:55 GMT  
		Size: 92.5 KB (92460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:396bcb1ae646a1eb234538a6bf406490001b6067e5626f4858b3d3ab115a1338`  
		Last Modified: Wed, 28 Jan 2026 03:58:56 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636ece6788bea2909cc3a17231a1a4827c4db266c991df7770a909ecdb8d3fd0`  
		Last Modified: Wed, 28 Jan 2026 03:58:57 GMT  
		Size: 66.6 MB (66619579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb2987d59bbd2b711c1759725d9ccc5891b03def0602234c4f49beb1e5c2be1`  
		Last Modified: Wed, 28 Jan 2026 03:58:57 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ac6a5de045400bc7b163e70c2cd9429f6202144cb50ed4b85688aded44f58e`  
		Last Modified: Wed, 28 Jan 2026 03:58:57 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:733f26c740596bada2273b63c30df575d6fe75108c34ae59cf6cce23eb6fde38`  
		Last Modified: Wed, 28 Jan 2026 04:49:58 GMT  
		Size: 3.4 MB (3419936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9b0d647df5d90a456bfb18e7fe3512570e5501e17a96c28d0673f36c7de2ab`  
		Last Modified: Wed, 28 Jan 2026 04:49:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2266ba1a98fbf4bf56e7477a64291015ffc22febbdef7b5c52756c0bccea91bc`  
		Last Modified: Wed, 28 Jan 2026 04:49:58 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e7bef04bfc2f8ecbd179e44e594aea6870289cac0095619a71f9ae48c070b2`  
		Last Modified: Wed, 28 Jan 2026 04:49:59 GMT  
		Size: 17.4 MB (17375872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de36060bb1e57bb0070a546b5af68c0c667dfc7c88ad9c5e0b4b58cd903fdd5f`  
		Last Modified: Wed, 28 Jan 2026 04:49:59 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:304a9bab4d48983bd4f25caa7723d4ff17feec1769ef4b9d815a85818b33f85a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18a9fa96564b6f3cbe5f035361ffe48a58c26e0d28c673a4517c0afb4d19bd17`

```dockerfile
```

-	Layers:
	-	`sha256:f20e17ed780eccbdcae7df7f23b087c7750a8fca8f1ef231ace886ff1ec41145`  
		Last Modified: Wed, 28 Jan 2026 04:49:58 GMT  
		Size: 30.6 KB (30589 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:10185cf7e9ecf2d725eabaed0f994c40d28c4ca77f04234d07c2bb0efcd4c588
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154355521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f80a4777f73ae85118338e6c79bca8a28937df9dc8a5f912a5066951db75e2a7`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:15:20 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:15:20 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:15:20 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:15:22 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:15:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:15:22 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:15:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:15:23 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:15:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:15:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:15:24 GMT
CMD ["sh"]
# Wed, 28 Jan 2026 04:19:44 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 Jan 2026 04:19:44 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 Jan 2026 04:19:45 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 04:19:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 Jan 2026 04:19:48 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 Jan 2026 04:19:48 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 Jan 2026 04:19:48 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 04:19:48 GMT
VOLUME [/var/lib/docker]
# Wed, 28 Jan 2026 04:19:48 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 Jan 2026 04:19:48 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 Jan 2026 04:19:48 GMT
CMD []
# Wed, 28 Jan 2026 05:26:30 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Wed, 28 Jan 2026 05:26:30 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 28 Jan 2026 05:26:30 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 05:26:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 28 Jan 2026 05:26:31 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 28 Jan 2026 05:26:31 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 28 Jan 2026 05:26:31 GMT
USER rootless
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23cd2c872bdff3a89f69a977eea6049f005ee667e33468764b0584c9a8959fe3`  
		Last Modified: Wed, 28 Jan 2026 02:15:31 GMT  
		Size: 8.5 MB (8453525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a2f891a573bd6b7ff30782766b7564cfd2718e91c2399081bdf0ffb44fabba`  
		Last Modified: Wed, 28 Jan 2026 02:15:30 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f26d33b7e75cf64b24043a967d4288b682c0eba3866ed27897136240d3f4cbe`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 17.3 MB (17349909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fadf59f99eaf4a5457883e92f5eb0e9f05304f32b91ff429c77b5d12c399d17`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 25.5 MB (25539742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bbb75472d83a88fcf93366d31a9685491eaee5051b271d7e9822962477745c`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 10.0 MB (9954517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982182610648dbb0778b184ecff3e692201a2114ba00657d6fd977582e60c802`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c47f152455dabd15e5d73f9f555e031f1bf91be0a42bb7899543ca32f4be842`  
		Last Modified: Wed, 28 Jan 2026 02:15:34 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d60b69639960857109359648f1dd0dd6cb3d2cce9bdd6b1a594fd99159bf8f`  
		Last Modified: Wed, 28 Jan 2026 02:15:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf3426000179b3492ca41ec23019609bae7bd020884ba682b730f4920dcdadd`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 7.2 MB (7213335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d0c859c41e3ca1cc276016f6151a0a02e77f672f849df7d283d4657b2fd464`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 101.3 KB (101289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6748b522881f24eb97f2eed26e32bdb49ae5819b2477eae3a4976874142ff758`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:407dff81deac15d5750c410b3b45d2888514fd7173fad465cdb860a9e18a068c`  
		Last Modified: Wed, 28 Jan 2026 04:19:59 GMT  
		Size: 60.4 MB (60431745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae84a81436627202044f15c8bfbb21c37acd9371efb16eac52fa88d19fd035c`  
		Last Modified: Wed, 28 Jan 2026 04:19:58 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66e9c5f6367f5ce3bcd7921fbcd7ecdee44c87e2b3fb4e91c0953fdefb902bb`  
		Last Modified: Wed, 28 Jan 2026 04:19:58 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b2ca6f15a1175824a8ac624e8e96c03e577d7045335b3b8da66fa925ac730e`  
		Last Modified: Wed, 28 Jan 2026 05:26:37 GMT  
		Size: 3.4 MB (3394379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aae4fb46b816b0c2dabc0ce7fb6de979a1297033cfc1d63f2330898b865858f`  
		Last Modified: Wed, 28 Jan 2026 05:26:37 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0ee34b605800e64fa4c7d8ae1e8b3a28b7a99fb9273d49a13ddc555bda1daa5`  
		Last Modified: Wed, 28 Jan 2026 05:26:37 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4850780d6ebb6a4c34ff107ae6908c6afecf589851309b1c501eea08aadde6b2`  
		Last Modified: Wed, 28 Jan 2026 05:26:38 GMT  
		Size: 17.7 MB (17710501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b19d5a6a20d8289c916e7596e72a2d20595e4e8c11ae662f0ce57a9c05814f1`  
		Last Modified: Wed, 28 Jan 2026 05:26:38 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:c4559aefd8beb1182fc0607820b2e0c38fe82f9a6af4f47c78173a966859ba4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50641e7994aded7de3b8033e71f36c7fa1b0b852dc54cb3365dbfd3de2e376b6`

```dockerfile
```

-	Layers:
	-	`sha256:2e936dbc59719f822df84bc05b46cb1f559506d9e7912ed2c9c670c5b0a6d64c`  
		Last Modified: Wed, 28 Jan 2026 05:26:37 GMT  
		Size: 30.8 KB (30753 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:latest`

```console
$ docker pull docker@sha256:a284d31e4db9a9916fd9be44380263eaeafedf0e3048a859f978922b5a0c16fc
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
$ docker pull docker@sha256:99aa88f75d8d401c30e395db1d2e679a89ff0be9b415f020b8e2383c517e1fda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.8 MB (143799092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ca04087ca24aa6deade38370d033555d14dacd022c6a5d275f038b89eaf131`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:15:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:15:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:15:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:15:17 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:15:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:15:17 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:15:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:15:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:15:19 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:15:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:15:19 GMT
CMD ["sh"]
# Wed, 28 Jan 2026 03:58:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 Jan 2026 03:58:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 Jan 2026 03:58:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 Jan 2026 03:58:45 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:58:45 GMT
VOLUME [/var/lib/docker]
# Wed, 28 Jan 2026 03:58:45 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 Jan 2026 03:58:45 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 Jan 2026 03:58:45 GMT
CMD []
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03ce8e2700f1129dc15f38a5e1e7d27cdd2b98175c4d9ac08dc5646c3c35ba4`  
		Last Modified: Wed, 28 Jan 2026 02:15:26 GMT  
		Size: 8.4 MB (8399638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dabc00febb6a9a0d9954ef0b62272b11dabac7697dd7a0f94f9a96e241fbfd2`  
		Last Modified: Wed, 28 Jan 2026 02:15:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9408125f9d0c694cc95efc06409f73e6d6907c853a7f861c85b36824fb02ed25`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 18.8 MB (18774054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1765bbbd236eff12d3ecffaab470c2a8ade7f1432cbf0f1efe2f520cb9d74bfc`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 28.3 MB (28308902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d4f1a3f89cb924cc72cf031843e7490b98f39a276e6628c0ef444a871ff92f`  
		Last Modified: Wed, 28 Jan 2026 02:15:27 GMT  
		Size: 10.8 MB (10799762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ca730a0591b75f8b903f70ff08c4b2959f397bd8775ba1a873cbb344b15c1a0`  
		Last Modified: Wed, 28 Jan 2026 02:15:28 GMT  
		Size: 533.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc93a580b636b3173550ee5a31a23ae95eb17558288345a26091285a5f477d5`  
		Last Modified: Wed, 28 Jan 2026 02:15:28 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9745309fb9885c647e35e9d55ab83308f9c212460ad5f9b73c2e518179059b72`  
		Last Modified: Wed, 28 Jan 2026 02:15:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:effa5c3a383e3a584de2fe9ef352f8fcde727e8db088492f0c8e49fc27f7abaa`  
		Last Modified: Wed, 28 Jan 2026 03:58:56 GMT  
		Size: 6.9 MB (6934734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a8f8addf621601263b2bfea9efe7ffac5903b85bfe7b9f628f7a2ff6bd4fce`  
		Last Modified: Wed, 28 Jan 2026 03:58:55 GMT  
		Size: 92.5 KB (92460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:396bcb1ae646a1eb234538a6bf406490001b6067e5626f4858b3d3ab115a1338`  
		Last Modified: Wed, 28 Jan 2026 03:58:56 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636ece6788bea2909cc3a17231a1a4827c4db266c991df7770a909ecdb8d3fd0`  
		Last Modified: Wed, 28 Jan 2026 03:58:57 GMT  
		Size: 66.6 MB (66619579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb2987d59bbd2b711c1759725d9ccc5891b03def0602234c4f49beb1e5c2be1`  
		Last Modified: Wed, 28 Jan 2026 03:58:57 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ac6a5de045400bc7b163e70c2cd9429f6202144cb50ed4b85688aded44f58e`  
		Last Modified: Wed, 28 Jan 2026 03:58:57 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:2d2c0973782cdccc69752fb841755627c37546ebbf2f68f0bf070bf51d23ec60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0784b32a62dac2ebed2ad0ae726d2901f105b39654d58a2d2d351b4eaea7d818`

```dockerfile
```

-	Layers:
	-	`sha256:161b2e45f0098aead317dd0674b614a4e1252835a147f30b88ddc0667bf7ba93`  
		Last Modified: Wed, 28 Jan 2026 03:58:55 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v6

```console
$ docker pull docker@sha256:70dcad0b903a121c11d71a23834267a49327cd21053d8a2a83529cf94a2d9fbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135630532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:438bd2c6733062a94188c3067ba6118e7dda4560c7d7eb98ecec81192d5273b2`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:19:28 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:19:29 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:19:29 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:19:32 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:19:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:19:32 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:19:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:19:34 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:19:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:19:36 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:19:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:19:36 GMT
CMD ["sh"]
# Wed, 28 Jan 2026 03:49:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 Jan 2026 03:49:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 Jan 2026 03:49:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 03:49:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 Jan 2026 03:49:21 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 Jan 2026 03:49:21 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 Jan 2026 03:49:21 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:49:21 GMT
VOLUME [/var/lib/docker]
# Wed, 28 Jan 2026 03:49:21 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 Jan 2026 03:49:21 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 Jan 2026 03:49:21 GMT
CMD []
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08efb619161971b8dbf3d2d18d22c25f3caf7baea4b18537b77a961fee285e4d`  
		Last Modified: Wed, 28 Jan 2026 02:19:43 GMT  
		Size: 8.3 MB (8301019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11eae5034a08f196af9949aec8c0d0a5c776062160fbfa6839f4e91eb25c523`  
		Last Modified: Wed, 28 Jan 2026 02:19:42 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b811dd811e1e6a5a185faf36f1f9dd7bd483290fc51d98ccb7f5014b5bd19ab`  
		Last Modified: Wed, 28 Jan 2026 02:19:43 GMT  
		Size: 17.6 MB (17576540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395a6e19e8b08ce81dbf6939f7000c5eaaa78657497cffd3559c4d3586ad6f25`  
		Last Modified: Wed, 28 Jan 2026 02:19:44 GMT  
		Size: 26.6 MB (26570467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b3f84acb2b12fc7c649c003ff8e9348dabfff644a17daad4b02eef0bd9b40b6`  
		Last Modified: Wed, 28 Jan 2026 02:19:44 GMT  
		Size: 10.2 MB (10213042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746007c626ec304c1dfcf1e9084f31b26345a6079f9efe6f265b8fa508abf11a`  
		Last Modified: Wed, 28 Jan 2026 02:19:44 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f144bc5ce89728429c7674f4da3e2efbf3439669eae61e270d13a77809b4b9b7`  
		Last Modified: Wed, 28 Jan 2026 02:19:45 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b078b00f266ba4e03e79da886e567e61c21f493be073a7001f1e3db1345ccf57`  
		Last Modified: Wed, 28 Jan 2026 02:19:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6f4b2cf4256d701c8e551ce6b913b60516e7a6812dd2a6b150737145528fdf`  
		Last Modified: Wed, 28 Jan 2026 03:49:31 GMT  
		Size: 7.3 MB (7271609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b290e764c28e19f2f21aa7790d801cc6056a53cd51c8fb1bb6faf2e2346d4145`  
		Last Modified: Wed, 28 Jan 2026 03:49:30 GMT  
		Size: 91.8 KB (91775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:894eda0b2167abb0c583bbf993071a8d219941e2dd3bc2fcd1f8bfd8ca024a34`  
		Last Modified: Wed, 28 Jan 2026 03:49:30 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661a756971591996ae71af31b4d76fd40c1ba5140d25d52487a63a2ce33123b3`  
		Last Modified: Wed, 28 Jan 2026 03:49:32 GMT  
		Size: 62.0 MB (62028111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0fea802a7e013543afeb57c94b421ff42c6cc94e875a7a48079633d5b32cf0`  
		Last Modified: Wed, 28 Jan 2026 03:49:31 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89262e7e7a4c52344f56768909e409e4d52e23b7e5f872f34c6f8f05f600ced1`  
		Last Modified: Wed, 28 Jan 2026 03:49:32 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:77efd8773fd21feb58c996858580a066f8336af75ce15a65d1e94fbfc662939f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8937de610607274348941cf30b97eee5b16a47a2a3e355daae965571f78e1b8e`

```dockerfile
```

-	Layers:
	-	`sha256:b2c9967356bfd5048f745045eb7a61d4c51f3b8a396da52f925736b964896609`  
		Last Modified: Wed, 28 Jan 2026 03:49:30 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v7

```console
$ docker pull docker@sha256:136f2e805834a4247060b8060063ba782a2fdce6083a3cb47d02e83936623504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133715469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a4604f36042cbaaba3fd792ec4e26bfaf62d2d45b48d38a8697760ddf3306fa`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:19:33 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:19:33 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:19:34 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:19:37 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:19:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:19:37 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:19:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:19:39 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:19:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:19:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:19:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:19:41 GMT
CMD ["sh"]
# Wed, 28 Jan 2026 03:51:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 Jan 2026 03:51:44 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 Jan 2026 03:51:44 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 03:51:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 Jan 2026 03:51:47 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 Jan 2026 03:51:47 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 Jan 2026 03:51:47 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:51:47 GMT
VOLUME [/var/lib/docker]
# Wed, 28 Jan 2026 03:51:47 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 Jan 2026 03:51:47 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 Jan 2026 03:51:47 GMT
CMD []
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef74ac3c65992e7acddcc2a2c02498d51d5fda8b771538e5411d2d5f3a3e9eec`  
		Last Modified: Wed, 28 Jan 2026 02:19:47 GMT  
		Size: 7.6 MB (7597810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01925faabefdbedf8efebb820b152e94fb287b72138d282a76557993132623ca`  
		Last Modified: Wed, 28 Jan 2026 02:19:47 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ad13ec2588fba164870da3d93ba8b5ad34e242b5bc6fb7b5df1bd055e194e0`  
		Last Modified: Wed, 28 Jan 2026 02:19:48 GMT  
		Size: 17.6 MB (17566458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc3d6d20d26654203dbb33aecb823850102a06ee1d8826eeea313f51053947d`  
		Last Modified: Wed, 28 Jan 2026 02:19:48 GMT  
		Size: 26.5 MB (26544669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309b43a06105801e72a4057c9a98aa39f845292f118ed5364be6f2c58fff6fb2`  
		Last Modified: Wed, 28 Jan 2026 02:19:48 GMT  
		Size: 10.2 MB (10198593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c018df83e09983e9c86c614e37738e0c9913c07f571d99ca7464a8eead3114`  
		Last Modified: Wed, 28 Jan 2026 02:19:49 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff08fbe96bdc955d67587b7154a9e64b5fd0933ad18112a10502a2d2ee351334`  
		Last Modified: Wed, 28 Jan 2026 02:19:49 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82766871530b6d5c5faaefb052706696dbc1f4936a761d57fe77b41476c57e81`  
		Last Modified: Wed, 28 Jan 2026 02:19:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966fa3b3930581a719871ad9cc50569b5b949938c666c5f604128567586dcc98`  
		Last Modified: Wed, 28 Jan 2026 03:51:58 GMT  
		Size: 6.6 MB (6572989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8288f87d3ec8e6d2c73fad07643b43f2c5a333b046f21c81531e877d6eaf19d4`  
		Last Modified: Wed, 28 Jan 2026 03:51:58 GMT  
		Size: 88.1 KB (88136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd5922158e4b006788c6366971c7c91cc1404b01a100da81d4c9a0477a74027`  
		Last Modified: Wed, 28 Jan 2026 03:51:58 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842a3b5326d8c1c6b696edd5624246ed13391ce31743771eb92561f224c0e672`  
		Last Modified: Wed, 28 Jan 2026 03:52:00 GMT  
		Size: 61.9 MB (61856931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f666916210054b0fd5f72affa9ac152fa7c42d927442f2dd309d354e89b9277`  
		Last Modified: Wed, 28 Jan 2026 03:51:59 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cf19ee261d3469335adb02771df03de4d7bd57f3cb5c06bb5841ae7b93697c`  
		Last Modified: Wed, 28 Jan 2026 03:51:59 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:8457bbc8972fac13450e367c97a9a1b851c44540331c9f631abe6ecc6da554fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d30df9382a2c15c97b7086f993412c3a0f44e8ed81f835508748d782eabe5345`

```dockerfile
```

-	Layers:
	-	`sha256:0a1c8b9290fc1e34c2f218c7730ca8fc83fc55704982e288265ea392b6f0447c`  
		Last Modified: Wed, 28 Jan 2026 03:51:58 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:2cd37b1da26b3d7bdae2014ffafb6543a3c40f32973395bdf6e402afc6818e38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.2 MB (133249301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a287877d76e510dc36d4294bef0d4540628445c54cbf477d32ad4aef68e7bb0a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:15:20 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 28 Jan 2026 02:15:20 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:15:20 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 28 Jan 2026 02:15:22 GMT
ENV DOCKER_VERSION=29.2.0
# Wed, 28 Jan 2026 02:15:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 28 Jan 2026 02:15:22 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Wed, 28 Jan 2026 02:15:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 28 Jan 2026 02:15:23 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Wed, 28 Jan 2026 02:15:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 28 Jan 2026 02:15:24 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 28 Jan 2026 02:15:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:15:24 GMT
CMD ["sh"]
# Wed, 28 Jan 2026 04:19:44 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 28 Jan 2026 04:19:44 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 28 Jan 2026 04:19:45 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 28 Jan 2026 04:19:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 28 Jan 2026 04:19:48 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 28 Jan 2026 04:19:48 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 28 Jan 2026 04:19:48 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 04:19:48 GMT
VOLUME [/var/lib/docker]
# Wed, 28 Jan 2026 04:19:48 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 28 Jan 2026 04:19:48 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 28 Jan 2026 04:19:48 GMT
CMD []
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23cd2c872bdff3a89f69a977eea6049f005ee667e33468764b0584c9a8959fe3`  
		Last Modified: Wed, 28 Jan 2026 02:15:31 GMT  
		Size: 8.5 MB (8453525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a2f891a573bd6b7ff30782766b7564cfd2718e91c2399081bdf0ffb44fabba`  
		Last Modified: Wed, 28 Jan 2026 02:15:30 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f26d33b7e75cf64b24043a967d4288b682c0eba3866ed27897136240d3f4cbe`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 17.3 MB (17349909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fadf59f99eaf4a5457883e92f5eb0e9f05304f32b91ff429c77b5d12c399d17`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 25.5 MB (25539742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bbb75472d83a88fcf93366d31a9685491eaee5051b271d7e9822962477745c`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 10.0 MB (9954517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982182610648dbb0778b184ecff3e692201a2114ba00657d6fd977582e60c802`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c47f152455dabd15e5d73f9f555e031f1bf91be0a42bb7899543ca32f4be842`  
		Last Modified: Wed, 28 Jan 2026 02:15:34 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d60b69639960857109359648f1dd0dd6cb3d2cce9bdd6b1a594fd99159bf8f`  
		Last Modified: Wed, 28 Jan 2026 02:15:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf3426000179b3492ca41ec23019609bae7bd020884ba682b730f4920dcdadd`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 7.2 MB (7213335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d0c859c41e3ca1cc276016f6151a0a02e77f672f849df7d283d4657b2fd464`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 101.3 KB (101289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6748b522881f24eb97f2eed26e32bdb49ae5819b2477eae3a4976874142ff758`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:407dff81deac15d5750c410b3b45d2888514fd7173fad465cdb860a9e18a068c`  
		Last Modified: Wed, 28 Jan 2026 04:19:59 GMT  
		Size: 60.4 MB (60431745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae84a81436627202044f15c8bfbb21c37acd9371efb16eac52fa88d19fd035c`  
		Last Modified: Wed, 28 Jan 2026 04:19:58 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66e9c5f6367f5ce3bcd7921fbcd7ecdee44c87e2b3fb4e91c0953fdefb902bb`  
		Last Modified: Wed, 28 Jan 2026 04:19:58 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:76d7445bd6915a9080071a3680a3a2dd3bfb0697d214d61d429692ed178b2519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee53cf6ac36a1613efdfec96533f5b66f1bac362f162eeed2703924705574c2d`

```dockerfile
```

-	Layers:
	-	`sha256:51f7535efd28fb94f257372f96380d2a49634a8b4664d35a295a7201ee67d470`  
		Last Modified: Wed, 28 Jan 2026 04:19:57 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:windowsservercore`

```console
$ docker pull docker@sha256:79cb1793605b4f2d7317cea6706862e4b002e6ace6375912bab555eebfdf6ed2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `docker:windowsservercore` - windows version 10.0.26100.32230; amd64

```console
$ docker pull docker@sha256:c5d3ecbfcaeb424c90459ac8317405555d19b1b8b3e578390234d4a8e7c24c64
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1556599774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d647b193ba9f5cb583f9fb294f2d532c6d85295880ef0649d60793cc309abcd1`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Tue, 03 Feb 2026 17:28:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 03 Feb 2026 17:29:28 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 03 Feb 2026 17:29:30 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:29:32 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.1.zip
# Tue, 03 Feb 2026 17:29:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 03 Feb 2026 17:29:46 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:29:48 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.windows-amd64.exe
# Tue, 03 Feb 2026 17:29:48 GMT
ENV DOCKER_BUILDX_SHA256=b49832d4ac46bde05006f7ad3506b9d5060b60e5c566545d8e10c1a80df08a4a
# Tue, 03 Feb 2026 17:29:59 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 03 Feb 2026 17:30:00 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:30:01 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Tue, 03 Feb 2026 17:30:01 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Tue, 03 Feb 2026 17:30:08 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3345d2727a1883e3d335172c07a1f0f478ed9c744e1aa4ec455219fd5b041b31`  
		Last Modified: Tue, 03 Feb 2026 17:30:17 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c2b758f14303d714990de0fad8eacb8f18d18925809a064fa024e0a8203573a`  
		Last Modified: Tue, 03 Feb 2026 17:30:16 GMT  
		Size: 402.8 KB (402791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c544aebc260938057720752277d7e0b5a599ebf13c36d8be0403e694d8929db8`  
		Last Modified: Tue, 03 Feb 2026 17:30:15 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54275eb139ff712b0a5f139cdba772a69cd2371fcb0b65f6371b8d8b22f92c19`  
		Last Modified: Tue, 03 Feb 2026 17:30:15 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff99eb3d4bee14899afa2383e60cfa18a0f63d88f5c759afcbfa0cef9bae50bb`  
		Last Modified: Tue, 03 Feb 2026 17:30:18 GMT  
		Size: 19.5 MB (19477937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d8a57f5276cfc049bae3b7a853039be549c9bada93ef2e8d868ea54e9c04236`  
		Last Modified: Tue, 03 Feb 2026 17:30:14 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be178348f9fba72db323ad766660239b1363bbe80d1f01cf90cd2531b5f01b03`  
		Last Modified: Tue, 03 Feb 2026 17:30:14 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca77ca63bd7d4b72f07134cb3691a9edeba02acdb61fb8ff15a7f6c7f44734ce`  
		Last Modified: Tue, 03 Feb 2026 17:30:14 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51aa328a4c51fa2977445e97c24b485b2fbf132d207a9adfa58cf7406f3f8a1f`  
		Last Modified: Tue, 03 Feb 2026 17:30:30 GMT  
		Size: 29.5 MB (29453041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c300d10089e1c370f164537efd3c43df949644198f422eb4863dccfe9930a4f`  
		Last Modified: Tue, 03 Feb 2026 17:30:12 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5356d434dcd14c58d539907321e96d2a0e794ac74a29c08aa2df1dbaa611e231`  
		Last Modified: Tue, 03 Feb 2026 17:30:12 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b03bbb60e30cb160ee1c1c6844849f758718d7111a7cb510a1b0ec1702120fd`  
		Last Modified: Tue, 03 Feb 2026 17:30:12 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2d04ad8db9950e63dbd9118d08d70484b5aed5cf9dadf9591e16f2a8339e8e`  
		Last Modified: Tue, 03 Feb 2026 17:30:14 GMT  
		Size: 11.5 MB (11493926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.20348.4648; amd64

```console
$ docker pull docker@sha256:ba1e9a93d62651a48e0592e4a6010300708e2422e46df2b25d54b1d2f1e7fb47
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1896494534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a09c7520bcdba0cceb87d9e1fe705ea6641137be025705d09eaba1893561ddea`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Tue, 03 Feb 2026 17:28:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 03 Feb 2026 17:29:49 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 03 Feb 2026 17:29:49 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:29:50 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.1.zip
# Tue, 03 Feb 2026 17:30:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 03 Feb 2026 17:30:17 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:30:18 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.windows-amd64.exe
# Tue, 03 Feb 2026 17:30:18 GMT
ENV DOCKER_BUILDX_SHA256=b49832d4ac46bde05006f7ad3506b9d5060b60e5c566545d8e10c1a80df08a4a
# Tue, 03 Feb 2026 17:30:49 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 03 Feb 2026 17:30:50 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:30:52 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Tue, 03 Feb 2026 17:30:52 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Tue, 03 Feb 2026 17:31:09 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1610c61d22cce1c0da1f89bcf2b2b93db5d1ee6703ddda8c50c992a55a3a3273`  
		Last Modified: Tue, 03 Feb 2026 17:31:19 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35301633ca92d436f45505192a1ef4f18618178fd179a0275e79d55f1cdba61d`  
		Last Modified: Tue, 03 Feb 2026 17:31:19 GMT  
		Size: 502.0 KB (501985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc76ce47c4de88873c339dee382928f8c2afe957a1f67eaa1bc1745de35e796e`  
		Last Modified: Tue, 03 Feb 2026 17:31:18 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c0a93da300b8f2017782995a21ddcc03360f0068884e95f2c90a34943b5a853`  
		Last Modified: Tue, 03 Feb 2026 17:31:18 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4642a451e4aa3a689441cf53a384a5333b79045931964aecc32acb75dab6242f`  
		Last Modified: Tue, 03 Feb 2026 17:31:20 GMT  
		Size: 19.4 MB (19440499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f80fcdb722aba8bdf0a57b047c109edce18d999e3bc1649781fa0d3de37c6e29`  
		Last Modified: Tue, 03 Feb 2026 17:31:16 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52573eb20ed9e08365fa5f5e972f07f60f80fd44870b2c8c2e00435b86e529d7`  
		Last Modified: Tue, 03 Feb 2026 17:31:16 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc93a0644ac21577feac91654ceef3e9cb714742257794765b8f41f26967f84e`  
		Last Modified: Tue, 03 Feb 2026 17:31:16 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c020b7de7a60805f5e0f214c5933b5730ce1e22475c6c0637dbe59005c03baa4`  
		Last Modified: Tue, 03 Feb 2026 17:31:33 GMT  
		Size: 29.4 MB (29425091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:538b00d976a03c45b55d387636033ba066f8d59660d195f26399a156232cb079`  
		Last Modified: Tue, 03 Feb 2026 17:31:14 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f8c0456ab18eeca4e06f6a4f1edc155807d2fd8565b3c71217f4895c0778536`  
		Last Modified: Tue, 03 Feb 2026 17:31:14 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525c0f16947c0cc46484ca50b3cbe0be998327c9e218a8f15dd79b3752be1f84`  
		Last Modified: Tue, 03 Feb 2026 17:31:14 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f29f86a605fc1d2ecf16f261c2beeb1261773d00bba4c7341e76d2363f15db4a`  
		Last Modified: Tue, 03 Feb 2026 17:31:16 GMT  
		Size: 11.5 MB (11456032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:315827d701f9fef8731fca2a65b1c5960422bfb5d0e6f335995310b4c2c2bf07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull docker@sha256:ba1e9a93d62651a48e0592e4a6010300708e2422e46df2b25d54b1d2f1e7fb47
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1896494534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a09c7520bcdba0cceb87d9e1fe705ea6641137be025705d09eaba1893561ddea`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Tue, 03 Feb 2026 17:28:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 03 Feb 2026 17:29:49 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 03 Feb 2026 17:29:49 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:29:50 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.1.zip
# Tue, 03 Feb 2026 17:30:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 03 Feb 2026 17:30:17 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:30:18 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.windows-amd64.exe
# Tue, 03 Feb 2026 17:30:18 GMT
ENV DOCKER_BUILDX_SHA256=b49832d4ac46bde05006f7ad3506b9d5060b60e5c566545d8e10c1a80df08a4a
# Tue, 03 Feb 2026 17:30:49 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 03 Feb 2026 17:30:50 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:30:52 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Tue, 03 Feb 2026 17:30:52 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Tue, 03 Feb 2026 17:31:09 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1610c61d22cce1c0da1f89bcf2b2b93db5d1ee6703ddda8c50c992a55a3a3273`  
		Last Modified: Tue, 03 Feb 2026 17:31:19 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35301633ca92d436f45505192a1ef4f18618178fd179a0275e79d55f1cdba61d`  
		Last Modified: Tue, 03 Feb 2026 17:31:19 GMT  
		Size: 502.0 KB (501985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc76ce47c4de88873c339dee382928f8c2afe957a1f67eaa1bc1745de35e796e`  
		Last Modified: Tue, 03 Feb 2026 17:31:18 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c0a93da300b8f2017782995a21ddcc03360f0068884e95f2c90a34943b5a853`  
		Last Modified: Tue, 03 Feb 2026 17:31:18 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4642a451e4aa3a689441cf53a384a5333b79045931964aecc32acb75dab6242f`  
		Last Modified: Tue, 03 Feb 2026 17:31:20 GMT  
		Size: 19.4 MB (19440499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f80fcdb722aba8bdf0a57b047c109edce18d999e3bc1649781fa0d3de37c6e29`  
		Last Modified: Tue, 03 Feb 2026 17:31:16 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52573eb20ed9e08365fa5f5e972f07f60f80fd44870b2c8c2e00435b86e529d7`  
		Last Modified: Tue, 03 Feb 2026 17:31:16 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc93a0644ac21577feac91654ceef3e9cb714742257794765b8f41f26967f84e`  
		Last Modified: Tue, 03 Feb 2026 17:31:16 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c020b7de7a60805f5e0f214c5933b5730ce1e22475c6c0637dbe59005c03baa4`  
		Last Modified: Tue, 03 Feb 2026 17:31:33 GMT  
		Size: 29.4 MB (29425091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:538b00d976a03c45b55d387636033ba066f8d59660d195f26399a156232cb079`  
		Last Modified: Tue, 03 Feb 2026 17:31:14 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f8c0456ab18eeca4e06f6a4f1edc155807d2fd8565b3c71217f4895c0778536`  
		Last Modified: Tue, 03 Feb 2026 17:31:14 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525c0f16947c0cc46484ca50b3cbe0be998327c9e218a8f15dd79b3752be1f84`  
		Last Modified: Tue, 03 Feb 2026 17:31:14 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f29f86a605fc1d2ecf16f261c2beeb1261773d00bba4c7341e76d2363f15db4a`  
		Last Modified: Tue, 03 Feb 2026 17:31:16 GMT  
		Size: 11.5 MB (11456032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:ed671d3152d0f57a459cd9f0838f7e48071ccef5c71ad1188693f4540f24cf19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32230; amd64

### `docker:windowsservercore-ltsc2025` - windows version 10.0.26100.32230; amd64

```console
$ docker pull docker@sha256:c5d3ecbfcaeb424c90459ac8317405555d19b1b8b3e578390234d4a8e7c24c64
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1556599774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d647b193ba9f5cb583f9fb294f2d532c6d85295880ef0649d60793cc309abcd1`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Tue, 03 Feb 2026 17:28:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 03 Feb 2026 17:29:28 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 03 Feb 2026 17:29:30 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:29:32 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.1.zip
# Tue, 03 Feb 2026 17:29:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 03 Feb 2026 17:29:46 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:29:48 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.windows-amd64.exe
# Tue, 03 Feb 2026 17:29:48 GMT
ENV DOCKER_BUILDX_SHA256=b49832d4ac46bde05006f7ad3506b9d5060b60e5c566545d8e10c1a80df08a4a
# Tue, 03 Feb 2026 17:29:59 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 03 Feb 2026 17:30:00 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:30:01 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Tue, 03 Feb 2026 17:30:01 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Tue, 03 Feb 2026 17:30:08 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3345d2727a1883e3d335172c07a1f0f478ed9c744e1aa4ec455219fd5b041b31`  
		Last Modified: Tue, 03 Feb 2026 17:30:17 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c2b758f14303d714990de0fad8eacb8f18d18925809a064fa024e0a8203573a`  
		Last Modified: Tue, 03 Feb 2026 17:30:16 GMT  
		Size: 402.8 KB (402791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c544aebc260938057720752277d7e0b5a599ebf13c36d8be0403e694d8929db8`  
		Last Modified: Tue, 03 Feb 2026 17:30:15 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54275eb139ff712b0a5f139cdba772a69cd2371fcb0b65f6371b8d8b22f92c19`  
		Last Modified: Tue, 03 Feb 2026 17:30:15 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff99eb3d4bee14899afa2383e60cfa18a0f63d88f5c759afcbfa0cef9bae50bb`  
		Last Modified: Tue, 03 Feb 2026 17:30:18 GMT  
		Size: 19.5 MB (19477937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d8a57f5276cfc049bae3b7a853039be549c9bada93ef2e8d868ea54e9c04236`  
		Last Modified: Tue, 03 Feb 2026 17:30:14 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be178348f9fba72db323ad766660239b1363bbe80d1f01cf90cd2531b5f01b03`  
		Last Modified: Tue, 03 Feb 2026 17:30:14 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca77ca63bd7d4b72f07134cb3691a9edeba02acdb61fb8ff15a7f6c7f44734ce`  
		Last Modified: Tue, 03 Feb 2026 17:30:14 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51aa328a4c51fa2977445e97c24b485b2fbf132d207a9adfa58cf7406f3f8a1f`  
		Last Modified: Tue, 03 Feb 2026 17:30:30 GMT  
		Size: 29.5 MB (29453041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c300d10089e1c370f164537efd3c43df949644198f422eb4863dccfe9930a4f`  
		Last Modified: Tue, 03 Feb 2026 17:30:12 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5356d434dcd14c58d539907321e96d2a0e794ac74a29c08aa2df1dbaa611e231`  
		Last Modified: Tue, 03 Feb 2026 17:30:12 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b03bbb60e30cb160ee1c1c6844849f758718d7111a7cb510a1b0ec1702120fd`  
		Last Modified: Tue, 03 Feb 2026 17:30:12 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2d04ad8db9950e63dbd9118d08d70484b5aed5cf9dadf9591e16f2a8339e8e`  
		Last Modified: Tue, 03 Feb 2026 17:30:14 GMT  
		Size: 11.5 MB (11493926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
